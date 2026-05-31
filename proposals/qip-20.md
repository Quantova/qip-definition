---
qip: 20
title: QRC20 Fungible Token Standard
status: Final
type: QRC
category: QRC
author: Quantova Inc
created: 2026-05-31
---

# QIP-20: QRC20 Fungible Token Standard

## Abstract

QRC20 is the fungible-token standard for the Quantova Virtual Machine (QVM). It defines a common
interface for fungible tokens — balances, transfers, and approvals — and adds an optional
post-quantum permit: a gasless approval authorized by a NIST post-quantum signature and verified
on-chain through the Falcon precompile.

## Motivation

A single, interoperable fungible-token interface lets wallets, exchanges, and contracts support
any QRC20 token uniformly. Quantova adds a post-quantum permit so approvals can be authorized
off-chain with the same post-quantum keys that secure every account, without spending gas.

## Specification

A compliant QRC20 token exposes:

- **Views:** `name`, `symbol`, `decimals`, `totalSupply`, `balanceOf(account)`,
  `allowance(owner, spender)`.
- **State-changing:** `transfer(to, value)`, `approve(spender, value)`,
  `transferFrom(from, to, value)`.
- **Events:** `Transfer(from, to, value)`, `Approval(owner, spender, value)`.

**Post-quantum permit (optional).** A holder authorizes a spender by signing an approval off-chain
with their post-quantum key. The contract verifies the signature via the Falcon-verify precompile
and applies the approval, consuming no gas from the holder. A per-account monotonic **nonce**
provides replay protection.

## Rationale

Mirroring a familiar fungible-token surface maximizes tooling compatibility and lowers the
barrier for developers. The permit path reuses the chain's existing post-quantum signature
schemes rather than introducing a new primitive.

## Backwards Compatibility

QRC20 is a new application-layer standard for the QVM; it does not alter protocol consensus.
Tokens implementing only the core surface (without the permit) remain fully compliant.

## Security Considerations

The permit path depends on the Falcon precompile and correct nonce handling; implementations
must enforce nonce monotonicity to prevent signature replay. Standard fungible-token
considerations (allowance race conditions, overflow protection) apply.

## Reference Implementation

A reference QRC20 contract is provided in the
[`dev-base-template`](https://github.com/Quantova/dev-base-template) repository and the developer
documentation.

## Copyright

© 2026 Quantova Inc. See [LICENSE.md](../LICENSE.md).
