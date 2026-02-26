# Microbial biomass measurements from an upland grassland liming experiment [NERC Soil Biodiversity Programme] Johnson, D., Leake, J. R., & Read, D. J. University of Sheffield

- Context and aims
  - Part of the NERC Soil Biodiversity Thematic Programme (1999) focused on understanding soil biota diversity and functional roles.
  - Centreed on a large field experiment at Sourhope (Macaulay/Hutton Institute), with 24 projects exploring soil structure, processes (carbon and nitrogen cycles), and microbial and faunal roles.
  - Dataset pertains to Project 2117: examining the effect of mycorrhizal mycelium on soil microbial communities and its role in carbon and nutrient cycles.

- Study site and design
  - Location: Sourhope field site, Kelso, Scotland (NGR NT 854196; altitude ~500 m).
  - Experimental setup: 20 turfs from upland grassland inside a 5-block x 4-treatment completely randomized design.
  - Treatments: control, lime (CaCO3), N, lime + N.
  - Lime and N application details: lime at 0.6 kg m^-2; NH4NO3 at 12 g m^-2; plots mown in summer; absence of fertilizer for 40 years prior.
  - Plant community: mixture of 24 species, many forming AM-mycorrhizas; soil type acidic brown earths (pH 4.5–5.0), ~40% clay in 2 mm fraction.
  - Horizons studied: FH and Ah.

- Data collected and methods
  - Measurements: soil microbial biomass carbon (Cmic), basal respiration, and enzyme activities (through respiration-based assays).
  - Experimental manipulation and sampling: seeds of Agrostis capillaris used to perturb AMF responses; seedlings inserted into turfs and later removed to preserve AMF dynamics.
  - Respiration measurements: sealed Respicond system with intact soil cores; incubation at 22°C; respiration logged over 8 hours.
  - Cmic estimation: substrate-induced respiration using glucose amendment; maximum rate used to estimate Cmic.
  - Metabolic quotient (qCO2): basal respiration divided by Cmic.

- Data product and structure
  - Main dataset: 1081 – Soil microbial biomass 1.0 (P2117_SOIL_MICROBIAL_BIOMASS_1.csv).
  - Key fields:
    - SAMPID: unique sample identifier
    - SAMPLE_DATE: date of sampling
    - BLOCK: experimental block (1–5)
    - MAIN_PLOT: main plot label (A–F)
    - HORIZON: soil horizon (FH or Ah)
    - TREATMENT: applied treatment (control, lime, N, lime+N)
    - CMIC: microbial biomass carbon (mg C per g soil dw)
    - BASAL: basal respiration rate (mg CO2 g soil dw^-1 hr^-1)
    - QC02: metabolic quotient (mg CO2 g Cmic^-1 hr^-1)
  - Data dictionary and data type notes are provided, including units and descriptions for each field.

- Quality assurance and limitations
  - QA steps included numeric range checks, format conformity, and logical integrity checks.
  - Data quality: subject to QA procedures, but NERC disclaims warranty of accuracy or suitability for a particular use; no liability for data use.
  - Additional context: references, coursework, and field data handbooks cited to support interpretation and provenance (e.g., Scott et al. 2003; Johnson et al. 2005; Usher et al. 2006).

- Access, governance, and metadata
  - Associated with the NERC Soil Biodiversity Programme; documented in the SOURHOPE Field Data Handbook and related publications.
  - Dataset includes a clear metadata schema (sample IDs, dates, experimental design, horizons, treatments, and measured variables) to support discoverability and reuse.
  - Data provenance links to the broader project context (Project 2117) and the long-term field site record.

- Implications for data leadership
  - Demonstrates the importance of a well-documented data dictionary, clear experimental design metadata, and standardized variables to enable cross-study integration and meta-analyses.
  - Highlights challenges in long-term ecological data sharing: complex site histories, multiple horizons, and multi-dimensional measurements requiring careful attention to harmonization and metadata completeness.
  - Underlines the need for explicit data quality statements and disclaimers to manage user expectations and responsibilities.
  - Suggests opportunities for improved data stewardship: centralized access points, consistent naming conventions, and explicit licensing to enhance discoverability and reuse across networks.