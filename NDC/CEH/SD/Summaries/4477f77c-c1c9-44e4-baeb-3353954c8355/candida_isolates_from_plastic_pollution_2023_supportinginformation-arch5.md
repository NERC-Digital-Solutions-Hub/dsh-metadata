# Candida isolates from plastics: data on minimum inhibitory concentration, thermotolerance and virulence in a Galleria model of infection

- Purpose and scope
  - Study screening for pathogenic Candida species on environmental plastics (marine, estuarine, freshwater) to assess thermotolerance, antifungal resistance, and pathogenicity in a Galleria mellonella model.
  - Supports UKRI NERC grants on microbial hitchhikers of marine plastics and related projects.

- Datasets and data files
  - Four CSV files:
    - candida_isolates.csv: core isolate information including sampling location, plastic type, species IDs (PCR and BLAST), sequencing data, and basic metadata.
    - mic_of_candida_isolates.csv: links isolates to antifungal minimum inhibitory concentrations (MIC) across multiple drugs.
    - thermotolerance_of_candida_isolates.csv: growth/absorbance data across temperatures (18, 28, 38°C) and corresponding CFU metrics.
    - virulence_of_candida_isolates.csv: Galleria mellonella survival data at multiple time points (24–120 h) for each isolate.

- Data collection: where and when
  - Locations: six beaches in Scotland’s central belt (marine, estuarine, freshwater), including A–F site codes and coordinates.
  - Dates: plastic sampling on 27 Mar, 2 May, and 26 May 2023; analysis conducted Mar–Sep 2023.
  - Sample collection: sterile forceps, sterile bags; replicate composite samples per plastic type per site.

- Laboratory and analytical methods
  - Isolation and culture: enrichment in YPD with antibiotics, plating on SG with chloramphenicol and antifungals, incubation at 30°C.
  - Identification: CHROMagar Candida Plus for presumptive identification, followed by colony PCR targeting ITS for common pathogenic species (C. albicans, C. glabrata, C. krusei, C. parapsilosis, C. tropicalis); sequencing of ITS1 for confirmation with BLAST.
  - MIC testing: EUCAST broth microdilution method for yeasts; tested amphotericin B, caspofungin, fluconazole, voriconazole across defined ranges.
  - Thermotolerance: pre-exposure at 18°C or 38°C for 24 h, then growth at 18/28/38°C with absorbance measurements and CFU enumeration.
  - Virulence: Galleria mellonella infection model with 10 µL of 10^5 CFU per larva, incubation at 37°C, survival tracked for 120 h; PBS-injected controls included.

- Data completeness and quality assurance
  - Data checked for anomalies and bounds; no missing data reported.
  - Documentation ties each MIC, thermotolerance, and virulence measurement to the corresponding isolate entry.

- Provenance and responsibility
  - Responsible for collection and interpretation: Rebecca Metcalf.
  - Data collected and organized to enable cross-dataset linking via isolate numbers (candida_isolates.csv) and cross-referenced with MIC, thermotolerance, and virulence datasets.

- Data structure and field highlights (high-level)
  - candida_isolates.csv: isolate number, sampling location, sampling coordinates, plastic type, PCR/BLAST species IDs, sequence data (No. bases, % GC, accession numbers), and initial growth/survival indicators.
  - mic_of_candida_isolates.csv: isolate reference, antifungal tested, MIC values.
  - thermotolerance_of_candida_isolates.csv: isolate reference, species, absorbance at 570 nm under various temperature pairings, dilution, CFU counts, and calculated averages.
  - virulence_of_candida_isolates.csv: isolate reference, replicate, and numbers alive at 24, 48, 72, and 120 hours.

- Reuse considerations
  - Studies focused on environmental colonization by Candida spp. on plastics; data can support meta-analyses on antifungal resistance, environmental thermotolerance, and virulence potential.
  - Governing references include EUCAST methods and Candida identification protocols; proper citation recommended for reuse.

- References
  - EUCAST (2020) Definite document for antifungal MIC methods.
  - Carvalho et al. (2007) Multiplex PCR identification of Candida species.
  - Trost et al. (2004) PCR/RFLP identification of clinically relevant yeasts.