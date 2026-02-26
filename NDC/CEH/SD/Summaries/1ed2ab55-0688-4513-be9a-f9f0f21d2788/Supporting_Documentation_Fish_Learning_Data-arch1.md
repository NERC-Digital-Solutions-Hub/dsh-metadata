# Bolder stickleback fish make faster decisions, but they are not less accurate.

## Study subjects and housing
- Laboratory population of 48 three-spined sticklebacks (G. aculeatus) collected April 2011 from Histon and Swaffham Bulbeck, River Cam, UK.
- Housed in a holding aquarium (120×40×30 cm) at 16°C with 8:16 h light:dark cycle; fed defrosted bloodworms daily.
- During experiments, housed individually in 2.8-L transparent tanks within a rack system (4 rows × 12 tanks). Conditions and feeding identical across fish.
- One fish died at the start of the decision-making trials; final sample for analyses: 47 fish.

## Boldness assessment
- Assessed prior to the decision task using:
  - Proportion of time spent out of cover (foraging context).
  - Catch order (predation context): order in which fish were net-caught from their aquarium.
- Findings: time out of cover and catch order correlated over two days; males tended to be bolder (higher scores).
- Boldness index created by:
  - Ranking each fish on both measures (higher rank for bolder traits).
  - Summing the two ranks (0–96 range) and dividing by 96 to yield a 0–1 index (1 = boldest).

## Decision-making task
- T-maze: three arms; arms had removable panels with a smaller entrance to control viewing of end-chambers.
- Two experiments run simultaneously to increase data yield; each fish acclimated in groups of five for 3 hours, three days prior to trials.
- Reward: bloodworm consistently placed in either left or right arm per fish (left n=24; right n=23; alternating by fish).
- Trial order within a day randomized; each fish did 2 trials per day for 2 weeks; weekend break included with no significant impact on outcomes; total per fish: 18 trials.
- Trial procedure:
  - Fish placed in start box at center; left in maze for 10 minutes.
  - After each trial, maze washed and refilled with aerated water.
  - If a fish did not find the reward in a trial, it was fed in its tank afterward.

## Measures of decision speed and accuracy
- Time to First Decision: time from leaving the start box to fully entering either end chamber.
- Time to Correct Decision: time from leaving the start box to entering the chamber containing the reward.
- Task engagement: number of trials in which a decision was made; some trials (median) had no decision.
- Accuracy: whether the first decision was to the rewarded arm.
- Learning score: +1 if the first decision on a trial was correct, -1 if incorrect; tracks learning across consecutive trials (positive = learning, 0 = chance, negative = repeated incorrect choices).
- Each fish completed a total of 18 trials.

## Data structure and variables
- Data file: single file with 847 rows (plus header), 8 columns.
- Key columns:
  - Trial_Number: trial index
  - FishID (catchorder): ID assigned by catch order
  - Sex: 0 = Female, 1 = Male
  - Boldness_index: 0–1 index from boldness assessment
  - Time_to_First_Decision (log): log10(seconds) to first decision
  - Time_to_Correct_Decision (log): log10(seconds) to correct decision
  - Learning_Score: +1 for correct first decision, -1 for incorrect
  - Total_number_Trials_Completed: number of trials completed by the fish

## Data-analytic considerations for use
- Transformations: times are log-transformed, enabling linear modeling of speed; consider back-transformation for interpretation.
- Potential analyses:
  - Relationship between Boldness_index and decision speed/accuracy (speed-accuracy trade-offs).
  - Learning trajectories across trials by fish, potentially with mixed-effects models (random intercepts/slopes for FishID).
  - Effects of Sex on boldness, decision metrics, and learning.
  - Influence of Task Engagement on measured performance and learning.
- Data quality and scope:
  - Sample size after attrition: N=47; two experiments run concurrently, which may require accounting for experimental session effects.
  - Data include repeated measures per fish (longitudinal learning data) and cross-sectional traits (boldness, sex).
- Data limitations:
  - Some trials lacked a decision; consider using engagement as a covariate or filtering those trials depending on analysis goals.
  - Boldness index relies on two correlated measures; interpretation assumes these measures capture stable personality trait variants.