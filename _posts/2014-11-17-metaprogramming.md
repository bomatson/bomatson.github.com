---
layout: post
title:  "Metaprogramming"
---

> code that thinks of program structure as just another thing to manipulate

Object#send
-------------

Treats object as giant case statement (sending a message to an object)

Really a way to pass args to another method (send) where the actual code it triggered

{% highlight ruby %}
  class Foo
    def bar(*args)
    end
  end

  foo = Foo.new
  foo.send(:bar, 'args', 1)
{% endhighlight %}

> Look into cont_get

#method_missing
------------

{% highlight ruby %}

Project#name_changed?
Project#milestone_changed?

{% endhighlight %}

This is called after Ruby has tried looking up the method call on the class & superclasses

Need a fallback to super. The lookup chain will stop at that class and error (if its a subclass, this would be bad!)

Need to define a `respond_to_missing?`

Need to define the method within the method_missing call

> Method missing is good for dynamic DSLs, delegators

#define_method
------------

{% highlight ruby %}

['url', 'name'].each do |method|
  define_method "photo_#{method}" do
    photo.send(method)
  end
end

{% endhighlight %}

#include
---------

Defines an anonymous module at the end of the class definition. `include instance_methods`

#hooks
----------

* .inherited
* .included
* .extended

Her advice: don't use these!
