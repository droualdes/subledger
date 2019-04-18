---
layout: post
title: Challenges with building your own in-app accounting system
date: 2013-03-05 12:00
author: Tom Mornini
---
<img class="img-responsive" alt="money team" src="{{ "http://placehold.it/640x300?text=Missing" | relative_url }}">

Interview with Nick Giancola, Partner at <a href="http://gophilosophie.com" target="_blank">gophilosophie.com</a>.

Dan: Tell us a little about your background and what you do?

Nick: I’m a partner at philosophie. We’re a software consultancy specializing in designing and developing web applications for clients, ranging from early-stage startups to large enterprises. Personally, I’ve been building web software for the past decade.

Dan: What sorts of clients typically require ‘in-app accounting’ functionality?

Nick: Any company dealing with a large number of transactions. In my experience, mostly e-commerce companies.

Dan: What is the main reason they build ‘in-app accounting’?

Nick: Businesses tend to manage their accounting manually for as long as possible, pulling CSV data to run reports and manage accounts offline. However, as a business scales, whether it be more transactions between users or more partners becoming involved, really any substantial increase in volume, you’re faced with the decision to either hire more accountants to manage this higher volume or invest in automating the accounting-related tasks and build in-app accounting functionality.

Dan: What is ‘in-app accounting’? What does it do?

Nick: Essentially it manages the effect of transactions on involved accounts. For example, as an order is placed, ‘in-app accounting’ may be responsible for dividing up that order among multiple partner accounts based on a predetermined, or sometimes variable, revenue share agreement. It should also be able to generate reports on that data in ways that are useful for the accounting and business teams as well as investors.

Dan: How do you do this today? How much developer time does it take?

Nick: Most of the serious in-app accounting implementations I’ve seen and worked on have been custom built from the ground up. The time and resources required vary wildly depending on the needs of each business… I’d say on average you should be prepared to invest 2 months and 1 or 2 developers to get it done right.

Dan: What are the ongoing maintenance requirements for a DIY accounting solution like this?

Nick: Pretty much the same as any custom software: Server maintenance, constantly increasing data storage requirements, developer resources to handle bug fixes and technical debt like that…

Dan: We’ve talked about using Subledger instead of building your own solution, what do you see the benefits of this approach being?

Nick: Implementing a pre-built solution like Subledger could save your entire team a whole lot of time. Building custom solutions requires a lot of coordination and commitment from the whole team (not just the devs) to ensure the resulting system performs as needed. With a service like Subledger that could meet the needs of the accounting team and handle the financial subtleties of the business, you can build, launch, and iterate your product faster—saving your resources to focus on what really matters: the user.
