---
layout: post
title: "Rails 5 deprecation warning about HTTP request methods"
date:  2016-07-22 13:08:09
categories: rails
---

Recently while testing a Rails 5 api only application using Rspec I came across this warning message in my logs.

{% highlight ruby %}
DEPRECATION WARNING: ActionController::TestCase HTTP request methods will accept only
keyword arguments in future Rails versions.

Examples:

get :show, params: { id: 1 }, session: { user_id: 1 }
process :update, method: :post, params: { id: 1 }
DEPRECATION WARNING: ActionController::TestCase HTTP request methods will accept only
keyword arguments in future Rails versions.

{% endhighlight %}

In Rails 5, request methods accept only [keyword arguments](https://github.com/rails/rails/pull/18323/). To stop getting the above deprecation warning just edit your request methods like below.

{% highlight ruby %}
describe '#create' do
  it 'responds with a 200' do
    # post :create, loan_id: loan.id,
            payment: { amount: 25.0, payment_date: Time.now } #old method
    process :create, method: :post,
      params: { loan_id: loan.id, payment: { amount: 25.0, payment_date: Time.now  } }
    expect(response).to have_http_status(:ok)
  end
end  
{% endhighlight %}
