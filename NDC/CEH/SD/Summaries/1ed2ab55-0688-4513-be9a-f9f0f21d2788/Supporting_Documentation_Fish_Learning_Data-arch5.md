# Bolder stickleback fish make faster decisions, but they are not less accurate.

## Overview and study design
- Population: laboratory-bred 3-spined sticklebacks (Gasterosteus aculeatus), N = 48 at start; net-caught from River Cam, UK (April 2011).
- Housing: initial holding aquarium; individual 2.8-L tanks in a rack system for experiments; identical water and feeding conditions; post-experiment housing in holding tank.
- Boldness assessment (pre-task): two correlated behavioral measures:
  - Proportion of time spent out of cover (foraging context).
  - Catch order (predation context).
  - These were combined into a single Boldness_index (0–1) by ranking each measure, summing ranks, and scaling by 96; higher values = bolder.
- Decision-making task: two simultaneous experiments in a T-maze to study speed and accuracy of decisions to obtain a food reward.
  - Each trial began with the fish in a start box; reward located consistently in left or right arm per fish.
  - Trials: 18 per fish (2 per day for 2 weeks; weekend break included).
  - Data collection: video recording from above; 3 h acclimation to maze prior to testing.
  - Sample note: one fish died at trial start, reducing sample to 47 for analyses.
- Ethical and procedural controls: randomized trial order within a day; daily maze cleaning to avoid cross-contamination.

## Data collected and key measures
- Decision speed and accuracy metrics:
  - Time_to_First_Decision (log10 seconds): time from leaving start box to fully entering either end chamber.
  - Time_to_Correct_Decision (log10 seconds): time to enter the chamber with the reward after leaving the start box.
  - Task engagement: number of trials in which the fish made a decision.
  - Accuracy: whether the first decision was correct.
  - Learning_score: +1 for a correct first decision, -1 for an incorrect first decision across consecutive trials (positive = learning, 0 = chance, negative = maladaptive choices).
- Additional engagement measure: learning trajectory inferred from trial-by-trial first-decision outcomes.
- Experimental structure notes: 2 experiments ran in parallel; 18 trials per fish; some trials lacked a decision, affecting data completeness.

## Data structure and provenance
- Data file: single dataset with 847 rows (including header) and 8 columns.
- Columns and meanings:
  - Trial_Number: identifier for each trial.
  - FishID (catchorder): ID assigned based on order of capture.
  - Sex: 0 = Female, 1 = Male.
  - Boldness_index: derived from proportion of time out of cover and catch order (see Boldness assessment).
  - Time_to_First_Decision (log): log10(seconds) to first decision.
  - Time_to_Correct_Decision (log): log10(seconds) to correct decision.
  - Learning_Score: +1 or -1 per trial as defined above.
  - Total_number_Trials_Completed: number of trials completed by the fish.
- Data lineage and derived variables:
  - Boldness_index calculated via ranking two measures, summing ranks, scaling to 0–1.
  - Time metrics log-transformed for normality considerations in analyses.
- Data accessibility and documentation:
  - Accompanied by supporting documentation detailing variable definitions and calculation methods.
  - Data captured under controlled conditions with consistent reward location and maze configuration.

## Data quality, limitations, and governance considerations
- Sample size and completeness:
  - Final N = 47 due to one death at trial start.
  - Not all trials produced a decision; a median of 3 out of 18 trials lacked a decision per fish.
- Experimental variability:
  - Two simultaneous experiments; potential need for careful data merging and labeling by experiment.
  - Weekend break did not significantly affect measures, per study notes.
- Metadata considerations for data stewards:
  - Clear, explicit column descriptions and derived Boldness_index definition aid reuse.
  - Documentation required for any reanalysis to reproduce the Boldness_index calculation and learning score derivation.
  - Ensure consistent handling of log-transformed time variables and missing decision trials in analyses.
- Potential data governance implications:
  - Reuse requires understanding the two-experiment design and the exact reward-left/right conditioning per fish.
  - Data should be stored with traceable provenance and versioning, given multiple related measures per subject and trial.

## Practical takeaways for data stewardship
- The dataset provides a compact, well-documented structure linking personality trait (boldness) to decision speed/accuracy and learning in a controlled behavioral assay.
- Key reuse opportunities:
  - Analyses of speed–accuracy trade-offs in decision tasks.
  - Exploration of personality–cognition relationships in fish.
  - Longitudinal or cross-task comparisons using the Boldness_index and Learning_Score.
- Recommendations for future sharing:
  - Maintain the single-file structure with 8 clearly described columns.
  - Include the Boldness assessment calculation steps in metadata or supporting docs.
  - Provide a data dictionary and, if possible, a code snippet or notebook to reproduce the derived metrics (Boldness_index, Learning_Score) from raw trial data.