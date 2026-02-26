# SANH WP 1.3 Harmonised Individual Questionnaire

## Overview of the included sections (Section 9–15)

- Section 9: Livestock
  - Multi-species livestock module capturing ownership over the past 12 months for multiple species (e.g., Cattle, Buffalo, Yak, Goat, Sheep, Horse, Camel, Pig, Poultry, and hybrids).
  - For each species:
    - Reasons for keeping animals (e.g., revenue, home milk/food, festivals, dowry, transport, draft, etc.).
    - Counts per species and related movements out of the farm (sale, barter, slaughter, gifts, theft, etc.).
    - Weeks spent in various housing types (yard, open animal house, closed animal house).
    - Identification of the species with the highest livestock units and specific follow-ups (leaving farm, housing timeframes).
  - Design implies nested, repeatable blocks per species with high data density and cross-species comparability requirements.

- Section 10: Information Sources
  - Captures exposure to crop demonstrations/trainings in the last 2 years.
  - Tracks where fertiliser/advice information is sought and whether decisions are informed by guidance tools, etc.
  - Gathers information on sources used for fertiliser decisions and barriers to information uptake.

- Section 11: Adoption – Drivers and Barriers
  - Assesses awareness, current use, and dis-adoption of selected practices/technologies.
  - Includes country-specific or project-specific practice IDs (e.g., leaf colour chart, green manure, anaerobic digestion, foliar fertilisation, etc.).
  - Captures whether adoption is active, ceased, and which practices are reported.

- Section 12: Attitude, Behaviour, Perception and Opinion
  - Measures general attitudes toward technology adoption and risk tolerance.
  - Includes questions on what could drive changes in fertiliser use and perceptions of the benefits/risks of fertilisers and manure.
  - Contains multi-item scales and repeated prompts to assess attitudes toward soil and crop management practices, risk-taking, and decision-making processes.

- Section 13: Household Expenditure
  - Lists average monthly expenditures across food, clothing, education, health, taxes, festivals, investments, debt, and other categories.
  - Distinguishes between own production versus purchased food and allows multiple entries per category.

- Section 14: Household Wealth/Asset
  - Ownership and characteristics of the dwelling (ownership status, rooms, floor material, lighting, cooking fuel, water source).
  - Asset ownership (TVs, smartphones, internet access, power tillers, irrigation pumps, money transfer tools, transport modes, etc.).
  - Loan history for farm investments and access to financial institutions.
  - Distance to financial institutions and crop insurance details.

- Section 15: Subsidy
  - Records direct subsidies received in the past 12 months (e.g., synthetic fertilizer, machinery, irrigation charges, price support, seeds, other).
  - Allows country-specific adaptations.

## Data governance and stewardship implications

- Standardization and interoperability
  - The livestock module requires standardized species codes, unit conventions, and consistent coding across all questions for each species.
  - Ensure uniform handling of “Other (specify)” responses via a controlled vocabulary or mapping to codes.

- Data structure and complexity
  - Section 9 uses repeated, nested blocks per species with age/ownership, reasons, counts, and movements; expect high relational complexity (households → species → events).
  - Two-season or 12-month recall elements imply careful date handling and potential need for season tagging or versioning.

- Metadata, provenance, and versioning
  - Capture enumerator ID, date/time, household/plot identifiers, and any deviations from the standard administration script.
  - For multi-season data, maintain clear documentation of which records pertain to which season or recall period.

- Data quality and validation
  - Implement plausible-range checks for counts, weeks in housing, and expenditures.
  - Enforce cross-field consistency (e.g., ownership implies non-null counts; zero values where appropriate).
  - Standardize and validate “Leaving farm” reasons to enable aggregation (sale, slaught er, gifts, etc.).

- Privacy and data sharing
  - Given detailed household and farm practices, apply privacy-preserving handling (anonymization of identifiers, location masking where necessary).
  - Document consent and any restrictions on sharing raw data or derived datasets.

- Documentation and accessibility
  - Provide a machine-readable data dictionary and codebook linking each question to a variable, including derived fields (e.g., total livestock units, per-species totals).
  - Document data transformations and mappings (e.g., conversion of free-text to codes, unit standardizations).

## Practical guidance for Data Stewards

- Build a comprehensive data dictionary
  - Map every livestock question per species to standardized variables and codes.
  - Include derived metrics such as per-species totals and overall livestock-unit indicators.

- enforce robust data validation
  - Implement per-record validation rules for Section 9 (e.g., non-negative counts, consistent season/recall periods).
  - Apply cross-section checks across Sections 9–15 to support integrated analyses (e.g., correlate subsidy receipts with adoption statuses).

- plan for derived variables and analytics
  - Create variables for most-livestock species, total livestock units, and movement patterns.
  - Prepare restructuring logic to align nested per-species data into flat tables suitable for cross-site comparisons.

- ensure traceability and reproducibility
  - Document all transformations, coding decisions, and deviations from the instrument scripts.
  - Maintain versioned datasets with clear season/recall identifiers.

- support discoverability and reuse
  - Align the data with portal/catalog standards and ensure metadata completeness (provenance, data quality notes, and usage constraints).

## Key takeaways for Data Stewards

- The SANH WP 1.3 Harmonised Individual Questionnaire contains a rich, multi-section instrument with an emphasis on detailed livestock data (Section 9), followed by Information Sources (Section 10), Adoption drivers/barriers (Section 11), Attitudes and perceptions (Section 12), Household expenditures (Section 13), Household assets (Section 14), and Subsidies (Section 15).
- Section 9 requires careful handling due to nested, per-species data, frequent use of “Other (specify)” codes, and the need to compute derived measures like total livestock units.
- Effective governance hinges on standardized coding, robust metadata, clear versioning, rigorous data quality checks, privacy protections, and thorough documentation to enable cross-site comparability and long-term reuse.