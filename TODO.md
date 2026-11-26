# TODO

- [ ] Save reusable skill evaluation scenarios and pass criteria in the repository.

Purpose: When changing the skill in the future, fixed inputs can be used to check that its behavior meets requirements and prevent previously fixed problems from recurring. Temporary evaluation materials from the current session are located at `/tmp/legal-analysis-mode-review/` and may serve as a starting point for organizing this work, but the formal evaluations must not depend on that temporary directory.

Work remaining:

- Record the inputs, tool and network conditions, expected behavior, and pass and fail criteria for each scenario.
- Cover mode selection, source verification status and citation support relationships, full rewriting when an answer is seriously deficient, confirmation to continue offline, two-stage file handoffs, verification records, and search completion.
- Distinguish workflow tests that do not depend on real legal authorities from legal-content tests that require verification of legal authorities, to avoid using fictional rules in actual legal analysis.
- Explain how to run the evaluations: run the relevant scenarios when changing the corresponding rules; evaluations need not run every time a legal Q&A task is performed.
- Define how evaluation results are recorded, including at least the skill version, run date, model or environment used, pass/fail status, and specific deviations. Maintain the fixed scenarios over time and record run results separately; do not commit every complete output to the repository by default.

This TODO only records future work; a formal evaluation suite and execution mechanism have not yet been established.
