Candida isolates from plastics in marine, estuarine, and freshwater environments for pathogenic species of Candida, and subsequently assessed these isolates for their thermotolerance, anti-fungal drug resistance, and their pathogenicity in a Galleria model of infection.

## Overview of the dataset
- Four CSV data files:
  - candida_isolates.csv
  - mic_of_candida_isolates.csv
  - thermotolerance_of_candida_isolates.csv
  - virulence_of_candida_isolates.csv
- Data describe Candida isolates associated with plastic pollution and their biological traits:
  - Species identification (PCR and ITS sequencing)
  - Antifungal resistance (MIC to four antifungals)
  - Thermotolerance profiles at multiple temperatures
  - In vivo virulence data using Galleria mellonella model
- Completeness: data were checked for anomalies; no missing data reported.

## Spatial and temporal coverage
- Sampling locations: six beaches in Scotland's central belt (A–F), with site-type classifications:
  - Marine, Estuarine, Freshwater, and Bathing water beaches
- Coordinates provided for each site
- Sampling dates: spring 2023 (27 March, 2 May, 26 May)
- Analysis period: March–September 2023

## Data collection and laboratory methods (GIS-friendly summary)
- Sample collection: sterile forceps, sterile bags
- Microbiological processing:
  - Pre-enrichment in YPD with antibiotics; incubate at 30°C
  - Plating on SG agar with chloramphenicol, gentamicin, and fluconazole at multiple concentrations
  - Isolation on CHROMagar Candida Plus; colony morphology used for presumptive ID
- Species identification:
  - PCR targeting ITS region for five Candida species
  - Sanger sequencing of ITS1 region; BLAST confirmation
- Antifungal susceptibility testing (MIC):
  - EUCAST broth dilution method for yeasts
  - Drugs tested: amphotericin B, caspofungin, fluconazole, voriconazole
- Thermotolerance testing:
  - Pre-incubation at environmental (18°C) or human body (38°C) temperature
  - Growth at 18°C, 28°C, or 38°C; absorbance measured as growth proxy
- Virulence testing (Galleria mellonella model):
  - Inoculation with 10^5 CFU per larva; incubation at 37°C; survival tracked up to 120 h
  - Controls with PBS to account for handling/contamination mortality

## Data structure and field relationships
- candida_isolates.csv
  - Isolate_id, Sampling_location (A–F), Location name, Plastic_type (Soft, Hard, Polystyrene)
  - PCR_Species_ID, BLAST_Species_ID, species details, GenBank accession, sequence metrics
  - Microbial Genes/GenBank data, Percent_GC, Percentage_Identity
  - Percentage_Survival_at_120h from virulence tests
- mic_of_candida_isolates.csv
  - Links to candida_isolates.csv via Isolate
  - Antifungal, MIC (mg/L)
- thermotolerance_of_candida_isolates.csv
  - Isolate_Number links to candida_isolates.csv
  - Species, absorbance data at multiple temperature combinations (18/28/38°C pairs)
  - Dilution and CFU measurements, Average_CFU_per_ml
- virulence_of_candida_isolates.csv
  - Isolate links to candida_isolates.csv
  - Replicate, Number_alive at 24, 48, 72, 96, 120 hours
- Key linking: Isolate identifiers connect across datasets to allow integrated analysis

## Purpose and provenance
- Primary aim: assess the ability of Candida spp. to colonise environmental plastic pollution
- Funding and use: aligned with UKRI NERC grants
  - Microbial hitchhikers of marine plastics: NE/S005196/1
  - NERC-GCRF SPACES project: NE/V005847/1
- Lead contact: Rebecca Metcalf

## Quality assurance and completeness
- Data checked for anomalies and plausible ranges
- No missing data reported

## Potential GIS and data visualization applications
- Map distribution of Candida isolates by sampling site (A–F) with coordinates
- Spatial analysis of species distribution and plastic type across beaches
- Multivariate maps showing MIC values by location and plastic type
- Temporal mapping: compare across the three sampling dates (27 Mar, 2 May, 26 May)
- Overlay with environmental layers (water type, substrate, site type) to explore drivers of colonization and virulence
- Link to supplier and reference sequences for reproducibility and cross-study comparison

## References
- EUCAST Def 7.3.2 method for antifungal susceptibility testing of yeasts
- Carvalho et al. 2007, Multiplex PCR identification of eight clinically relevant Candida species
- Trost et al. 2004, Identification of clinically relevant yeasts by PCR/RFLP