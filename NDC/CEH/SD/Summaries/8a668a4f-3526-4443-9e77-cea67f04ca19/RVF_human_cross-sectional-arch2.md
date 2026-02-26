# Rift Valley fever virus seroprevalence data from people involved in a cross-sectional survey in Tana River and Garissa counties, Kenya (December 2013 - February 2014)

## Purpose and Study Context
- Part of a study on land use change (irrigation schemes in pastoral rangelands) and access to ecosystem services, using Rift Valley fever (RVF) as a case study disease.
- Aimed to profile RVF risk in irrigated vs. pastoral areas; cross-sectional household survey including individuals aged 5 years and above.

## Experimental Design and Sampling Regime
- Sample size: 220 households per land-use type, determined by formal power calculations for comparing two independent proportions (two-sided test).
- Sites: Bura and Hola irrigation schemes in Tana River; adjacent pastoral villages; Ijara and Sangailu divisions in Garissa County (transhumance pastoralism).
- Sampling frame: household lists from registers (cleaned for duplicates/new entries); random selection of households and individuals within households.
- Design: cross-sectional; single sampling occasion; sampling conducted once for profiling RVF risk.
- Primary sampling units: households; eligible individuals: ≥5 years.

## Field Work and Data Collection
- Ethics: approval from AMREF Ethics and Scientific Review Committee; informed consent at community, household, and subject levels.
- Community engagement: group meetings to review objectives and plans.
- Data capture: electronic forms via Open Data Kit (ODK) on smartphones; geographic coordinates collected (decimal degrees) but withheld for ethical reasons.
- Personnel and procedures: trained enumerators; sampling tubes barcoded; samples linked to household data via barcodes; field-preservation with dry ice; weekly replenishment of dry ice.
- Blood collection: venous sampling with volume scaled to age (≤5 ml for 5–12, 5–10 ml for 13–17, ≤10 ml for 18+).
- Sample types: serum for RVFV IgG testing and whole blood in heparinized tubes; duplicates prepared for storage.
- Storage and transport: serum/whole blood aliquoted to 2 ml cryo tubes; transported on dry ice to ILRI Nairobi biorepository for long-term storage in liquid nitrogen.
- Laboratory staffing: field sampling coordinated with health authorities; analyses performed in a dedicated lab.

## Laboratory Analysis
- Serology: RVFV IgG screening using an RVF virus inhibition ELISA validated for humans, domestic and wild ruminants (Paweska et al., 2005).
- Analysis practices: assay performed in duplicates; borderline results re-analyzed.

## Dataset and Data Structure
- Data file: DDDAC_Kenya_human RVF seroprevalence.csv (23 variables).
- Key variable categories: sampling date and site details (county, district, division, location, sublocation, village); household identifiers; relationships to head of household; gender and age of both household head and sampled individuals; sampling area classification (irrigation, pastoral, riverine); test result (positive/negative); altitude; livestock within the household.
- Data accessibility: geographic coordinates withheld; data linked via household and individual identifiers; some blank cells indicate non-recorded or undisclosed data.

## Quality Control and Data Management
- Data capture quality: ODK used to reduce transcription errors through relational data coding.
- Data transmission: daily uploads to a central ODK Aggregate server at ILRI.
- Sample handling: tubes pre-identified with barcodes; barcodes scanned with smartphones to link samples to records; dry ice replenishment and sample integrity monitored.
- Laboratory quality: duplicate analyses; re-testing of borderline results.

## Ethical and Data Governance
- Ethics approval: AMREF Ethics and Scientific Review Committee.
- Consent: community, household, and individual consent obtained.
- Data privacy: coordinates withheld; study data encoded with household/individual identifiers; missing data indicated where applicable.

## Relevance for Environmental Monitoring and Data Sharing
- Demonstrates an end-to-end data pipeline: field sampling, biological testing, and data curation within a standardized framework.
- Structured dataset supports integration with other environmental and health data for broader monitoring and policy evaluation over time.
- Emphasizes data provenance, quality assurance, and reproducibility, enabling transparent audits and potential data sharing with appropriate governance.

## Key Takeaways for Analysts Monitoring the Environment
- Utilize standardized, auditable data collection and laboratory procedures to monitor environmental health proxies across land-use types.
- Ensure robust data governance: link field data to laboratory results with stable identifiers, and manage ethical constraints on data access (e.g., withheld coordinates).
- Design datasets to support future integration, mapping, and temporal monitoring, aligning with the goal of evaluating environmental health and policy performance over time.