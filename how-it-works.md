---
title: How It Works
permalink: /how-it-works/
description: The thread, the protected payload, and what each side records.
---
<!-- DRAFT for Josh. Claims trace to RCP-57 and to the reference implementation
     in reference/src. The purity rule and the Note-for-verbless-state rule are
     both enforced in code, not just described. -->
# How It Works

## The Thread

A listing is the root. An offer replies to it. A counter replies to the offer. Every turn names the turn it answers, so the order is in the data rather than in a timestamp.

That has three consequences worth stating plainly.

Earlier turns are never edited. A counter does not modify the offer it answers, it adds to the thread.

Both sides read the same order, because the order comes from what each turn replies to rather than from when it arrived.

An ended negotiation stays ended. Acceptance, rejection and withdrawal close it, and nothing appends to it afterward.

## Accepting Adds No Turn

Acknowledging, accepting, rejecting and withdrawing do not create a submission. A submission exists when terms change. An acceptance names the submission it accepts, which in a countered negotiation is the most recent counter rather than the original offer.

## Each Side Records Its Own Status

The submitting side and the receiving side each keep their own status, and each records only what it observed. A difference between the two is expected rather than an error. The current status sits on the highest numbered turn.

## Three Proposed Resources

**Offer** is one negotiation on one listing.

**OfferSubmission** is one turn, carrying the terms.

**OfferPropertyGroup** is the subject property.

All three are additive. No existing resource changes.

## What Travels, and What Does Not

The message on the wire is ordinary ActivityPub. It carries the actor, the time, the turn it replies to, and a link. It does not carry a price, a buyer or a financing arrangement. Those sit behind a protected link, and reading them needs permission granted in advance.

This is also why the message uses standard Activity Streams vocabulary and nothing else. An implementation must not extend the format with its own terms, because a term one system invents is a term the other cannot read. The playground enforces that rule rather than trusting it: an activity carrying any term outside the vocabulary is refused before it can be sent.

## The Same Shape Fits More Than Offers

Offers needed new resources because the Dictionary had none. Showings and open houses already have theirs. The same threaded pattern applies to both with no new data elements, which is the reason to care about this beyond offers.
