---
qip: 2
title: Deterministic Slot Leadership Without a VRF
status: Final
type: Core
category: Core
author: Quantova Inc
created: 2026-05-31
---

# QIP-2: Deterministic Slot Leadership Without a VRF

## Abstract

Quantova removes Verifiable Random Function (VRF) based leader election from consensus and
replaces it with deterministic, round-robin slot leadership. Randomness the protocol needs
elsewhere is sourced from post-quantum primitives rather than from an elliptic-curve VRF. This is
a foundational design decision, recorded here as a Final Core specification.

## Motivation

Classical BABE selects block authors with a VRF, whose unpredictability rests on classical
public-key cryptography. No widely accepted post-quantum VRF exists today. Rather than ship a
primitive with an unproven quantum-security story, Quantova removes VRF-based leader election
entirely, eliminating an elliptic-curve dependency from the hot path of consensus and from the
randomness path.

## Specification

- Slot assignment is round-robin, deterministic, and predictable. The eligible author for each
  slot is fixed by the active validator order elected through NPoS:

  ```
  slot_author(slot) = active_validators[ slot mod len(active_validators) ]
  ```

- Block production is slot-based. Because leadership is deterministic, peers verify that the
  author was the legitimate validator for that slot without checking a randomized eligibility
  proof. Target block time is ~2.5 s.
- Randomness needed elsewhere is sourced from Quantova's post-quantum primitives.
- Validator authority and finality-vote keys are post-quantum (Falcon / FN-DSA).

## Rationale

A VRF's unpredictability is purchased with classical public-key cryptography — exactly what
Shor's algorithm targets on a fault-tolerant quantum computer. Deterministic leadership has no
secret to recover in the leader-election step, so there is nothing there for Shor's algorithm to
break. Predictable leadership is an acceptable trade for removing that quantum exposure, given
the network's institutional-settlement focus.

## Backwards Compatibility

Quantova does not inherit a classical BABE/VRF deployment; this is the design from genesis. For
developers migrating mental models from Substrate: validator authority keys are Falcon (not
classical EC), and slot leadership is deterministic (not VRF-based).

## Security Considerations

The change strengthens the post-quantum posture by removing an elliptic-curve primitive from
consensus. The known trade-off is that block authors are predictable per slot; this is mitigated
by NPoS validator-set protections and by post-quantum authority keys at the finality layer. A
post-quantum VRF with an accepted security proof is tracked as future work and, if it matures,
could be proposed in a later Core QIP.

## Reference Implementation

The consensus behavior is specified in the
[`consensus-specs`](https://github.com/Quantova/consensus-specs) repository.

## Copyright

© 2026 Quantova Inc. See [LICENSE.md](../LICENSE.md).
