---
layout: post
date:   2025-08-06
categories: housekeeping
---

## What is your technology estate? 
### Before you can secure something, you need to know what you've got, and how important it is &mdash; to the business, to customers, to you. 

### This post is all about building out that inventory, and a helpful tip (towards the end) of comparing your findings with finance records.

The Asset Register (or if we're old school CMDB &mdash; configuration management database) will be helpful for a lot of other purposes too &mdash; it's worth getting right, but also updating regularly (or automatically).


For those coming to this new, you'll probably want to start with a paper and pen, ipad, or spreadsheet. In a lot of cases, you **don't** want to start buying an inventory system (but if you've got one, hopefully it doesn't suck). 

Here are some highlevel categories to think about:
 - laptops, pcs
 - phones (company issued **and** [BYOD](/glossary/#byod))
 - tablets
 - Software as a Service (SaaS)
 - Platforms as a Service (PaaS)
 - Infrastructure as a Service (IaaS)
 - Cloud Service Providers (and which products)
 - Offices
 - Datacenters
 - People (current, future)
 - People (leavers, movers)
 - Paper records (permanent)
 - Paper records (transient)

 This will most likely give you plenty to work with, so don't worry *too* much about freemium things or shadow IT. We'll come back to those in a bit.

This list now gives us something we can work with. We're going to want to collect some information, and depending on the approach to take, might want to make some config changes as we go… but remember, `we're human focussed`, so it's vital to communicate.

#### Laptops, pcs, tablets, phones

My checklist for laptops at this stage goes something like:
  - a description or asset ID
    - > I'm a convert to using device serial numbers
    - they're more permanent/less tacky than stickers
  - age of device (i.e. will it need replacing soon?)
  - operating system and version (is it supported?)
  - disk encryption status
  - primary user(s) (link back to your org-chart)
    - its use type (data manipulation, email/web/slack, dev, hr, general purpose etc)
  - if it's standalone or managed

#### SaaS
For SaaS I want to know:
 - does it support MFA, and is MFA turned on for everyone (no exceptions)
 - does it work with single-sign on:
   - **at all**
   - via an upgrade or add-on
   - only a handful of SSO providers
- if a lot of old users are still enabled in the system (this is an easy thing to do then and there &mdash; tidy-up)[^1]
- are accounts shared / does everyone have their own login [^2].
- what types of data are held: are they 
  - `auth(orization|entication)` data
  - payments data
  - personal data
  - special category data
  - health data
  - card(holder) data
  - corporate secrets
  - customer data
- if there's a contract stored anywhere, or if it's online 
- where the data's stored (data residency)
- who are the responsible people for **managing**:
  - the SaaS itself (the system owner)
  - the users (system admin)
  - the data (data owner)
  - contracts (relationship owner)
  - any integrations/data reuse (devs, third-party vendors)
  - performance (vendor/incident manager)
- what the single points of failure are/might be (hypotheses to (dis)prove)
- how critical it is and to whom

As you can see, this is getting to be quite a big spreadsheet. 

### Critical or not?

At first, you'll probably find that every single system is `critical` to someone. 

A good way to measure this is to understand:
 -  what business process it is involved in, 
 - how many people can undertake that process, 
 - when the playbook was last reviewed
 - the business continuity scenarios
 - the date of the last backup being verified
 - the *"if it's not available for six hours, who will notice"* test.

Suddently, thrrough asking these questions, you'll be able to identify if it's that critical or not.

 (more on this in a future post on how I map tools to processes, to business functions, to Business Impact Assessments, to Desktop Exercises and continual improvement)

 Anyhow, we got distracted *already*.

 

 

There is a nice benefit to this &mdash; at the end there will be a list of things, and with review, you might be able to highlight duplication of systems, similar things doing the same task, user-seat license savings, and some possible economies of scale.

> I like comparing my list against finance records to work out what's actually being paid for. More often than not, a year of spend-data will show these including the annual subscriptions, the quarterly bills, the monthly spends. With a bit of luck, these line-item costs will exist in a spreadsheet or seven already. 


[^1]: we don't want people who no longer need access having access, so if they don't have a need, remove them. Don't delay further. I typically don't notify people about this in advance, if they need it, they'll ask for it (usually loudly).

[^2]: this is so we can trace actions to an individual, not have a guessing game.