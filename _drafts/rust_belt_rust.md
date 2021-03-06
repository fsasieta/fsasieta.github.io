---
layout: post
title: "Rust Belt Rust"
date: 2017-10-28 11:00:00
comments: true
category: conferences
---

# Discovering Rust

In the past couple of days I was fortunate to attend the [Rust Belt Rust][rust_belt_rust] 
conference. 
I have been an avid reader of [Y Combinator's Hacker News][hackernews] for about a
year now, and all through that time I had been hearing about this new systems programming 
language called [Rust][rust], that was considered to be a strong contender to replace C++ 
(and maybe C) as the new systems programming language of choice. I was very curious about this, 
since I've been incresingly been interested in the areas of operating systems, ubiquitous systems
and compilers. At some point while reading the comments of one of these articles, I came across
a comment that mentioned an upcoming conference, and after looking at the web page I was amazed
to find out they also had open applications for people who were from underepresented groups in
the technology industry. Since I hadn't seen many mexicans like myself, I thought I'd give it a
try. Two weeks later, I was ecstatic to find out that I had received the scholarhsip! Not only
did it covered the flight, but it also covered my lodging at a nearby hotel, and it offered me a
spot in the Rustbrige workshop, which would be an all-day introduction to the language. Super 
awesome!

# Getting to the conference and Day 1

I arrived on Wednesday evening to my hotel, and Thursday morning I headed for the conference.
After an introduction, everyone headed to their respective workshops. I headed to the Rustbridge
one, where we learned about syntax, how Rust implements the functional paradigm and
tried to test our knowledge by coding some exercises.Not only wasthe workshop lead by awesome 
instructors, we even had a member of the Rust Core team there to 
answer any and all questions that we had. Coming from Scala, there was a lot of crossover
concepts wise, but a lot of surprising things as well ('println!' a macro instead of a function
anyone?). For lunch we split into groups, and adventured into the city. After, we decided to keep
learning a bit more by taking on building a simple web server in rust. And when I say simple, I
mean simple (less than 30 lines long!). The instructors had made a framework heavily inspired by
the NodeJs example and we were able to have a website up and running in no time. This was really
exciting as, I had in some previous era implemented a simple C server and man was that not very
straightforward to beginners at all. Thank you Ashley and Steve!

[Swag given at the conference, cute crab!]( {{site.url}}/assets/rustbelt_scarf_minified.jpg )

After the end of the day, everyone went to a Facebook sponsored beer/food dinner gathering. 
You have to give it to large tech companies, they really try to recruit everyone qualified, 
everywhere. 

# Day 2

Day 2 was focused exclusively on presentations. I got to listen to recent developments of the
language, whose focus group on ergonomics and the current "Impl" period. The Impl period is the
section of the year where the rust language team stops any discussion on features of the language
and purely concentrates on the implementation of said features. So avoids the talking the talk
and walks the walk on everything that had been discussed during the previous months.
Interestingly to me was finding out the design of the language happened through [RFC][rfc]
documents specific to the [language](https://github.com/rust-lang/rfcs). 

Of particular interest to me were the development of Rust IDE support for the open-source IDE
KDevelop, the lightning talk on Rust running on bare metal, and the motivational talk about 
becoming a contributor. I would be interested in trying my luck on 
[using Rust for to make an operating system][rust_embedded] since it seems it might be more
approachable than C or C++. But we'll see what happens, and if I even have time to do that.
On another note, I absolutely loved Chris Krycho's talk about becoming a contributor. 
The sense of empowerment had after seeing how one of the most well known [voices][podcast] of the
language and its ecosystem had started by just fixing a typo as its first contribution is
something you don't hear everyday. In fact I think the "getting started in X project" stories 
should be something more widely discussed, since contributing to a large project 
can be daunting to many people. 

Overall, this was a great experience and I'm very happy I was able to be a part of it. I honestly
look forward in being a contributor to the Rust project, since it shows much promise.

Rustbridge group photo (our hands are crab claws; Rust adopted the crab as its mascot):

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">thanks so much for learning with us today, <a href="https://twitter.com/rustbeltrust?ref_src=twsrc%5Etfw">@rustbeltrust</a> columbus! you are all amazing ✨✨✨✨ <a href="https://t.co/FoyyJHBpyZ">pic.twitter.com/FoyyJHBpyZ</a></p>&mdash; RustBridge (@RustBridge) <a href="https://twitter.com/RustBridge/status/923671105755369473?ref_src=twsrc%5Etfw">October 26, 2017</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


[rust_belt_rust]: https://www.rust-belt-rust.com
[hackernews]: https://news.ycombinator.com/news
[rust]: https://www.rust-lang.org/en-US/
[rfc]: https://en.wikipedia.org/wiki/Request_for_Comments
[embedded_rust]: https://users.rust-lang.org/t/rust-for-embedded-development-where-we-are-and-whats-missing/10861
[podcast]: http://www.newrustacean.com/
