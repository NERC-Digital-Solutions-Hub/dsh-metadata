# VIRAQUA survey

- UK-based academic survey designed to gather data on upset stomachs, shellfish-related risks, water exposure, and perceptions of life hazards to inform risk assessment and behavioral insights.
- Designed for academic research; responses are confidential and not used for marketing.

## Survey structure and topics

- Demographics and household context
  - Self-identified gender; age group; occupation-based class for Chief Income Earner; regional/location data.
- Shellfish and consumption module
  - Focus on filter-feeding shellfish (mussels, oysters, cockles, clams, scallops) with multiple consumption formats:
    - Eaten raw or cooked in restaurants, ready meals at home, eaten at home, etc.
  - Detailed frequency and context-based responses (e.g., restaurant, abroad, takeaway, home-cooked).
- Water exposure
  - Frequency of contact with UK recreational waters (seas, rivers, lakes, etc.).
- Upset stomach risk and knowledge
  - Self-reported upset stomach in the last 12 months, attribution to eating shellfish, and setting of illness (home/restaurant/abroad).
  - Behavioral changes after illness (permanently cease or take breaks from shellfish, etc.).
  - Behavioral changes after water exposure illness (stop using waters, change locations/activities, use hand sanitizer, inform others).
  - Guidance seeking and sources of advice (websites, government tools, healthcare channels).
  - Awareness of specific pathogens/bugs (e.g., MRSA, Norovirus, E. coli, Campylobacter, Listeria, Shigella, Salmonella, etc.) with familiarity levels.
- Hazards of Life: fear and control
  - Sets of four hazards presented repeatedly; tasks include identifying the hazard most/least feared and most/least control over in each set.
  - Hazards include heart attack, fire, common cold, dementia, antibiotic resistance, pesticide residues, diabetes, cancer types, norovirus, dog bites, biota/mould spores (bioaerosols), Salmonella, lightning, etc.
  - Measures of understanding of hazards (ease of understanding, difficulty of making choices) and respondent’s ability to articulate risk perceptions.
  - Later sections capture personal or close-one experiences with listed hazards.
- Final risk reduction and comments
  - Questions on actions taken to reduce risk from listed hazards.
  - Open-ended space for additional comments about the survey or risk topics.

## Key variables and data types

- Demographic and socio-economic categories (e.g., occupation class, region).
- Food consumption indicators
  - Frequency and format of shellfish consumption (raw, cooked, ready meals, at home vs. away, single/multiple contexts).
- Water contact frequency and recent exposure measures.
- Health outcomes
  - Upset stomach occurrence (past year), attributed causality to shellfish or water exposure; consequent behavior changes.
- Information behavior
  - Sources used, usefulness of UK government guidance, likelihood of consulting online tools in the future.
- Pathogen familiarity
  - Self-reported knowledge levels for multiple pathogens.
- Hazards perception
  - Fear and control ratings across many hazard items, captured in multiple paired questions per set.
- Personal and close-contact exposure
  - Whether the respondent or someone close has experienced each hazard.
- Open-ended feedback
  - Additional thoughts on the survey and risk topics.

## Data quality considerations

- Instrument appears to be complex with numerous coded variables (e.g., effs, wsfsf, hcsf, fear/control prefixes), which requires careful data dictionary alignment and variable mapping.
- Some encoding irregularities are visible (e.g., truncated tokens like ageoe, shell, etc.), indicating potential data parsing or formatting issues to address during cleaning.
- Self-reported data subject to recall bias (past year exposures/illness) and social desirability, especially around health guidance and risk behaviors.
- Length and complexity may affect respondent fatigue and item completion rates; plan for handling partial responses and attention checks.

## Potential analyses and modeling ideas

- Descriptive analytics
  - Demographic breakdowns, shellfish consumption patterns by region and age/occupation.
  - Prevalence of self-reported upset stomach and its attribution to shellfish vs. water exposure.
- Behavioral and risk relationships
  - Association between illness history and subsequent avoidance or changes in shellfish consumption.
  - Relationship between water exposure frequency and reported illness or precautionary behaviors (e.g., hand sanitizer use).
- Information sources and guidance uptake
  - Correlations between trust/use of UK government information and knowledge/behavioral responses.
- Hazard perception and risk stratification
  - Factor analysis or clustering on fear and control responses to derive risk-perception profiles.
  - Segmentation to identify groups with high fear/low control vs. low fear/high control for targeted risk communication.
- Pathogen familiarity and risk awareness
  - Examine gaps between knowledge of specific pathogens and reported illness or precautionary actions.
- Causal caveats
  - Cross-sectional design; interpret associations cautiously; consider weighting to population benchmarks if available.

## Data governance and dissemination notes

- Instrument designed for academic research; confidentiality assurances and non-marketing use.
- Emphasizes metadata, traceability of data sources, and potential portal-based sharing of datasets with proper documentation.
- Final sections capture personal impact and risk-reduction behaviors, contributing to evidence on public risk perception and information needs.