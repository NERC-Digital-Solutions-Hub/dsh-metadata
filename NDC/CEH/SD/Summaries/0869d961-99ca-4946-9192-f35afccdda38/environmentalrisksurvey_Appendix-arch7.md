# VIRAQUA survey

- Web-based survey designed to gather opinions on upset stomachs, shellfish-related illness, and knowledge about related pathogens, plus risk perception and control related to life hazards.
- Approximately 15 minutes to complete; conducted by Bangor University and the University of Manchester; confidential and for academic research only (not for marketing).

## Purpose and scope

- Assess personal experience with upset stomachs, links to eating filter-feeding shellfish (mussels, oysters, cockles, clams, scallops), and contact with UK recreational waters.
- Explore awareness of pathogens causing upset stomachs and sources of information.
- Examine how people perceive and feel about various life hazards (fear and control) across multiple sets of hazards.
- Produce data suitable for analysis and potential map-based visualization to support public health communication and risk assessment.

## Methodology

- Self-administered online questionnaire with iterative sections and repeated choice tasks.
- Uses multiple coded response formats (e.g., effs_r1, wsfsf, fear_*, control_*, eoh_r*) to capture granular responses.
- Includes demographic questions (gender, age, household income earner occupation) and geographic/behavioral exposure questions (shellfish consumption, water contact).
- Questions on illness attribution (food poisoning and water-related illness), behavior changes, seeking guidance, and use of government information sources.
- Sections on knowledge of specific pathogens (MRSA, Cryptosporidium, Norovirus, E. coli, Campylobacter, Listeria, Shigella, Rotavirus, etc.).

## Survey sections and key content

- Demographics and household context
  - Self-identified gender; age; occupation category of Chief Income Earner.
- Exposure and consumption
  - Location in the UK; frequency and type of shellfish consumption (raw, cooked, ready meals, pickled) and other eating patterns.
  - Contact with UK recreational waters (swimming, paddling, sailing, etc.) in the last year.
- Illness and behavior changes
  - Upset stomach linked to eating or water exposure; seeking guidance; changes in eating or buying shellfish; ensuring shellfish is well cooked.
  - Behavior changes in response to shellfish illness (e.g., avoid certain shellfish, avoid eating out, cook more thoroughly).
  - Sources of advice and UK government information use; attitudes toward government-provided information.
- Pathogen knowledge
  - Reported familiarity with multiple pathogens (e.g., MRSA, Cryptosporidium, Norovirus, E. coli, Campylobacter, Listeria, Shigella, Rotavirus, etc.) and self-assessed knowledge levels.
- Hazards of Life (fear and control)
  - Repeated sets of four hazards; participants select which hazard they fear most and least, first for fear, then for control.
  - Hazards include heart attack, fire, common cold, dementia, food- and environment-related risks, and others (e.g., Salmonella, Norovirus, pesticide residues, etc.).
  - Additional sections assess personal or close-contact experiences with hazards and the extent of control or fear.
  - Post-set questions evaluate understanding and ease of decision-making, with scale-based responses (Very difficult to Very easy, etc.).
- Experience and impact
  - Questions about whether either the participant or someone close has experienced listed hazards.
  - Final questions capture actions taken to reduce risk and any additional thoughts.

## Data structure, quality, and processing notes

- Data are captured with a diverse set of coded fields corresponding to each question and option (e.g., effs, wsfsf, hcsf, hcwc, advn, eoh_r, fear_*, control_*, und_r, ffb_r, etc.).
- The instrument relies on self-reported data and voluntary participation, which may introduce recall bias and weekend-to-week variance.
- The survey uses iterative, set-based choices to map risk perception (fear) and perceived control across multiple hazard concepts, enabling cross-hazard analysis and clustering.

## GIS relevance: potential data products and analyses

- Geospatial mapping of shellfish consumption patterns, water contact frequency, and reported shellfish-related illness across UK regions.
- Overlay risk perception data (fear and control) with environmental and public health layers to identify regions that may benefit from targeted risk communication and education.
- Integration with environmental datasets (water quality, pathogen prevalence, seasonal trends) to produce map-based risk dashboards for policymakers, public health agencies, and the public.
- Identification of gaps in data (e.g., regions with low survey response or limited data on certain hazards) to guide future data collection or sampling strategies.

## Challenges and considerations for GIS teams

- Data heterogeneity: disparate data types (demographics, behaviors, illness, knowledge, and opinion) require careful normalization before geospatial analysis.
- Resolution and privacy: ensuring regional aggregation preserves respondent anonymity while enabling meaningful maps.
- Temporal aspects: cross-sectional design; the survey captures a snapshot, which may limit temporal trend analyses unless repeated over time.
- Coding complexity: numerous internal codes necessitate thorough data documentation and mapping to standard GIS-compatible fields.

## Privacy, ethics, and use of data

- Responses are retained for academic research only and are not used for marketing.
- Survey design includes confidentiality assurances and anonymization considerations.
- Final outputs should respect respondent privacy, with appropriate aggregation for geospatial products.

## Summary of survey flow and delivery

- Initial consent and introduction; basic demographic and exposure questions.
- Sections on shellfish consumption, water exposure, illness attribution, and information-seeking behavior.
- Pathogen knowledge assessment with multiple pathogens listed.
- Hazards of Life: repeated blocks of four hazards, capturing fear and control rankings, plus experiential questions.
- Final section on reducing risk, additional thoughts, and completion.
- Completion status and redirect notes for different survey modes (regular vs. non-regular) provided by the survey platform.

## Takeaways for GIS-focused use

- The VIRAQUA survey yields rich, multi-dimensional data that could underpin geospatial analyses of health risk, information access, and risk perception related to shellfish and water exposure in the UK.
- Proper GIS use will require careful data cleaning, standardization of categorical responses, regional aggregation thoughtfully balancing privacy, and integration with environmental datasets to produce actionable map-based insights.