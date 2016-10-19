---
layout: post
title: "Telecom Hacking"
date: 2016-10-16 12:00:00
comments: true
category: computer science
---

It seems I caught the hackathon bug! 

Yesterday was my second hackathon of the week and my third hackathon ever. 
I participated in [TADHack][tadhack], which is a global hackathon that specializes in the 
use of telecommunications technology. This means that the hacks made during the weekend had
to be somewhat related, or rather, were strongly encouraged to use a communications technology.
(or develop one!). There were several companies sponsoring the event, such as Cisco with 
[Spark][cisco_spark] and [Tropo][tropo], [hSenid][hsenid], [Matrix][matrix], [reTHINK][rethink],
 [Telestax][telestax] & Dialogic, [Canonical][canonical] (the creators of Ubuntu) with 
[snaps][snaps]  and [VoxImplant][voximplant].  It was hosted at [Covo][covo] which provided us
with an amazing venue to meet new hackers and exchange thoughts, ideas and dreams. Great spot,
great hosts, great food even! (we were fed the entire hack weekend!) 

The very first day was spent deciding what to hack. I talked and met new people discussed ideas
I had, learned new ideas and had a back and forth with many people. I honestly had not come
prepared with an idea, but had wanted to explore communications in an application. I initially 
started talking with 2 other people and then we expanded to 4 team members total. By the end of 
Friday we didn't have a set idea, nor had we started coding. At the moment I was a little
stressed about this, but in retrospect it turned out rather well.

![covo workspace]({{site.url}}/assets/covo_workspace.jpg)
The place where the hackathon was hosted

Saturday came and I was the first one to get there. It is always kind of awkward to be the only 
one in a coders competition, but it wasn't long before other people came so it turned out fine.
The competition started at 8 am so I guess I was there pretty early. At some point discussing the
our idea another team approached us and we ended up merging into an 8 person team to work on a 
novel  proximity based social application for sharing content with business enabled real time 
promotions. We called it *I'm Here*. The novel part of our application was that
any person could create groups based on location and interest, and meet with strangers that could
be interested by the idea of the group. the groups were temporary, so you would not be 
constrained to a specific geographic area. I wasn't initially convinced about the idea, but I 
ended up liking it after I saw myself using it for a specific purpose (finding a running partner)
 
I ended up working on the demo for the website of the application. We needed to use the spark API
but we decided we also needed a marketing tool (every application ever needs a website). It
served as goog practice to me since I had little experience with NodeJS and Bootstrap, and I was
able to set up a Node server to give a simple website that illustrated our concept. I must say
that before using bootstrap I had no idea front-end development could be complicated, [but now I
do][medium_js]. It was a great learning experience.

![finished webpage]({{site.url}}/assets/imhere_frontpage.png)
Finished view of the front (and only) page of the website.

![scroll of website]({{site.url}}/assets/imhere_examplescroll.png)
Example scroll of the website.

The key parts of the mobile app and the integration with the Cisco Spark API was done by other
members of the team (shoutout to Dan). and they made a really cool prototype app for it, as well
as an app demo that was used during our presentation.

Our team ended up winning first place, which I am ecstatic about. We got a cash price which will
be divided amongst the team members and some really cool swag.

Many thanks to Roy, Alex, Patrick, Travis, Roy, Milin, Preyansh and Dan for being part of the awesome team.
Many thanks to all of the organizers of the event
for letting us use this weekend to learn new technologies and let us use the incredible space.
I look forward to going to more hackathons!


EDIT: I found a link to our presentations in [youtube](https://www.youtube.com/watch?v=uDMALXgzIfc).
My team's presentation starts at minute 34.


[tadhack]:     http://tadhack.com/2016/
[cisco_spark]: https://www.ciscospark.com/ 
[tropo]:       https://www.tropo.com/
[hsenid]:	   www.hsenid.com/
[matrix]:      https://matrix.org/
[rethink]:     https://rethink-project.eu/
[telestax]:    https://telestax.com/
[canonical]:   http://www.canonical.com/
[snaps]:       http://snapcraft.io/docs/snaps/intro
[voximplant]:  https://voximplant.com/
[covo]:        www.hellocovo.com/
[medium_js]:   https://medium.com/@kitze/how-it-actually-feels-to-write-javascript-in-2016-46b5dda17bb5#.lew2uhcbe

