---
layout: post
title: Programmable Commerce &amp; the High Velocity Back Office
date: 2013-12-18 12:00
author: Dan Murphy
---
The high velocity business model is becoming more and more common, with e-commerce platforms like <a title="Uber" href="https://www.uber.com/" target="_blank">Uber</a> processing over <a href="http://techcrunch.com/2013/12/04/leaked-uber-numbers-which-weve-confirmed-point-to-over-1b-gross-revenue-213m-revenue/" target="_blank">1M transactions per week</a>. High velocity businesses are driven by super scalable customer acquisition and product delivery channels, but the back office often relies on homegrown software, spreadsheets and boring data entry work (seriously this still happens today!).

A new wave of companies are making the high velocity back office possible by providing core back office functions via API. A few key players include:

1. <a title="Balanced Payments" href="https://www.balancedpayments.com/" target="_blank">Balanced</a>, <a title="Braintree" href="http://braintreepayments.com" target="_blank">Braintree</a>, and <a title="Stripe" href="https://stripe.com/" target="_blank">Stripe</a> handle payments.

2. <a href="https://coinbase.com/" target="_blank">Coinbase</a> for accepting Bitcoin payments.

3. <a href="http://standardtreasury.com/" target="_blank">Standard Treasury</a>, <a href="http://www.corefx.com/" target="_blank">COREFX</a>, <a href="http://www.bancbox.com/" target="_blank">Bancbox</a>, <a title="plad.io" href="https://plaid.io/" target="_blank">plaid.io</a> and more manage banking.

4. <a href="{{ site.url }}">Subledger</a> (us!) takes care of accounting.

5. Companies like <a href="https://www.lob.com/" target="_blank">Lob</a> do printing and posting.

6. <a href="http://ripple.com/" target="_blank">Ripple</a> is excellent for currency exchange.

7. <a href="https://getcardflight.com/" target="_blank">Card Flight</a> enables card present payments.

Independently, these companies handle specific pieces of the back office, but still don’t create a holistic, automated solution. However, by combining these APIs together using preconfigured commerce logic we can create a completely automated high velocity back office for the commerce application. We are calling this open, modular approach programmable commerce.

<img class="img-responsive" alt="Programmable Commerce Photo" src="{{ "/images/ProgrammableCommerce.jpg" | relative_url }}">

### An Example: How Programmable Commerce Works

Take an example from an <a title="Uber" href="https://www.uber.com/" target="_blank">Uber</a> or <a title="Uber" href="https://www.lyft.com/" target="_blank">Lyft</a> style application. There are several events required to process a transaction, and each have commerce logic associated with them:

#### Event 1: Ride Complete

Step 1: Calculate ride_charge

Step 2: Get relevant sales tax sales from sales tax API.

Step 3: Add sales tax to ride_charge

Step 4: Account for ride_charge receivable from customer and earnings payable to driver.

#### Event 2: Charge Customer Card

Step 1: Charge customer’s card for ride_charge with payment API

Step 2: If the customer’s card is successfully processed, account for ride_charge received

#### Event 3: Pay Driver (end of month)

Step 1: Payout driver for earnings during month with payment API

Step 2: Account for earnings payout made to driver

In this simple example the payments, accounting, and sales tax APIs are all working seamlessly together throughout the process.

#### What’s Next for Programmable Commerce?

Here at Subledger, we’re working on making programmable commerce easily accessible. Our newest application, Plug N’ Play, is a simple rails app you can send transaction data to and it will account for the transaction automatically using pre-configured accounting-logic.

When Plug N’ Play is ready early next year, we believe it can be tweaked to incorporate other core commerce functions such as banking, payments, and more. Our hope is this will enable developers to copy/paste an entire back-office into their application.

We’re at the beginning of a new era of programmable commerce, and there are so many great startups making it possible. We are looking forward to working with everyone to build an open and modular financial ecosystem.

Please leave your thoughts on #ProgrammableCommerce in the comments below or ping me an email on <a href="mailto:info@subledger.com">info@subledger.com</a>

If <a href="{{ site.url }}{{ page.url | relative_url }}">#programmablecommerce</a> excites you, please share with everyone  ;-)

Here’s a tweet: “How do you create a high-velocity back office? Welcome to <a href="{{ site.url }}{{ page.url | relative_url }}">#programmablecommerce</a>
