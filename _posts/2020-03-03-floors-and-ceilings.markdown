---
layout: post
title:  "Floors and ceilings"
date:   2020-03-20 12:00:00 -0800
categories: vc
---

*Which ideas in [hard software](/what-is-hard-software) can grow into big businesses? I'm going to try to answer this question (the way I see it) over a few blog posts.*

For a developer tool to be venture scale, let's say that it roughly needs to achieve $100M in high-quality (software margin) annual recurring revenue, within 10 years or so. This is a daunting task, and the rare company achieves it. But look at the NASDAQ, among top unicorns, and large acquisitions, and you'll see several examples. Stripe, Segment, GitHub, Elastic, RedHat, Pivotal, Atlassian, Stack Overflow, Twilio, New Relic, Pager Duty, 10gen, Algolia, CircleCI, Snowflake, and the list goes on...

One framework I like to think about in large developer tools opportunities is what I'm trying to call lowering the floor and raising the ceiling ([trying to make fetch happen](https://www.youtube.com/watch?v=Pubd-spHN-0).)

## Lowering the floor
Look at the history of how we've built software, and an obvious trend emerges. **What used to be hard, becomes easy, and then eventually free.**

When PayPal was being founded, according to one tale, a bank told them that credit cards would never be processed over the internet. It's funny to think about now, but PayPal had to invent a number of **hard** technologies for security, encryption, and transaction guarantees. Years later, Braintree built on innovations from PayPal to make it **easy** to integrate credit card processing with an online service. Then Stripe came along, and made a somewhat cumbersome integration five lines of code, or essentially **free** in developer time.

More broadly, you can see in the world of programming, that we are constantly building abstractions that improve productivity, and in some sense, lessen the need to understand underlying technology and difficult abstractions in all but the complicated edge cases (where of course, depth of knowledge is invaluable.) Where once, all programmers built and allocated memory for strings of characters by hand using pointers and malloc, manipulating them with handwritten functions, almost all programming languages now include powerful list comprehension methods that are teachable to new programmers quite quickly.

This is one major benefit of products that raise the floor. When we make hard things free, we not only improve productivity of our projects and teams, we open the door for a new type of software developer.

My best heuristic for a true floor lowerer is:

> Can I teach this to someone in a three month bootcamp?

Today, we've seen a movement of hard to easy in: robust mobile applications, highly interactive web applications, stable and repeatable server deployment, and integrations with all kinds of third-party services from payments with [Stripe](https://stripe.com), to text messaging with [Twilio](https://twilio.com), to real-time streaming video with [Daily](https://daily.co).

We've seen a movement from easy to free in: content management systems with [Wordpress](https://wordpress.com), e-commerce with [Shopify](https://shopify.com), static websites with [Webflow](https://webflow.com), and several early attempts at doing the same with mobile applications.

Some people say that easy or free includes AI & deep learning, but I disagree. Certainly this is true for computer vision applications, natural language processing, and other simple models. But I've seen junior developers even with computer science degrees struggle to achieve a useful quality of prediction for pose detection, or facial recognition, even using great libraries like TensorFlow, Keras, and PyTorch. In these algorithms, the model architecture, and sometimes even the data, isn't enough. The efficacy depends on model tuning that requires deep domain expertise in the fundamentals of both mathematics and computer science. Most deep learning problems are therefore somewhere between hard and easy, but will be nowhere near free until better tooling is invented.

I expect this is one area where we will see the floor raised soon. Other areas might include game development, even more movement in devops, AR & VR experiences, embedded software, and outside of pure software: CAD, hardware design, and autonomy. But I doubt we'll know it until we see it.

## Raising the ceiling
On the other end of the spectrum, we have software that pushes the boundary from **impossible** to **possible**.

The most salient example of this is machine learning. Under old programming paradigms, it was essentially impossible to imagine software that could read unbounded datasets of human handwriting. In the 1970's computer scientists proposed algorithms based on linear algebra that could do just that, and by the 2010's, hardware was good enough to implement these algorithms at large scale.

Today the boundaries of what is possible with software are moving rapidly. We are [training robotic grasping manipulators to complete arbitrary tasks](https://arxiv.org/abs/1808.00177), completely in simulation that translates to near perfect behavior in the real world. [AlphaGo](https://deepmind.com/research/case-studies/alphago-the-story-so-far) was able to beat the best Go player in the world, a task experts from the 90's predicted would take 100 years to achieve. [DeepFake](https://en.wikipedia.org/wiki/Deepfake), now [widely available](https://github.com/deepfakes/faceswap), can already fool many humans with realistic, completely fabricated video and audio. And it is improving at this task rapidly.

In all of these situations, the paradigms changed to make them possible. In simulation, we can generate training data for machine learning models that teach it faster, and sometimes cheaper, than any real world experience could. Where the computer that beat chess Grandmaster Gary Kasparov was built on complex logic, AlphaGo was built on a handful of novel learning algorithms. The generative adversarial networks behind DeepFake are even newer academic inventions, and even later became feasible on real hardware with large datasets. They all have one thing in common, which is my heuristic for software that raises the ceiling.

> Does this software let us do something we didn't think was possible before?

One place to look for new possibilities in software is advances in hardware. We've clearly seen theoretical algorithms become feasible as Moore's Law has continued over the years, and we've seen linear acceleration become the primary driver of GPU-based computation of late. But we also see that low-power processors are enabling inference, and sometimes training, at the edge, unlocking new opportunities like [fully autonomous aerial drones](https://skydio.com). The proliferation and low cost of sensors combined with novel sensor fusion algorithms is bringing powerful capabilities to even more devices.

What will constant connectivity, even more ubiquitous sensors (especially always-on cameras and microphones,) and federated learning bring? We can get crazier and think about low-cost commodity LiDAR, infrared, millimeter wave, and even sonar. Can we imagine new algorithms that can achieve the performance of complex models trained on huge datasets, that work just as well on smaller datasets, and therefore less capable compute? Which algorithms are prohibitively expensive (such as [GPT-2](https://openai.com/blog/better-language-models/),) that will become more affordable with changes in compute?

## Other criteria
Software that raises the ceiling is categorically different from software that lowers the floor. But they both have the potential to disrupt. It's not a necessary criteria for a venture-scale business, nor is it sufficient. But evidence of one of these two things can strongly indicate that there's at least opportunity. More on this later.
