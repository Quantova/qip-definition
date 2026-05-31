# QIP Types & Categories

Every QIP has a **type**. Technical types also carry a **category**.

## Types

| Type | Describes |
| --- | --- |
| **Core** | Consensus, block/transaction validity, or anything requiring a coordinated network upgrade — for example cryptographic-primitive changes or consensus parameters. |
| **Networking** | The peer-to-peer networking layer. |
| **Interface** | Client API/RPC specifications and standards for how applications interact with the chain (for example, the `q_` JSON-RPC namespace). |
| **QRC** | Quantova Request for Comment — application-layer standards and conventions (for example, the QRC20 token standard). |
| **Meta** | Process or governance proposals (like QIP-1). |
| **Informational** | Guidelines or information that do not propose a protocol change and require no consensus. |

## Categories

`Core`, `Networking`, `Interface`, and `QRC` QIPs set the `category` field to match their type.
`Meta` and `Informational` QIPs omit the category.

## How type affects the path

- **Core** QIPs that are `Accepted` are scheduled into a network upgrade and become `Final` once
  the specification is agreed; activation is a separate governance step.
- **QRC** standards become `Final` once the interface is stable and a reference implementation
  exists.
- **Meta** documents that govern the process (like QIP-1) are typically `Living`.

## Security Considerations apply to every type

Because Quantova is post-quantum, any QIP — not only Core — must state in its **Security
Considerations** whether it introduces, removes, or modifies a cryptographic assumption, or
touches the randomness path, validator authority keys, or account signatures. A QIP that weakens
the post-quantum posture will not reach `Final`.

See also: [lifecycle](lifecycle.md) · [template](qip-template.md).
