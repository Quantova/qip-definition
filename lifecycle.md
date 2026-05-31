# QIP Lifecycle

A QIP moves through defined states. **Status reflects review and agreement, not deployment** — a
QIP can be `Final` (the specification is agreed and stable) before, or independently of, the
change being activated on the canonical network through governance.

```
Idea ──► Draft ──► Review ──► Last Call ──► Accepted ──► Final
                      │                          │
                      ▼                          ▼
                  Deferred                  Living (process docs)
                      │
                      ▼
                  Rejected / Withdrawn
```

| State | Meaning |
| --- | --- |
| **Idea** | A pre-draft concept discussed publicly; not yet in the repository. |
| **Draft** | Formally tracked; merged for iteration. The first state with a number. |
| **Review** | The author marks the QIP ready for peer review. |
| **Last Call** | A final review window before a decision. |
| **Accepted** | Endorsed and queued. For Core QIPs: queued for a network upgrade. |
| **Final** | The specification is agreed and stable. |
| **Living** | Continually updated, never finished (e.g. QIP-1 and process docs). |
| **Deferred** | Valid but parked; may be revived later. |
| **Rejected** | Declined after review. |
| **Withdrawn** | Retired by the author(s). |

## Final is not deployment

A `Final` Core QIP describes an agreed specification. Whether and when that change is **activated
on the canonical network** is a separate decision made through on-chain governance and signed
releases (see [Scope and Authority](../README.md#scope-and-authority)). The two are deliberately
decoupled: agreement on a design does not, by itself, change the live network.

See also: [types and categories](types-and-categories.md) · [contributing](contributing.md).
