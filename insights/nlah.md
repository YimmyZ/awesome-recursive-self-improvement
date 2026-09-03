Title — Natural-Language Agent Harnesses

  What is the paper about? — The paper introduces Natural-Language Agent Harnesses (NLAHs), editable documents that encode run-level harness policies, and an Intelligent Harness Runtime (IHR) that realizes those policies through agent calls, handoffs, state updates, validation gates, and artifact contracts.

  Novelty of this paper — Its main novelty is treating high-level harness policy as a first-class executable and ablatable natural-language representation while retaining precision-critical mechanisms such as tools, parsers, validators, and sandboxing in code.

  - Strength — The paper compares code harnesses, prompted NLAHs, and IHR-executed NLAHs across coding, terminal-use, and computer-use benchmarks, supplementing task scores with mechanism audits and module-level ablations.

  - future work — The comparisons do not fully isolate the effect of the NLAH representation because conditions differ substantially in calls and token usage, rely on a single runtime-model configuration, and include a code baseline evaluated outside the model environment for which it was opt  imized.

  - conclusion: treat the harness as an explicit, modular research object and argue that end-to-end pass rates should be supplemented with evidence that the intended harness mechanisms were actually realized.
