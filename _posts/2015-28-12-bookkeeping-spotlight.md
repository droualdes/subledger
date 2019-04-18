---
layout: post
title: Bookkeeping Spotlight
date: 2013-03-03 12:00
author: Tom Mornini
---
We typically think of sales & marketing as the “beginning” of the sales funnel and the payment as the “end”. But if you look at things from the perspective of the back-office, payment/payout transactions are actually where the work begins. This post hopes to shine a little light on the bookkeeping and financial reporting part of the back-office.

### What is bookkeeping?

Financial transactions have to be accounted for in the merchant’s ERP system (aka: accounting system or general ledger) in order to produce financial reports for business management and audit purposes.<! -- more -->

<img class="img-responsive" alt="money team" src="{{ "/images/OldSchoolAccounting.jpg"| relative_url }}">

Bookkeeping is the process of structuring raw transaction data (e.g. payment gateway Excel dump) in accounting format and recording it in the ERP.

Here’s an example of a very simple transaction and it’s associated accounting entry.

Transaction: $100 purchase, where the seller takes 80% of transaction value and 20% goes to the marketplace.

<div class="code red">
<p>debit.cash(100)</p>
<p>credit.revenue(20)</p>
<p>credit.seller_accounts_payable(80)</p>
</div>

As you can see it’s not a simple copy/paste job and therein lies the art of bookkeeping. As the transaction volume increases it becomes an unwieldy task to close the books every month. Typically these three areas become real pain points at scale:

### Finance team time burn

Bookkeeping and financial reporting is a labor intensive monthly process for the finance team that scales with payment volume. The stopgap solution is to add more people to the finance department.

### Audit risk

With a semi-manual process like bookkeeping there is inherent human error risk. To mitigate this risk a lot of finance team time is spent re-checking financials to ensure that they are ready for external audit.

### Engineering time burn

At scale accounting for in-application transactions become unwieldy and the solution is typically:

— Start building some sort of automated subledger internally to automate the process or

— Implement an enterprise style ‘all in one’ billing solution like <a href="http://www.zuora.com/how-it-works/new-features/index.html" target="_blank">Zuora</a>.

Both options require significant engineering effort and distract from the business from it’s core competency.

We think the day has come where you can mash-up your payment API and Subledger to automate the payments and bookkeeping part of your back-office. [#ProgrammableCommerce](/{{ page.url}})
