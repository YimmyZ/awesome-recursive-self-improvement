# Awesome Recursive-Self-Improvement

> A curated bibliography of research on agent-harness optimization, model self-improvement, model-harness co-evolution, and rigorous evaluation of adaptive agents.
>
> Last updated: **2026-09-03**

<p align="center">
  <b>Harness Engineering · Inference-Time Adaptation · Model Self-Improvement · Co-Evolution · Evaluation</b>
</p>

---

## Scope and Taxonomy

An **agent harness** is the model-external system that constructs context, manages state and memory, exposes tools, coordinates execution, performs verification, and enforces runtime policy. This list groups papers by their **primary optimization target**, rather than by terminology such as *learning*, *RL*, or *evolution*. Each paper appears once; important secondary mechanisms are summarized in its description.

| Category | Primary state updated | Inclusion criterion |
| --- | --- | --- |
| **Harness optimization** | Prompts, context, memory, tools, skills, workflows, decoding, runtime code, or harness-selection policy | The task model's weights remain fixed during the reported improvement loop |
| **Model optimization** | Task-model parameters | The model is updated through SFT, RL, self-training, or another learning rule without joint harness optimization |
| **Model-harness co-evolution** | Harness state and model parameters | Both are updated through a coupled, joint, or alternating process |
| **Evaluation and benchmarks** | Evaluation protocol, task suite, or diagnostic evidence | The principal contribution measures, audits, or benchmarks improvement claims |

## Contents

- [1. Harness Optimization](#1-harness-optimization)
  - [1.1 Foundations, Engineering, Diagnosis, and Recovery](#11-foundations-engineering-diagnosis-and-recovery)
  - [1.2 Automated and Self-Evolving Harnesses](#12-automated-and-self-evolving-harnesses)
  - [1.3 Prompt, Logit, Memory, Retrieval, and Skill Enhancement](#13-prompt-logit-memory-retrieval-and-skill-enhancement)
  - [1.4 Tool, Workflow, and Agent-Architecture Optimization](#14-tool-workflow-and-agent-architecture-optimization)
  - [1.5 Harness Selection and Generalization](#15-harness-selection-and-generalization)
- [2. Model Optimization](#2-model-optimization)
  - [2.1 Self-Adaptation, Reinforcement Learning, and Post-Training](#21-self-adaptation-reinforcement-learning-and-post-training)
- [3. Model-Harness Co-Evolution](#3-model-harness-co-evolution)
  - [3.1 Joint or Alternating Optimization](#31-joint-or-alternating-optimization)
  - [3.2 Harness-Generated Data for Model Improvement](#32-harness-generated-data-for-model-improvement)
- [4. Evaluation, Benchmarks, and Critical Studies](#4-evaluation-benchmarks-and-critical-studies)
  - [4.1 Self-Improvement and Harness Evaluation](#41-self-improvement-and-harness-evaluation)
  - [4.2 General Agent and Coding Benchmarks](#42-general-agent-and-coding-benchmarks)

---

## 1. Harness Optimization

Research that improves the software and inference-time system around a model while keeping the task model's parameters fixed.

### 1.1 Foundations, Engineering, Diagnosis, and Recovery

- **From Failed Trajectories to Reliable LLM Agents: Diagnosing and Repairing Harness Flaws (HarnessFix)** — Maps failed execution evidence to concrete harness artifacts through HTIR, then applies scoped, regression-aware repairs.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2606.06324)

- **Harness Handbook: Making Evolving Agent Harnesses Readable, Navigable, and Editable** — Builds a behavior-centric map from harness behavior to implementation locations to support reliable modification.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.13285) · [GitHub](https://github.com/Ruhan-Wang/Harness_Handbook) · [Project](https://ruhan-wang.github.io/Harness-Handbook/)

- **Code as Agent Harness** — Surveys code as the executable, inspectable, and stateful substrate for agent reasoning, action, memory, tools, and verification.<br>
  `arXiv 2026 · Survey` · [Paper](https://arxiv.org/abs/2605.18747) · [GitHub](https://github.com/YennNing/Awesome-Code-as-Agent-Harness-Papers)

- **Natural-Language Agent Harnesses** — Externalizes run-level harness policy as editable natural-language documents and executes it through a shared runtime that materializes roles, handoffs, state updates, validation gates, and artifact contracts.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2603.25723) · [Insights](./insights/nlah.md) · [GitHub](https://github.com/curated-skills/LinguaClaw)

- **LongHorizon-Harness: Advancing Long-Horizon Agents for Real-World Tasks** — Separates state management, execution, and read-only auditing through a Manage-Execute-Audit loop.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.01964) · [GitHub](https://github.com/AMAP-ML/LongHorizon-Harness)

- **openJiuwen: Beyond Static Harnesses for Long-Horizon Coding Agents** — Provides composable single-agent, delegated-agent, and swarm execution with runtime adaptation around a fixed model policy.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.27969) · [GitHub](https://github.com/openJiuwen-ai)

- **StateM: Reaching 95.3% Raw Accuracy, or a $15 Frontier Run, on Terminal-Bench 2.1 via Harness Scaling** — Uses durable state, checked transitions, recoverable runbooks, and versioned procedures to scale a fixed model's execution.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.15089) · [GitHub](https://github.com/henryqin1997/statem)

- **AgentRewind: Recoverable Execution for Long-Horizon LLM Agents** — Checkpoints aligned agent context and environment state so an agent can rewind and resume after propagated errors.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.14380) · [GitHub](https://github.com/Futuresis/replay-agent-recorder) · [Dataset](https://github.com/Kelvin-Coffee/MettleBench)

### 1.2 Automated and Self-Evolving Harnesses

- **Agentic Harness Engineering: Observability-Driven Automatic Evolution of Coding-Agent Harnesses** — Evolves prompts, tools, middleware, skills, subagents, and memory through component, experience, and decision observability.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2604.25850) · [Insights](./insights/ahe.md) · [GitHub](https://github.com/china-qijizhifeng/agentic-harness-engineering)

- **Meta-Harness: End-to-End Optimization of Model Harnesses** — Searches over harness source code using scores and execution traces from the full history of prior candidates.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2603.28052) · [GitHub](https://github.com/stanford-iris-lab/meta-harness)

- **Self-Harness: Harnesses That Improve Themselves** — Lets an agent mine its own weaknesses, propose minimal model-specific harness edits, and retain them only after regression testing.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2606.09498) · [GitHub](https://github.com/qzzqzzb/Self-Harness)

- **TTHE: Test-Time Harness Evolution** — Adapts executable control programs from unlabeled test-time traces without updating model weights or training an adaptation model.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.08124)

- **Recursive Harness Self-Improvement** — Iteratively refines a prompt-level agent-loop specification using pairwise feedback over its revision history. It implements the harness side, or first half, of a proposed co-evolution loop.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.15524)

- **HARBOR: Automated Harness Optimization** — Formulates harness configuration as constrained, noisy Bayesian optimization over mixed variables and heterogeneous costs.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2604.20938)

- **EvoUndo: Recoverability-Constrained Self-Evolution for LLM Agent Harnesses** — Makes safe reversibility a first-class constraint for model-generated changes to prompts, tools, middleware, resources, and runtime state.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.28363)

- **Verify Smarter, Evolve Further: Efficient Harness Evolution through Behavior-Aware Verification** — HarnessLens verifies proposed harness changes only on behavior-relevant tasks and gates them with attributable evidence.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.27311) · [GitHub](https://github.com/jhxu5214/HarnessLens)

- **JIT-Agent: Scaling Harness Intelligence via Just-in-Time Harness Evolution** — Trains a dedicated harness-intelligence model to generate, repair, and evolve task-adaptive harnesses for off-the-shelf agents.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.25593) · [GitHub](https://github.com/bingreeky/JIT)

- **StarHarness: Evolving Harnesses with Stratified Search for Enterprise Environments** — Evolves prompts, tools, skills, providers, subagents, and loop settings over stratified tasks while holding model weights fixed.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.24804) · [GitHub](https://github.com/ServiceNow/StarHarness)

- **Harness Continual Learning: Continual Adaptation Beyond Model Parameters** — Treats prompts, memory, capability maps, and routing as continually learned state and guards updates against harness-level forgetting.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.19013)

- **Evo-Harness: Context-to-Harness Skill Compilation for Self-Evolving Agents** — Compiles noisy one-shot execution contexts into reusable skills for a frozen agent and validates cross-task adaptation.<br>
  `EMNLP 2026 · Main` · [Paper](https://arxiv.org/abs/2608.15071) · [GitHub](https://github.com/A-EVO-Lab/a-evolve/tree/release/evo-harness)

- **Darwin Gödel Machine: Open-Ended Evolution of Self-Improving Agents** — Maintains an archive of coding agents that modify their own source and empirically validates offspring while the underlying foundation model remains frozen.<br>
  `ICLR 2026 · Oral` · [Paper](https://arxiv.org/abs/2505.22954) · [GitHub](https://github.com/jennyzzt/dgm)

### 1.3 Prompt, Logit, Memory, Retrieval, and Skill Enhancement

- **Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates (JitRL)** — Retrieves trajectories from dynamic non-parametric memory, estimates action advantages, and directly adjusts output logits without weight updates.<br>
  `ICML 2026` · [Paper](https://arxiv.org/abs/2601.18510) · [GitHub](https://github.com/liushiliushi/JitRL)

- **Recursive Experiential-Working Memory Evolution for Long-Horizon Agent Harnesses** — Recuris couples working memory with experiential skill memory and uses localized, validation-gated skill updates over time.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.24876) · [GitHub](https://github.com/Gen-Verse/Recuris)

- **EvolveR: Self-Evolving LLM Agents through an Experience-Driven Lifecycle** — Distills interaction trajectories into reusable strategic principles, retrieves them online, and continually curates their measured utility.<br>
  `arXiv 2025` · [Paper](https://arxiv.org/abs/2510.16079) · [GitHub](https://github.com/Edaizi/EvolveR)

- **SPARKLE: A Structured and Plug-and-play Agentic Retrieval Policy for Adaptive RAG Models** — Trains an external proxy policy with RL to control retrieval while treating the retriever and task LLM as the environment.<br>
  `ACL 2026 · Long Paper` · [Paper](https://aclanthology.org/2026.acl-long.1793/) · [GitHub](https://github.com/jyfang6/sparkle)

- **The Missing Piece in Pre-trained Model Evaluation: Reward-Guided Decoding Unlocks Task-Oriented Behavior Without Parameter Updates** — Uses an external reward model to steer frozen-model decoding toward high-utility responses without post-training.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2605.28020)

### 1.4 Tool, Workflow, and Agent-Architecture Optimization

- **GPTSwarm: Language Agents as Optimizable Graphs** — Represents agents as computational graphs and optimizes both node prompts and inter-agent graph connectivity.<br>
  `ICML 2024 · Oral` · [Paper](https://proceedings.mlr.press/v235/zhuge24a.html) · [GitHub](https://github.com/metauto-ai/gptswarm)

- **Large Language Models as Tool Makers (LATM)** — Splits tool creation from tool use so a stronger model can build and cache reusable Python tools for cheaper models.<br>
  `ICLR 2024` · [Paper](https://arxiv.org/abs/2305.17126) · [GitHub](https://github.com/ctlllll/LLM-ToolMaker)

- **EvoAgentX: An Automated Framework for Evolving Agentic Workflows** — Provides a framework for representing, evaluating, and automatically evolving multi-agent workflows.<br>
  `EMNLP 2025 · System Demonstrations` · [Paper](https://aclanthology.org/2025.emnlp-demos.47/) · [GitHub](https://github.com/EvoAgentX/EvoAgentX)

- **EvoFSM: Controllable Self-Evolution for Deep Research with Finite State Machines** — Evolves constrained state-transition flows, state-specific skills, and memory instead of free-form workflow code.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2601.09465)

- **SE-Agent: Self-Evolution Trajectory Optimization in Multi-Step Reasoning with LLM-Based Agents** — Revises, recombines, and refines prior trajectories to expand the inference-time reasoning search space.<br>
  `NeurIPS 2025` · [Paper](https://arxiv.org/abs/2508.02085) · [GitHub](https://github.com/JARVIS-Xs/SE-Agent)

### 1.5 Harness Selection and Generalization

- **Automated Discovery Has No Universally Superior Harness** — Decomposes discovery harnesses into search components and shows that harness choice is model- and problem-dependent; it also studies adaptive budget reallocation from early signals.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.18235) · [Insights](./insights/auto-openevolve.md) · [GitHub](https://github.com/akshat57/harness-generalization)

---

## 2. Model Optimization

Research whose primary persistent state is the task model's parameters, without jointly evolving the surrounding harness.

### 2.1 Self-Adaptation, Reinforcement Learning, and Post-Training

- **Self-Adapting Language Models (SEAL)** — Lets a model generate its own training data and update directives, then applies gradient-based SFT for persistent weight adaptation; an RL outer loop trains the self-edit policy.<br>
  `NeurIPS 2025` · [Paper](https://arxiv.org/abs/2506.10943) · [Project](https://jyopari.github.io/posts/seal) · [GitHub](https://github.com/Continual-Intelligence/SEAL)

---

## 3. Model-Harness Co-Evolution

Research that closes the loop between evolving harness state and updating model parameters. This section excludes work that only optimizes a harness for several fixed models.

### 3.1 Joint or Alternating Optimization

- **Co-Harness: Co-Evolving Harnesses and Model Weights for LLM Agents** — Alternates localized harness repair with model fine-tuning on high-quality trajectories generated by the improved harness.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.22688)

- **Continual Harness: Online Adaptation for Self-Improving Foundation Agents** — Alternates online prompt, subagent, skill, and memory refinement, then closes the loop by updating an open model from teacher-relabeled harness rollouts.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2605.09998) · [GitHub](https://github.com/sethkarten/continual-harness)

- **Frontis-MA1: Training an AI4AI Model towards Recursive Self-Improvement in Machine Learning Engineering** — Aligns SFT/RL post-training with the same program-evolution operators used by the OpenMLE-Evo search harness.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.28568) · [GitHub](https://github.com/FrontisAI/OpenRSI)

### 3.2 Harness-Generated Data for Model Improvement

- **HELIX: Model-Harness Co-evolution for Recursive Self-Improvement** — Evolves source-traceable harness portfolios that improve execution and generate verified SFT, critic, filter, and preference records for the next model update.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.13951) · [GitHub](https://github.com/HKUDS/HELIX)

---

## 4. Evaluation, Benchmarks, and Critical Studies

Work that primarily evaluates self-improvement claims, exposes failure modes, or supplies environments and verifiers.

### 4.1 Self-Improvement and Harness Evaluation

- **The Meta-Agent Challenge: Are Current Agents Capable of Autonomous Agent Development?** — Evaluates whether a meta-agent can build and iteratively improve another agent under fixed resources and reward-hacking defenses.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2606.04455) · [Insights](./insights/meta-agent-challenge.md) · [GitHub](https://github.com/ant-research/meta-agent-challenge) · [Project](https://meta-agent-challenge.com/)

- **PostTrainBench: Can LLM Agents Automate LLM Post-Training?** — Benchmarks autonomous post-training of a base LLM under a ten-hour, single-GPU compute budget and audits shortcut and reward-hacking behavior.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2603.08640) · [Project](https://posttrainbench.com/)

- **ASPIRE: Can Models Self-Evolve from Vague Goals?** — Tests whether agents can turn underspecified goals into successful self-development processes.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.31111) · [Project](https://self-developing-agents.github.io/)

- **HarnessRisk: A Lifecycle-Oriented Benchmark for Agent Harness Safety** — Evaluates safety risks across the lifecycle of agent harness design, execution, and evolution.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.17597) · [Project](https://baiyajing.github.io/harness-risk/)

- **Rethinking the Evaluation of Harness Evolution for Agents** — Compares harness evolution with budget-matched test-time search and checks whether evolved changes generalize to held-out tasks.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2607.12227) · [GitHub](https://github.com/rethinking-harness-evolution)

- **On the Fragility of Self-Improving Agents: Variance, Task Order, and Underspecification** — Stress-tests memory-based self-improvement across repeated runs and task orderings, exposing variance and hidden curricula.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.18066) · [GitHub](https://github.com/SalesforceAIResearch/self-improve-fragility) · [Dataset](https://huggingface.co/datasets/Salesforce/self-improve-fragility)

- **Demystifying Agent Skills: Why They Work—Until They Don't** — Studies skill representation, retrieval, procedural anchoring, framework transfer, and failure modes instead of reporting aggregate gains alone.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2608.14036)

### 4.2 General Agent and Coding Benchmarks

- **SWE-bench: Can Language Models Resolve Real-World GitHub Issues?** — Evaluates repository-level issue resolution against executable tests from real GitHub projects.<br>
  `ICLR 2024 · Oral` · [Paper](https://arxiv.org/abs/2310.06770) · [GitHub](https://github.com/SWE-bench/SWE-bench) · [Project](https://www.swebench.com/)

- **Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces** — Evaluates agents on long-horizon, verifiable tasks performed in terminal environments.<br>
  `arXiv 2026` · [Paper](https://arxiv.org/abs/2601.11868) · [GitHub](https://github.com/harbor-framework/terminal-bench) · [Project](https://www.tbench.ai/)

- **LiveCodeBench: Holistic and Contamination Free Evaluation of Large Language Models for Code** — Uses time-stamped competitive-programming problems to evaluate generation, repair, execution, and test-output prediction.<br>
  `ICLR 2025` · [Paper](https://arxiv.org/abs/2403.07974) · [Insights](./insights/livecode.md) · [GitHub](https://github.com/LiveCodeBench/LiveCodeBench) · [Project](https://livecodebench.github.io/)

---

## Contributing

Contributions are welcome. Please open an issue or pull request with:

- the paper title and canonical publication link;
- the venue and publication year;
- official code, data, or project links when available;
- a concise description of the primary contribution; and
- the proposed category, determined by the primary state updated during improvement.

Please avoid duplicate entries, non-authoritative mirrors, and claims that are not supported by the cited paper.
