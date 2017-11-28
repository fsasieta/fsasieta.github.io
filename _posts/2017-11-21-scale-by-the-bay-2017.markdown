---
layout: post
title: "Scale by the Bay"
date: 2017-11-28 21:00:00
comments: true
category: conferences
---

# Scale by the Bay

Last week I was fortunate to attend [Scale by the Bay](https://web.archive.org/web/20171120012950/http://scale.bythebay.io/), the premier 
Scala conference organized in San Francisco. The conference was hosted on the second floor
of the the Twitter Headquarters, taking up the entire floor. It was an amazing experience, and
I felt privileged to be one of the people in my company selected to attend. Rather than repeat 
all of the talks given (which will be posted [here](https://www.youtube.com/user/FunctionalTV/playlists) soon, if they are not
already) I will recall some of my favorite ones/the ones that I thought were the most
insightful.

The very first talk of the conference was given by Helena Edelson (who is not allowed to say
from what company she comes from) from Apple. Her talk was titled "Disorder and Tolerance in 
Distributed Systems at Scale". Being the first talk, she was tasked with giving an
overview of the conference and what possiblities there could be by handling large scale
distributed systems with hundreds of nodes. Being from a liberal arts background, it was 
interesting to hear an interdisciplinary talk in a highly technical conference, especially one 
that appealed to the solutions found in
nature by scientists. Elena appealed to nature's models of possible behaviors and strategies 
to design systems that could
withstand the extreme load of requests of modern applications (and do so in a manner that didn't
break the bank). She mentioned how fish banks worked together, birds flew in synchronized
triangles during a migration and hoped that the audience would reach more towards the scientists
who already study this. This was appealing to me for several reasons: 1) While I studied math and
computer science in college, I went to a liberal arts school, which emphasized breadth of 
knowledge and curiosity in other areas of study. 2) Scientists have been criticized for not
collaborating enough between each other and it is great to see someone advocate against the
reinvention of the wheel and really just making scientists talk more 
(see the podcast on a [TED talk](https://web.archive.org/web/20171120020218/https://www.npr.org/programs/ted-radio-hour/551030943/citizen-science) for what I mean) and 3) It was just a great talk
to start to conference with.

The next talk I will write about is one by [Adelbert Chang](https://twitter.com/adelbertchang) from Target, titled "The
Functor, Applicative, Monad talk". Coming to the conference and having but a single year of 
Scala development experience, I was a little worried most of the talks would be too advanced or 
specific and hence I wouldn't learn much either. This one was the opposite, and turned out to be
one of the most useful ones (which I see myself redirecting people to in the future). The talk 
aimed to explain some of the most important concepts in functional programming in the time
alloted for the talk (40 min) and in my opinion succeeded spectacularly at doing it. He was even
kind enough to [post the slides online](https://speakerdeck.com/adelbertc/the-functor-applicative-monad-talk). Having studied math in college, grasping what a
monad is was easy to me, but I have noticed that people without a similar background may
struggle with the concept and I learned a new approach to show what these concepts are all
about.

While I'm not building data pipelines using Spark in my day to day job, I found the talk by 
Matei Zaharia, the creator of Spark, very insightful. Matei started by explaining how software composability
had been the main driver of productivity among software engineers for a long time. He explained 
the history of Hadoop and MapReduce (which I got to use in college!) and showed us how the main
innovation with Spark was to keep everything in memory in order to speed execution and be able
to make iterative computations effectively (instead of writing the intermediate files to disk
and then process them by batches). 
The purpose of the talk was to introduce his new work like SparkSQL,
in which he showed increases in performance by treating the hardware of a computer in manner 
similar to a distributed system, avoiding unnecessary loading of data into memory when it wasn't
required. I thought approach taken was great and I'm interested in exploring similar ideas in
the future.

I will stop here and highly encourage everyone that is interested in watching some of the talks,
especially the ones put above and as many other as you can (in particular Rob Norris's talk was
great in my opinion).  Hopefully this sparked some interest in them.

[scale_by_the_bay]: "https://web.archive.org/web/20171120012950/http://scale.bythebay.io/"
[videos_of_talks]: "https://www.youtube.com/user/FunctionalTV/playlists"
[ted_podcast]: "https://web.archive.org/web/20171120020218/https://www.npr.org/programs/ted-radio-hour/551030943/citizen-science"
[adelbert_twitter]: "https://twitter.com/adelbertchang"
[slides_fp_talk]: "https://speakerdeck.com/adelbertc/the-functor-applicative-monad-talk"
