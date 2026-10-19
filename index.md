---
title: Home
permalink: /
description: A standard way for offers to travel between the systems that make and receive them, without either side giving up its own.
---
<!-- Landing page. DRAFT for Josh. Every factual claim traces to RCP-57 or to the
     reference implementation; nothing here is invented. The register follows
     uli.reso.org so the two specification sites read as one system. -->
# Offer Management

An offer is a conversation, and today it travels as forms, PDFs and email between systems that cannot speak to each other.
{:.lede}

A listing agent and a buyer's agent are usually on different platforms. An offer is written in one, sent as an attachment, and typed into another. A counter goes back the same way. Nothing connects the two sides except the people, so the record of what was offered and when lives in an inbox.

The Data Dictionary has nowhere to put any of it. There are forty three resources today and none of them is an offer. Offers appear only as two values on a field about transactions. So every system invented its own shape, and none of them agree.

## Three Things Worth Knowing

**An offer is a thread, not a record.** Each turn replies to the one before it. A counter is a new turn, earlier turns stay exactly as they were, and both sides read them in the same order.

**The terms never travel in the message.** The activity on the wire carries who, when and what it replies to. Price, buyer and financing sit behind a protected link that only an authorized party can open.

**Nothing you publish today changes.** Three new resources are proposed and no existing resource is modified.

## Where to Go Next

<ul class="routes">
  <li><a href="/how-it-works/">How It Works</a><span>The thread, the protected payload, and what each side records.</span></li>
  <li><a href="/specification/">Specification</a><span>RCP-57, as proposed on RESO Transport.</span></li>
  <li><a href="/tools/">Tools</a><span>The reference implementation and the artifacts built alongside it.</span></li>
</ul>

## Try It

A **[browser playground](/playground/)** plays both desks. Make an offer, counter it, accept or withdraw, and watch exactly what crosses the network at each turn. Nothing is saved and nothing leaves the page.
