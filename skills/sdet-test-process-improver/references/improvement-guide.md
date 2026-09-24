# Test Process Improvement Guide

## A Small Improvement Cycle

Agree on a goal, understand the current situation, select changes, try them, and learn from the outcome. This adapts the intent of the IDEAL improvement cycle to the size of the team and task. It does not require a large formal program.

Use process data and team observations together. Group defects by a meaningful category before choosing patterns to investigate. Cause-and-effect analysis or repeated why questions can generate hypotheses; they do not prove those hypotheses by themselves.

## Select Useful Measures

Start with the outcome, ask a question, then choose a measure that answers it. For example: to reduce feedback delay, ask how long failures wait for investigation and measure that interval with a consistent start and end event. Include sample size and reporting period. Define the baseline before claiming improvement.

Consider possible side effects. Faster feedback achieved by disabling failing tests can reduce coverage. Fewer recorded defects can reflect less testing or under-reporting. Compare similar scopes and investigate alternative explanations.

## Example

Repeated escaped discount defects occur in combinations of eligibility rules. A supported action might be to pilot decision-table reviews on the next discount changes. Record which rule combinations are reviewed, defects caught before release, review effort, and later escapes. An initial absence of escapes in a small sample is encouraging but does not prove the process problem is solved.

## Output

| Problem and evidence | Proposed change and hypothesis | Trial scope | Responsible role | Success measure | Side-effect check | Review point |
|---|---|---|---|---|---|---|

Explain priority and effort qualitatively unless reliable numbers exist. Keep proposed ownership distinct from agreed ownership. At the review point, document actual outcomes and whether to continue, adjust, expand, or stop.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Management v3.0, sections 1.5.1-1.5.4, pages 38-41: the IDEAL cycle, process improvement models, analytical approaches, goal-question-metric reasoning, and retrospectives. The example and experiment table are project conventions.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.
