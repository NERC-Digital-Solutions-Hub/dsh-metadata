# Metadata for natureupclose_data.csv

## Overview
- Metadata for a dataset from a randomised controlled experiment on nature-focused activities and their impact on connectedness to nature and wellbeing.
- Recruited 1,295 participants for pre-participation surveys; randomized into six groups; 500 participants completed post-participation survey and met inclusion as full participants.
- Data include pre- and post-participation survey responses; missing data represented by blank cells.

## Study Design and Sample
- Randomised controlled design with six groups:
  - pollinator
  - butterfly
  - noticingnature
  - combinedpollinator
  - combinedbutterfly
  - acontrol (wait-list control)
- Intervention for non-control groups: ten-minute nature activities five times over eight days (locations near nature).
- Control group: wait-listed; post-participation survey only.
- Sample sizes:
  - Pre-participation: 1,295
  - Post-participation/full participants: 500
- Key identifiers:
  - PersonID, LineSurvey1/LineSurvey2, ResponseIDSurvey1/2, DateSurvey1/DateSurvey2
  - Participant flag: 1 = full participant (N=500)

## Data Content and Structure
- Contains both pre- and post-participation survey data.
- Demographics and background:
  - Age, Sex, Ethnicgroup, postcode (district), latitude/longitude (if UK postcode provided), IMD indicators (Median/Mean IMD for postcode district)
- Primary psychometric and wellbeing measures:
  - INS_pre / INS_post (Nature Relatedness: Inclusion of Nature in Self; scale 1–7)
  - NR6sum_pre / NR6sum_post (sum of six NR6 components; note: original usage uses mean)
  - SatisfiedWithLife_pre / _post (0–10, 11-point wellbeing scale)
  - WorthwhileLife_pre / _post (0–10, 11-point)
  - PROCOBScivilaction_pre / post; PROCOBSgarden_pre / post; PROCOBS_pre / post (pro-nature conservation behaviours; 8 items total; 1–7 scale)
  - Health_pre / Health_post (1–5)
  - Happiness_pre / Happiness_post (0–10)
- Activity engagement and experience:
  - Engagementwiththetask (0–3)
  - Post-participation response ratings (37–42): perceptual items about engagement, calm/joy, closeness to nature, meaning, helping nature, frustration (scale 1–5 for some items; 0–3 for engagement)
  - Timespentoutsideduringthetask (0–4 scale)
  - Howmanytimesdidyoudotheactivities (0–6 scale)
- Open-ended response data and thematic coding (qualitative components):
  - Openquestionanswers; subsequent thematic codes:
    - liketheme_noticingnature
    - liketheme_intrinsicbenefits
    - liketheme_contributing
    - liketheme_learning
    - liketheme_socialconnections
    - liketheme_other
    - disliketheme_weather
    - disliketheme_lackoftime
    - disliketheme_complexity
    - disliketheme_technology
    - disliketheme_lackofsuccess
    - disliketheme_interferedwithnatureengagement
    - disliketheme_nothing
    - disliketheme_other
- Miscellaneous:
  - Condition and conditiontext: six groups (pollinator, butterfly, noticingnature, combinedpollinator, combinedbutterfly, acontrol)
  - conditiontypetext: recoded categories (citsci, noticingnature, combined, control)
  - 62–65: Median_IMD_postcodedistrict, Mean_IMD_postcodedistrict, latitude, longitude

## Key Variables and Scales (Selection)
- INS_pre / INS_post: 1–7 scale for nature inclusion in self (Nature Relatedness)
- NR6sum_pre / NR6sum_post: sum of six NR components (use mean for compatibility with Nisbet & Zelenski 2013)
- PROCOBS_pre / PROCOBS_post: eight pro-nature behaviours; two components include PROCOBScivilaction and PROCOBSgarden (7-point scale for each item)
- Health_pre / Health_post: 1–5
- Happiness_pre / Happiness_post: 0–10
- Age, Sex, Ethnicgroup: demographic factors
- Postcode-related measures: IMD, latitude, longitude
- Engagementand experience metrics: engagement (0–3), Likert-style responses (1–5), time spent outside, number of times activities completed

## Data Quality and Cleaning Notes
- Missing data are represented by blank cells.
- NR6sum is a sum; to align with the referenced paper, divide by six to obtain the mean equivalent.
- Postcode data may not be provided for non-UK entries; latitude/longitude provided only when UK postcode district is present.
- Open-ended responses are qualitatively coded into thematic categories for downstream analysis.

## Derived Measures and Computations
- Change scores: post minus pre for INS, NR6sum, SatisfiedWithLife, WorthwhileLife, PROCOBS composites, Health, Happiness.
- Group comparisons: standard experimental contrasts across six conditions (pollinator, butterfly, noticingnature, combined variants, control).
- Integration with geospatial indicators: IMD, latitude/longitude for area-level context.

## Open-Ended Responses and Themes
- Qualitative data captured via structured theme coding:
  - Positive themes: noticing nature, intrinsic benefits, contributing, learning, social connections, other
  - Negative themes: weather, time constraints, complexity, technology issues, lack of success, interference with nature engagement, nothing, other
- Useful for understanding user-perceived benefits and barriers to participation and for enriching quantitative findings with context.

## Demographics and Geography
- Demographic coverage includes age, sex, ethnicity, and UK postcode districts (where provided).
- Geographic indicators include median/mean IMD by postcode district and latitude/longitude for spatial analyses or mapping.

## Potential Analyses and Outputs
- Descriptive summaries of pre/post measures by group.
- Within-subject analyses of change from pre to post for key scales.
- Between-group comparisons to assess impact of different nature activities.
- Integration of qualitative themes with quantitative findings (mixed-methods insights).
- Dashboards or reports enabling end users to self-serve: exploration of INS, NR6, wellbeing, and pro-nature behaviours, plus engagement and subjective experience metrics.

## Limitations and Considerations
- Sample size for post-participation analysis is 500 full participants; generalisability limited to similar populations.
- Missing data handling needed for incomplete responses.
- NR6sum interpretation requires adjustment (mean vs sum) to compare with established literature.
- Qualitative themes require careful coding replication if used with other datasets.