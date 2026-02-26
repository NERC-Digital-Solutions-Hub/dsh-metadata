# Metadata for natureupclose_data.csv

- A randomized controlled experiment dataset investigating the impact of nature-focused activities on connectedness to nature and wellbeing.
- Recruited 1,295 participants who completed a pre-participation survey and were allocated to one of six groups; eight-day activities occurred for non-control groups.
- 500 participants completed the post-participation survey and were included as full participants; missing data are represented by blank cells.

## What the dataset contains

- Pre- and post-participation survey data for full participants (N = 500).
- A wait-list control group (no prior activities) included for comparison.
- Data structure includes unique identifiers, timestamps, group assignment, and inclusion status.
- Derived and scored measures based on established scales, with notes on calculation where relevant.
- Rich qualitative elements coded into themes alongside quantitative measures.

## Key fields and constructs (summary)

- Identifiers and timing
  - PersonID, LineSurvey1, ResponseIDSurvey1, DateSurvey1 (pre), LineSurvey2, ResponseIDSurvey2, DateSurvey2 (post)
  - Participant flag: 0 = not a full participant, 1 = full participant (N = 500)

- Demographics and context
  - Age, Age_comments, Sex, Ethnicgroup, spendtimeoutsideatleastafewtimesperweek, postcode (UK-specific), latitude/longitude (when UK postcode provided)

- Group assignment and conditions
  - condition (six groups: pollinator, butterfly, noticingnature, combinedpollinator, combinedbutterfly, acontrol)
  - conditiontext and conditiontypetext (mapping to training activities and control)

- Primary psychological and wellbeing measures
  - INS_pre / INS_post (Nature Connectedness – Inclusion of Nature in Self)
  - NR6sum_pre / NR6sum_post (Nature Relatedness – sum of six components; note: original paper uses the mean; users should divide by six to compare)
  - SatisfiedWithLife_pre / SatisfiedWithLife_post
  - WorthwhileLife_pre / WorthwhileLife_post
  - Health_pre / Health_post (single-item 1–5 scale)
  - Happiness_pre / Happiness_post (11-point scale, 0–10)

- Pro-nature conservation behaviours
  - PROCOBScivilaction_pre / PROCOBScivilaction_post
  - PROCOBSgarden_pre / PROCOBSgarden_post
  - PROCOBS_pre / PROCOBS_post (overall 8-item scale; includes gardening and civil action components)

- Engagement and experiential responses
  - Engagementwiththetask (0–3 scale)
  - Responses to “How did you find taking part in the experiment?” (37–42; Likert-type items for closeness to nature, calming/joyful feelings, noticing beauty, meaningfulness, sense of helping, frustration)

- Activity participation and open responses
  - Timespentoutsidemduringthetask (0–4)
  - Howmanytimesdidyoudotheactivities (0–6)
  - Openquestionanswers (0/1 for whether open answers were provided)
  - Thematic codes for what participants liked/disliked (liketheme_noticingnature, liketheme_intrinsicbenefits, liketheme_contributing, liketheme_learning, liketheme_socialconnections, liketheme_other; disliketheme_* themes similarly)

- Data quality and geography
  - Median_IMD_postcodedistrict, Mean_IMD_postcodedistrict ( deprivation indices by postcode district)
  - latitude, longitude (when UK postcode provided)

- Data provenance and quality notes
  - Missing data are represented as blank cells.
  - NR6sum components are scored on a 1–5 scale; sum reported in NR6sum_pre/post with a caution to convert to mean if aligning with Nisbet & Zelenski (2013).
  - Open-ended responses were subjected to thematic analysis; excerpts coded into predefined themes.

## Data structure and interpretation notes

- Six experimental groups enable comparisons between citizen-science tasks, nature-noticing activities, and their combinations, plus a wait-list control.
- Data include both quantitative scales (ordinal/interval) and qualitative thematic codes derived from participant responses.
- Derived scores require attention to scoring conventions (e.g., NR6sum mean vs. sum) when comparing to original literature.
- Geographic and socioeconomic contextual data (IMD, postcode, coordinates) allow contextual analyses while mindful of privacy considerations.

## How this supports data leadership objectives

- Demonstrates end-to-end data lifecycle management: clear identifiers, group assignment, pre/post measurement, and post-processing notes.
- Provides a robust data asset for evaluating data strategy in practice: standardized, multi-dimensional measures of wellbeing and nature relatedness across a randomized design.
- Illustrates integration of quantitative and qualitative data, enabling richer analyses and informed decision-making about program design and impact.
- Highlights data quality considerations and metadata clarity essential for data discoverability, reuse, and cross-network collaboration.
- Emphasizes the importance of documenting scoring conventions, data transformations, and provenance to ensure reproducibility and usability across teams and partners.