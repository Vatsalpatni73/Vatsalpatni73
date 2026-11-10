<div align="center">
  <h1>Hi, I'm Vatsal Patni 👋</h1>
  <h3>Kubernetes & Systems Contributor · LFX Mentee at CNCF Koordinator · Competitive Programmer</h3>
  <p><sub>B.Tech Civil Engineering, IIT (BHU) Varanasi · Class of 2027</sub></p>

  <p align="center">
    <a href="mailto:vatsalpatni73@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/></a>
    <a href="https://www.linkedin.com/in/vatsal-patni-5676482a4"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
    <a href="https://codeforces.com/profile/LASTAV"><img src="https://img.shields.io/badge/Codeforces-Expert%20%7C%201665-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white" alt="Codeforces"/></a>
    <a href="https://leetcode.com/vatsalpatni"><img src="https://img.shields.io/badge/LeetCode-Knight%20%7C%201911-FFA116?style=for-the-badge&logo=leetcode&logoColor=white" alt="LeetCode"/></a>
  </p>
</div>

---

## 👨‍💻 About Me

I like working deep in the stack: **Kubernetes scheduling and descheduling**, **cluster resource management**, and **concurrent C++**. I completed the **LFX Mentorship (2026 Term 2)** with [Koordinator](https://github.com/koordinator-sh/koordinator), a CNCF project for QoS-based Kubernetes scheduling, where I designed and implemented two descheduler plugins in Go.

- 🌐 **Koordinator**: LFX mentee and contributor across the descheduler, koordlet, and admission webhook
- 🔧 **QuantLib**: Fixed a floating-point test failure that only appeared under `g++ 12 -O3` (shipped in QuantLib 1.42)
- ⚔️ **Meta Hacker Cup 2025**: Global Rank 1570 in Round 2
- 🧮 **Competitive Programming**: 700+ problems solved, 90+ rated contests

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| ⌨️ **Languages** | Go, C++, Python, JavaScript, C, SQL |
| ⚙️ **Systems** | Kubernetes (client-go, CRDs, API machinery, scheduling framework), Linux, Prometheus, multithreading, cache-aware design |
| 🧰 **Tools** | Git, kubectl, SFML, React, Vite, Tailwind CSS |

---

## 🚀 Featured: LFX Mentorship at [Koordinator](https://github.com/koordinator-sh/koordinator)
> **Jun 2026 - Aug 2026** · Project: *Fragmentation-Aware Rescheduling and Scale-Down Binpack* · `Go` `client-go` `CRD APIs` `Descheduler framework`

Designed and implemented two descheduler plugins, with **52 unit tests** (up to a 2.4:1 test-to-code ratio), versioned `v1alpha2` APIs, auto-defaulting, and field-level validation. Completed with a positive mentor evaluation.

| 🔌 Plugin | 🎯 What it does | 📈 Result (simulated) |
|---|---|---|
| **ScaleDownBinpack** | Ranks scale-down victims with **RRBS** (Residual Resource Binpack Score, `O(N log N + k)`) so workloads drain onto the fewest nodes. Writes the rank to the native `pod-deletion-cost` annotation, or evicts directly. | Up to **3x more reclaimable idle nodes** than default scale-down (about $219/month projected on a 10-node cluster). |
| **FragmentationAware** | Ranks nodes by the standard deviation of per-resource utilization and evicts the pod with the highest gain, using `O(n)` incremental scoring. Uses `ReservationFirst` eviction so replacement capacity is secured before a pod moves. | About **93%** less resource imbalance and about **67pp** more schedulable capacity freed per node (18-node CPU/memory/GPU cluster). |

**Pull requests:** [#3092](https://github.com/koordinator-sh/koordinator/pull/3092) ScaleDownBinpack ranker and tests · [#3117](https://github.com/koordinator-sh/koordinator/pull/3117) ScaleDownBinpack plugin and registration · [#3160](https://github.com/koordinator-sh/koordinator/pull/3160) fix pod listing panic · [#3093](https://github.com/koordinator-sh/koordinator/pull/3093) FragmentationAware balance plugin · [#3159](https://github.com/koordinator-sh/koordinator/pull/3159) remove dead code in FragmentationAware

## 🌍 Open Source

### 🌩️ [Koordinator](https://github.com/koordinator-sh/koordinator)

All of my pull requests: [`is:pr author:Vatsalpatni73`](https://github.com/koordinator-sh/koordinator/pulls?q=is%3Apr+author%3AVatsalpatni73)

| PR | Area | Change |
|---|---|---|
| [#2918](https://github.com/koordinator-sh/koordinator/pull/2918) | util | BE (Batch) resource helpers now account for init containers and `pod.Spec.Overhead` |
| [#2926](https://github.com/koordinator-sh/koordinator/pull/2926) | koordlet | `--default-qos-class-for-guaranteed-pods` flag with parse-time validation |
| [#2958](https://github.com/koordinator-sh/koordinator/pull/2958) | webhook | Shared `runMutatingPlugins` flow so Pod UPDATE requests can be mutated behind an opt-in label |
| [#2980](https://github.com/koordinator-sh/koordinator/pull/2980) | koordlet | Priority-aware, cold-start-ramped sample weighting for histograms in `predict_server` |
| [#2944](https://github.com/koordinator-sh/koordinator/pull/2944) | webhook | Structured error codes in webhook metrics instead of a binary rejected status |
| [#2953](https://github.com/koordinator-sh/koordinator/pull/2953) | scheduler | Runtime GPU/NPU resource registration in the `gpudeviceresource` plugin |
| [#3045](https://github.com/koordinator-sh/koordinator/pull/3045) | koordlet | Configurable CPU and memory percentiles for the peak predictor |
| [#3006](https://github.com/koordinator-sh/koordinator/pull/3006), [#3014](https://github.com/koordinator-sh/koordinator/pull/3014), [#3016](https://github.com/koordinator-sh/koordinator/pull/3016) | e2e | Bootstrapped the koordlet e2e suite with BECPUSuppress/BECPUEvict, BlkIOQoS and resctrl tests |

### 📊 [QuantLib](https://github.com/lballabio/QuantLib)
- **[PR #2435](https://github.com/lballabio/QuantLib/pull/2435)** ✅ *(merged, released in 1.42)*: Diagnosed a `testCachedHullWhite` failure that only showed up under `g++ 12.x -O3` and adjusted the tolerance in `shortratemodels.cpp` (`1.2e-5` to `1.3e-5`) to absorb legitimate floating-point variance without weakening the test.

---

## 🏗️ Projects

### 🗜️ [Multithreaded Huffman Compression Engine](https://github.com/Vatsalpatni73/Multithreaded_Text_File_Compressor)
> `C++` `Multithreading` `Mutexes`

Lossless Huffman compressor with worker threads synchronized by mutexes and condition variables. On a 500 MB dataset, going from 1 to 4 workers cut runtime by **63%** (25.1s to 9.3s).

### 🗺️ Cache-Optimized Pathfinding Visualizer
> `C++` `SFML` `Data Structures`

Real-time Dijkstra and Bidirectional A* visualizer. Flattened 2D grids into contiguous 1D arrays for better **L1/L2 cache locality**. A Manhattan-distance heuristic focuses the search toward the goal, and searching from both ends reduces the explored space from `O(b^d)` to roughly `O(b^(d/2))`.

---

## 🏆 Leadership & Recognition

- 🗣️ **Head, Branding & Publicity**, Research Cell (2025-26): Led outreach for a 900+ member community, increasing engagement by **30%**.
- 📢 **Manager, Public Relations**, Kashiyatra (2025-26): Executed PR for 50+ events reaching **80,000+** attendees.
- 🎓 **JEE Advanced** qualifier · **STSE 2020** Rank 365
