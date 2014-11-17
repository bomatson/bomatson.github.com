---
layout: post
title:  "RubyConf 2014: The Clash of Types"
---

After a vicious delay of Matz' keynote, he finally started up by describing how Rubyists need to maintain interest and curiousity if we're going to survive

Matz Predictions that have come true:

* RubyConf 2001 - Ruby VM
* RubyConf 2002 - M17N, Native Thread, Generational GC
* RubyConf 2003 - Keyword args, multiple assignment
* RubyConf 2005 - Stabby lambda
* Ruby Kaigai 2009 - Complex literal, bitmap marking
* RubyConf 2010 - mruby, refinement
* RubyConf 2014 - Ruby 3.0

Kinda obvious observation: if you're the maintainer of a language you have the most insight into its future

Coming next:

* JIT
* Concurrency improvements
* Static Typing?

We don't need static typing for speed? JIT is for that

Compile-time check is important! Find errors early in the dev cycle

Static is less flexible - Duck typing is more dynamic

Static types can be used for documentation, better than comments

>"Static typing is against duck typing"

Guy Decoux - Optional static typing "not a good idea"

Static Typing tends not to be DRY

_Soft typing:_ An approach to type checking without declaration in the code

{% highlight ruby %}
def foo(x)
  print x.to_int
  # requires the to_int method
end

foo(1) # OK: 1 has to_int
foo('s') #Error: 's' does not have to_int
{% endhighlight %}

Ruby should be able to detect that the wrong type is being used, since to_int is
not an available method on string

_Type_ is represented by set of methods (name, number and type of args), or class (as set of methods)

Soft typing can be implemented using a static analyzer, bringing us closer to the compiler.
