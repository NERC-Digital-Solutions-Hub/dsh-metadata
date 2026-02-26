# Metadata for natureupclose_data.csv

## Overview
- Randomised controlled experiment investigating whether nature-focused activities affect people’s connectedness to nature and wellbeing.
- Recruited 1295 participants who completed pre-participation surveys; randomly assigned to six groups and asked to perform 10-minute activities five times over eight days (in any natural setting).
- Six groups: pollinator, butterfly, noticing nature (3GTiN), combined pollinator, combined butterfly, and a wait-list control.
- 500 participants completed the post-participation survey and fulfilled study inclusion ("full participants").
- Dataset includes pre- and post-participation survey data for these 500 participants; missing data are blank cells.

## Study design and participants
- Pre- and post-participation surveys linked by unique identifiers; times of completion recorded.
- Six conditions (groupings) described, with recoded category labels for analysis (e.g., cit-sci for citizen science groups, noticingnature, combined, control).
- Post-participation survey collected engagement measures and participant reflections on the experience.
- Data include both quantitative scales (various wellbeing and pro-nature behaviours measures) and qualitative open-ended responses.

## Dataset contents and key variables
- Identification and timing:
  - PersonID: unique participant identifier.
  - LineSurvey1 / ResponseIDSurvey1 / DateSurvey1: pre-participation survey details.
  - LineSurvey2 / ResponseIDSurvey2 / DateSurvey2: post-participation survey details.
  - Participant: flag for full participation (1 = yes; 0 = no); N(Participant==1) = 500.
- Wellbeing and nature related measures (pre/post):
  - INS_pre / INS_post: Inclusion of Nature in Self (1–7 scale).
  - NR6sum_pre / NR6sum_post: Sum of six Nature Relatedness components (note: original NR6 uses mean; dataset provides sum; to compare with Nisbet & Zelenski, divide by 6).
  - SatisfiedWithLife_pre / post: 0–10 scale.
  - WorthwhileLife_pre / post: 0–10 scale.
  - Health_pre / Health_post: 1–5 scale.
  - Happiness_pre / Happiness_post: 0–10 scale.
  - PROCOBScivilaction_pre/post; PROCOBSgarden_pre/post; PROCOBS_pre/post: sums from the pro-nature conservation behaviour scale (eight items total; four civil action, four gardening; 1–7 scaling per item).
- Demographics and background:
  - Age; Age_comments; Sex; Ethnicgroup.
  - spendtimeoutsideatleastafewtimesperweek: frequency of time spent outdoors (1–various; 0 for lower categories).
  - postcode: UK postcode district (e.g., OX10); latitude/longitude available only if UK postcode provided.
- Group assignment and task-related data:
  - condition / conditiontext / conditiontypetext: six study groups (pollinator, butterfly, noticingnature, combinedpollinator, combinedbutterfly, acontrol).
  - Engagementwiththetask: self-rated engagement with the task (0–3).
  - 37–42: post-survey ratings of subjective experience (e.g., closeness to nature, calming/joyful experience, noticing beauty, meaningfulness, contributing to nature care, frustration) on 1–5 scale.
  - Timespentoutsideduringthetask: outdoor time during the task (0–4 scale).
  - Howmanytimesdidyoudotheactivities: number of times activities were done (0–6; 6 = more than five times).
- Qualitative open-ended responses (thematic analysis):
  - 45: Open question indicator for presence of open responses.
  - 46–52: Thematic codes for what participants liked about taking part (noticing nature; intrinsic benefits; contributing; learning; social connections; other).
  - 53–59: Thematic codes for what participants didn’t like (weather, time constraints, complexity, technology, lack of success, interference with nature engagement, nothing, other).
- Geography and deprivation:
  - Median_IMD_postcodedistrict / Mean_IMD_postcodedistrict: deprivation indices by postcode district.
  - latitude / longitude: geographic coordinates (only if UK postcode district provided).

## Spatial information and GIS relevance
- Postcode district provides a geographic anchor for mapping participants at a district level.
- Latitude and longitude offer precise point data when available (enables spatial joins with environmental layers).
- IMD indices enable spatial analysis of deprivation-related patterns in wellbeing and nature connectedness.
- Range of demographic and outcome variables supports geospatial correlation analyses with environmental and policy-relevant layers.

## Data quality, limitations, and notes
- Missing data represented by blank cells; not all fields populated for all participants.
- The NR6sum is a sum rather than the mean; to replicate the referenced scale, users should divide by six.
- Open-ended responses (themes 46–59) require qualitative analysis; structured themes are provided for analysis but may contain personally identifiable information if not handled carefully (though the dataset notes that PII checks were performed).
- Spatial data are limited to postcode district and, where available, latitude/longitude; precise locations may be inferred only with caution to preserve privacy.
- The dataset is designed for pre/post analysis on wellbeing and nature connectedness, with group comparisons across six conditions.

## Potential GIS applications and workflows
- Map participant distribution by postcode district and relate to IMD scores to examine geographic patterns in outcomes.
- Overlay with environmental features (green space, nature accessibility) to explore spatial correlates of wellbeing gains.
- Spatially visualize engagement and experience measures (e.g., clustering of high engagement with nature-related improvements).
- Combine with external spatial datasets to assess whether geographic factors influence responses to nature-based activities.
- Use latitude/longitude (when available) for more precise spatial analyses or hotspot mapping, while respecting privacy constraints.

## Usage notes and interpretation guidance
- Pre/post comparisons can be made for key scales (INS, NR6sum, Wellbeing scales, PROCOBS, Health, Happiness).
- For NR6sum, compute mean by dividing the sum by 6 to align with the original Nisbet & Zelenski interpretation.
- Group labels can be recoded as:
  - cit-sci for pollinator and butterfly groups
  - noticingnature for the 3GTiN group
  - combined for combinedpollinator and combinedbutterfly
  - control for acontrol
- Qualitative themes (46–59) provide context on participant experiences; these should be analyzed if qualitative insights are required in GIS-driven reporting.