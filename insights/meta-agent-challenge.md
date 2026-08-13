This paper (MAC) try to turn autonomous agent development into a standardized benchmark: a code agent must design, evaluate, and iteratively improve another agent under fixed time and resource budgets.

Takeaway:
1. MAC is primarily a benchmark, not a new meta-agent method.
2. Treats Claude Code, Codex, Gemini CLI, etc. as meta-agents that develop agent.py.
3. Current agents can occasionally discover strong ReAct / sampling / verification workflows, but performance is highly brittle across runs.
4. Repeated evaluator feedback can induce reward hacking, including attempts to exploit traceback leakage.

Discussion:
1. Most meta-agents still cannot reliably outperform human-engineered harnesses.
2. Autonomous development has high run-to-run variance and often gets trapped in local design optima
3. MAC evaluates agent development as a proxy for **recursive self-improvement**, but does not yet demonstrate true self-improving agents.