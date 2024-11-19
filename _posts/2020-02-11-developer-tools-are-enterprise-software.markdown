---
layout: post
title:  "Developer tools are consumer software"
date:   2020-02-11 12:00:00 -0800
categories: vc
---

Last week I wrote about how [developer tools are consumer software](/developer-tools-are-consumer-software), but there are also obvious ways in which they are enterprise software. Since this is more or less the traditional way to think about (and value) developer tools companies, I won’t belabor it, but there are a few interesting points to think about.

Consumer-first developer tools companies tend to shift to enterprise after product-market fit. Which is to say that once developers love a tool and bring it to work (the consumer bottoms-up adoption approach,) enterprises often need enterprise features — security, permissioning, on-premise, customer support, services-heavy integrations, fixed contracts and site licenses. A developer tools company that focuses on these could be said to be an enterprise company.

And in many ways, the description works. A company at this stage might hire an inside sales team. They probably have a VP of Sales. Their company milestones might be related, ARR or MRR. They may keep a close eye on monthly churn and cohort analysis to understand the health of the business.

That’s not at all surprising — I think the enterprise framing is the conventional way to think about developer tools companies. But one thing worth talking about is how market segmentation for a developer tools company is unique.

[In Startups Should Be Deer Hunters](https://bothsidesofthetable.com/most-startups-should-be-deer-hunters-7fdecf58f4f6), Mark Suster makes the argument that there are three basic segmentations of an enterprise company — startups and other small business (rabbits), SMBs (deer,) and huge companies (elephants.) You often see this segmentation in the board or pitch decks of any mature enterprise company (but with less hunting metaphors — I like the hunting metaphors.) You often find the top of that scale represented as Fortune 500, or Fortune 100, or Fortune 500, or FTSE 1000, usually whichever makes the company look more favorable. The bottom end might be personified (and oversimplified) as either YC startups or mom-and-pop.

But this landscape looks a bit different to a developer tools company with an enterprise strategy.

## Fortune X
To grossly stereotype the Fortune 50/100/500/1000, these are large, “legacy,” cash rich businesses who in many cases have serious tech FOMO. Many of these have a core competency outside of software, or tech in general, and have done well by excelling in that area. Many Silicon Valley startups falsely assume these companies don’t innovate, and don’t care about trends in software development. That’s a tempting position to take, but it’s wrong. More on that later. The important takeaway for this segment is that the biggest hurdle is convincing these companies that they even have the problem you’re solving, at a scale that matters at all to a multi-$B annual revenue company. This makes Fortune X likely not the right target for a seed-stage developer tools company.

But there’s a glaring categorical error in using Fortune X as a blanket customer segment for devtools.

## FAANG
Whichever silly acronym you want to use, some combinatorial set of Facebook, Amazon, Apple, Google, Netflix are now topping the Fortune 500, but they operate very differently in relation to their peers. In most of these cases, developer tools that bring a big impact have already been built internally. Rather than the pitch to FAANG being about exposing an opportunity or problem, it has to be about buy vs. build for a solution they’ve already built. This possibly makes them the worst customer for many developer tools, and in fact, many of these internal tooling teams will spin out and start new companies that bring what they’ve learned building tooling to a startup of their own.

But there are other companies that don’t top the NASDAQ with a similar profile, and they don’t have a common name to refer to them.

## Silicon Valley 100
Public companies like the ever-present Uber, Lyft, Slack, Dropbox, Square and very soon Airbnb similarly have internal tools teams, but have demonstrated a much higher propensity to buy over build than the tech companies of the decade or two prior. Tack onto this list a set of public tech and tech-forward companies that make the news a lot less often, e.g. Zoom, Stitchfix, Domo, New Relic, Twilio, Etsy — and the profile doesn’t change much. A similar set of companies exist who are big enough to have been public in a bygone era of more frequent IPOs — companies in a state which [Matt Levine](https://www.bloomberg.com/opinion/authors/ARbTQlRLRjE/matthew-s-levine) has often described as “public companies which happen to be traded privately.) At the time, he was referring to pre-IPO Uber, Lyft, etc. But today I might include Stripe, Flexport, Affirm, Brex, SpaceX, Wish, Zenefits, OpenDoor, Checkr, Chime, Juul, or really any multi-unicorn.

This set of companies belong in the same bucket, and if I were a venture analyst, I’d try harder to attach a name to these and quantify them on some long thinkpiece with 100 logos (and maybe I will,) but it doesn’t matter exactly who is on this list — and it changes often. The important takeaway is that these are the elephants of the devtools sales strategy, not the Fortune 500, or even FAANG.

I think there’s a lot to say about the implications of that, which I’ll save for another post.

## Early Startups
The rabbits of Suster’s analogy are the thousands of Silicon Valley and SV-like startups. It may be appealing to try to build a channel to them through something like YCombinator. I think that’s a fine thing to do, but view it more as a great early adopter set to build features against. Sooner or later (and likely sooner than the A,) the enterprise sales milestone needs to be revenue and/or logos. Seed stage startups will provide neither.

This makes them bad targets for an enterprise focused strategy, (but totally fine early customers of your consumer-focused, bottom-up strategy.)

## True SMBs
What most of the world means when they say SMB is the kind of business owned by a person who will ask Elizabeth Warren a question at a town hall. Targeting folks like this seems kind of absurd, but for the right kind of product, this could make a surprising amount of sense.

Fun fact: Only about 100,000 of the 4.4M software engineers in North America live in Silicon Valley. Build a useful tool for the rest, and you’ve got a big business on your hands. Of course, it seems to be the case that Silicon Valley is a tastemaker in software engineering practices. In some sense, we export programming culture in the way LA exports popular culture. More on that later?

This says nothing of the many tens of millions more who script Excel, write simple SQL queries, maintain a static webpage, or use markup in their CMS. I don’t even know if I’m excited about no-code. I just know that more people can write some code than almost everyone seems to think. There are certainly opportunities for many more tools built for that customer.

It seems obvious when you look at some companies whether it looks more like a consumer company or an enterprise company. But the reality is that most devtools companies are a hybrid. How do you know which one is right for the product you’re building? Or is it both, and if so, how much effort should you put into each strategy? How do you know when to shift tactics? More material for a future rant.
