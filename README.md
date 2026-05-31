# Quantova Improvement Proposals

This repository defines what a **Quantova Improvement Proposal (QIP)** is and how QIPs are used
within the Quantova protocol ecosystem.

A QIP is a design document that provides information to the Quantova community or describes a new
feature, protocol change, or architectural standard. QIPs are the primary mechanism for
proposing, documenting, and reviewing protocol evolution in a transparent and auditable manner.

> **Network status.** Quantova is on **testnet** ahead of mainnet. The core architecture is
> already built, so the active proposal set is intentionally small. This repository is the
> framework for protocol evolution and the public [roadmap](process/roadmap.md) toward mainnet.

---

## Start here

| Document | What it is |
| --- | --- |
| [What is a QIP](#what-is-a-qip) | The definition and scope (below). |
| [QIP-1 — Process](proposals/qip-1.md) | The governing process document. |
| [Template](process/qip-template.md) | Copy this to write a new QIP. |
| [Lifecycle](process/lifecycle.md) | The states a QIP moves through. |
| [Types & Categories](process/types-and-categories.md) | The classes of QIP. |
| [Contributing](process/contributing.md) | How to submit and review a QIP. |
| [Roadmap](process/roadmap.md) | Testnet → mainnet, and where proposals fit. |
| [Proposal index](proposals/index-of-proposals.md) | Every QIP and its status. |

---

## What Is a QIP

A Quantova Improvement Proposal (QIP) is a formal technical specification that may describe:

- Core protocol behavior
- Changes to execution semantics
- New protocol interfaces or data models
- Architectural clarifications
- Governance or process updates

QIPs are written to be implementation-independent and focus on protocol-level intent rather than
application-specific behavior.

## Goals of the QIP System

The QIP system is designed to:

- Provide a clear technical record of protocol design decisions
- Encourage open technical review and discussion
- Separate proposal from implementation
- Reduce ambiguity in protocol behavior
- Preserve long-term interpretability of the protocol

QIPs document **what** is proposed and **why**, not **how** it is deployed.

## Scope and Authority

QIPs define design intent and specification. They do not, by themselves:

- Modify live network behavior
- Enforce implementation
- Replace governance decisions
- Guarantee activation or deployment

Final authority for protocol changes remains with Quantova governance and canonical network
deployment. Quantova has no superuser or emergency key; protocol changes activate only through
on-chain governance and signed, canonical releases.

## QIP Structure

Each QIP should include the following sections unless explicitly justified. The
[template](process/qip-template.md) lays them out:

`Title` · `Author(s)` · `Status` · `Type` · `Category` · `Abstract` · `Motivation` ·
`Specification` · `Rationale` · `Backwards Compatibility` · `Security Considerations` ·
`Reference Implementation` (if applicable)

This structure keeps proposals consistent and clear. For a post-quantum chain, **Security
Considerations** is not optional boilerplate — a QIP must state whether it touches a
cryptographic assumption, the randomness path, validator authority keys, or account signatures.

## QIP Lifecycle

A QIP progresses through defined states — `Draft → Review → Accepted → Final`, with
`Deferred`, `Rejected`, and `Living` as terminal or holding states. Status reflects the
proposal's review and agreement level, **not** its deployment status. See
[lifecycle](process/lifecycle.md).

## Relationship to Other Repositories

This repository defines the concept of a QIP and hosts the proposals. Other Quantova
repositories carry the artifacts a QIP refers to:

| Repository | Role |
| --- | --- |
| [consensus-specs](https://github.com/Quantova/consensus-specs) | Normative consensus specification a Core QIP may amend. |
| [developer-content](https://github.com/Quantova/developer-content) | Developer documentation updated when a QIP reaches Final. |
| [dev-base-template](https://github.com/Quantova/dev-base-template) | Reference for QRC standards proposed as QIPs. |
| [security-documentation-repository](https://github.com/Quantova/security-documentation-repository) | Security policy referenced by Security Considerations. |

Each repository serves a distinct purpose within the framework.

## Audience

Protocol and systems engineers · contributors and reviewers · governance participants ·
auditors and institutional stakeholders.

## Links

- Website: https://quantova.org
- Developer documentation: https://quantova.org/static/pdfjs/web/viewer.html?file=/static/pdf/Gitbook-Quantova-Developer-Documentation.pdf#nameddest=cover&page=1&pagemode=bookmarks

## Copyright

© 2026 Quantova Inc. Licensed under the Business Source License 1.1 (BUSL-1.1). See
[LICENSE.md](LICENSE.md).
