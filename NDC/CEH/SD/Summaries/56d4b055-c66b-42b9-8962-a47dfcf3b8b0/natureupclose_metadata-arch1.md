# Metadata for natureupclose_data.csv

## What this dataset is
- Metadata for a dataset from a randomised controlled experiment studying the impact of nature-focused activities on connectedness to nature and wellbeing.
- Recruited 1,295 people for pre-participation surveys; 500 participants completed post-participation surveys after engaging in assigned activities or being in a wait-list control.
- Data include pre- and post-participation survey responses, with missing data represented as blank cells.

## Study design and participants
- Randomised controlled design with six groups:
  - pollinator (Pollinator Flower-Insect Timed Counts)
  - butterfly (iRecord Butterfly app)
  - noticingnature (Three Good Things in Nature, 3GTiN)
  - combinedpollinator (pollinator + 3GTiN)
  - combinedbutterfly (butterfly + 3GTiN)
  - acontrol (wait-list control)
- Intervention: ten-minute activities, five times over eight days; post-participation survey administered after eight days.
- Inclusion criterion for “full participants”: completed both pre- and post-surveys and met conditions (N = 500).

## Variables and measures

### Identifiers and timing
- PersonID, ResponseIDSurvey1/2 (pre/post survey identifiers)
- LineSurvey1/LineSurvey2, DateSurvey1/DateSurvey2 (timestamps for surveys)
- Participant (1 = full participant; 0 = not, N(Participant==1) = 500)

### Demographics and group assignment
- Age, Age_comments
- Sex, Ethnicgroup
- postcode (district), latitude, longitude (lat/long provided only for UK postcodes)
- condition, conditiontext, conditiontypetext (group assignment; recoded as citsci, noticingnature, combined, control)

### Key scales and measures (pre and post)
- INS_pre/INS_post: Inclusion of Nature in Self (1–7)
- NR6sum_pre/NR6sum_post: Sum of Nature Relatedness 6 components (1–5 for each item; note: original uses mean; sum should be divided by six to align with Nisbet & Zelenski 2013)
- SatisfiedWithLife_pre/SatisfiedWithLife_post: 11-point scale (0–10)
- WorthwhileLife_pre/WorthwhileLife_post: 0–10 (11-point scale)
- PROCOBScivilaction_pre/post, PROCOBSgarden_pre/post, PROCOBS_pre/post: sums for pro-nature conservation behaviours (eight items total; four civil action, four gardening)
- Health_pre/Health_post: single-item 1–5
- Happiness_pre/Happiness_post: 0–10 (overall happiness)
- 46–52 Open-ended theme codes derived from responses (liketheme_* and disliketheme_*)
  - liketheme_noticingnature, liketheme_intrinsicbenefits, liketheme_contributing, liketheme_learning, liketheme_socialconnections, liketheme_other
  - disliketheme_weather, disliketheme_lackoftime, disliketheme_complexity, disliketheme_technology, disliketheme_lackofsuccess, disliketheme_interferedwithnatureengagement, disliketheme_nothing, disliketheme_other
- 53–59 Open-ended response indicators and themes for what participants liked or disliked

### Engagement and experiential data
- Engagementwiththetask: self-rated engagement (0–3)
- 37–42 Post-participation evaluations (Likert 1–5) about connection to nature, calm/joy, noticing beauty, meaningfulness, helping nature, frustration
- Timespentoutsideduringthetask: outside time during the task (0–4)
- Howmanytimesdidyoudotheactivities: number of times activities were performed (0–6; 6 = more than five times)
- 45 Openquestionanswers: indicator of whether open-ended answers were provided

### Contextual and location data
- Median_IMD_postcodedistrict, Mean_IMD_postcodedistrict: deprivation indices by postcode district
- latitude, longitude: geographic coordinates (only for UK postcodes)

## Data quality and considerations
- Missing data represented as blank cells
- NR6sum is a sum; to compare with the original mean-based approach, divide by six
- Postcode and location data introduce privacy considerations; latitude/longitude provided only for UK postcodes
- Open-ended responses were subjected to thematic analysis and coded into predefined theme categories

## Potential analyses and uses
- Compare pre- and post-participation changes across the six groups on wellbeing, nature connectedness, and pro-nature behaviours
- Examine relationships between nature relatedness (NR6), inclusion of nature in self (INS), life satisfaction, and health
- Assess engagement and experiential responses as mediators or moderators of outcomes
- Use deprivation (IMD) and location data to explore geographic or socio-economic heterogeneity
- Qualitative analysis of themes to complement quantitative findings (noting themes for liking/disliking aspects)

## Source and citation
- Pocock, M.J.O., Hamlin, I., Christelow, J., Passmore, H.-A. & Richardson, M.