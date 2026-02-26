# Bolder stickleback fish make faster decisions, but they are not less accurate.

## Aim
- Investigate whether boldness is related to decision speed and accuracy in a controlled decision-making task using three-spined sticklebacks.

## Subjects and housing
- 48 Gasterosteus aculeatus (three-spined sticklebacks) net-caught Apr 2011 from the River Cam, UK.
- Housed in a holding aquarium; during experiments, 47 remained (one died at start).
- Individual 2.8 L tanks within a rack system; same water conditions and feeding.
- Temperature: 16°C; light cycle 8:16 h; acclimation period with grouped exposure before trials.

## Boldness assessment
- Two prior behavioral measures: proportion of time spent out of cover (foraging context) and catch order (predation context).
- These measures were correlated; a boldness index was created by ranking each measure, summing ranks, and scaling to produce a 0–1 index (1 = boldest).

## Decision-making task
- T-maze task with a consistent food reward placed in either left or right arm, depending on the fish’s experimental condition.
- Two experiments run simultaneously; groups acclimated in groups for 3 hours prior to testing, then 3 days of testing.
- Trials: each fish performed up to 18 trials across ~2 weeks (2 trials per day, weekdays separated by a weekend break; no significant weekend effect found).
- Encountered mortality reduced sample to 47.
- Upon each trial, fish started from a central “start box,” then had up to 10 minutes to choose a chamber.

## Measures of decision speed and accuracy
- Time to first decision: time from leaving start box to entering either end chamber (log10(seconds)).
- Time to correct decision: time from leaving start box to entering the rewarded arm (log10(seconds)).
- Task engagement: number of trials in which a fish made a decision.
- Accuracy: whether the first choice was the correct (rewarded) arm.
- Learning score: +1 if the first decision was correct on a trial, -1 if incorrect; positive scores indicate learning toward the reward, 0 indicates chance, negative indicates repeated incorrect choices.

## Data structure
- One data file comprising 847 rows (plus header) and 8 columns.
- Columns and descriptions:
  - Trial_Number: trial identifier
  - FishID (catchorder): ID based on order fish were caught
  - Sex: 0 = Female, 1 = Male
  - Boldness_index: composite boldness measure (0–1)
  - Time_to_First_Decision (log): log10(seconds) to first decision
  - Time_to_Correct_Decision (log): log10(seconds) to correct decision
  - Learning_Score: +1 for correct first decision, -1 for incorrect
  - Total_number_Trials_Completed: number of trials completed by the fish

## Notes on data collection and quality
- Video recording used to capture decisions; maze dimensions and layout specified.
- Data include transformation to log scale for reaction times and a derived learning metric to capture learning progression.
- Minor attrition due to a death; weekend break analyzed and found not to affect results.