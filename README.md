<h1 align="center">Vatsal Patni</h1>

<p align="center">
  Software Engineer · Kubernetes & CNCF Contributor · Competitive Programmer<br/>
  <sub>B.Tech Civil Engineering, IIT (BHU) Varanasi · Class of 2027</sub>
</p>

<p align="center">
  <a href="mailto:vatsalpatni73@gmail.com"><img src="https://img.shields.io/badge/Gmail-vatsalpatni73-D14836?style=flat&logo=gmail&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/vatsal-patni-5676482a4"><img src="https://img.shields.io/badge/LinkedIn-Vatsal%20Patni-0A66C2?style=flat&logo=linkedin&logoColor=white"/></a>
  <a href="https://codeforces.com/profile/LASTAV"><img src="https://img.shields.io/badge/Codeforces-Expert%20%7C%201623-1F8ACB?style=flat&logo=codeforces&logoColor=white"/></a>
  <a href="https://leetcode.com/vatsalpatni"><img src="https://img.shields.io/badge/LeetCode-Knight%20%7C%201911-FFA116?style=flat&logo=leetcode&logoColor=white"/></a>
</p>

---

## About

I like working deep in the stack: Kubernetes internals, distributed resource management, and concurrent C++. I'm an LFX mentee on **Koordinator** (CNCF Sandbox), where I built two production descheduler plugins in Go, and I also compete in contests on the side.

- 🌐 Koordinator contributor, 7 PRs across resource management, koordlet, and admission webhooks
- 🔧 Merged fix in **QuantLib** for a floating-point failure that only appeared under `g++ 12 -O3`
- ⚔️ **Meta Hacker Cup 2025**: global rank 1570 in Round 2
- 🧮 700+ problems solved, 90+ rated contests

## Tech Stack

| | |
|---|---|
| **Languages** | Go, C++, Python, JavaScript, C, SQL |
| **Systems** | Kubernetes (client-go, CRDs, API Machinery), Linux, Prometheus, multithreading, cache-aware design |
| **Tools** | Git, kubectl, SFML, React, Vite, Tailwind CSS |

---

## Featured: LFX Mentorship at [Koordinator](https://github.com/koordinator-sh/koordinator)
`Jun 2026 - Aug 2026` · Go · client-go · CRD APIs · Kubernetes Scheduling Framework

Designed and built two descheduler plugins (**5,000+ LOC**, **52 unit tests**, up to 2.4:1 test-to-code ratio) with versioned `v1alpha2` APIs, auto-defaulting, and field-level validation.

| Plugin | What it does | Result |
|---|---|---|
| **ScaleDownBinpack** | Ranks scale-down victims with **RRBS** (Residual Resource Binpack Score, O(N log N + k)) so workloads drain onto the fewest nodes, using the native pod-deletion-cost annotation | Up to **3x more idle nodes** than default (~$219/month projected, 10-node cluster) |
| **FragmentationAware** | Ranks nodes by std-dev imbalance and evicts the highest-gain pod via O(n) incremental scoring, gated by `ReservationFirst` pre-checks for zero-downtime migration | **~93%** less simulated fragmentation, **~67pp** more free capacity per node (18-node CPU/memory/GPU cluster) |

## Open Source

**[Koordinator](https://github.com/koordinator-sh/koordinator)**

| PR | Change |
|---|---|
| [#2918](https://github.com/koordinator-sh/koordinator/pull/2918) | BE resource helpers now account for init containers and `pod.Spec.Overhead` *(milestone v1.8.1)* |
| [#2940](https://github.com/koordinator-sh/koordinator/pull/2940) | Registered `MidCPU` / `MidMemory` in `ExtendedResourceNames` |
| [#2926](https://github.com/koordinator-sh/koordinator/pull/2926) | Added `--default-qos-class-for-guaranteed-pods` flag with parse-time validation |
| [#2980](https://github.com/koordinator-sh/koordinator/pull/2980) | Priority-aware, cold-start-ramped histogram weighting in `predict_server` |
| [#2958](https://github.com/koordinator-sh/koordinator/pull/2958) | Shared `runMutatingPlugins` handler to support UPDATE in the pod webhook |
| [#2944](https://github.com/koordinator-sh/koordinator/pull/2944) | Structured error codes in webhook metrics instead of binary `StatusRejected` |
| [#2953](https://github.com/koordinator-sh/koordinator/pull/2953) | Runtime GPU/NPU resource registration in the `gpudeviceresource` plugin |

**[QuantLib](https://github.com/lballabio/QuantLib)** · [#2435](https://github.com/lballabio/QuantLib/pull/2435) *(merged)*
Diagnosed a `testCachedHullWhite` failure that only showed up under `g++ 12.x -O3` and adjusted the tolerance in `shortratemodels.cpp` (`1.2e-5` → `1.3e-5`) to absorb legitimate floating-point variance without weakening the test.

---

## Projects

**[Multithreaded Huffman Compression Engine](https://github.com/Vatsalpatni73/Multithreaded_Text_File_Compressor)** · C++
Lossless Huffman compressor with worker threads synchronized by mutexes and condition variables. On a 500 MB dataset, going from 1 to 4 workers cut runtime by **63%** (25.1s → 9.3s).

**Cache-Optimized Pathfinding Visualizer** · C++ · SFML
Real-time Dijkstra and Bidirectional A\* visualizer. Flattened 2D grids into contiguous 1D arrays for better L1/L2 cache locality, and used Manhattan-distance heuristics to cut the search space from O(b^d) to O(b^(d/2)).

---

## Leadership & Recognition

- **Head, Branding & Publicity**, Research Cell (2025-26): led outreach for a 900+ member community, engagement up 30%
- **Manager, Public Relations**, Kashiyatra (2025-26): PR for 50+ events reaching 80,000+ attendees
- **JEE Advanced** qualifier (top 1%) · **STSE 2020** rank 365
