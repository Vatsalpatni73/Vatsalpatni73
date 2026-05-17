<h1 align="center">Hey there 👋, I'm Vatsal Patni</h1>

<p align="center">
  <b>Third Year Undergrad · IIT (BHU) Varanasi · Civil Engineering</b><br/>
  Systems programmer, open-source contributor & competitive coder
</p>

<p align="center">
  <a href="mailto:vatsalpatni73@gmail.com"><img src="https://img.shields.io/badge/Gmail-vatsalpatni73-D14836?style=flat&logo=gmail&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/vatsal-patni"><img src="https://img.shields.io/badge/LinkedIn-Vatsal%20Patni-0A66C2?style=flat&logo=linkedin&logoColor=white"/></a>
  <a href="https://codeforces.com/profile/LASTAV"><img src="https://img.shields.io/badge/Codeforces-LASTAV%20%7C%201518-1F8ACB?style=flat&logo=codeforces&logoColor=white"/></a>
  <a href="https://leetcode.com/vatsalpatni"><img src="https://img.shields.io/badge/LeetCode-vatsalpatni%20%7C%201878-FFA116?style=flat&logo=leetcode&logoColor=white"/></a>
  <a href="https://github.com/Vatsalpatni73"><img src="https://img.shields.io/badge/GitHub-Vatsalpatni73-181717?style=flat&logo=github&logoColor=white"/></a>
</p>

---

## 🧑‍💻 About Me

I'm a systems-focused developer who loves working deep in the stack — Kubernetes internals, concurrent C++, and distributed resource management. Currently contributing to CNCF projects while honing DSA and competitive programming skills.

- 🎓 &nbsp;B.Tech in Civil Engineering at **IIT (BHU) Varanasi** (CGPA: 7.97, Class of 2027)
- 🌐 &nbsp;Active **CNCF / Kubernetes** open-source contributor (Koordinator project)
- 🏆 &nbsp;**JEE Advanced** qualifier — top 1% of engineering aspirants nationwide
- ⚔️ &nbsp;**Meta Hacker Cup 2025** — progressed to Round 2, ranked **1,570th globally**

---

## 🔧 Tech Stack

| Domain | Technologies |
|---|---|
| **Languages** | C / C++, Go, Python, JavaScript, SQL |
| **Core Areas** | DSA, OOP, Kubernetes Internals, Distributed Systems, Multithreading & Concurrency, Memory & Cache Management |
| **Frameworks & Platforms** | React.js, Vite, Tailwind CSS, Recharts, Koordinator, Kubernetes Admission Webhook Framework, Prometheus |
| **Developer Tools** | Git, GitHub, kubectl, Vercel, Jupyter Notebook, Codecov |

---

## 🚀 Open Source Contributions

### [Koordinator](https://github.com/koordinator-sh/koordinator) — CNCF Kubernetes QoS-based Resource Management &nbsp;`May 2026`
> **Go · Kubernetes Internals · koordlet · Admission Webhooks · slo-controller**

**Resource Management**
- Fixed BE resource helpers (`GetPodBEMilliCPU*`, `GetPodBEMemoryByte*`) to correctly account for init containers and `pod.Spec.Overhead` per Kubernetes semantics — [#2918](https://github.com/koordinator-sh/koordinator/pull/2918) *(milestone v1.8.1)*
- Registered `MidCPU` / `MidMemory` into `ExtendedResourceNames` — [#2940](https://github.com/koordinator-sh/koordinator/pull/2940)

**koordlet & Prediction**
- Added `--default-qos-class-for-guaranteed-pods` flag with parse-time validation — [#2926](https://github.com/koordinator-sh/koordinator/pull/2926)
- Introduced `computePodSampleWeight` for priority-aware and cold-start-ramped histogram weighting in `predict_server` — [#2980](https://github.com/koordinator-sh/koordinator/pull/2980)

**Webhook & Device Plugin**
- Refactored pod mutating handler into shared `runMutatingPlugins` for UPDATE support — [#2958](https://github.com/koordinator-sh/koordinator/pull/2958)
- Replaced binary `StatusRejected` with structured error codes in webhook metrics — [#2944](https://github.com/koordinator-sh/koordinator/pull/2944)
- Added runtime GPU/NPU resource registration to `gpudeviceresource` plugin — [#2953](https://github.com/koordinator-sh/koordinator/pull/2953)

### [QuantLib](https://github.com/lballabio/QuantLib) — Industry-Standard Quantitative Finance C++ Library &nbsp;`Merged`
> **C++ · Numerical Methods · Hull-White Model · Compiler Optimization**

- Diagnosed and fixed a test failure in `testCachedHullWhite` triggered specifically under **g++ 12.x with `-O3` optimization** — a subtle floating-point precision issue that only surfaced at high compiler optimization levels — [#2435](https://github.com/lballabio/QuantLib/pull/2435)
- Adjusted numerical tolerance in `test-suite/shortratemodels.cpp` from `1.2e-5` → `1.3e-5` to correctly accommodate valid floating-point variance introduced by aggressive compiler optimizations, without relaxing test integrity

---

## 🛠️ Projects

### [Multithreaded Text File Compressor](https://github.com/Vatsalpatni73/Multithreaded_Text_File_Compressor)
> **C++ · Memory Management · File I/O · Huffman Coding**

A high-performance lossless file compressor leveraging Huffman coding and multi-core concurrency.

- Implemented lossless Huffman compression with mutexes and condition variables for thread synchronization
- Benchmarked on a **500 MB dataset** — achieved a **63% reduction in execution latency** (25.1s → 9.3s) by scaling from single-threaded to 4-worker concurrent execution

---

### Codeforces Profile Visualizer &nbsp;·&nbsp; [Live Link](#) &nbsp;·&nbsp; [GitHub](#)
> **React.js · Vite · Tailwind CSS · Recharts · Codeforces API · Vercel**

A responsive single-page analytics dashboard to visualize and compare Codeforces user profiles side-by-side.

- Built a full-featured SPA with **React + Vite + Tailwind CSS** rendering contest history, rating trends, and problem tag distribution with interactive **Recharts** components — submission heatmaps, rating history graphs, and tag distribution charts for granular performance analysis
- Engineered a robust data-fetching layer against the **Codeforces REST API**; implemented `sessionStorage` caching (capped at **2,000 entries**) and graceful retry logic to handle **HTTP 429** rate-limiting and minimize network overhead

---

### Pathfinding Visualizer
> **C++ · SFML · STL (Vector, Queue, Priority Queue)**

A real-time graph traversal engine with visual rendering of pathfinding algorithms.

- Engineered runtime execution of **Dijkstra & Bidirectional A\*** optimized for low-latency visual output
- Flattened 2D grid allocations into contiguous 1D arrays — reduced heap fragmentation and maximized **L1/L2 CPU cache locality**
- Implemented Bidirectional A\* with Manhattan distance heuristics, cutting the search space from **O(b^d) → O(b^(d/2))**

---

## 🏅 Achievements

| | |
|---|---|
| 🥇 | **JEE Advanced** — Top 1% of engineering aspirants nationwide |
| 🌍 | **Meta Hacker Cup 2025** — Qualified & progressed to Round 2 · **1,570th globally** |
| ⚡ | **Codeforces** — Specialist · Rating **1518** · Handle: [LASTAV](https://codeforces.com/profile/LASTAV) |
| 💡 | **LeetCode** — Knight · Rating **1878** · Handle: [vatsalpatni](https://leetcode.com/vatsalpatni) |
| 📜 | **STSE** — Secured **Rank 365** in the State Talent Search Examination |
