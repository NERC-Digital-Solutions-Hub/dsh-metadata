# What has been recorded and what form does the data take?

- Purpose: Document a study screening environmental plastic pollution for pathogenic Candida species, assessing thermotolerance, antifungal resistance, and virulence in a Galleria mellonella infection model.
- Data scope: Four CSV files containing isolate metadata, antifungal susceptibility, thermotolerance, and virulence outcomes.

## Data collection overview

- Sampling locations: Six beaches in Scotland's central belt (labeled A–F; bathing water beaches), with site types spanning marine, estuarine, and freshwater.
- Sampling dates: Spring 2023 (27 Mar, 2 May, 26 May).
- Analysis period: March–September 2023.
- Sample handling: Sterile collection with forceps into sterile bags; replicate composite samples processed from each plastic type.

## Data collection and laboratory methods

- Candida recovery and isolation:
  - Pre-enrichment in YPD broth with antibiotics; incubation at 30°C.
  - Plating on sabouraud glucose agar with chloramphenicol and gentamicin, plus fluconazole at varying concentrations.
  - Subculture to CHROMagar Candida Plus for presumptive ID.
  - Glycerol stocks prepared from colonies.
- Species identification:
  - Colony morphology on CHROMagar for presumptive ID.
  - PCR targeting ITS region to identify C. albicans, C. glabrata, C. krusei, C. parapsilosis, C. tropicalis; included positive clinical controls.
  - ITS1 sequencing to confirm species; BLAST against NCBI databases for final ID.
- Antifungal susceptibility (MIC):
  - EUCAST broth dilution method for yeasts.
  - Four antifungals tested (amphotericin B, caspofungin, fluconazole, voriconazole) across ten concentrations.
- Thermotolerance assay:
  - Initial incubation at 18°C or 38°C for 24 h, then exposure to 18°C, 28°C, or 38°C.
  - Growth assessed via absorbance at 570 nm; cell preparation and plating for CFU counts; temperature monitoring with iButton loggers.
- In vivo virulence assay:
  - Galleria mellonella infection model: groups of 10 larvae injected with 10^5 CFU per larva; 120 h observation; control injections with PBS.
  - Experiments conducted in biological triplicate.

## Data quality and provenance

- Completeness: No missing data reported; data checked for anomalous values and plausible ranges.
- Data ownership: Collected and interpreted by Rebecca Metcalf.
- Data formats: Four CSV files with linked identifiers to connect isolates across datasets.

## Data file contents and structure

- candida_isolates.csv
  - Isolate number; sampling_location; location code (A–F); plastic_type (soft, hard, or polystyrene); PCR_Species_ID; BLAST_Species_ID; sequence metrics (No._bases, %GC, % identity, GenBank Accession); 120h survival; MIC values for fluconazole, amphotericin B, caspofungin, voriconazole; thermotolerance absorbance at various temperature pairs; CFU data and derived averages.
- mic_of_candida_isolates.csv
  - Isolate link; antifungal (drug name); MIC (mg/L).
- thermotolerance_of_candida_isolates.csv
  - Isolate link; species; absorbance readings at 570 nm for 18/18, 18/28, 18/38, 38/18, 38/28, 38/38 combinations; dilution; CFU data (replicate 1–3); average CFU per mL.
- virulence_of_candida_isolates.csv
  - Isolate link; replicate; number alive at 24, 48, 72, and 96, 120 hours.

## Geographic and temporal details

- Sampling sites:
  - A (Marine, 55.640°N, -4.808°W; 2 May 2023; Sand)
  - B (Estuarine, 55.919°N, -4.464°W; 2 May 2023; Sand/Silt)
  - C (Freshwater, 55.731°N, -3.906°W; 2 May 2023 and 26 May 2023; Grass bank, silt riverbed)
  - D (Freshwater, 56.021°N, -3.759°W; 27 Mar 2023; Mud/silt)
  - E (Marine, 55.968°N, -3.136°W; 26 May 2023; Sand)
  - F (Marine, 55.954°N, -3.109°W; 27 Mar 2023; Sand)

## Purpose and grant context

- Primary aim: Assess the ability of environmental Candida spp. to colonise plastic pollution and survive under varying conditions.
- Funding: UKRI NERC grants for projects on microbial hitchhikers of marine plastics (NE/S005196/1) and SPACES (NE/V005847/1).

## References and methodology basis

- EUCAST definitive document for antifungal susceptibility testing (E.DEF 7.3.2).
- Multiplex PCR identification of clinically relevant Candida species (Carvalho et al., 2007).
- Identification of yeasts by PCR/RFLP (Trost et al., 2004).