# Metadata for natureupclose_data.csv

## Overview
- Dataset from a randomized controlled experiment testing the impact of nature-focused activities on connectedness to nature and wellbeing.
- Recruited 1,295 participants, randomly assigned to six groups; post-participation survey completed by 500 full participants.
- Includes pre- and post-participation survey data, with missing values represented as blank cells.
- Data combined from both quantitative scales and qualitative open responses, with some derived metrics.

## Study design and scope
- Six groups: pollinator, butterfly, noticing nature (3GTiN), combined pollinator, combined butterfly, and control (wait-list).
- Intervention: 10-minute activity sessions for eight days (two citizen science options, 3GTiN, or combinations).
- Primary data: pre- and post-participation surveys measuring nature relatedness, wellbeing, pro-nature behaviors, health, happiness, and related constructs.
- Post-participation survey completed after eight days; 500 participants met criteria for full participation.

## Key data content and structure
- Identifiers and timing
  - PersonID: unique participant identifier.
  - LineSurvey1 / ResponseIDSurvey1 / DateSurvey1: references and timing for pre-participation survey.
  - LineSurvey2 / ResponseIDSurvey2 / DateSurvey2: references and timing for post-participation survey.
  - Participant: 1 = full participant (N=500); 0 = not a full participant.
- Core scales and measures (pre- and post-)
  - INS_pre / INS_post: Inclusion of Nature in Self scale (1–7).
  - NR6sum_pre / NR6sum_post: Sum of six Nature Relatedness scale items (each 1–5); note to divide by six to align with original mean scores.
  - SatisfiedWithLife_pre / SatisfiedWithLife_post: 0–10 wellbeing rating.
  - WorthwhileLife_pre / WorthwhileLife_post: 0–10 life worthwhileness rating.
  - PROCOBScivilaction_pre / PROCOBSgarden_pre / PROCOBS_pre: Pro-nature conservation behaviours (pre-participation); composite of eight items (7-point scale) with subcomponents for gardening and civil action.
  - PROCOBScivilaction_post / PROCOBSgarden_post / PROCOBS_post: corresponding post-participation measures.
  - Health_pre / Health_post: single-item 1–5 health rating.
  - Happiness_pre / Happiness_post: 0–10 general happiness.
- Demographics and context
  - Age: respondent age (years); Age_comments: age-related notes.
  - Sex: female, male, other, prefer not to say.
  - Ethnicgroup: categorical ethnicity.
  - spendtimeoutsideatleastafewtimesperweek: frequency of outdoor time (binary-like coded 0/1 with nuanced categories).
  - postcode: UK postcode district (optional; included for IMD/latitude/longitude when provided).
  - latitude / longitude: geographic coordinates, provided only if UK postcode district was supplied.
  - Median_IMD_postcodedistrict / Mean_IMD_postcodedistrict: area deprivation metrics derived from postcode district.
- Group assignment and engagement
  - condition / conditiontext / conditiontypetext: six study groups and their textual/type recoding (e.g., citsci for citizen science, noticingnature, combined, control).
  - Engagementwiththetask: self-rated engagement with the assigned task (0–3).
  - 37–42: post-participation ratings on experience during the task (Likert 1–5): closeness to nature via senses, calming/joyful, noticed beauty, meaningfulness, sense of helping nature, frustration.
  - 43: Timespentoutsideduringthetask: amount of outdoor time during the task (0–4).
  - 44: Howmanytimesdidyoudotheactivities: number of times activities were completed (0–6, with 6 representing more than five times).
- Qualitative data and coding
  - 45: Openquestionanswers: indicator of whether open-ended responses were provided.
  - 46–61: Thematic coding fields derived from open-ended responses, including themes on noticing nature, intrinsic benefits, contributing, learning, social connections, other, and various disliking themes.
- Data quality and geography
  - 62 Median_IMD_postcodedistrict and 63 Mean_IMD_postcodedistrict: area-level deprivation indicators.
  - 64 latitude and 65 longitude: geographic coordinates when postcode district was provided.

## Data quality, provenance, and preparation
- Derived fields and notes
  - NR6sum values are sums; users should divide by six to obtain the original mean-like metric (as per Nisbet & Zelenski 2013).
  - Postcode-derived metrics (IMD, latitude, longitude) are provided when UK postcodes are available; otherwise blank.
- Data handling and privacy
  - Blanks represent missing data; qualitative responses were reviewed for personally identifiable information and text was managed accordingly.
  - Geographic data are aggregated to postcode district level or higher to support privacy.
- Documentation and reusability
  - The dataset includes a comprehensive data dictionary-like description of each field, aiding reproducibility and cross-study comparison.
  - Open-ended responses are organized into thematic categories for secondary qualitative analysis.

## Governance considerations for data stewards
- Standardization and metadata completeness
  - Ensure consistent interpretation of field names, scales, and derived metrics (e.g., NR6sum calculation instruction included).
  - Maintain the mapping between conditiontext and conditiontypetext for reproducible group definitions.
- Privacy and disclosures
  - Verify de-identification measures (e.g., district-level geography, avoidance of direct coordinates) and maintain access controls if sharing raw qualitative content.
- Data quality and provenance
  - Preserve original survey references and dates to support traceability of responses.
  - Document any data cleaning or transformation steps (e.g., calculation of NR6sum, aggregation of IMD metrics).
- Reuse and limitations
  - Acknowledge sample size differences (1295 pre-participants vs. 500 full participants) and potential biases related to non-completion.
  - Provide guidance on combining pre/post measures and handling missing data as blanks.
- Citation and lineage
  - Include citation guidance for the primary publication and any methodological papers referenced (e.g., NR6, 3GTiN, or pro-nature scales) to support interpretation of derived metrics.

## Practical notes for researchers and data users
- When analyzing, treat NR6sum as a sum; convert to mean-equivalent by dividing by six if aligning with Nisbet & Zelenski (2013) literature.
- Pay attention to group coding and recoded condition fields to avoid misclassification between “citizen science,” “noticing nature,” “combined,” and “control” groups.
- Consider using IMD and postcode-derived geography only at aggregated levels to protect privacy; latitude/longitude should be used with caution or omitted in shared datasets.
- Leverage the qualitative theme fields (46–61) for mixed-method analyses, ensuring appropriate handling of potentially sensitive responses.