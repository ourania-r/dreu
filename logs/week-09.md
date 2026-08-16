# Week 9

**Dates:** 08-10 to 08-16

## Goals

- Present the Shaw (2026) reproduction results and prose-line pre-filter fix to Dr. Zhang.
- Receive feedback and direction on next steps for the research.
- Begin organizing research materials for sharing and publication preparation.

## Approach and Implementation

Presented the Week 9 findings to Dr. Zhang on Thursday, covering three deliverables: the full reproduction of Shaw's evaluation results, the root cause analysis of the 71.98% precision gap, and the prose-line pre-filter fix. The reproduction confirmed an exact match with Shaw's published figures: 71.98% precision, 100% recall, 83.71% F1, verified by running Shaw's own evaluation script against his published labeled sample and pre-computed audit results. The root cause analysis broke the 110 FP-Context false positives into three categories: pure documentation prose (30 cases, easiest), string constant assignments (~21 cases, moderate), and genuine context ambiguity (~60 cases, hardest). The prose-line pre-filter targeted the easiest category, eliminating 30 false positives while retaining zero true positives, raising precision to 77.60% and F1 to 87.39% with recall preserved at 100%.

Dr. Zhang was pleased with the results, particularly that the reproduction matched Shaw's paper exactly and that the fix improved precision while keeping recall at 100% as planned.

Direction from Dr. Zhang for the coming weeks: upload everything to the shared Google Drive folder including screenshots, as this was originally due last week but was delayed due to a permissions issue that has since been resolved. Create a private GitHub repository containing all new source code and testing results, with zhangl64 added as a contributor, to ensure the work is tracked and reproducible. The repository will be made public once the paper publishes, at which point results need to be fully reproducible since the community will scrutinize them. The research is targeting a workshop paper, currently still in the experiment phase, with a target completion window of September to October.

## Results

- Reproduction confirmed: exact match with Shaw (2026): 71.98% precision, 100% recall, 83.71% F1.
- Root cause identified and categorized into three buckets by difficulty.
- Prose-line pre-filter implemented and tested: precision 71.98% to 77.60%, recall held at 100%, F1 83.71% to 87.39%, zero true positives lost.
- Dr. Zhang confirmed the direction and expressed satisfaction with the results.

## Notes

- Google Drive upload pending; permissions issue now resolved, upload to happen immediately.
- Private GitHub repo to be created with zhangl64 as contributor; will go public upon paper publication.
- Source code and evaluation results must be fully traceable and reproducible on the repo.
- Target venue: workshop paper, experiment phase ongoing, completion target September to October.
- Next root cause to address: string constant assignments (~21 cases), prompt-level fix, moderate effort.
