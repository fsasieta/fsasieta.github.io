---
layout: post
title: "Buying and setting up a custom domain on github pages"
date: 2016-09-10 19:50:00
comments: true
category: computer science
---

What is promised is due, and so here is a quick guide as to how to link a custom domain to
your newly created github pages website.

## First things first

Have you bought a domain name? There are many places to buy one. I got mine from [godaddy](
www.godaddy.com), but there is also [domain.com](www.domain.com) (great if you have one of those
free domain cards given at any hackathon), [register.com](www.register.com), [domains.google](
domains.google), etc. the list is endless. The vendor will then make you fill a form to get
your domain registered with ICANN (Internet Corporation for Assigned Names and Numbers), which is
the entity that actually manages registration. By the way, you do not actually own the domain, 
you are actually "leasing" it for a determined period of time. For a personal website this is not 
that important, but if you ever have a company, chances are you want to keep the domain you 
bought from the start, or [if you're google, buy it anyway](http://www.marketwatch.com
/story/someone-paid-12-for-the-googlecom-domain-heres-how-google-got-it-back-2016-01-31). On
another note, you can find godaddy domain coupons in Groupon.

## Setting up github

After, you need to let github know that you've bought a domain, so head over to your github
pages sit repository and find the `settings` button. Under custom domain, add your domain's name.
So you should write something like `yourDomainName.com`.

After you're don with that, head to your webpage files in your computer. Specifically open the
`config.yml` file and change the value of your `url` variable to be the same as your domain. As
an example, I have mine as `url: http://francosasieta.com `. This is done so that it is easier
 to organize files later on (I think, someone correct me if I'm wrong).

## Setting up your domain routing.

Almost done! Now that we have bought the domain and told github that we will be using the domain,
We actually have to tell the domain registrar (company that you bought the domain from) to 
forward the traffic from our site to our github hosted site. Note: this doesnt mean that when 
you type `www.youDomainName.com` you'll get `youGithubUsername.github.io` in your browser. It 
simply means that you will see you domain name *instead* of your github pages page. 

As a first step, login to the account that you created with your domain registrar; I used godaddy,
so I just log into the godaddy webpage. After, go to your domasn's DNS management page. The first
step is to setup something called and ANAME. This basically tells your domain company what server
you are hosting your webpage in. After setting those up you should have something like:

[ANAME example]( {{site.url}}/assets/Screen Shot 2016-09-09 at 9.18.06 PM.png )

The `@` simply means "from the host (domain registrar) company". The IP addresses in the picture
are the ones used by github for github pages. The next thing to do is set up a [CNAME][cname] 
record. You should set up one from `youUsername.github.io` to your domain name (without the
".com" and another from `www` to `youUsername.github.io`.

[CNAME example]( {{site.url}}/assets/Screen Shot 2016-09-10 at 2.40.10 PM.png)


After that it should be done! now you only have to wait some time for the changes to
propagate through the network (they ask about 1 to two days but I only waited for 1 to 2 hours)
Thanks for reading!.



[cname]: https://en.wikipedia.org/wiki/CNAME_record
