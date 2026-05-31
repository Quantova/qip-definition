# Roadmap

Where Quantova is and where QIPs fit. Quantova is on **testnet**, after multiple years of
protocol development, ahead of mainnet. The core architecture is built, so the active QIP set is
small by design. As the network matures, this roadmap and the QIP process track what follows.

Dates are directional, not commitments.

## Phase 1 — Testnet Hardening (current)

- [ ] Independent third-party security audits (protocol, QVM, bridges, cryptography).
- [ ] Validator onboarding at scale and long-running stability testing.
- [ ] Performance validation against throughput targets.
- [ ] Tooling and documentation maturity.

## Phase 2 — Mainnet Readiness

- [ ] Audit remediation and sign-off.
- [ ] Genesis specification finalization, including the post-quantum genesis hash.
- [ ] Validator-set bootstrapping toward the active cap (200 at maturity).
- [ ] Governance activation for forkless runtime upgrades.

## Phase 3 — Mainnet Launch

- [ ] Canonical mainnet genesis (signed releases, post-quantum genesis hash, signed runtime).
- [ ] Native QTOV in production; staking and validator rewards live.

## Phase 4 — Post-Mainnet Evolution (research-tracked)

Each item below would be proposed and reviewed as a QIP if and when it matures:

- [ ] **Post-quantum VRF research.** A PQ-VRF with an accepted security proof would allow
      revisiting randomized leader election. Tracked as future work; not in the current design.
- [ ] **Hash-function headroom.** Forkless path to SHA3-512+ if Grover margins require it.
- [ ] **Additional NIST PQ schemes** as standards evolve.
- [ ] **Expanded bridge routes** and interoperability.

## How proposals enter

Once the network is live and the community contributes, changes follow the
[QIP process](contributing.md). Until then, this repository is the record of the architecture
already built and the roadmap toward mainnet.
