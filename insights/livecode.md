# LiveCodeBench

> Model → Code → Executor → Score

## Problem Representation

Each problem is represented as:

$$
x_i = (P_i, T_i, S_i, D_i),
$$

where:

- $P_i$ is the problem description;
- $T_i$ is the set of test cases;
- $S_i$ is the set of correct solutions; and
- $D_i$ is the problem's initial release date.

The problems come from LeetCode, AtCoder, and Codeforces. Their release dates are used to split the benchmark data.

## Evaluation Settings

| Setting | Input | Output | What It Tests |
| --- | --- | --- | --- |
| Code Generation | Problem description | Complete program | The model's code-generation ability |
| Self-Repair | Problem, incorrect code, and failure information | Repaired program | Whether the model can use failure information to repair code |
| Code Execution | Program and input | Program output | Whether the model can understand program execution |
| Test Output Prediction | Problem and input | Correct output | Whether the model can understand the problem logic and predict its behavior |

## Advantages for Recursive Self-Improvement

For recursive self-improvement (RSI), the system must determine whether a modification produces a genuine improvement rather than a false positive.

LiveCodeBench provides an execution environment and a verifier. An RSI system can modify the harness or the model's parameters and then evaluate those changes on the benchmark.

The improvement loop is:

> Failure → Extract experience → Change the system → Try again → Verify
