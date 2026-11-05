# APT-EviRank

**APT Evidence-based Actor Ranking Dataset**

APT-EviRank supports research on threat actor attribution and evidence analysis using public APT reports. It organizes report observations, entities, relations, provenance, temporal information, and links to supporting text for evidence-based candidate actor ranking.

## Dataset Overview

A corpus of 600 higher-quality reports was selected from 1,843 candidate reports. Automatic extraction, manual selection, and verification were used to construct the following resources:

| Resource | Size | Purpose |
| --- | --- | --- |
| Report corpus | 600 reports | Information extraction, structured data preparation, and graph construction |
| Gold attribution set | 100 reports covering 30 actor classes | Evaluation of candidate actor ranking |
|                      |                                       |                                                              |

Both evaluation sets are drawn from the 600-report corpus. Gold actor labels are manually verified. The entities, relations, temporal information, and supporting text spans used by the attribution model are automatically extracted.

## Tasks and Evaluation

- **Threat actor ranking:** Actor names, aliases, and explicit attribution statements are masked in query reports. Methods rank a fixed set of 30 candidate actors. Metrics include Hit@1/3/5, MRR@5, NDCG@5, and Macro-F1.
- **Information extraction and evidence localization:** Evaluate entity and core relation extraction, together with their links to supporting text.

Attribution experiments use five-fold cross-validation with three random seeds. Historical attribution evidence is restricted to gold-labeled reports in the current training fold that were published before the query report. Candidate ranking and selective release decisions are evaluated separately.

- 
