---
layout: post
title:  "Math in Ruby"
---

Numerical Coercion
---------------

* Finding a common `numeric` type in Ruby

Vectors
--------

* Wrap a magnitude and a direction (velocity, acceleration)
* Often mapped as arrows. ========>
* [Source](http://ruby-doc.org/stdlib-2.1.1/libdoc/matrix/rdoc/Vector.html)

{% highlight ruby %}

v = Vector.new(3,4)
2 * v
v.coerce(2).reduce(:*)
[v,2].reduce(:*)
v * 2
Vector.new(3*2, 4*2)

{% endhighlight %}

Scalars
-------
* Affects the magnitude by making them longer or shorter (population, battery life, finite values)

Dimensional Analysis
-------------

* The analysis of the dimensions of measurements (60 mph, 2.7GHz)
* Conversion of complex units to a simple one
* [Unitary](https://github.com/yarmiganosca/unitary) library does the conversion for you

{% highlight ruby %}

speed = 5 * :mi/:hr

{% endhighlight %}

Ruby needs to be better at Math
---------------

Why can't we do things like:

{% highlight ruby %}

4.dollars == 6.5.euros
g = 2 * Math::tan
f = Math::sin * Math::cos

{% endhighlight %}

