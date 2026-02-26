# Metadata for natureupclose_data.csv

## Overview
- Metadata for a randomized controlled experiment assessing how nature-focused activities affect connectedness to nature and wellbeing.
- Recruited 1,295 participants; assigned to six groups (two citizen science, one nature-noticing, two combined groups, and a wait-list control).
- Intervention: ten-minute activities, five times over eight days, in nature-adjacent locations; post-participation survey after eight days.
- Outcome-oriented dataset includes pre- and post-participation survey data for 500 participants who met inclusion criteria (full participants).

## Study design and participants
- Design: randomized controlled exercise with six conditions:
  - pollinator (citizen science)
  - butterfly (citizen science)
  - noticingnature (3GTiN)
  - combinedpollinator (pollinator + noticing nature)
  - combinedbutterfly (butterfly + noticing nature)
  - acontrol (wait-list control)
- Inclusion: 500 participants completed post-survey and fulfilled criteria for inclusion as full participants (Participant == 1).
- Data collection: pre-participation survey (1295 respondents) and post-participation survey (500 participants).

## Data structure and key variables
- Identifiers and timing:
  - PersonID, LineSurvey1/ResponseIDSurvey1/DateSurvey1 (pre), LineSurvey2/ResponseIDSurvey2/DateSurvey2 (post)
  - Condition and conditiontext describing group assignment (six groups)
- Core psychological and wellbeing measures (pre and post):
  - INS_pre / INS_post: Inclusion of Nature in Self scale (1–7)
  - NR6sum_pre / NR6sum_post: Sum of Nature Relatedness 6 items (1–5 per item; note: sum, not mean)
  - SatisfiedWithLife_pre / _post: 11-point scale for life satisfaction
  - WorthwhileLife_pre / _post: 11-point scale for perceived life worth
  - Health_pre / Health_post: single-item 1–5 scale (Poor to Excellent)
  - Happiness_pre / Happiness_post: 11-point scale for general happiness
  - PROCOBScivilaction_pre / _post: sum of civil-action related items (4 items)
  - PROCOBSgarden_pre / _post: sum of gardening-related items (4 items)
  - PROCOBS_pre / _post: sum of eight items across gardening and civil action
- Demographics and context:
  - Age, Age_comments
  - Sex (female, male, other, prefer not to say)
  - Ethnicgroup (White, Asian/Asian British, Black/Black British, Mixed, Other, Prefer not to say)
  - spendtimeoutsideatleastafewtimesperweek (monthly outside time)
  - postcode (district, e.g., "OX10"); latitude/longitude available if UK postcode provided
  - IMD (median and mean IMD across postcode district) for deprivation context
- Engagement and qualitative data:
  - Engagementwiththetask: self-rated engagement level (0–3)
  - 37–42: responses to how participants found taking part (Likert 1–5)
  - Timespentoutsideduringthetask: outside time during the task (0–4)
  - Howmanytimesdidyoudotheactivities: number of times activities were performed (0–6)
  - Open-question responses and thematic analyses (Whatyou liked/about taking part; What you didn’t like), with themes such as noticing nature, intrinsic benefits, contributing, learning, social connections, etc. (lines 46–61 and 53–61)
- Miscellaneous:
  - Median_IMD_postcodedistrict, Mean_IMD_postcodedistrict
  - latitude, longitude (derived from postcode district when available)

## Grouping and interventions
- Condition types and recoded labels:
  - citsci: citizen science activities
  - noticingnature: 3GTiN nature-noticing activity
  - combined: combined citizen science and noticing nature
  - control: wait-list control
- Open-text responses analyzed thematically to identify aspects participants liked or disliked, with subthemes (noticing nature, intrinsic benefits, contributing, learning, social connections, other).

## Data quality, limitations, and use
- Missing data indicated by blank cells.
- PRE/POST structure enables assessment of change across multiple psychological and wellbeing metrics.
- NR6sum is a sum (not the mean); users should divide by six to convert to the Nisbet & Zelenski (2013) mean if needed.
- Geography: Postcode-based location data supplemented by deprivation metrics and coordinates when available; geographic context supports environmental health monitoring analyses.
- Caution for analysts: results pertain to five to eight-day nature-based activities and may not generalize beyond short-term interventions; consider group differences when integrating across activity types.

## Relevance for environmental monitoring and policy
- Demonstrates how standardized environmental-behavioral data (nature relatedness, wellbeing, pro-nature behaviors) can be collected alongside engagement metrics in nature-based interventions.
- Provides a structured dataset suitable for longitudinal-like comparisons (pre vs. post) and cross-group analyses to inform policy on nature engagement programs.
- Emphasizes data quality and accessibility by including a broad range of standardized scales, demographic context, and openness to data reuse (storage/portal-ready metadata).

## Notes for analysts
- Ensure correct interpretation of scale types and the NR6sum adjustment if comparing to published means.
- Leverage deprivation and geographic context (IMD, latitude/longitude) to explore environmental equity implications.
- Use engagement and qualitative themes to contextualize quantitative changes in wellbeing and nature connectedness.
- When aggregating across groups, account for the six-group design (two citizen-science groups, two noticing-nature groups, two combined groups, plus control).