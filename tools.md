---
title: Tools
permalink: /tools/
description: The reference implementation and the artifacts built alongside it.
---
<!-- DRAFT for Josh. Links are placeholders until the repository is public and
     its path is settled. Everything described here exists on disk today. -->
# Tools

## Reference Implementation

Offer exchange over ActivityPub, built against the proposal. It is laid out to house conventions from the start, as ESM on Node 22 with strict TypeScript and Vitest, so it drops into `reso-tools` or stands alone.

A reference implementation is a test of the specification rather than a product. Building this one found two defects in a document that had already been through a review pass the same day, and the second would have failed certification against the specification's own example.

**Status:** the activity layer works and is checked against the specification's worked examples. The server, client and certification tools are in progress.

[REPOSITORY LINK]

## Playground

A browser [playground](/playground/) plays both desks of a negotiation. It builds every activity through the same shared Activity Streams module the ULI playground uses, so a term outside the standard vocabulary is refused rather than sent.

Nothing is saved and nothing leaves the page.

## Artifacts

A working sheet mapping the proposed resources and fields, a certification log, and two scripts that check the specification's examples against its own tables.

[ARTIFACT LINKS]

## Related

The [Unique Licensee Identifier](https://uli.reso.org) shares the same underlying pattern. Two specifications, one federated shape.
