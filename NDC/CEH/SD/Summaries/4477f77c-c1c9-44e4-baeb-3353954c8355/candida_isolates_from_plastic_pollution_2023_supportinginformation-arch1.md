# Candida isolates from plastic pollution: thermotolerance, antifungal resistance, and virulence in a Galleria model of infection

## Overview
- Study screens plastic pollution for pathogenic Candida species in marine, estuarine, and freshwater environments.
- Data describe isolates and their characteristics: thermotolerance, antifungal drug resistance (MIC), and pathogenicity in a Galleria mellonella infection model.
- Four CSV data files capture isolate metadata, drug resistance, thermotolerance, and virulence outcomes.

## Data collected (data types and structure)
- candida_isolates.csv: core isolate metadata (ID, sampling location, plastic type, species ID from PCR/BLAST, sequencing details, and preliminary survival indicators).
- mic_of_candida_isolates.csv: links to candida_isolates and MIC values for selected antifungals.
- thermotolerance_of_candida_isolates.csv: links to candida_isolates with growth/absorbance data across temperature conditions (18°C, 28°C, 38°C) after initial environmental or human-physiology temperature pretreatment.
- virulence_of_candida_isolates.csv: links to candida_isolates with Galleria mellonella survival data at multiple time points (24, 48, 72, 96, and 120 hours), across replicates.

## Sampling locations and context
- Six beaches in Scotland’s central belt (A–F), covering marine, estuarine, and freshwater sites.
- Bathing water beaches include A*, B, C, D, E, F*.
- Substrates varied: sand, sand/silt, grass bank, mud/silt.

## Temporal scope
- Sampling dates in spring 2023: 27 March, 2 May, 26 May.
- Analysis of samples conducted March–September 2023.

## Data collection and laboratory methods
- Field collection: sterile forceps; samples placed into sterile bags.
- Candida recovery: replicate composite samples enriched in yeast extract peptone dextrose (YPD) with gentamicin and chloramphenicol; incubation at 30°C for 48 h with shaking.
- Isolation and identification:
  - Plating on Sabouraud dextrose agar with antibiotics and fluconazole at varying concentrations.
  - Subculture to CHROMagar Candida Plus for presumptive identification by colony colour/morphology.
  - Colony freezing in glycerol stocks.
  - PCR targeting ITS region to identify five common pathogenic Candida species (C. albicans, C. glabrata, C. krusei, C. parapsilosis, C. tropicalis); sequencing confirmation via ITS1 region.
  - BLAST comparison against NCBI databases for species confirmation.
- Antifungal susceptibility (MIC):
  - EUCAST broth microdilution method for yeasts, four antifungals (amphotericin B, caspofungin, fluconazole, voriconazole) across ten concentrations.
- Thermotolerance assay:
  - Initial incubation at 18°C or 38°C for 24 h to simulate environmental versus human-body temperatures.
  - Subsequent exposure to 18°C, 28°C, or 38°C; growth assessed by absorbance at 570 nm and corroborated by cell handling and CFU estimates.
  - Temperature monitoring using iButton data loggers.
- Galleria mellonella infection model:
  - Groups of 10 larvae injected with 10 µL of Candida suspension (10^5 CFU/larvae).
  - Biological triplicate experiments; PBS control for handling/inoculation effects.
  - Incubation at 37°C; survival tracked every 24 h for up to 120 h.

## Purpose and rationale
- To assess the ability of environmental Candida spp. to colonise plastic pollution ( Plastisphere).
- To fulfill requirements of UKRI NERC grants related to microbial hitchhikers on marine plastics and related ecological studies.

## Responsible personnel and quality assurance
- Data collection and interpretation led by Rebecca Metcalf.
- Quality control: data checked for anomalies and boundary limits; no missing data reported.

## Completeness and data quality considerations
- Completeness: reported as complete with no absent data.
- Data integration: multiple datasets link via isolate IDs to enable cross-dataset analyses (species, MIC, thermotolerance, virulence).

## Data file contents (high-level schema)
- candida_isolates.csv
  - Isolate number; sampling_location; location code; plastic_type; PCR_Species_ID; BLAST_Species_ID; sequence metrics; GenBank accession; % survival at 120 h; antifungal MIC placeholders; temperature absorbance measurements.
- mic_of_candida_isolates.csv
  - Isolate; Antifungal; MIC.
- thermotolerance_of_candida_isolates.csv
  - Isolate_Number; Species; Absorbance at 570 nm under 18/18, 18/28, 18/38; Absorbance under 38/18, 38/28, 38/38; Dilution; CFU data for three replicates; Average CFU per mL.
- virulence_of_candida_isolates.csv
  - Isolate; Replicate; Number_alive at 24, 48, 72, 96, 120 hours.

## Potential analyses and questions for analysts
- Correlations between plastic type and Candida species distribution and virulence profiles.
- Associations between antifungal resistance (MIC) and thermotolerance across environmental conditions.
- Relationship between environmental site characteristics (marine/estuarine/freshwater, substrate) and isolate pathogenic traits.
- Predictive modeling of virulence outcomes from combined metadata (species, MIC, thermotolerance, sampling site).
- Temporal trends across sampling days and their relation to environmental factors and plastic availability.

## References (methodological basis)
- EUCAST broth dilution method for antifungal susceptibility testing of yeasts (Arendrup et al., 2020).
- Multiplex PCR identification of Candida species (Carvalho et al., 2007).
- Identification of clinically relevant yeasts by PCR/RFLP (Trost et al., 2004).