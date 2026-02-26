# Bolder stickleback fish make faster decisions, but they are not less accurate

- Overview
  - Investigates the relationship between boldness and decision-making speed and accuracy in three-spined sticklebacks.
  - Uses a T-maze task to assess decision speed, accuracy, and learning over repeated trials.

- Subjects and housing
  - N = 48 sticklebacks; G. aculeatus; net-caught April 2011 from the River Cam, UK.
  - Fish housed in a holding aquarium, then in 47 individual 2.8-L tanks during experiments.
  - Conditions: 16 °C, 8:16 h light cycle, daily feeding of bloodworms.
  - After the experiment, fish returned to the holding aquarium; no further use.

- Boldness assessment
  - Two measures: proportion of time spent out of cover (foraging context) and order of net-catch (predation context).
  - These measures are correlated and form a single Boldness_index (0–1), where 1 is the boldest.
  - Boldness_index calculation: rank each measure, sum of ranks (0–96), divided by 96.
  - Average boldness in the sample: ~0.48 (SE ~0.03); higher values indicate bolder individuals.

- Decision-making task
  - A three-arm T-maze with a consistent food reward placed in either the left or right arm per fish.
  - Each fish completed up to 18 trials across ~2 weeks; two trials per day, with a 3-hour acclimation per day.
  - Start box in the central arm; after exit, fish could choose left or right chamber.
  - If a fish failed to find the reward in a trial, it was fed in its tank afterward.
  - One fish died at the start, resulting in N = 47 for analyses.
  - Weekend break between testing days did not significantly affect outcomes.

- Measures and data computations
  - Time_to_First_Decision: time from leaving the start box to entering a chamber (log10 seconds).
  - Time_to_Correct_Decision: time to enter the chamber with the reward (log10 seconds).
  - Task engagement: number of trials in which a decision was made.
  - Accuracy: whether the first decision was correct.
  - Learning_score: +1 for a correct first decision, -1 for an incorrect first decision; tracks learning across trials.
  - Total_number_Trials_Completed: total trials per fish.

- Data structure
  - Single data file with 847 rows (including header) and 8 columns.
  - Columns include Trial_Number, FishID (catch order), Sex, Boldness_index, Time_to_First_Decision (log), Time_to_Correct_Decision (log), Learning_Score, Total_number_Trials_Completed.

- Data quality and limitations
  - Sample size reduced to 47 due to one death.
  - Some trials did not result in a decision (marked as non-decision events); handled via engagement measure and learning score.
  - Data collected under standardized conditions with camera-based tracking, enabling precise timing and choice recording.

- Potential analyses and uses for data leaders
  - Examine correlations between Boldness_index and decision speed (Time_to_First_Decision) and accuracy (first-choice correctness).
  - Assess whether bolder individuals show faster decision-making without sacrificing accuracy.
  - Analyze learning trajectories (Learning_score) across trials and their relation to boldness.
  - Explore effects of sex, trial number, and engagement on speed and accuracy.
  - Use the dataset to illustrate data governance: measurement reliability, data transformation (log scales), and handling of incomplete trials.