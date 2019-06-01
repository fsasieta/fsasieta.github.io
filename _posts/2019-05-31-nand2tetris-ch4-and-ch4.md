---
layout: post
title: "Nand2Tetris, machine language and RAM"
date: 2019-05-31 23:55:00
comments: true
category: learning
---


I'm having a bad habit of writing these posts late at night, right at the end of the month. Oh well,
whatever works right?

This month I was even more productive, and was able to make further progress in the Nand2Tetris
course/book. In chapter 3 I implemented a basic Random Access Memory hardware addressing
architecture, which was fun. One part of the assignment was to make a program counter as well, which
turned out to be the hardest section of the chapter. There were lots of nested mutexes to be found.

In chapter 4 things got more interesting. We finally took a step back from dealing with hardware
directly (verilog really but still counts in my mind) and we learned how a computer conceptually
structured, from the basic abstractions of Memory, Processor and Registers. We then got introduced
to the book's own computer structure and its addressing and command scheme. The book followed by introducing
how this scheme was in fact directly made up of only 1's and 0's and were the instructions the
computer executed. 

Of course the book saves the reader from anxiety (me) and continues explaining how we are not
expected to write in machine language directly, but rather use an intermediate language called
assembly that is then translated to machine language by a program called an assembler, which is
supplied with the cpu emulator. All machines have their own flavor of assembly, ours included.

All of this brought memories to my OS class in college. I knew tangentially of assembly but I
couldn't say that I had written any flavor of it extensively, if at all. Interestingly, I was able
to make a quick connection between book assembly for funsies and real assembly flavors, all thanks
to reading the Spring edition of [2600 Magazine](https://www.2600.com). It turns out that when you
have the mental model of a computer is it not terribly hard to read other types of assembly
languages written for other architectures, since the mental model is the same. Consider for example
a few sample lines of SMALI code of the [Dalvik Java VM](https://en.wikipedia.org/wiki/Dalvik_(software)):


{% highlight java %}

invoke-virtual {p0}, Lcom/headsup/model/Deck;->getSkul()Ljava/lang/String

move-result-object v0

invoke-virtual {v0}, Ljava/lang/String;->isEmpty()z

move-result v0

{% endhighlight %}

Before reading the chapter, complete gibberish. After, while still not understanding it fully I can
somewhat get a sense of where the code is going. The commands `move-result` and `move-result-object`
move some information toa particular register, whether it's an entire object or a value and the
`invoke-virtual` does some operation. Amazing that I am able to put the things I'm learning into
practice instantly to learn something interesting in other domains. Maybe not so amazing, but I did
find this very interesting.

On another note, 2600 magazine is dope, definitely check it out if you haven't. Lots of interesting
reading stories, not just hardcore technical. That is all for today, thanks for reading!

