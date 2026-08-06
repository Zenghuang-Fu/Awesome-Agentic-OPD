# Awesome-Agentic-OPD

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![Agentic OPD](mainv1.png)](https://github.com/Zenghuang-Fu/Awesome-Agentic-OPD)

A curated list of papers, benchmarks, methods, and resources for **On-Policy Distillation (OPD) and On-Policy Self-Distillation (OPSD) in Agentic RL** — i.e. multi-turn, tool-integrated, long-horizon settings, as opposed to conventional single-turn OPD.

---

## 📢 News

- 🚀 2026-08-06: Repository initialized.
- 📝 2026-08-06: Taxonomy for agentic OPD / OPSD released (10 categories).
- 📚 2026-08-06: First batch indexed — 189 entries covering 186 unique papers (2023 foundations + 2025–2026 agentic works), 59 with code links.
- ✅ 2026-08-06: All titles, dates, venues and code links verified programmatically against the arXiv API.

---

## 📚 Table of Contents

- [Awesome-Agentic-OPD](#awesome-agentic-opd)
  - [📢 News](#-news)
  - [🧭 Taxonomy](#-taxonomy)
    - [1️⃣ Foundations & Single-Turn OPD / OPSD](#1️⃣-foundations--single-turn-opd--opsd)
    - [2️⃣ Trajectory-Level Agentic OPD](#2️⃣-trajectory-level-agentic-opd)
    - [3️⃣ Turn- and Step-Level OPD / OPSD](#3️⃣-turn--and-step-level-opd--opsd)
    - [4️⃣ Token-Level Selection, Gating and Advantage Shaping](#4️⃣-token-level-selection-gating-and-advantage-shaping)
    - [5️⃣ Privileged- and Hindsight-Conditioned OPSD](#5️⃣-privileged--and-hindsight-conditioned-opsd)
    - [6️⃣ Teacher Construction and Multi-Teacher OPD](#6️⃣-teacher-construction-and-multi-teacher-opd)
    - [7️⃣ Coupling OPD with RLVR and Policy Gradient](#7️⃣-coupling-opd-with-rlvr-and-policy-gradient)
    - [8️⃣ Skill, Memory and Self-Evolving Agents](#8️⃣-skill-memory-and-self-evolving-agents)
    - [9️⃣ Domain Agents: Search, GUI, Coding, Multimodal, Embodied](#9️⃣-domain-agents-search-gui-coding-multimodal-embodied)
    - [🔟 Diagnostics, Theory, Benchmarks and Frameworks](#-diagnostics-theory-benchmarks-and-frameworks)
  - [📄 Papers](#-papers)
  - [🤝 Contributing](#-contributing)
  - [⭐ Star History](#-star-history)
  - [📌 Citation](#-citation)

---

## 🧭 Taxonomy

### 1️⃣ Foundations & Single-Turn OPD / OPSD

Reverse-KL / f-divergence objectives on student-sampled data, on-policy vs. off-policy knowledge distillation, self-distillation with a same-model teacher, and the single-turn reasoning recipes that agentic OPD builds on.

### 2️⃣ Trajectory-Level Agentic OPD

Whole-rollout distillation in multi-turn environments: trajectory-level KL, rollout-horizon and window control, prefix replay and prefix trap, exposure bias and trajectory refinement.

### 3️⃣ Turn- and Step-Level OPD / OPSD

Turn-aware and action-step-aware supervision: per-turn intervention and switching, turn-normalized losses, turn-level credit from a teacher, step-level preference/advantage shaping, curriculum over turns.

### 4️⃣ Token-Level Selection, Gating and Advantage Shaping

Where to apply the distillation signal: entropy/divergence-based token typing, gating and masking, sibling-rollout counterfactual token credit, advantage reweighting and fusion, top-K support truncation effects.

### 5️⃣ Privileged- and Hindsight-Conditioned OPSD

Self-teachers conditioned on information the student never sees — gold answers, evidence, future observations, skills, reflections, sibling rollouts — plus the privilege illusion / hindsight-leakage problem this creates.

### 6️⃣ Teacher Construction and Multi-Teacher OPD

Choosing and building the teacher: multi-teacher and domain-routed OPD (MOPD), specialize-and-merge, weak-to-strong, teacher debate, relay/handoff execution, teacher refresh schedules, and large-scale technical reports that ship MOPD in production.

### 7️⃣ Coupling OPD with RLVR and Policy Gradient

How distillation coexists with verifiable-reward RL: annealing and interleaving, dense-signal-plus-sparse-reward hybrids, direction-vs-magnitude decomposition, and keeping policy gradient in charge.

### 8️⃣ Skill, Memory and Self-Evolving Agents

Distilling experience into reusable artifacts and back into weights: skill libraries, hindsight skills, memory hierarchies, world models, self-evolution loops, and context-space vs. parameter-space distillation.

### 9️⃣ Domain Agents: Search, GUI, Coding, Multimodal, Embodied

Agentic OPD / OPSD instantiated per domain — deep search and RAG agents, GUI and computer-use agents, SWE and coding agents, multimodal / speech / video agents, embodied and robotic policies, and small-model agent distillation.

### 🔟 Diagnostics, Theory, Benchmarks and Frameworks

Failure-mode studies and phenomenology, geometry of OPD updates, safety and privacy of distillation, plus the environments, evaluation testbeds and open-source training frameworks that support agentic OPD research.

---

## 📄 Papers

### 1️⃣ Foundations & Single-Turn OPD / OPSD

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [MiniLLM: On-Policy Distillation of Large Language Models](https://arxiv.org/abs/2306.08543) | MiniLLM | 2023-06 | [Code](https://github.com/microsoft/LMOps/tree/main/minillm) | ICLR |
| [On-Policy Distillation of Language Models: Learning from Self-Generated Mistakes](https://arxiv.org/abs/2306.13649) | GKD | 2023-06 | - | ICLR |
| [DistiLLM: Towards Streamlined Distillation for Large Language Models](https://arxiv.org/abs/2402.03898) | DistiLLM | 2024-02 | [Code](https://github.com/jongwooko/distillm) | ICML |
| [SWITCH: Studying with Teacher for Knowledge Distillation of Large Language Models](https://arxiv.org/abs/2410.19503) | SWITCH | 2024-10 | - | Findings of NAACL |
| [Speculative Knowledge Distillation: Bridging the Teacher-Student Gap Through Interleaved Sampling](https://arxiv.org/abs/2410.11325) | SKD | 2024-10 | - | ICLR |
| [DistiLLM-2: A Contrastive Approach Boosts the Distillation of LLMs](https://arxiv.org/abs/2503.07067) | DistiLLM-2 | 2025-03 | - | ICML(Spotlight) |
| [Online Knowledge Distillation with Reward Guidance](https://arxiv.org/abs/2505.18952) | - | 2025-05 | - | arXiv |
| [KDRL: Post-Training Reasoning LLMs via Unified Knowledge Distillation and Reinforcement Learning](https://arxiv.org/abs/2506.02208) | KDRL | 2025-06 | - | arXiv |
| [More Than One Teacher: Adaptive Multi-Guidance Policy Optimization for Diverse Exploration](https://arxiv.org/abs/2510.02227) | AMPO | 2025-10 | [Code](https://github.com/SII-Enigma/AMPO) | arXiv |
| [AdaSwitch: Balancing Exploration and Guidance in Knowledge Distillation via Adaptive Switching](https://arxiv.org/abs/2510.07842) | AdaSwitch | 2025-10 | - | arXiv |
| [Stable On-Policy Distillation through Adaptive Target Reformulation](https://arxiv.org/abs/2601.07155) | Veto | 2026-01 | - | Findings of ACL |
| [Self-Distilled Reasoner: On-Policy Self-Distillation for Large Language Models](https://arxiv.org/abs/2601.18734) | OPSD | 2026-01 | [Code](https://github.com/siyan-zhao/OPSD) | arXiv |
| [Privileged Information Distillation for Language Models](https://arxiv.org/abs/2602.04942) | π-Distill / OPSD | 2026-02 | - | arXiv |
| [Learning beyond Teacher: Generalized On-Policy Distillation with Reward Extrapolation](https://arxiv.org/abs/2602.12125) | GOPD | 2026-02 | - | arXiv |
| [Fast and Effective On-policy Distillation from Reasoning Prefixes](https://arxiv.org/abs/2602.15260) | - | 2026-02 | - | arXiv |
| [Entropy-Aware On-Policy Distillation of Language Models](https://arxiv.org/abs/2603.07079) | - | 2026-03 | - | ICML |
| [Scaling Reasoning Efficiently via Relaxed On-Policy Distillation](https://arxiv.org/abs/2603.11137) | REOPOLD | 2026-03 | - | arXiv |
| [CRISP: Compressed Reasoning via Iterative Self-Policy Distillation](https://arxiv.org/abs/2603.05433) | CRISP | 2026-03 | [Code](https://github.com/HJSang/OPSD_Reasoning_Compression) | arXiv |
| [A Survey of On-Policy Distillation for Large Language Models](https://arxiv.org/abs/2604.00626) | Survey | 2026-04 | - | arXiv |
| [Hybrid Policy Distillation for LLMs](https://arxiv.org/abs/2604.20244) | HPD | 2026-04 | [Code](https://github.com/zwhong714/Hybrid-Policy-Distillation) | arXiv |
| [SODA: Semi On-Policy Black-Box Distillation for Large Language Models](https://arxiv.org/abs/2604.03873) | SODA | 2026-04 | - | arXiv |
| [The Illusion of Certainty: Decoupling Capability and Calibration in On-Policy Distillation](https://arxiv.org/abs/2604.16830) | CaOPD | 2026-04 | [Code](https://github.com/SalesforceAIResearch/CaOPD) | arXiv |
| [OPSDL: On-Policy Self-Distillation for Long-Context Language Models](https://arxiv.org/abs/2604.17535) | OPSDL | 2026-04 | - | arXiv |
| [Uni-OPD: Unifying On-Policy Distillation with a Dual-Perspective Recipe](https://arxiv.org/abs/2605.03677) | Uni-OPD | 2026-05 | - | arXiv |
| [Tailoring Teaching to Aptitude: Direction-Adaptive Self-Distillation for LLM Reasoning](https://arxiv.org/abs/2605.22263) | DASD | 2026-05 | - | arXiv |
| [OPD+: Rethinking the Advantage Design for On-Policy Distillation](https://arxiv.org/abs/2606.01039) | OPD+ | 2026-05 | - | arXiv |
| [Trust Region On-Policy Distillation](https://arxiv.org/abs/2606.01249) | TrOPD | 2026-05 | - | arXiv |
| [Learning from the Self-future: On-policy Self-distillation for dLLMs](https://arxiv.org/abs/2606.18195) | d-OPSD | 2026-06 | [Code](https://github.com/xingzhejun/d-OPSD) | arXiv |
| [Distilled Reinforcement Learning for LLM Post-training](https://arxiv.org/abs/2607.17247) | DistilledRL | 2026-07 | [Code](https://github.com/597358816/Distilled-RL) | arXiv |
| [DemoPSD: Disagreement-Modulated Policy Self-Distillation](https://arxiv.org/abs/2607.02502) | DemoPSD | 2026-07 | - | arXiv |

### 2️⃣ Trajectory-Level Agentic OPD

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [TCOD: Exploring Temporal Curriculum in On-Policy Distillation for Multi-turn Autonomous Agents](https://arxiv.org/abs/2604.24005) | TCOD | 2026-04 | [Code](https://github.com/kokolerk/TCOD) | arXiv |
| [Same Evidence, Different Answers: Canonical-Context On-Policy Distillation for Multi-Turn Language Models](https://arxiv.org/abs/2605.30251) | CCOPD | 2026-05 | - | arXiv |
| [ADWIN: Adaptive Windows for Horizon-Aware On-Policy Distillation](https://arxiv.org/abs/2605.28396) | ADWIN | 2026-05 | - | arXiv |
| [Backtracking When It Strays: Mitigating Dual Exposure Biases in LLM Reasoning Distillation](https://arxiv.org/abs/2605.19433) | MOTAB | 2026-05 | - | arXiv |
| [Trajectory-Refined Distillation](https://arxiv.org/abs/2606.08432) | TRD | 2026-06 | [Code](https://github.com/louieworth/trd) | arXiv |
| [Prefix-Guided On-Policy Distillation: Mining Golden Trajectories from Rollouts](https://arxiv.org/abs/2606.21994) | PG-OPD | 2026-06 | - | arXiv |
| [From Trajectories to Prefixes: Reusing Teacher Trajectories via Replayed Prefixes and Online Continuation](https://arxiv.org/abs/2607.19395) | Prefix-GRPO | 2026-07 | [Code](https://github.com/HappynessI/Prefix_GRPO) | arXiv |
| [Multi-Turn On-Policy Distillation with Prefix Replay](https://arxiv.org/abs/2607.04763) | ReOPD | 2026-07 | - | arXiv |
| [The Physics of Multi-Turn Long-Horizon Planning: From Pre-training to Post-training via Single- and Multi-Teacher On-Policy Agentic Distillation](https://arxiv.org/abs/2607.24720) | MOPD | 2026-07 | - | arXiv |
| [Adaptive FastOPD: Progress-Aware Rollout Horizon Expansion for Efficient On-Policy Distillation](https://arxiv.org/abs/2607.29494) | Adaptive FastOPD | 2026-07 | - | arXiv |
| [Look Ahead Before You Distill: Future Trajectory Validation of Teacher Guidance for Agentic On-Policy Distillation](https://arxiv.org/abs/2608.01953) | FutureBridge-OPD | 2026-08 | [Code](https://github.com/ChenChiShui/FutureBridge-OPD) | arXiv |
| [HindSearch: Trajectory-Level Hindsight Critique for Search-Augmented Reinforcement Learning](https://arxiv.org/abs/2608.01597) | HindSearch | 2026-08 | - | arXiv |
| [Not Every Divergence Should Be Suppressed: Counterfactual Recoverability in On-Policy Distillation](https://arxiv.org/abs/2608.04408) | - | 2026-08 | - | arXiv |

### 3️⃣ Turn- and Step-Level OPD / OPSD

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [Adaptive Milestone Reward for GUI Agents](https://arxiv.org/abs/2602.11524) | ADMIRE | 2026-02 | - | arXiv |
| [SLEA-RL: Step-Level Experience Augmented Reinforcement Learning for Multi-Turn Agentic Training](https://arxiv.org/abs/2603.18079) | SLEA-RL | 2026-03 | - | arXiv |
| [UI-Voyager: A Self-Evolving GUI Agent Learning via Failed Experience](https://arxiv.org/abs/2603.24533) | Group Relative Self-Distillation | 2026-03 | [Code](https://github.com/ui-voyager/UI-Voyager) | arXiv |
| [Healthcare AI GYM for Medical Agents](https://arxiv.org/abs/2605.02943) | TT-OPD | 2026-05 | - | arXiv |
| [SOD: Step-wise On-policy Distillation for Small Language Model Agents](https://arxiv.org/abs/2605.07725) | SOD | 2026-05 | [Code](https://github.com/YoungZ365/SOD) | arXiv |
| [StepOPSD: Step-Aware Online Preference Distillation for Agent Reinforcement Learning](https://arxiv.org/abs/2605.27140) | StepOPSD | 2026-05 | - | arXiv |
| [Graph-GRPO: Dependency-Aware Credit Assignment for Generative E-commerce Search Relevance](https://arxiv.org/abs/2605.31003) | Graph-GRPO | 2026-05 | - | arXiv |
| [On-Policy Distillation with Curriculum Turn-level Guidance for Multi-turn Agents](https://arxiv.org/abs/2606.15912) | Guided-OPD | 2026-06 | - | arXiv |
| [SAGE-OPD: Selective Agent-Guided Intervention for Multi-Turn On-Policy Distillation](https://arxiv.org/abs/2606.19659) | SAGE-OPD | 2026-06 | - | arXiv |
| [ATOD: Annealed Turn-Aware On-Policy Distillation for Multi-Turn Agentic Tasks](https://arxiv.org/abs/2606.27814) | ATOD | 2026-06 | - | arXiv |
| [TurnOPD: Making On-Policy Distillation Turn-Aware for Efficient Long-Horizon Agent Training](https://arxiv.org/abs/2607.05804) | TurnOPD | 2026-07 | - | arXiv |
| [CAST: Game Solvers as Turn-Level Teachers for LLM Agents](https://arxiv.org/abs/2607.25308) | CAST | 2026-07 | [Code](https://github.com/Wloner0809/CAST) | arXiv |
| [DASH-OPD: Discrepancy-Aware Switching with Hysteresis for On-Policy Distillation](https://arxiv.org/abs/2607.29078) | DASH-OPD | 2026-07 | - | arXiv |
| [TCPO: Turn-Level Credit Policy Optimization](https://arxiv.org/abs/2608.01667) | TCPO | 2026-08 | - | arXiv |
| [TurnSight: Turn-Level Hindsight Self-Distillation for Tool-Integrated Reasoning](https://arxiv.org/abs/2608.04007) | TurnSight | 2026-08 | [Code](https://github.com/quchangle1/TurnSight) | arXiv |

### 4️⃣ Token-Level Selection, Gating and Advantage Shaping

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [TIP: Token Importance in On-Policy Distillation](https://arxiv.org/abs/2604.14084) | TIP | 2026-04 | [Code](https://github.com/HJSang/OPSD_OnPolicyDistillation) | arXiv |
| [SCOPE: Signal-Calibrated On-Policy Distillation Enhancement with Dual-Path Adaptive Weighting](https://arxiv.org/abs/2604.10688) | SCOPE | 2026-04 | - | arXiv |
| [GEAR: Granularity-Adaptive Advantage Reweighting for LLM Agents via Self-Distillation](https://arxiv.org/abs/2605.11853) | GEAR | 2026-05 | - | arXiv |
| [AMR-SD: Asymmetric Meta-Reflective Self-Distillation for Token-Level Credit Assignment](https://arxiv.org/abs/2605.18529) | AMR-SD | 2026-05 | - | arXiv |
| [Blockwise Policy-Drift Gating for On-Policy Distillation](https://arxiv.org/abs/2606.24084) | - | 2026-06 | - | arXiv |
| [Learning from Own Solutions: Self-Conditioned Credit Assignment for Reinforcement Learning with Verifiable Rewards](https://arxiv.org/abs/2606.18810) | SC-GRPO | 2026-06 | - | arXiv |
| [CRAFT: Counterfactual Credit Assignment from Free Sibling Rollouts for Self-Distilled Agentic Reinforcement Learning](https://arxiv.org/abs/2606.29476) | CRAFT | 2026-06 | - | arXiv |
| [Keep Policy Gradient in Charge: Sibling-Guided Credit Distillation for Long-Horizon Tool-Use Agents](https://arxiv.org/abs/2606.12634) | SGCD | 2026-06 | - | arXiv |
| [Correcting What You Cannot See: Credit Assignment for Perception Distillation in Multimodal Reasoners](https://arxiv.org/abs/2607.28336) | PCD | 2026-07 | - | arXiv |
| [Flux-OPD: On-Policy Distillation with Evolving Contexts](https://arxiv.org/abs/2607.28022) | Flux-OPD | 2026-07 | - | arXiv |
| [SAF-OPD: Stable Advantage Fusion for On-Policy Distillation](https://arxiv.org/abs/2607.29209) | SAF-OPD | 2026-07 | - | arXiv |
| [Distill Where You Fail: Recovering Learning Signals of Negative RL-Groups from Adaptive Teacher Guidance](https://arxiv.org/abs/2608.00782) | RSTG | 2026-08 | - | arXiv |
| [SPOT: Sparse Probing and Outcome Calibration for On-Policy Distillation](https://arxiv.org/abs/2608.04419) | SPOT | 2026-08 | - | arXiv |
| [When Teachers Mislead: Spurious-Signal-Aware On-Policy Distillation](https://arxiv.org/abs/2608.03632) | SA-OPD | 2026-08 | - | arXiv |

### 5️⃣ Privileged- and Hindsight-Conditioned OPSD

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [Self-Distilled RLVR](https://arxiv.org/abs/2604.03128) | RLSD | 2026-04 | - | arXiv |
| [Skill-SD: Skill-Conditioned Self-Distillation for Multi-turn LLM Agents](https://arxiv.org/abs/2604.10674) | Skill-SD | 2026-04 | [Code](https://k1xe.github.io/skill-sd/) | arXiv |
| [π-Play: Multi-Agent Self-Play via Privileged Self-Distillation without External Data](https://arxiv.org/abs/2604.14054) | π-Play | 2026-04 | [Code](https://github.com/zhyaoch/pi-play) | arXiv |
| [Self-Distilled Agentic Reinforcement Learning](https://arxiv.org/abs/2605.15155) | SDAR | 2026-05 | - | arXiv |
| [HINT-SD: Targeted Hindsight Self-Distillation for Long-Horizon Agents](https://arxiv.org/abs/2605.17873) | HINT-SD | 2026-05 | - | arXiv |
| [SD-Search: On-Policy Hindsight Self-Distillation for Search-Augmented Reasoning](https://arxiv.org/abs/2605.18299) | SD-Search | 2026-05 | - | arXiv |
| [What and When to Distill: Selective Hindsight Distillation for Multi-Turn Agents](https://arxiv.org/abs/2605.19447) | SERL | 2026-05 | - | arXiv |
| [Adaptive Teacher Exposure for Self-Distillation in LLM Reasoning](https://arxiv.org/abs/2605.11458) | ATESD | 2026-05 | - | arXiv |
| [EDGE-OPD: Internalizing Privileged Context with Evidence Guided On-Policy Distillation](https://arxiv.org/abs/2605.23493) | EDGE-OPD | 2026-05 | - | arXiv |
| [Skill-Conditioned Gated Self-Distillation for LLM Reasoning](https://arxiv.org/abs/2605.28791) | SGSD | 2026-05 | [Code](https://github.com/walawalagoose/SGSD) | arXiv |
| [Beyond Absolute Imitation: Anchored Residual Guidance for Privileged On-Policy Distillation](https://arxiv.org/abs/2606.10385) | AR-OPD | 2026-06 | [Code](https://vanhowe.github.io/AR-OPD) | arXiv |
| [PBSD: Privileged Bayesian Self-Distillation for Long-Horizon Credit Assignment](https://arxiv.org/abs/2606.09348) | PBSD | 2026-06 | - | arXiv |
| [HERO: Hindsight-Enhanced Reflection from Environment Observations for Agentic Self-Distillation](https://arxiv.org/abs/2606.11559) | HERO | 2026-06 | - | arXiv |
| [V-Zero: Answer-Label-Free On-Policy Distillation with Contrastive Evidence Gating for Fine-Grained Visual Reasoning](https://arxiv.org/abs/2606.25319) | V-Zero | 2026-06 | [Code](https://github.com/eVI-group-SCU/V-Zero) | arXiv |
| [UCOB: Learning to Utilize and Evolve Agentic Skills via Credit-Aware On-Policy Bidirectional Self-Distillation](https://arxiv.org/abs/2606.29502) | UCOB | 2026-06 | [Code](https://github.com/TU2021/UCOB) | arXiv |
| [KbSD: Knowledge Boundary aware Self-Distillation for Behavioral Calibration in Agentic Search](https://arxiv.org/abs/2606.29863) | KbSD | 2026-06 | - | arXiv |
| [DOPD: Dual On-policy Distillation](https://arxiv.org/abs/2606.30626) | DOPD | 2026-06 | - | arXiv |
| [From Scoring to Acting: Outcome-Verified Comparative Self-Distillation for LLM Agents](https://arxiv.org/abs/2607.27937) | OVCSD | 2026-07 | - | arXiv |
| [Contrastive Reinforced Policy Optimization via Privileged Self-Distillation](https://arxiv.org/abs/2607.28026) | CRPO | 2026-07 | - | arXiv |
| [Group-Reflective Self-Distillation for Agentic Reinforcement Learning](https://arxiv.org/abs/2607.28076) | GRSD | 2026-07 | - | arXiv |
| [PCSD: Persistent Consistency for Self-Distillation in Agentic Reinforcement Learning](https://arxiv.org/abs/2608.01837) | PCSD | 2026-08 | - | arXiv |
| [EviSD: Evidence-Conditioned Self-Distillation for Search-Augmented Agents](https://arxiv.org/abs/2608.01359) | EviSD | 2026-08 | [Code](https://github.com/JiananXie/EviSD) | arXiv |
| [DAPD: Dual-Anchored Policy Distillation](https://arxiv.org/abs/2608.01735) | DAPD | 2026-08 | - | arXiv |
| [Agentic Reinforcement Learning with Self-Distilled Reward Shaping](https://arxiv.org/abs/2608.03223) | ADRS | 2026-08 | [Code](https://github.com/gitrxh/ADRS-arxiv) | arXiv |
| [Agentic Reinforcement Learning with Observation-Calibrated Self-Distillation](https://arxiv.org/abs/2608.04788) | OCSD | 2026-08 | [Code](https://github.com/yiy1x/OCSD) | arXiv |
| [Privileged, but Biased: How PI-Conditioned Teachers Break Self-Distillation](https://arxiv.org/abs/2608.04794) | PI Bias Score | 2026-08 | - | arXiv |

### 6️⃣ Teacher Construction and Multi-Teacher OPD

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [Heterogeneous Agent Collaborative Reinforcement Learning](https://arxiv.org/abs/2603.02604) | HACPO | 2026-03 | - | arXiv |
| [Nemotron-Cascade 2: Post-Training LLMs with Cascade RL and Multi-Domain On-Policy Distillation](https://arxiv.org/abs/2603.19220) | Nemotron-Cascade 2 | 2026-03 | [Code](https://huggingface.co/collections/nvidia/nemotron-cascade-2) | arXiv |
| [KAT-Coder-V2 Technical Report](https://arxiv.org/abs/2603.27703) | KAT-Coder-V2 | 2026-03 | - | arXiv |
| [Lightning OPD: Efficient Post-Training for Large Reasoning Models with Offline On-Policy Distillation](https://arxiv.org/abs/2604.13010) | Lightning OPD | 2026-04 | [Code](https://github.com/jet-ai-projects/Lightning-OPD) | arXiv |
| [Co-Evolving Policy Distillation](https://arxiv.org/abs/2604.27083) | CoPD | 2026-04 | - | arXiv |
| [MAD-OPD: Breaking the Ceiling in On-Policy Distillation via Multi-Agent Debate](https://arxiv.org/abs/2605.01347) | MAD-OPD | 2026-05 | [Code](https://github.com/chiefovoavicii/MAD-OPD) | arXiv |
| [Multi-Rollout On-Policy Distillation via Peer Successes and Failures](https://arxiv.org/abs/2605.12652) | MOPD | 2026-05 | - | arXiv |
| [Teacher-Guided Policy Optimization for On-Policy Reasoning Distillation under Large Policy Divergence](https://arxiv.org/abs/2605.13230) | TGPO | 2026-05 | - | arXiv |
| [Adversarial Dual On-Policy Distillation from Expressive Teacher](https://arxiv.org/abs/2605.27095) | FA-OPD | 2026-05 | [Code](https://github.com/vanzll/FA-OPD) | arXiv |
| [When Should the Teacher Move? Temporal Coupling and Stability in Self On-Policy Distillation](https://arxiv.org/abs/2606.03532) | CGTR | 2026-06 | - | arXiv |
| [Kwai Keye-VL-2.0 Technical Report](https://arxiv.org/abs/2606.10651) | Keye-VL-2.0 | 2026-06 | - | arXiv |
| [Scaling the Horizon, Not the Parameters: Reaching Trillion-Parameter Performance with a 35B Agent](https://arxiv.org/abs/2606.30616) | Agents-A1 | 2026-06 | [Code](https://github.com/InternScience/Agents-A1) | arXiv |
| [KAT-Coder-V2.5 Technical Report](https://arxiv.org/abs/2607.05471) | KAT-Coder-V2.5 | 2026-07 | - | arXiv |
| [When Top-K Misses the Decision: Tool-Call Drift in Multi-Teacher On-Policy Distillation](https://arxiv.org/abs/2607.07050) | - | 2026-07 | [Code](https://github.com/shen-jiabin/topk-support-opd) | arXiv |
| [Mach-Mind-4-Flash Technical Report](https://arxiv.org/abs/2607.09375) | MOPD / HMPO | 2026-07 | - | arXiv |
| [REGEN: Replay-recycling for Expert-to-Generalist distillation with Offline Reinforcement Learning](https://arxiv.org/abs/2607.19450) | REGEN | 2026-07 | [Code](https://github.com/yunjie-sysu/REGEN) | arXiv |
| [Solar Open 2 Technical Report](https://arxiv.org/abs/2607.20062) | Solar Open 2 | 2026-07 | - | arXiv |
| [Weak-to-Strong On-Policy Distillation](https://arxiv.org/abs/2607.26246) | W2S-OPD | 2026-07 | [Code](https://github.com/Yu-Fangxu/W2S-OPD) | arXiv |
| [Pass the Baton: Trajectory-Relayed On-Policy Distillation](https://arxiv.org/abs/2607.26057) | Relay-OPD | 2026-07 | [Code](https://github.com/zju-real/Relay-OPD) | arXiv |
| [Beyond the Best Teacher: Expanding and Compressing the Reasoning Solution Manifold](https://arxiv.org/abs/2607.27770) | RGRPO / TU-OPD | 2026-07 | - | arXiv |
| [Lightning OPD 2.0: Mitigating Style Bias in Cross-Teacher On-Policy Distillation for Large Reasoning Models](https://arxiv.org/abs/2607.28449) | Lightning OPD 2.0 | 2026-07 | - | arXiv |
| [SMOPD: Multi-Reward Reinforcement Learning via Specialize-and-Merge Online Policy Distillation](https://arxiv.org/abs/2608.03092) | SMOPD | 2026-08 | - | arXiv |
| [Cross-Domain Hybrid OPD for Generalizable Search Agents](https://arxiv.org/abs/2608.02101) | Yuanbao Search Agent | 2026-08 | - | arXiv |

### 7️⃣ Coupling OPD with RLVR and Policy Gradient

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [Surgical Post-Training: Proximal On-Policy Distillation for Reasoning with Knowledge Retention](https://arxiv.org/abs/2603.01683) | SPoT | 2026-03 | [Code](https://github.com/Visual-AI/SPoT) | arXiv |
| [Beyond SFT-to-RL: Pre-alignment via Black-Box On-Policy Distillation for Multimodal RL](https://arxiv.org/abs/2604.28123) | PRISM | 2026-04 | [Code](https://github.com/XIAO4579/PRISM) | arXiv |
| [HyperEyes: Dual-Grained Efficiency-Aware Reinforcement Learning for Parallel Multimodal Search Agents](https://arxiv.org/abs/2605.07177) | HyperEyes | 2026-05 | [Code](https://github.com/DeepExperience/HyperEyes) | arXiv |
| [Search-E1: Self-Distillation Drives Self-Evolution in Search-Augmented Reasoning](https://arxiv.org/abs/2605.22511) | Search-E1 | 2026-05 | - | arXiv |
| [Physics-Guided Policy Optimization with Self-Distillation](https://arxiv.org/abs/2606.03620) | PGPO / SDPO | 2026-06 | - | arXiv |
| [Distill Where the Student Goes: Teacher-Regularized RL for English-Evidence Cross-Lingual RAG](https://arxiv.org/abs/2607.02966) | TR-RAG | 2026-07 | - | arXiv |
| [Verifier-Induced Support Reshaping in On-Policy Optimization](https://arxiv.org/abs/2608.00220) | Support Reshaping | 2026-07 | [Code](https://github.com/sylvain-wei/verifier-induced-support-reshaping) | arXiv |

### 8️⃣ Skill, Memory and Self-Evolving Agents

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [Internalizing Meta-Experience into Memory for Guided Reinforcement Learning in Large Language Models](https://arxiv.org/abs/2602.10224) | MEL | 2026-02 | - | arXiv |
| [Structured Distillation for Personalized Agent Memory: 11x Token Reduction with Retrieval Preservation](https://arxiv.org/abs/2603.13017) | - | 2026-03 | [Code](https://github.com/Process-Point-Technologies-Corporation/searchat) | arXiv |
| [PRIME: Training Free Proactive Reasoning via Iterative Memory Evolution for User-Centric Agent](https://arxiv.org/abs/2604.07645) | PRIME | 2026-04 | - | arXiv |
| [MMG2Skill: Can Agents Distill In-the-Wild Guides into Self-Evolving Skills?](https://arxiv.org/abs/2606.01993) | MMG2Skill | 2026-06 | [Code](https://github.com/NJU-LINK/MMG2Skill) | arXiv |
| [COMAP: Co-Evolving World Models and Agent Policies for LLM Agents](https://arxiv.org/abs/2606.02372) | COMAP | 2026-06 | [Code](https://github.com/loyiv/CoMAP) | arXiv |
| [Language Models Need Sleep: Learning to Self-Modify and Consolidate Memories](https://arxiv.org/abs/2606.03979) | Sleep / Dreaming | 2026-06 | - | arXiv |
| [Better with Experience: Self-Evolving LLM Agents for Evidence-Grounded Health Community Notes](https://arxiv.org/abs/2606.02215) | EvoNote | 2026-06 | - | arXiv |
| [OPID: On-Policy Skill Distillation for Agentic Reinforcement Learning](https://arxiv.org/abs/2606.26790) | OPID | 2026-06 | [Code](https://github.com/jinyangwu/OPID) | arXiv |
| [OPD-Evolver: Cultivating Holistic Agent Evolver via On-Policy Distillation](https://arxiv.org/abs/2606.17628) | OPD-Evolver | 2026-06 | - | arXiv |
| [DuoMem: Towards Capable On-Device Memory Agents via Dual-Space Distillation](https://arxiv.org/abs/2606.29961) | DuoMem | 2026-06 | - | arXiv |
| [Automating the Design of Embodied Agent Architectures](https://arxiv.org/abs/2606.30111) | AgentCanvas / KDLoop | 2026-06 | - | arXiv |
| [DeepSearch-World: Self-Distillation for Deep Search Agents in a Verifiable Environment](https://arxiv.org/abs/2607.07820) | DeepSearch-World | 2026-07 | - | arXiv |
| [SEED: Self-Evolving On-Policy Distillation for Agentic Reinforcement Learning](https://arxiv.org/abs/2607.14777) | SEED | 2026-07 | [Code](https://github.com/jinyangwu/SEED) | arXiv |
| [TransMem: Transforming Hidden States into Memory for Large Language Models](https://arxiv.org/abs/2607.29032) | TransMem | 2026-07 | [Code](https://github.com/Haodong-Lei-Ray/TransMem) | arXiv |
| [EvoReason: Self-Evolving Reasoning Primitive-Guided On-Policy Distillation for Latent Reasoning in Generative Recommendation](https://arxiv.org/abs/2607.29010) | EvoReason | 2026-07 | - | arXiv |

### 9️⃣ Domain Agents: Search, GUI, Coding, Multimodal, Embodied

| 📖 Title | 🛠 Model / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [Distilling LLM Agent into Small Models with Retrieval and Code Tools](https://arxiv.org/abs/2505.17612) | Agent Distillation | 2025-05 | [Code](https://github.com/Nardien/agent-distillation) | NeurIPS(Spotlight) |
| [Structured Agent Distillation for Large Language Model](https://arxiv.org/abs/2505.13820) | Structured Agent Distillation | 2025-05 | - | AAMAS |
| [AgentDistill: Training-Free Agent Distillation with Generalizable MCP Boxes](https://arxiv.org/abs/2506.14728) | AgentDistill | 2025-06 | - | arXiv |
| [Chain-of-Agents: End-to-End Agent Foundation Models via Multi-Agent Distillation and Agentic RL](https://arxiv.org/abs/2508.13167) | Chain-of-Agents / AFM | 2025-08 | - | arXiv |
| [Can Compact Language Models Search Like Agents? Distillation-Guided Policy Optimization for Preserving Agentic RAG Capabilities](https://arxiv.org/abs/2508.20324) | DGPO | 2025-08 | - | ACL(Main) |
| [Student-Centered Distillation Narrows the Agentic Gap Between Small and Large LLMs](https://arxiv.org/abs/2509.14257) | SCoRe | 2025-09 | - | ICML |
| [Knowledge Graph-Guided Multi-Agent Distillation for Reliable Industrial Question Answering with Datasets](https://arxiv.org/abs/2510.06240) | KG-MASD | 2025-10 | [Code](https://github.com/erwinmsmith/KG-MAD) | arXiv |
| [O-Researcher: An Open Ended Deep Research Model via Multi-Agent Distillation and Agentic RL](https://arxiv.org/abs/2601.03743) | O-Researcher | 2026-01 | - | arXiv |
| [X-OPD: Cross-Modal On-Policy Distillation for Capability Alignment in Speech LLMs](https://arxiv.org/abs/2603.24596) | X-OPD | 2026-03 | - | arXiv |
| [Search, Do not Guess: Teaching Small Language Models to Be Effective Search Agents](https://arxiv.org/abs/2604.04651) | - | 2026-04 | - | arXiv |
| [HY-Embodied-0.5: Embodied Foundation Models for Real-World Agents](https://arxiv.org/abs/2604.07430) | HY-Embodied-0.5 | 2026-04 | [Code](https://github.com/Tencent-Hunyuan/HY-Embodied) | arXiv |
| [Efficient Rationale-based Retrieval: On-policy Distillation from Generative Rerankers based on JEPA](https://arxiv.org/abs/2604.23336) | Rabtriever | 2026-04 | - | arXiv |
| [GUI Agents with Reinforcement Learning: Toward Digital Inhabitants](https://arxiv.org/abs/2604.27955) | Survey | 2026-04 | [Code](https://github.com/Steve2457/Awesome-RL-GUI-Agents) | arXiv |
| [From Patches to Trajectories: Privileged Process Supervision for Software-Engineering Agents](https://arxiv.org/abs/2605.21996) | P2T | 2026-05 | - | arXiv |
| [Vision-OPD: Learning to See Fine Details for Multimodal LLMs via On-Policy Self-Distillation](https://arxiv.org/abs/2605.18740) | Vision-OPD | 2026-05 | [Code](https://github.com/VisionOPD/Vision-OPD) | arXiv |
| [Visual-Advantage On-Policy Distillation for Vision-Language Models](https://arxiv.org/abs/2605.21924) | VA-OPD | 2026-05 | - | arXiv |
| [Unlocking Proactivity in Task-Oriented Dialogue](https://arxiv.org/abs/2605.22240) | - | 2026-05 | - | arXiv |
| [Retrieval, Reward, and Training Protocols: What Matters in Training Search Agents?](https://arxiv.org/abs/2605.27881) | Empirical Study | 2026-05 | [Code](https://github.com/YiboZhao624/SearchAgentReview) | arXiv |
| [Self-Distilled Reinforcement Learning for Co-Evolving Agentic Recommender Systems](https://arxiv.org/abs/2604.10029) | CoARS | 2026-04 | - | arXiv |
| [Native Active Perception as Reasoning for Omni-Modal Understanding](https://arxiv.org/abs/2606.19341) | OmniAgent / TAURA | 2026-06 | [Code](https://github.com/harryhsing/omniagent) | ICML |
| [InternVideo3: Agentify Foundation Models with Multimodal Contextual Reasoning](https://arxiv.org/abs/2606.12195) | InternVideo3 | 2026-06 | - | arXiv |
| [Trust the Right Teacher: Quality-Aware Self-Distillation for GUI Grounding](https://arxiv.org/abs/2606.18101) | - | 2026-06 | - | arXiv |
| [UI-MOPD: Multi-Platform On-Policy Distillation for Continual GUI Agent Learning](https://arxiv.org/abs/2607.04425) | UI-MOPD | 2026-07 | [Code](https://elispectre.github.io/UI-MOPD/) | arXiv |
| [Teach it to stop, not just to click](https://arxiv.org/abs/2607.17136) | Reliability Study | 2026-07 | - | arXiv |
| [Why Does Feedback-Augmented Self-Distillation Fail to Improve Retrieval-Interleaved Search Agents?](https://arxiv.org/abs/2607.17558) | FA-SD | 2026-07 | - | arXiv |
| [MagicSelector: Joint Optimization for Agent Tool Selection via Counterfactual Decomposition and Progressive Reranking](https://arxiv.org/abs/2607.17751) | MagicSelector | 2026-07 | - | arXiv |
| [MAGA: Multi-Platform Self-Fusion of GUI Agents via Structured Action Distillation](https://arxiv.org/abs/2607.29320) | MAGA | 2026-07 | - | arXiv |
| [Distilling Knowledge from Large Language Models into Lightweight Reinforcement Learning Agents for Autonomous Cyber Operations](https://arxiv.org/abs/2607.28826) | - | 2026-07 | - | arXiv |
| [VAD: Attributing Visual Evidence for Target Reconstruction in Multimodal On-Policy Distillation](https://arxiv.org/abs/2607.28590) | VAD | 2026-07 | [Code](https://github.com/DeepExperience/VAD_Multimodal_OPD) | arXiv |

### 🔟 Diagnostics, Theory, Benchmarks and Frameworks

| 📖 Title | 🛠 Benchmark / Method | 📅 Date | 💻 Code | 🏛 Venue |
| --- | --- | --- | --- | --- |
| [Provable Partially Observable Reinforcement Learning with Privileged Information](https://arxiv.org/abs/2412.00985) | Theory | 2024-12 | - | NeurIPS |
| [Revisiting On-Policy Distillation: Empirical Failure Modes and Simple Fixes](https://arxiv.org/abs/2603.25562) | Truncated Reverse KL | 2026-03 | - | arXiv |
| [KDFlow: A User-Friendly and Efficient Knowledge Distillation Framework for Large Language Models](https://arxiv.org/abs/2603.01875) | KDFlow | 2026-03 | [Code](https://github.com/songmzhang/KDFlow) | arXiv |
| [Rethinking On-Policy Distillation of Large Language Models: Phenomenology, Mechanism, and Recipe](https://arxiv.org/abs/2604.13016) | Empirical Study | 2026-04 | [Code](https://github.com/thunlp/OPD) | arXiv |
| [Demystifying OPD: Length Inflation and Stabilization Strategies for Large Language Models](https://arxiv.org/abs/2604.08527) | StableOPD | 2026-04 | - | arXiv |
| [DP-OPD: Differentially Private On-Policy Distillation for Language Models](https://arxiv.org/abs/2604.04461) | DP-OPD | 2026-04 | - | arXiv |
| [Subliminal Transfer of Unsafe Behaviors in AI Agent Distillation](https://arxiv.org/abs/2604.15559) | Safety Study | 2026-04 | - | arXiv |
| [Healthcare AI GYM for Medical Agents](https://arxiv.org/abs/2605.02943) | Healthcare AI GYM | 2026-05 | - | arXiv |
| [Orchard: An Open-Source Agentic Modeling Framework](https://arxiv.org/abs/2605.15040) | Orchard | 2026-05 | - | arXiv |
| [The Many Faces of On-Policy Distillation: Pitfalls, Mechanisms, and Fixes](https://arxiv.org/abs/2605.11182) | Empirical Study | 2026-05 | - | arXiv |
| [Dense Supervision, Sparse Updates: On the Sparsity and Geometry of On-Policy Distillation](https://arxiv.org/abs/2606.13657) | Update Geometry | 2026-06 | [Code](https://github.com/SydCS/OPD-Param-Analysis) | arXiv |
| [Covert Influence Between Language Models](https://arxiv.org/abs/2606.04071) | Safety Study | 2026-06 | - | arXiv |
| [QVal: Cheaply Evaluating Dense Supervision Signals for Long-Horizon LLM Agents](https://arxiv.org/abs/2606.32034) | QVal | 2026-06 | - | arXiv |
| [MMG2Skill: Can Agents Distill In-the-Wild Guides into Self-Evolving Skills?](https://arxiv.org/abs/2606.01993) | MMG2Skill | 2026-06 | [Code](https://github.com/NJU-LINK/MMG2Skill) | arXiv |
| [DeepSearch-World: Self-Distillation for Deep Search Agents in a Verifiable Environment](https://arxiv.org/abs/2607.07820) | DeepSearch-World | 2026-07 | - | arXiv |
| [EasyOPD: An Easy-to-use On-Policy Distillation Framework for Large Language Models](https://arxiv.org/abs/2607.11012) | EasyOPD | 2026-07 | - | arXiv |
| [On-Policy Distillation for LLM Safety: A Routing Approach to Template-Robust Realignment](https://arxiv.org/abs/2607.27081) | ROPD | 2026-07 | - | arXiv |

---

## 🤝 Contributing

- Found a paper, benchmark, or codebase that is missing? Open a pull request or an issue.
- Spotted wrong metadata (venue, date, method name, broken link)? Corrections are very welcome.
- Have a suggestion for the taxonomy — a category to split, merge, or add? Please open an issue to discuss.
- Papers may appear under more than one category when they contribute along multiple axes.
- Metadata provenance: every title and date is taken from the arXiv API; `🏛 Venue` is only set to a conference when the paper's own arXiv `comment`/`journal_ref` states the acceptance, otherwise it stays `arXiv`; every `💻 Code` link is one announced in the paper itself and returned HTTP 200 at indexing time.

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Zenghuang-Fu/Awesome-Agentic-OPD&type=Date)](https://star-history.com/#Zenghuang-Fu/Awesome-Agentic-OPD&Date)

---

## 📌 Citation

If you find this repository useful, please consider citing it:

```bibtex
@misc{awesome-agentic-opd,
  title        = {Awesome-Agentic-OPD: A Curated List of On-Policy Distillation and On-Policy Self-Distillation for Agentic RL},
  author       = {Zenghuang Fu},
  year         = {2026},
  howpublished = {\url{https://github.com/Zenghuang-Fu/Awesome-Agentic-OPD}}
}
```
