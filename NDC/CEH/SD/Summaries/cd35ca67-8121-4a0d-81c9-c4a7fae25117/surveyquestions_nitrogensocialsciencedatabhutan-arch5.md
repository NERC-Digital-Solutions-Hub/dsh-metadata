SANH WP 1.3 Harmonised Individual Questionnaire

- The document extends a harmonised survey instrument focusing on livestock, information sources, adoption of practices, attitudes, household economics, assets, and subsidies, with a view to enabling cross-country comparability and data reuse.

## Section 9: LIVESTOCK (multi-species module)
- Households may own multiple livestock species (e.g., Cattle, Buffalo, Yak, Goat, Sheep, Horse, Camel, Pig, Poultry, etc.).
- For each species, data are collected on:
  - Ownership status over the past 12 months (which species owned; multi-select).
  - Reasons for keeping the species (e.g., revenue, home/magazine consumption, festivals, transport, animal power, etc.).
  - Counts and head-level details (numbers per species; highest livestock unit logic across species).
  - How animals left the farm in the last 12 months (sale, barter, slaughter, gift/dowry, etc.).
  - Time spent by species in different housing types (yard, open animal house, closed animal house) and weeks spent in each.
- The questions are repeated and coded per species, with references like 9.1–9.7 and a note that 9.5–9.7 focus on the species with the highest number of units.
- This structure requires careful data harmonisation across species, consistent unit definitions, and handling of multi-species entries.

## Section 10: INFORMATION SOURCES
- Captures how farmers obtain information for crop management and fertilizer use.
- Key items include:
  - Attendance at crop demonstrations/trainings in the last 2 years (Yes/No).
  - Whether trainings covered fertilizer and manure use.
  - Sources consulted for fertilizer decisions (family, traders, extension agents, government, media, internet, etc.).
  - Reasons for not using more information or for adopting guidance/tools.
  - Use and evaluation of decision-support tools or guidance (e.g., leaf colour charts, soil tests, apps).
  - Written records of fertilizer use and yield data (Yes/No).
- Emphasises provenance of information and the decision-making trail for governance and reproducibility.

## Section 11: ADOPTION - DRIVERS AND BARRIERS
- Documents awareness, current use, and prior adoption (dis-adoption) of various practices/technologies not crop-specific but farm-wide.
- Includes a structured list of practices (e.g., decision support tools, green manure, agroforestry, anaerobic digestion, midseason drainage, foliar fertilization) with:
  - Whether the farmer has heard of each practice.
  - Whether they are currently using it.
  - Whether they have ever dis-adopted the practice.
- Country-specific practices can be added, indicating a need for adaptable code lists and cross-country mapping.

## Section 12: ATTITUDE, BEHAVIOUR, PERCEPTION AND OPINION
- Measures psychological and behavioural dimensions related to fertilizer use and soil/crop management.
- Components include:
  - General attitudes toward technology adoption and risk tolerance.
  - Perceived triggers for change and what could drive changes in fertilizer use.
  - Perceived benefits and constraints of synthetic fertilizer vs. manure.
  - Importance of manure uses for household productivity and decision-making about soil management.
  - Numerous Likert-scale items (5-point scales) and several dichotomous prompts to capture nuanced beliefs and risk attitudes.
- Data supports analysis of adoption drivers and potential behavioural interventions.

## Section 13: AVERAGE MONTHLY EXPENSES
- Collects monthly expenditures across detailed categories (food, clothing, education, health, utilities, transportation, communications, festivals, debt, savings, etc.).
- Results enable cost-of-living profiling and cross-country comparisons of household economics.

## Section 14: HOUSEHOLD WEALTH/ASSET
- Assesses asset ownership and housing characteristics:
  - Home ownership status (full, partial, or non-owner) and dwelling features (rooms, floor material, lighting, cooking fuel, water source).
  - Asset inventory (TVs, smartphones, internet access, power tillers, irrigation pumps, money transfers, transport modes).
  - Access to credit: past farm investment loans and loan sourcing.
  - Distance to financial institutions; crop insurance status and season.
  - Inventory of transport assets (human-, animal-, motor-powered).
- Includes a dedicated sub-section (14.17) on crop insurance and season-specific compensated risk if crops fail.
- Data enable asset-based wealth indices and resilience analysis.

## Section 15: SUBSIDY
- Captures direct subsidies received in the past 12 months, country-adjusted.
- Subsidy types include:
  - Synthetic fertilizer, agricultural machinery, irrigation charges, output price support, seeds, and other subsidies.
- Structured as Yes/No per subsidy type, enabling fiscal support impact assessment and cross-country policy comparisons.

## Data Governance, Harmonisation and Metadata Implications for Data Stewards
- Coding and crosswalks:
  - Requires standardized, country-agnostic coding for livestock species, reasons for keeping, movement types, and housing types.
  - Develop crosswalks for country-specific practices (Section 11) and for subsidy categories (Section 15).
- Data structure and seriation:
  - Species-level repetition (for Section 9) necessitates robust data models that support multi-entry per household and per species with consistent units and validation rules.
  - Seasonal/round identifiers needed to link Section 9 livestock data with Sections 12–14 (household context, wealth, subsidies) for integrated analytics.
- Metadata and documentation:
  - Comprehensive data dictionary covering all Section 9–15 variables, including definitions of livestock units, housing categories, and subsidy types.
  - Clear provenance: enumerator IDs, interview date, season/round codes, and validation steps to support data quality assessments.
- Quality assurance:
  - Validation rules to prevent inconsistent entries across species (e.g., total livestock counts vs. per-species counts), and to ensure plausible transitions (e.g., movement out of farm).
  - Handling of multi-select fields and repeated questions to minimize missing data and maintain consistency.
- Privacy and consent:
  - Ensure alignment with the instrument’s consent framework (data use, confidentiality, and potential follow-up) in Sections 9–15, recognizing sensitive household economic and asset information.
- Reuse and interoperability:
  - Publish and document data schemas with machine-readable metadata to enable portal discovery and reuse, including country adaptations and versioning.
  - Consider providing explicit export formats and unit definitions to facilitate cross-country nitrogen management analytics and socio-economic research.

## Key Takeaways for Data Governance and Stewardship
- The SANH instrument’s Sections 9–15 deliver rich, multi-species livestock data alongside detailed information on information sources, technology adoption, attitudes, household finances, assets, and subsidies.
- Data Stewards should implement strong variable definitions, cross-country codebooks, and validation rules to ensure interoperability and reliable downstream analysis.
- Given the seasonal and multi-species structure, robust provenance, update mechanisms, and documentation are critical to enable discovery, reuse, and accurate cross-country nitrogen-management and agricultural-system analytics.