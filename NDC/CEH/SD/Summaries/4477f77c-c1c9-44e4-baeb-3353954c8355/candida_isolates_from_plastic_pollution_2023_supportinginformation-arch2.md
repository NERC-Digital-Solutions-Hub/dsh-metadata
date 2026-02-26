# Data record: Pathogenic Candida isolates from plastic pollution samples from Scottish beaches

## Overview
- A study screened plastic pollution from marine, estuarine, and freshwater environments for pathogenic Candida species, assessing thermotolerance, antifungal drug resistance (MIC), and pathogenicity in a Galleria mellonella infection model.
- Data are organized into four CSV files:
  - candida_isolates.csv
  - mic_of_candida_isolates.csv
  - thermotolerance_of_candida_isolates.csv
  - virulence_of_candida_isolates.csv
- Scope and methods align with environmental health monitoring practices: standardised data collection, verification, quality assurance, cleaning, transformation, and structured outputs (reports, maps, charts) with datasets stored for portal upload.

## Sampling locations and timeline
- Six beaches in Scotland’s central belt (bathlng water beaches) sampled.
- Site types include Marine, Estuarine, and Freshwater; coordinates and substrate types recorded.
- Sampling dates: 27 March 2023; 2 May 2023; 26 May 2023.
- Analysis conducted March–September 2023.

## Data collection methods
- Sample collection: sterile forceps; samples placed in sterile bags.
- Candida recovery:
  - Pre-enrichment in YPD broth with antibiotics at 30°C for 48 h.
  - Plating on sabouraud glucose agar with chloramphenicol and gentamicin; fluconazole at multiple concentrations.
  - Subculture on CHROMagar Candida Plus; presumptive identification by colony colour/morphology.
  - 27 colonies archived as glycerol stocks.
- Species identification:
  - PCR targeting ITS region to identify C. albicans, C. glabrata, C. krusei, C. parapsilosis, C. tropicalis.
  - Sequencing of ITS1 region for confirmation; BLAST for species confirmation; reference strains used as positive controls.
- Antifungal susceptibility testing (MIC):
  - EUCAST broth microdilution method for yeasts.
  - Four antifungals tested: amphotericin B, caspofungin, fluconazole, voriconazole; across ten concentrations.
- Thermotolerance:
  - Pre-incubation at 18°C or 38°C for 24 h, then growth at 18/28/38°C for 24 h.
  - Growth measured via absorbance (570 nm); temperature monitored with iButtons.
- Pathogenicity model:
  - Galleria mellonella larvae infected with 10^5 CFU Candida per larva; incubation at 37°C; survival tracked up to 120 h.

## Data files and structure
- candida_isolates.csv
  - Columns include: Isolate number, Sampling_location, Location code, Plastic_type (Soft, Hard, or Polystyrene), PCR_Species_ID, BLAST_Species_ID, No._bases, Percentage_GC, Percentage_Identity, GenBank_Accession_number, Percentage_Survival_at_120h, and links to thermotolerance and virulence data.
- mic_of_candida_isolates.csv
  - Columns include: Isolate, Antifungal, MIC (mg/L).
- thermotolerance_of_candida_isolates.csv
  - Columns include: Isolate_Number, Species, absorbance measurements at various temperature pairings (e.g., 18degC-18degC, 18degC-28degC, etc.), Dilution, CFU_per_20µl (replicates), Average_CFU_per_ml.
- virulence_of_candida_isolates.csv
  - Columns include: Isolate, Replicate, Number_alive_(24h), Number_alive_(48h), Number_alive_(72h), Number_alive_(96h), Number_alive_(120h).
- All datasets are interlinked via Isolate_IDs to enable cross-analysis across species identity, antifungal resistance, thermotolerance, and virulence outcomes.

## Data quality and governance
- Completeness: Data checked for anomalous values; no missing data reported.
- Quality assurance: Standardised experimental protocols, controlled conditions, and documentation of methods to ensure reproducibility.
- Data storage: Structured, machine-readable CSV formats suitable for upload to environmental data portals and integration with other datasets.

## Data usage and interpretation
- Enables assessment of environmental Candida colonisation on plastics across multiple water types and seasons.
- Facilitates cross-comparison of species, resistance profiles, thermotolerance across temperatures, and virulence potential.
- Data can support monitoring of environmental health indicators and policy-relevant analyses, including integration with other marine plastic microbiology datasets.

## Responsible party
- Rebecca Metcalf (data collection and interpretation).

## Context and references
- Methodological standards cited include EUCAST for antifungal MIC determination; multiplex PCR identification of Candida species; ITS-based sequencing for confirmation.
- References:
  - EUCAST (2020) E.DEF 7.3.2
  - Carvalho et al. (2007)
  - Trost et al. (2004)

## Reuse considerations for monitoring analysts
- Data are prepared in a standardised, openly shareable format with clear linking keys across assays, enabling reproducible, longitudinal environmental health monitoring.
- The dataset aligns with goals of increasing data value and enabling access to underlying data for broader analyses and policy evaluation.