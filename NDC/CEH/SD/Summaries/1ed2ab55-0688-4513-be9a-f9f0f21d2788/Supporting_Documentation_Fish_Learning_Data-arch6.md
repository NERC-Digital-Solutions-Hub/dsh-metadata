# Bolder stickleback fish make faster decisions, but they are not less accurate.

## Study design and subjects
- Laboratory population of 48 three-spined sticklebacks (G. aculeatus) collected April 2011 from Histon and Swaffham Bulbeck, UK.
- Initial housing: holding aquarium with plants, 16°C, 8:16 h light/dark cycle, fed defrosted bloodworms daily.
- Experimental housing: 48 individual 2.8-L tanks in a rack system (to control water and feeding conditions; positions rotated weekly).
- Sample size adjusted to 47 after one death at trial start.

## Boldness assessment
- Assessed before the decision task using two measures: (1) proportion of time spent out of cover (foraging context) and (2) catch order (predation context).
- Both measures were repeatable and males tended to score higher.
- Boldness index computation:
  - Rank each fish for both measures (higher boldness gets higher rank: 48 to 1).
  - Sum the two ranks and divide by 96 to yield a 0–1 index (mean ≈ 0.48; median ≈ 0.51).

## Decision-making task
- Maze: a T-maze constructed from opaque gray plastic; each arm had a removable panel and a visible end chamber to identify choices.
- Trials: two experiments run simultaneously (n = 47 after one death) to maximize data yield; 2 trials per day per fish for 2 weeks, totaling 18 trials per fish.
- Acclimation: groups of five allowed to acclimate to the maze for 3 hours on three days prior to testing.
- Reward: bloodworm consistently located in either the left or right arm per fish (left n=24; right n=23; alternating by fish); randomized order of trials within days.
- Trial procedure: start box in center; fish allowed 10 minutes in maze; maze cleaned between trials.
- Data collected per trial:
  - Time to first decision: time from leaving start box to entering either end chamber.
  - Time to correct decision: time from leaving start box to entering the arm containing the reward.
  - Decision engagement: whether a decision was made in a trial (some trials had no decision; a median of 3 out of 18 had no decision).
  - Accuracy: whether the first decision was correct.
  - Learning score: +1 for a correct first decision, -1 for an incorrect first decision across consecutive trials (positive indicates learning; 0 indicates chance; negative indicates repeated wrong choices).

## Data collection and quality
- Data captured via two video cameras positioned above the mazes.
- Weekend breaks (two days) did not significantly affect results; full results shown for all 18 trials per fish.
- Time measures are log-transformed (log10 seconds) to normalize distributions.

## Data structure and file contents
- Data file: single file with 847 rows (plus header) and 8 columns.
- Columns and meanings:
  - Trial_Number: trial identifier.
  - FishID (catchorder): ID assigned based on the order fish were caught.
  - Sex: 0 = Female, 1 = Male.
  - Boldness_index: 0–1 index derived from time-out-of-cover and catch order.
  - Time_to_First_Decision (log): log10 of time to make the first decision (seconds).
  - Time_to_Correct_Decision (log): log10 of time to enter the rewarded arm.
  - Learning_Score: +1 for a correct first decision, -1 for an incorrect one (across trials).
  - Total_number_Trials_Completed: number of trials in which a decision was made.

## Notes for data users
- The dataset enables analysis of relationships between boldness and decision speed/accuracy, as well as learning across repeated trials.
- Transformations and trial-level engagement should be considered when modeling, given the presence of non-decisions in several trials.