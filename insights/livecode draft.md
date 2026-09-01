live code bench

model -> code -> executor -> score.

For each question: $x_{i} = (P_{i},T_{i},S_{i},D_{i})$

$P_i$ is the question descripton.
$T_i$ is the test cases.
$S_i$ is the correct solutions.
$D_i$ is the first releasing time of this question.

The question is from LeetCode, AtCoder, CodeForces, and use the releasing time point for the split.

Livecode bench testing:
| Circumstance | Input | Output | Test What| 
| --- | --- | --- | --- |
| Code Generation | Question description | Entire Program | Vide Coding Ability.|
| Self-Repair | Question + False Code + Failure information | fixed programs | If the failure information can be reused.|
|Code Execution| A program + Input | Program Output | If the model can understand the program execution|
|Test Output Prediction| A question + an Input| Correct Output | If the model can understand the question's logic and test action|


Livecodebench Advantages:
For RSI, the system should know if the modification is the real improvement, but not the false positive improvement.

Livecodebench provides the Environment and Verifier. RSI can modify the harness and model's parameters at the Livecodebench.

Failure -> extract experience -> change system -> next attempt -> Verify


