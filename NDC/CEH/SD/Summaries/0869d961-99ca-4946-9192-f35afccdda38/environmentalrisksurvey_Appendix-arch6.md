# VIRAQUA survey

## Overview
- A 15-minute survey designed to collect data on demographics, shellfish consumption, water contact, upset stomachs, guidance-seeking behavior, knowledge of pathogens, and risk perceptions.
- Aimed at understanding how people perceive hazards, how they control them, and how they respond to information from government sources.
- Designed for academic research with confidentiality stated; not for private-sector marketing.

## Data Collected (variables and content)
- Demographics
  - Self-identified gender
  - Age group
  - Household income earner occupation (occupational class categories)
  - Where you live (location options)
- Diet and exposure
  - Filter-feeding shellfish consumption patterns (various modes: raw, cooked, ready meals, eaten at home/restaurant, etc.)
  - Frequency and context of contact with UK recreational waters
- Health and illness
  - Upset stomach history related to eating and to water exposure (nausea, vomiting, diarrhoea, abdominal cramping)
  - Perceived cause of illness (e.g., shellfish-related, food poisoning, water exposure)
  - Changes in behavior after illness (e.g., avoid certain foods or places)
  - Seeking guidance or advice about upset stomachs
- Knowledge and information sources
  - Use of UK government information and specific websites (e.g., FSA/FS Scotland)
  - Perceived usefulness and awareness of online tools
  - Preferences for where to seek advice (A&E, GP, NHS websites, newspapers, friends/family, internet searches, etc.)
- Hazards of Life (risk perception)
  - Repeated sets of four hazards to rate fear and control
  - For each set: identify the hazard you fear the most and the least
  - Later, rate which hazards you have the most and least control over
  - Examples of hazards include heart attack, fire, salmonella, pesticides, Norovirus, antibiotics resistance, diabetes, skin cancer, etc.
- Experience with hazards (eoh)
  - Whether you or someone close has experienced listed hazards (e.g., terrorist attack, dementia, car accident, etc.)
- Attitudes toward hazard reduction
  - Whether any actions have been taken to reduce risk from listed hazards
- Survey flow metrics
  - Completion status (complete, screenout, overquota)
  - Perceived ease of understanding and decision-making in hazard sets

## Structure and Flow
- Demographics and baseline questions (gender, age, occupation/class, location)
- Dietary and water-exposure sections (shellfish consumption, recreational water contact)
- Health and guidance sections (upset stomach, seeking advice, knowledge of pathogens)
- Hazards of Life: fear assessment (four-hazard sets repeated) to identify most/least feared hazards
- Hazard control assessment: most/least control over hazards (repeated sets)
- Experience with hazards and risk-reduction actions
- Final comments and finish screen
- Note: The instrument uses many coded response keys (e.g., effs_r1, wsfsf, hcwc) and includes sections with multi-select and Likert-style ratings

## Data Coding and Formats
- Extensive use of coded responses for multiple-choice and multi-select questions
- Examples of coding patterns
  - Food/water exposure and consumption: effs_r1, effs_r2, effs_r3, effs_r4, effs_r5, effs_r6
  - Shellfish-related questions and behaviors: wsfsf, hcsf
  - Water exposure and post-exposure behaviors: hcwc
  - Hazard fear and control: fear_*, control_*, fss, etc.
  - End-of-hazard questions: eoh_r*
- Repeated blocks and multi-hazard constructs require careful mapping to composite variables (e.g., overall fear index, control index)

## Data Quality and Cleaning Considerations
- Potential data quality issues
  - Placeholder text and inconsistent entries in some fields (e.g., miscellaneous text "shell", "effs", Script blocks)
  - Complex skip logic and many cross-referenced codes that must be reconciled during cleaning
  - High volume of coded variables across many sections increases risk of misalignment if mapping is manual
  - Some questions rely on prior responses (e.g., if ill more than once, consider all events)
- Data preparation needs
  - Establish a consistent variable naming and coding schema to flatten multi-select and repeated blocks
  - Create derived variables (e.g., total fear index, most/least feared hazard, most/least control) from repeated sets
  - Handle missing data and screenout/overquota indicators to track response completeness
  - Validate internal consistency between related sections (e.g., illness attribution vs. shellfish exposure)

## Potential Data Products and Insights (Data Support perspective)
- Interactive dashboards
  - Relationship between shellfish consumption patterns and self-reported shellfish-related illness
  - Distribution of fear and control across Hazards of Life, with breakdowns by demographics and exposure
  - Correlation between water exposure frequency and reported upset stomachs or precautionary behaviors
  - Use of UK government information sources by demographics and its association with knowledge scores
- Self-serve analyses
  - Cross-tab analyses of illness history by source of guidance and trust in information sources
  - Trend/ladder analyses showing which hazards people feel least in control of, and which they fear most
- Data quality dashboards
  - Track completion rates, sections with high item nonresponse, and common data quality issues (e.g., placeholder text)
- Policy and outreach implications
  - Identify gaps in public knowledge about specific pathogens and hazards
  - Inform targeted risk communication strategies based on fear/control profiles and information-source preferences

## Privacy, Ethics, and Use
- Responses are intended for academic research and maintained confidential
- Data not intended for marketing purposes
- Clear consent and ethical handling implied by the study description

This summary captures the survey’s purpose, structure, types of data collected, coding schemes, data quality considerations, and how a Data Support role might turn the collected data into practical, self-serve insights and dashboards for risk communication, public health education, and policy guidance.