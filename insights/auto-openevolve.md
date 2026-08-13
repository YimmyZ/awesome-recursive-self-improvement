Studies how to dynamically allocate inference budget among multiple harness candidates using early trajectory signals.

Takeaway：
1. No single fixed harness consistently performs best across different model–task pairs.
2. Harness effectiveness is highly dependent on the underlying model and task, making harness selection an important decision variable.
3. Partial execution signals can predict future performance before completing the full budget.
4. Adaptive pruning and budget reallocation outperform random fixed-harness selection and unpruned harness ensembles.
5. The main challenge shifts from designing a universally optimal harness to deciding where additional computation should be allocated.

Remaining work:
1. Relies on dense intermediate evaluators, which are unavailable in many real-world agent tasks such as coding agents.
2. Does not address how to estimate future success from partial trajectories under sparse rewards.
3. Treats harnesses as fixed candidates rather than evolving components.
4. Future work could explore trajectory-based prognosis and adaptive co-evolution of harnesses and models.