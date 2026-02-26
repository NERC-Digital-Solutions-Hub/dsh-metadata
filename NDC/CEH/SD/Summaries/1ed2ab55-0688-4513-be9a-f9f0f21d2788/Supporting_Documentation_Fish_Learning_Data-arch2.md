# Bolder stickleback fish make faster decisions, but they are not less accurate.

## Aim of the study (from the document)

- Investigates how boldness relates to decision speed, accuracy, and learning in a decision-making task (T-maze) using three-spined sticklebacks.

## Subjects and housing

- Species and origin: 3-spined sticklebacks (Gasterosteus aculeatus), n = 48, Net-caught from the River Cam, UK, April 2011.
- Initial housing: Group holding aquarium (120 × 40 × 30 cm) with plants, at 16 °C, 8:16 h light cycle, fed defrosted bloodworms daily.
- Experimental housing: 48 individual 2.8-L tanks in four rows of 12, with rotated positions weekly, allowing social visibility and uniform water/feeding conditions.
- Post-study: Fish returned to holding aquarium and not reused.

## Boldness assessment

- Pre-task behavioral tests to quantify boldness:
  - Proportion of time spent out of cover (foraging context).
  - Order of being net-caught (predation context).
- Findings used to create a boldness index:
  - Each measure ranked (higher for bolder traits), then summed (range 0–96 after normalization) and scaled to 0–1 (higher = bolder; mean ± SE = 0.48 ± 0.03; median = 0.51).
- Important notes: Male fish tended to be bolder and caught sooner; the two measures were correlated across two test days and repeatable over 9 months.

## Decision-making task

- Maze: Transparent 3-arm T-maze with removable panels to limit view of end chambers before entry.
- Setup: Two experiments run concurrently; bloodworm reward positioned consistently in left or right arm per fish (n = 24 left; n = 23 right; alternating).
- Acclimation: Groups of 5 for 3 hours on 3 days prior to trials; 3-hour light adaptation not specified beyond acclimation.
- Trials: Each fish completed 18 trials (2 per day for 9 days; weekend breaks occurred but did not affect results).
- Procedure: Fish placed in start box; allowed 10 minutes to explore; maze cleaned between trials.
- Data collected per trial:
  - Time to first decision: time from leaving start box to entering a chamber (log-transformed).
  - Time to correct decision: time to enter the chamber containing the reward (log-transformed).
  - Task engagement: whether a decision was made on a given trial; 18 total trials per fish.
  - Accuracy: whether the first choice was correct.
  - Learning score: +1 for a correct first decision, -1 for an incorrect first decision; positive values indicate learning toward the reward.

## Measures and data processing

- Derived metrics:
  - Time_to_First_Decision (log10 of seconds).
  - Time_to_Correct_Decision (log10 of seconds).
  - Learning_Score (based on first-decision correctness across trials).
  - Total_number_Trials_Completed per fish (out of 18).
- Data capture:
  - Video recorded for accuracy and timing.
  - Data structure designed for single-file export with 847 rows and 8 columns.
- Data file structure (columns):
  - Trial_Number
  - FishID (catchorder)
  - Sex (0 = Female, 1 = Male)
  - Boldness_index
  - Time_to_First_Decision (log)
  - Time_to_Correct_Decision (log)
  - Learning_Score
  - Total_number_Trials_Completed

## Summary of key design choices

- Standardized environmental conditions and handling to enable cross-fish comparisons.
- Integration of a prior boldness measure with decision-making performance to explore behavioral consistency.
- Use of log-transformed timing data to manage skew in response times.
- Transparent data structure aimed at enabling replication, re-analysis, and cross-study comparability.