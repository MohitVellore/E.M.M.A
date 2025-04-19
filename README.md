# E.M.M.A
_A physics‑inspired research project in active development._

## Project Overview
E.M.M.A. streams high‑frequency BTC/USDT limit‑order‑book data and compares  
two quoting policies:

1. **Avellaneda‑Stoikov** – industry‑standard optimal‑spread formula.  
2. **Minimum‑Energy Optimiser** – a new control rule derived from the  
   “principle of least action,” aiming to cut inventory variance without  
   sacrificing spread P&L.

## Current Milestones
| Status | Deliverable | Target date |
| ------ | ----------- | ----------- |
| ✅ setup | Repo, Overleaf sync, folder skeleton | *19/04/25* |
| 🔄 WIP | Live WebSocket → TimescaleDB pipeline | *08/06/25* |
| ⏳ next | Implement Avellaneda‑Stoikov baseline | *06/07/25* |
| ⏳ next | Derive & code minimum‑energy policy | *27/07/25* |
| ⏳ next | Replay simulator + results dashboard | *07/09/25* |

> **Note:** The project is a work‑in‑progress; done as a side project.
