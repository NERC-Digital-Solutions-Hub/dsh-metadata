# Cand Candida isolates from plastic pollution: identification, antifungal resistance, thermotolerance, and virulence in a Galleria model of infection

- Purpose and scope
  - Dataset from a study screening different types of plastic pollution in marine, estuarine, and freshwater environments for pathogenic Candida species.
  - Four CSV data files containing isolates, antifungal resistance, thermotolerance, and virulence data.
  - Aimed at assessing the ability of Candida spp. to colonise environmental plastic and informing environmental health monitoring efforts.

- Study locations and timing
  - Sampling sites: six beaches in Scotland's central belt (sites A–F; bath-ing water beaches; various site types: marine, estuarine, freshwater).
  - Coordinates and substrate types varied by site; sampling occurred on three spring dates in 2023: 27 March, 2 May, 26 May.
  - Analysis of samples conducted March–September 2023.

- Methods and instrumentation (overview)
  - Sample collection: sterile forceps, collected into sterile bags.
  - Isolation and enrichment: replicate composites pre-enriched in 100 ml YPD broth with gentamicin and chloramphenicol; incubated at 30°C for 48 h with shaking.
  - Culturing and preliminary identification: spread onto sabouraud glucose agar with antibiotics and fluconazole at graded concentrations; colonies streaked onto CHROMagar Candida Plus for presumptive species based on colour/morphology.
  - Cryopreservation: 27 colonies stored as glycerol stocks at -20°C.
  - Species confirmation: colony PCR targeting ITS region to identify five common pathogenic Candida species; sequencing and BLAST confirmation; positive controls included.
  - Antifungal susceptibility: MIC testing for four antifungals (amphotericin B, caspofungin, fluconazole, voriconazole) across ten concentrations following EUCAST methodology for yeasts.
  - Species confirmation by sequencing: ITS1 region sequenced after DNA extraction; confirmation via BLAST.
  - Thermotolerance testing: isolates incubated at 18°C or 38°C for 24 h, then exposed to 18°C/28°C/38°C; growth measured by absorbance and plate-based CFU counts; temperature monitored with iButton loggers.
  - Galleria mellonella infection model: injections of Candida suspensions into larvae; controls with PBS; survival tracked for 120 h.

- Data structure and file contents
  - candida_isolates.csv
    - Contains: isolate number, sampling location, code, plastic type, PCR species ID, BLAST species ID, sequence metrics (no. bases, %GC, % identity), GenBank accession, survival after 120 h in Galleria, antifungal MICs (fluconazole, amphotericin B, caspofungin, voriconazole), and thermotolerance absorbance data at multiple temperature pairings.
  - mic_of_candida_isolates.csv
    - Contains: link to isolate, antifungal tested, MIC value (mg/L).
  - thermotolerance_of_candida_isolates.csv
    - Contains: isolate link, species, absorbance readings for 18/18, 18/28, 18/38, 38/18, 38/28, 38/38 °C pairings, dilution, CFU counts (three replicates), and average CFU per mL.
  - virulence_of_candida_isolates.csv
    - Contains: isolate link, replicate, alive counts in Galleria at 24–120 h (numbers alive at 24, 48, 72, 96, 120 h).

- Data completeness and quality
  - Data were checked for anomalous values and defined limits; no missing data reported.

- Data provenance and responsibility
  - Responsible individual: Rebecca Metcalf.
  - Data collection and interpretation aligned with the UKRI NERC grant-supported project on microbial hitchhikers of marine plastics and related habitats.

- Key references
  - EUCAST method for antifungal MIC determination in yeasts.
  - Multiplex PCR identification of Candida species.
  - ITS region sequencing for species confirmation.