---
title: Tools
permalink: /tools/
description: The reference implementation and the artifacts built alongside it.
---
<!-- Links point at what is in the repository today, verified against
     RESOStandards/reso-offer-management main on 2026-10-19. The reference
     implementation and the artifacts are not pushed yet, so the page says so
     rather than linking a path that does not resolve. When they land, replace
     the status lines with the links. -->
# Tools

## Reference Implementation

Offer exchange over ActivityPub, built against the proposal. It is laid out to house conventions from the start, as ESM on Node 22 with strict TypeScript and Vitest, so it drops into `reso-tools` or stands alone.

A reference implementation is a test of the specification rather than a product. Building this one found two defects in a document that had already been through a review pass the same day, and the second would have failed certification against the specification's own example.

**Status:** the activity layer works and is checked against the specification's worked examples. The server, client and certification tools are in progress, and the source is not yet in the public repository. The activity layer itself can be read in the playground source below.

## Playground

A browser **[playground](/playground/)** plays both desks of a negotiation. Its **[source](https://github.com/RESOStandards/reso-offer-management/tree/main/playground)** is a single page with no build step, and it builds every activity through the same shared Activity Streams module the ULI playground uses, so a term outside the standard vocabulary is refused rather than sent.

Nothing is saved and nothing leaves the page.

## Artifacts

A working sheet mapping the proposed resources and fields, a certification log, and two scripts that check the specification's examples against its own tables. These are not yet in the repository.

## Related

The [Unique Licensee Identifier](https://uli.reso.org) shares the same underlying pattern. Two specifications, one federated shape.
