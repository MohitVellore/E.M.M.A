# E.M.M.A
_A physics‑inspired research project in active development._

## Project Overview
E.M.M.A. ingests a **100 ms BTC/USDT depth stream** and tests two rival quoting
engines on exactly the same order‑book tape:

| Engine | Core idea | What we measure |
|--------|-----------|-----------------|
| **Avellaneda‑Stoikov (A‑S)** | Uses closed‑form math to widen/narrow the spread based on current inventory and a Poisson fill model. | Acts as the industry benchmark for spread capture and risk. |
| **Minimum‑Energy Optimiser (MEO)** | Treats inventory as “potential energy.”  It chooses bid/ask distances (δ) that minimise the cumulative **action integral**  ∫ L(q, δ) dt, where L = inventory penalty + quote energy – spread reward. | Goal: cut inventory variance ≥ 20 % **without** lowering net spread P&L. |

Both engines read the same real‑time volatility estimate σ(t) and operate
under identical latency, fee, and position‑limit constraints, so any
performance gap is attributable to the control rule—not the plumbing.

## Current Milestones
| Status | Deliverable | Target date |
| ------ | ----------- | ----------- |
| ✅ setup | Repo, Overleaf sync, folder skeleton | *19/04/25* |
| 🔄 WIP | Live WebSocket → TimescaleDB pipeline | *08/06/25* |
| ⏳ next | Implement Avellaneda‑Stoikov baseline | *06/07/25* |
| ⏳ next | Derive & code minimum‑energy policy | *27/07/25* |
| ⏳ next | Replay simulator + results dashboard | *07/09/25* |

> **Note:** The project is a work‑in‑progress; done as a side project.

## Background Reading
1. **Avellaneda, M. & Stoikov, S. (2008)** - High‑frequency trading in a limit‑order book market.
2. **Manhire, S. (2022)** - Using the Principle of Least Action to Determine Probabilities of Asset‑Price Displacements.
