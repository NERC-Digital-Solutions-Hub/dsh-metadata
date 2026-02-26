# Metadata for natureupclose_data.csv

- Purpose and design
  - Randomised controlled experiment to test the impact of nature-focused activities on connectedness to nature and wellbeing.
  - Recruited 1,295 individuals who completed a pre-participation survey and were allocated to one of six groups.
  - Intervention groups: two citizen science activities (pollinator or butterfly), a nature-noticing activity (Three Good Things in Nature, 3GTiN) daily, or combinations of citizen science with 3GTiN.
  - Control group: wait-list control (no activity during the initial period).
  - Eight-day intervention period with a post-participation survey; 500 participants completed the post-survey and met inclusion criteria (full participants).

- Dataset contents and structure
  - Includes pre- and post-participation survey data for the 500 full participants.
  - Unique identifiers and time stamps:
    - PersonID, LineSurvey1, ResponseIDSurvey1, DateSurvey1, LineSurvey2, ResponseIDSurvey2, DateSurvey2.
  - Participant status:
    - Participant flag (0 = did not meet conditions; 1 = did meet conditions; N(Participant==1) = 500).
  - Core psychometric and wellbeing measures (pre and post):
    - INS_pre / INS_post: Nature Relatedness (Nature included in self) scale.
    - NR6sum_pre / NR6sum_post: Sum of six Nature Relatedness components.
    - SatisfiedWithLife_pre / post; WorthwhileLife_pre / post.
    - PROCOBScivilaction_pre / post; PROCOBSgarden_pre / post; PROCOBS_pre (overall) and breakdowns.
    - Health_pre / post (single-item global health rating).
    - Happiness_pre / post (11-point scale).
  - Demographics and context:
    - Age; Age_comments; Sex; Ethnicgroup; spendtimeoutsideatleastafewtimesperweek; postcode district; latitude/longitude (when UK postcode provided).
    - IMD_postcodedistrict metrics: Median_IMD_postcodedistrict; Mean_IMD_postcodedistrict.
  - Group assignment and condition details:
    - condition: six groups (pollinator, butterfly, noticingnature, combinedpollinator, combinedbutterfly, acontrol).
    - conditiontypetext: recoded categories (citsci, noticingnature, combined, control).
  - Engagement and qualitative feedback:
    - Engagementwiththetask: self-rated engagement (0–3).
    - Post-participation reflections (37–42): ratings on closeness to nature, calm/joy, noticing beauty, meaningfulness, care for nature, frustration.
    - Timespentoutsideduringthetask; Howmanytimesdidyoudotheactivities.
    - Open-ended response fields (Openquestionanswers; Whatyoulikedabouttakingpart; Whatyoudidntlikeabouttakingpart) with thematic coding (liketheme_* and disliketheme_* categories).
  - Data quality and geography:
    - Median_IMD_postcodedistrict; Mean_IMD_postcodedistrict; latitude; longitude (when UK postcode provided).

- Measures, scales and components
  - Nature and wellbeing:
    - INS (Nature in Self scale), NR6 (Nature Relatedness scale), life satisfaction, worthwhile life, happiness, general health.
  - Pro-nature behaviours:
    - PROCOBS_pre/post: engagement in eight pro-nature behaviours; subscales for civil action and gardening.
  - Engagement and participant experience:
    - Task engagement, subjective experiences during participation, time spent outside, frequency of activities.

- Data quality, metadata and governance
  - Missing data represented by blank cells.
  - Rich metadata linking column numbers to variable meanings (e.g., 9–12 for INS/NR6, 27–29 for demographics, 34–35 for condition coding).
  - Open-ended data subjected to thematic analysis; potential personally identifiable information considerations noted.
  - Location data (postcode, latitude/longitude) and IMD metrics offer environmental context but raise privacy considerations; data governance and sharing implications should be accounted for in dissemination.

- Relevance for monitoring frameworks and policy evaluation
  - Demonstrates linking experimental interventions (nature engagement activities) to validated psychosocial measures and pro-environmental behaviours.
  - Provides a structured data dictionary and data provenance suitable for monitoring framework development.
  - Enables assessment of short-term impacts on connectedness to nature and wellbeing, with detailed demographic and geographic context to explore equity and place-based patterns.
  - Includes both quantitative outcomes and qualitative feedback to inform communication of complex findings to policymakers and stakeholders.

- Limitations and considerations for use
  - Sample drawn via self-selection and randomisation within the study design; generalisability to broader populations should be considered.
  - Short follow-up window (eight days) limits inference about long-term effects.
  - Privacy considerations due to location data; appropriate data governance and potential data anonymisation required for public sharing.