---
layout: post
title: "Seven and a half Months as a Software Engineer"
date: 2017-07-04 12:00:00
comments: true
category: computer science
---

# And seven and half months with Scala

It has been more than seven months since I started working as a Software Engineer. I intended
to write about my experience a while ago. At first I said I'd do it one month after, then two,
three and so forth, until today I finally decided to get it done before the fireworks (Happy
Fourth of July Everyone!).

After looking for a job after my summer job adventures in 2016, I decided to accept a postion
at Rally, which is digital health company located in San Francisco and headquartered in 
Washington DC. Rally focuses on the gamification of health and fitness, and improving the 
experience users have with healthcare and healthi insurance. If that sounds a little vague,
well, it is. The company has three main products: Rally Engage, Find Price and Care, and 
improving the UHC health system. Rally engage focuses on user engagement to improve the health
of a company's employers (and therebey indirectly lowering their insurance costs). Find Price
and care is a better search for health providers so that consumer have the cheapest and best
option available allowed for their insurance. In 2014 United Health Group became a majority 
stakeholder in the company, and since then it has revamped their digital experience, notable the
UHG dashboard, which needed optimization and modernization. I work in their dashboard team, 
integrating with new services and leveraging some of their existing systems to make our work.

Which brings me to the title of the post. I have spent the majority of the past  almost eight 
months working in [Scala][scala_language] which is an functional, objected oriented, JVM based 
language. Scala compiles to java bytecode, which makes it completely interoperable with Java. 
In practice this means you can use you're favorite java frameworks with the language. This makes
the language versatile, since it can integrated with an existing java stack. At work we use the
 [Play][play] framework, which is a web framework that can be used with Gradle or Maven as
package managers.

Scala uses [sbt][sbt] ("scala build tool"), for compilation, which is a tool built using scala
itself. Coming from `javac` and `make` (or `cmake`) build processes, I thought that was pretty
neat. What is interesting about scala is that it allows you to model a problem both in an
Object Oriented style and a functional. So you could write a traditional MVC web application,
modeling each part as an object, but change the processing and interactions between the 
components to be functional (say, by making the controller accept a function by the model, etc.).
If you've never programmed a functional language, think of a functional process as a really big 
processing pipe, in which you give some input at the beginning and get some output at the end,
peeling unneeded information along the way.

It can make you're head spin a little, but it becomes a much simpler, less verbose way to code 
(personal opinion).
As an example, consider sa function where you'd like to have some behavior based on an
enumeration on a list, in java you'de do something like: 

{% highlight java%}

if (exVariable.isEqualTo(enumerationType.1) {
	// do something
}
else if (exVariable.isEqualTo(enumerationType.2) {
	// do something else 
}
else if (exVariable.isEqualTo(enumerationType.3) {
	// do something else
}
else {
	// do another different thing
}
{% endhighlight %}

Or maybe more effectively (correctly?) inspiring myself from an [SO][exampleSOAns] answer:

{%highlight java %}

try {
	enumerationType result = enumerationType.valueOf(exVariable)
} catch (IllegalArgumentException e) {
	// do something with this knowledge
}

{% endhighlight %}
(Forgive me, have't written java code in a while)

This can be a little hard to read if you need to put a bunch of thse everytime you're getting an
enum. Let's look at the equivalent Scala code:

{% highlight scala %}

result = exVariable match {
	case enumerationType.1 => // do something
	case enumerationType.2 => // do something
	case enumerationType.3 => // do something
	case Unknown(exVariable) => // do something
}

{% endhighlight %}

(with a simple matching). If we want to also return exception, we can use Trys: 

{% highlight scala %}
// I'm assuming we defined the enum using case objects

result = exVariable match {
	case enumerationType.1 => Success(enumerationType.1)
	case enumerationType.2 => Success(enumerationType.2)
	case enumerationType.3 => Success(enumerationType.3)
	case Unknown(exVariable) => Failure(IllegalArgumentException("some message here")
}

{% endhighlight %}

A Try is Scala's answer of the try-catch idiom in java (try catches are still available in
Scala, but is is easier to read and reason about a Try). Java's `valueOf` uses an underlying map
for its performance, which in the case of really big enums makes a difference. However if you're
dealing with enums that big a different abstraction might better encapsulate the problem.

I hope I shed light on a specific difference of Java vs Scala. Granted, this does make 
justice to either language as a whole, but hopefully it sparks curiosity.

[scala_language]: https://www.scala-lang.org/
[play]: https://www.playframework.com/
[sbt]: http://www.scala-sbt.org/
[exampleSOAns]: https://stackoverflow.com/a/4936872
