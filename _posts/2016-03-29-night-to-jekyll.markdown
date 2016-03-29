---
layout: post
title:  "A night with Jekyll!"
date:   2016-03-29 23:51:54 +0700
---
I'm playing with Jekyll without use existence themes.

{% highlight ruby linenos%}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}

Thanks for GOD!

@Mun