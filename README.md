# Awesome-Self-Improving-Harness-and-Agents

> A curated list of research on **agent harness engineering**, **self-evolving harnesses**, **automated harness optimization**, and related methods for building reliable and adaptive LLM agents.

<p align="center">
  <b>Harness Engineering · Harness Evolution · Agent Self-Improvement · Software Engineering · Benchmarks</b>
</p>

---

## Contents

- [Harness Software Engineering](#-harness-software-engineering)
- [Self-Evolving Harnesses](#-self-evolving-harnesses)
- [Model–Harness Co-Evolution](#-modelharness-co-evolution)
- [Agent & Workflow Self-Evolution](#-agent--workflow-self-evolution)
- [Related Adaptive Methods](#-related-adaptive-methods)
- [Benchmarks](#-benchmarks)

---

## 🛠 Harness Software Engineering

Research on the **design, representation, diagnosis, repair, and execution architecture** of agent harnesses.

- **From Failed Trajectories to Reliable LLM Agents: Diagnosing and Repairing Harness Flaws (HarnessFix)**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2606.06324) · [Insights](./insights/harnessfix.md)

- **Harness Handbook: Making Evolving Agent Harnesses Readable, Navigable, and Editable**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.13285) · [Insights](./insights/harness-handbook.md) · [GitHub](https://github.com/Ruhan-Wang/Harness_Handbook)

- **Code as Agent Harness**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2605.18747) · [Insights](./insights/code-as-agent-harness.md) · [Project](https://github.com/YennNing/Awesome-Code-as-Agent-Harness-Papers)

- **LongHorizon-Harness: Advancing Long-Horizon Agents for Real-World Tasks**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.01964) · [Insights](./insights/longhorizon-harness.md) · [GitHub](https://github.com/AMAP-ML/LongHorizon-Harness)

---

## 🧬 Self-Evolving Harnesses

Research where the **agent harness itself is automatically searched, optimized, repaired, or evolved** while model weights remain fixed.

- **Agentic Harness Engineering: Observability-Driven Automatic Evolution of Coding-Agent Harnesses**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2604.25850) · [Insights](./insights/agentic-harness-engineering.md) · [GitHub](https://github.com/china-qijizhifeng/agentic-harness-engineering)

- **Meta-Harness: End-to-End Optimization of Model Harnesses**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2603.28052) · [Insights](./insights/meta-harness.md) · [GitHub](https://github.com/stanford-iris-lab/meta-harness)

- **Self-Harness: Harnesses That Improve Themselves**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2606.09498) · [Insights](./insights/self-harness.md) · [GitHub](https://github.com/qzzqzzb/Self-Harness)

- **TTHE: Test-Time Harness Evolution**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.08124) · [Insights](./insights/tthe.md)

- **Recursive Harness Self-Improvement**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.15524) · [Insights](./insights/recursive-harness-self-improvement.md)

- **HARBOR: Automated Harness Optimization**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2604.20938) · [Insights](./insights/harbor.md)

- **RewardHarness: Self-Evolving Agentic Post-Training**
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2605.08703) · [GitHub](https://github.com/TIGER-AI-Lab/RewardHarness) · [Project](https://rewardharness.com)

---

## 🔁 Model–Harness Co-Evolution

Research that goes beyond frozen-model harness optimization and studies **joint or alternating evolution of model parameters and the surrounding harness**.

- **Co-Harness: Co-Evolving Harnesses and Model Weights for LLM Agents**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.22688) · [Insights](./insights/co-harness.md)

- **Continual Harness: Online Adaptation for Self-Improving Foundation Agents**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2605.09998) · [Insights](./insights/continual-harness.md) · [GitHub](https://github.com/sethkarten/continual-harness)

- **Automated Discovery Has No Universally Superior Harness**
  `arXiv 2026` · [Paper](https://arxiv.org/pdf/2607.18235) · [Insights](./insights/auto-openevolve.md) · [GitHub](https://github.com/akshat57/harness-generalization)
---

## 🤖 Agent & Workflow Self-Evolution

Related work that evolves **agent workflows, trajectories, programs, skills, or agentic reasoning processes**, rather than directly focusing on the harness as the primary software artifact.

- **Frontis-MA1: Training an AI4AI Model towards Recursive Self-Improvement in Machine Learning Engineering**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.28568) · [Insights](./insights/frontis-ma1.md) · [GitHub](https://github.com/FrontisAI/OpenRSI)

- **EvoAgentX: An Automated Framework for Evolving Agentic Workflows**  
  `EMNLP 2025 · System Demonstrations` · [Paper](https://aclanthology.org/2025.emnlp-demos.47/) · [Insights](./insights/evoagentx.md) · [GitHub](https://github.com/EvoAgentX/EvoAgentX)

- **EvoFSM: Controllable Self-Evolution for Deep Research with Finite State Machines**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2601.09465) · [Insights](./insights/evofsm.md)

- **SE-Agent: Self-Evolution Trajectory Optimization in Multi-Step Reasoning with LLM-Based Agents**  
  `NeurIPS 2025` · [Paper](https://arxiv.org/abs/2508.02085) · [Insights](./insights/se-agent.md) · [GitHub](https://github.com/JARVIS-Xs/SE-Agent)

---

## 🧭 Related Adaptive Methods

Methods that are not directly harness-evolution systems, but provide useful mechanisms for **training-free adaptation, retrieval control, selection, decoding, or inference-time optimization**.

- **SPARKLE: A Structured and Plug-and-play Agentic Retrieval Policy for Adaptive RAG Models**  
  `ACL 2026 · Long Paper` · [Paper](https://aclanthology.org/2026.acl-long.1793/) · [Insights](./insights/sparkle.md) · [GitHub](https://github.com/jyfang6/sparkle)

- **The Missing Piece in Pre-trained Model Evaluation: Reward-Guided Decoding Unlocks Task-Oriented Behavior Without Parameter Updates**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2605.28020) · [Insights](./insights/reward-guided-decoding.md)

---

## 🧪 Benchmarks

Benchmarks frequently used to evaluate coding agents, agent harnesses, and harness-evolution systems.

- **The Meta-Agent Challenge: Are Current Agents Capable of Autonomous Agent Development?**
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2606.04455) · [Insights](./insights/meta-agent-challenge.md) · [GitHub](https://github.com/ant-research/meta-agent-challenge) · [Project](https://meta-agent-challenge.com/)

- **SWE-bench: Can Language Models Resolve Real-World GitHub Issues?**  
  `ICLR 2024 · Oral` · [Paper](https://arxiv.org/abs/2310.06770) · [Insights](./insights/swe-bench.md) · [GitHub](https://github.com/SWE-bench/SWE-bench) · [Project](https://www.swebench.com/)

- **Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces**  
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2601.11868) · [Insights](./insights/terminal-bench.md) · [GitHub](https://github.com/harbor-framework/terminal-bench) · [Project](https://www.tbench.ai/)

---
