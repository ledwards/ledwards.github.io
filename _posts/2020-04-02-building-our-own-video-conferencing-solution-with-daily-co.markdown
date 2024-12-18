---
layout: post
title:  "Building our own video conferencing solution with daily.co"
date:   2020-04-02 12:00:00 -0800
categories: software
---

During lockdown, I decided to not spend all of my free time playing video games, and catch up on some programming instead. So a couple weeks ago, in between about 4-5 meetings, I put together a drop-in replacement for Zoom using the [daily.co](https://daily.co) API.

Presenting: [Meet](https://github.com/rootvc/meet). *Note: I first wrote this post before Google merged their several video conferencing solutions into one and named it Google Meet. Oops!*

Pull requests and Issues welcome. I've abstracted away all the Root-specific code, so you can now deploy your own instance of Meet to your own Netlify account with one click from the GitHub [README](https://github.com/rootvc/meet/blob/master/README.md) and a few short configuration steps.

We've now completely switched over to this side-project at Root. If you video chat with us any time in the future, you'll be using Meet.

## Why?
* I wanted to use more custom theming, and better custom domain/routing than Zoom allows.
* No application to download - video happens natively in the browser.
* I can actually make it load much, much faster than Zoom, using the magic of a static site builder and [Netlify](https://netlify.com).
* I [open-sourced](https://github.com/rootvc/meet) it to demonstrate how easy it is to build an app on daily.co. That's what we in the business call "content marketing."
* I have a number of [enhancements](https://github.com/rootvc/meet/issues) I want to make, like integrating with Google Calendar, SMS, and a few other things. (Maybe my reMarkable tablet?)
* I can 💫 Add Value 💫 by giving some feedback to the team, and I can speak a bit more credibly to daily.co's next investors about the product. (even More Value Add!)
* But most importantly, programming is fun, and so is dogfooding.

All that was reason enough, but since building Meet, as The Dude would say, [new shit has come to light](https://www.youtube.com/watch?v=gbIv7W7rhx4). It turns out Zoom is a privacy nightmare.

* According to their [privacy policy](https://zoom.us/privacy), [Zoom can record all of your conversations and use them for all kinds of purposes](https://twitter.com/terronk/status/1242893793591832576).
* [New York's Attorney General is looking into privacy violations now.](https://www.nytimes.com/2020/03/30/technology/new-york-attorney-general-zoom-privacy.html)
* [And most of the Zoom engineering team is located in China](https://twitter.com/jacobhelberg/status/1245101510272245760?s=20), putting them inside the surveillance of the state.

Daily.co uses a peer-to-peer architecture and end-to-end encryption. They offer a [HIPAA-compliant product](https://www.daily.co/blog/announcing-hipaa-compliance-for-the-daily-co-video-chat-api) to protect personal health information (PHI), being used by several telemedicine customers today. You can read their [privacy policy](https://www.daily.co/privacy) yourself.

How it works
Code here: [https://github.com/rootvc/meet]

Meet is a React app built on [create-react-app](https://create-react-app.dev/). Most of the relevant code for video conferencing is in `/src/Room.js`, which loads the daily.co iframe and builds the HTML/CSS around the iframe.

The [daily.co Javascript API](https://docs.daily.co/reference) is dead simple:

{% highlight javascript %}
window.callFrame = window.DailyIframe.createFrame(
    document.getElementById("frame"), {
    showLeaveButton: true,
    iframeStyle: {
        ...
     }
});

let url = `https://${config.DAILY_SUBDOMAIN}.daily.co/${roomName}`
window.callFrame.join({ url: url });
{% endhighlight %}

Styles are defined in `/src/index.css` for the generic styles and `/src/brand.css` defines the [Root Ventures](https://root.vc) specific styles. This should make it easy to brand it yourself if you fork the repo, without messing up the basic layout.

Finally `/src/config.js` loads a config object that stores values from the environment. The [README](https://github.com/rootvc/meet/blob/master/README.md) defines what each of these variables do, but the key one is `REACT_APP_DAILY_SUBDOMAIN`.

## Hosting
This simple app uses daily.co's [front-end API](https://docs.daily.co/reference#using-the-dailyco-front-end-library) only. Note that the front-end API can't do anything that would require your secret key (as that would then be served to the client.) You'll need the [REST API](https://docs.daily.co/reference) for anything like that (e.g. creating rooms, recordings, deleting rooms, getting meeting analytics.)

So that's great. The whole app is a handful of static files, so I can host it on [Netlify](https://netlify.com), a popular static site host that serves files from the edge.

Instructions for deploying on Netlify (with CI/CD hooks) are in the [README](https://github.com/rootvc/meet/blob/master/README.md).

## Your turn
Try it yourself either by forking the repo or deploying with the Deploy to Netlify button in the [README](https://github.com/rootvc/meet/blob/master/README.md). Then just follow the 5 steps in the readme to configure Netlify, Daily, and the app itself.

Hopefully this shows you how easy it is to create an app that has video chat built in. Go ahead and make an account on [daily.co](https://daily.co).

Code here: [https://github.com/rootvc/meet](https://github.com/rootvc/meet)

*Root Ventures is an investor in [Daily], a company that provides reliable, secure video chat and screensharing via a simple one-line API. Yes, I am totally talking my book. Sorry, not sorry.*
