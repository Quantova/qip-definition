---
qip: <assigned by an editor>
title: <a few words, not a sentence>
status: Draft
type: <Core | Networking | Interface | QRC | Meta | Informational>
category: <Core | Networking | Interface | QRC — omit for Meta/Informational>
author: <Name <email@example.com>, ...>
created: <YYYY-MM-DD>
requires: <optional; QIP numbers this depends on>
---

> Copy this file to `proposals/qip-N.md` (an editor assigns `N`). Fill in the preamble and every
> section below, then delete this note and any `<…>` guidance. Remove `category` for
> Meta/Informational. See [contributing](contributing.md).

## Abstract

A short (~200-word) technical summary of the proposal.

## Motivation

The problem this solves and why it is needed now. For a pre-mainnet network, state whether this
is required for mainnet or is a post-mainnet improvement.

## Specification

The precise, implementation-independent specification — enough detail for an independent
implementer. For Core QIPs, describe consensus, validity-rule, or cryptographic changes exactly,
and name the affected components (consensus, QVM, networking, RPC).

## Rationale

Design decisions, alternatives considered, and trade-offs. Reference related work.

## Backwards Compatibility

Incompatibilities and how they are handled. State whether the change is a forkless runtime
upgrade or requires a coordinated network upgrade.

## Security Considerations

Required. State whether this introduces, removes, or modifies any cryptographic assumption, and
whether it touches the randomness path, validator authority keys, or account signatures. For a
post-quantum chain this section is load-bearing, not boilerplate.

## Reference Implementation

Link to a reference implementation or test vectors where applicable (required for Core and QRC
before `Final`).

## Copyright

© 2026 Quantova Inc. See `LICENSE.md`.
