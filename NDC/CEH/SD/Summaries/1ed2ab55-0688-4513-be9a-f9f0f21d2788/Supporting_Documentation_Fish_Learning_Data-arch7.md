# Bolder stickleback fish make faster decisions, but they are not less accurate.

## Overview
- Investigates the relationship between boldness and decision-making in three-spined sticklebacks (Gasterosteus aculeatus).
- Laboratory study with 47–48 fish across a structured decision task to assess speed (latency) and accuracy, plus learning over trials.
- Data designed for analysis of behavioral traits (boldness, decision speed, accuracy, learning) at the individual and trial levels.

## Subjects, housing, and experimental setup
- Subjects: Laboratory population of 48 sticklebacks captured from the River Cam, UK (Histon and Swaffham Bulbeck), April 2011.
- Housing: Initial holding aquarium; individual testing tanks (2.8 L) in a rack system to standardize water and feeding; groups rotated weekly to equalize exposure.
- Environment: 16 °C; 8:16 light-dark cycle; daily feeding with defrosted bloodworms.
- Post-experiment: Fish returned to holding tank and not reused.

## Boldness assessment
- Two behavioral measures used: (1) proportion of time out of cover (foraging context) and (2) order of capture by an experimenter (predation context).
- Each measure was tested on two occasions; results were correlated and used to create a single boldness index.
- Boldness index calculation:
  - Rank fish for each measure (higher rank for bolder behavior).
  - Sum of the two ranks, divided by 96, producing an index between 0 and 1.
  - Higher values indicate greater boldness (mean 0.48, SE 0.03; median 0.51).

## Decision-making task
- Task design: T-maze with three arms; each trial offered a consistently rewarded arm (left or right) for each fish, while the other arm was empty.
- Acclimation: Fish habituated to the maze in groups (n = 5) for 3 hours, 3 days before trials.
- Trials: 2 trials per day for 2 weeks (18 trials per fish total). One fish died at the start, resulting in 47 fishes for analysis.
- Procedure: Fish started from central arm “start box”; after release, monitored for up to 10 minutes. Water in maze was refreshed between trials.
- Data captured: Myriad of trials across two simultaneous experiments to boost data yield.

## Measures of decision speed and accuracy
- Time to first decision: time from fully leaving the start box to fully entering either end chamber.
- Time to correct decision: time from leaving the start box to entering the rewarded arm.
- Task engagement: counted as the number of trials in which the fish made a decision (entered a chamber); some trials had no decision.
- Accuracy: whether the first choice was correct (rewarded arm).
- Learning score: over consecutive trials, +1 for a correct first decision, -1 for an incorrect first decision; higher positive scores indicate learning toward the reward.

## Data structure and variables
- Data file: One dataset containing all trials.
- Size: 847 rows (including header), 8 columns.
- Columns and meanings:
  - Trial_Number: Trial index.
  - FishID (catchorder): Identifier for each fish based on order caught.
  - Sex: 0 = Female, 1 = Male.
  - Boldness_index: Composite boldness score derived from the two boldness measures.
  - Time_to_First_Decision (log): Log10 of time to make the first decision (seconds).
  - Time_to_Correct_Decision (log): Log10 of time to reach the rewarded arm (seconds).
  - Learning_Score: +1 for correct first decision, -1 for incorrect.
  - Total_number_Trials_Completed: Number of trials completed by the fish.