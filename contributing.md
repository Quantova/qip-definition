# Contributing a QIP

QIPs follow the process in [QIP-1](../proposals/qip-1.md). This page is the short version.

> **Current phase.** Quantova is on testnet ahead of mainnet, and the protocol is intentionally
> stable. Most contributions now are Informational documents, roadmap input, or proposals
> targeting post-mainnet evolution. Core changes are expected to be rare until after mainnet.

## Steps

1. **Discuss first.** Raise the idea publicly through official Quantova channels before writing.
   Ideas are discussed before they are drafted.
2. **Draft.** Copy [`qip-template.md`](qip-template.md) to `proposals/qip-N.md` (leave `N` for an
   editor) and fill in every section.
3. **Open a pull request.** Your first PR is a first draft and must meet the formatting and
   metadata rules in QIP-1.
4. **Review.** An editor checks structure, metadata, and formatting, assigns a number, and merges
   the draft. Editors handle the editorial part only — they do not judge technical merit.
5. **Advance.** The QIP moves through `Review → Last Call → Accepted → Final` as consensus forms.
   See [lifecycle](lifecycle.md).

## Rules

- One H1 per document (the title); the preamble is YAML frontmatter.
- Required preamble fields: `qip`, `title`, `status`, `type`, `author`, `created`
  (`category` for Core/Networking/Interface/QRC).
- Address **Security Considerations** explicitly, including post-quantum implications.
- Images go in `assets/qip-N/` and are referenced relatively, e.g. `../assets/qip-1/diagram.png`.

## Editorial scope

Editors correct structure, grammar, and markup, assign numbers, and merge. Endorsement or
rejection on technical merits is decided through community consensus, not by editors.
