---
qip: 1
title: QIP Purpose and Guidelines
status: Living
type: Meta
author: Quantova Inc
created: 2026-05-31
---

# QIP-1: QIP Purpose and Guidelines

## What is a QIP?

A **Quantova Improvement Proposal (QIP)** is a design document that provides information to the
Quantova community or describes a new feature, protocol change, or architectural standard. QIPs
are the primary mechanism for proposing, documenting, and reviewing protocol evolution in a
transparent and auditable manner. They document **what** is proposed and **why**, not **how** it
is deployed.

QIPs are maintained as text files in this versioned repository, so their revision history is the
historical record of each proposal.

## Types and categories

Core · Networking · Interface · QRC · Meta · Informational. Technical types carry a matching
category. Definitions are in [types and categories](../process/types-and-categories.md).

## Status lifecycle

`Idea → Draft → Review → Last Call → Accepted → Final`, with `Living`, `Deferred`, `Rejected`,
and `Withdrawn`. Status reflects review and agreement, not deployment. See
[lifecycle](../process/lifecycle.md).

## Required structure

Every QIP includes, unless explicitly justified: a preamble (qip, title, status, type, category,
author, created), Abstract, Motivation, Specification, Rationale, Backwards Compatibility,
Security Considerations, and a Reference Implementation where applicable. The
[template](../process/qip-template.md) lays this out.

## Process

1. Discuss the idea publicly before drafting.
2. Draft using the template and open a pull request.
3. An editor checks formatting and metadata and assigns a number.
4. The QIP advances through Review and Last Call as consensus forms.
5. Core proposals that are Accepted are scheduled into a network upgrade and become Final once
   the specification is agreed; activation is a separate governance step.

Full contribution detail is in [contributing](../process/contributing.md).

## Scope and authority

A QIP defines design intent and specification. It does not, by itself, modify live network
behavior, enforce implementation, replace governance, or guarantee activation. Final authority
for protocol changes remains with Quantova governance and canonical network deployment. Quantova
has no superuser or emergency key.

## QIP editors

Editors handle the administrative and editorial parts of the process — assigning numbers,
checking structure and formatting, and merging. Editors do not pass judgment on a proposal's
merits.

## Assets

Images and diagrams for a QIP live under `assets/qip-N/` and are referenced relatively, e.g.
`../assets/qip-1/diagram.png`.

## History

This process is adapted from the Ethereum Improvement Proposal process (EIP-1), which derives
from Bitcoin's BIP-0001 and Python's PEP-0001, tailored to Quantova's post-quantum, pre-mainnet
context.

## Copyright

© 2026 Quantova Inc. See [LICENSE.md](../LICENSE.md).
