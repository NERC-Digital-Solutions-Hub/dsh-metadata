# Data from a study screening different types of plastic pollution in marine, estuarine, and freshwater environments for pathogenic species of Candida, and assessing their thermotolerance, antifungal drug resistance, and pathogenicity in a Galleria model of infection

- Scope and data structure
  - Study screens plastic pollution for pathogenic Candida species (C. albicans, C. glabrata, C. krusei, C. parapsilosis, C. tropicalis) across marine, estuarine, and freshwater environments.
  - Four CSV data files included:
    - candida_isolates.csv
    - mic_of_candida_isolates.csv
    - thermotolerance_of_candida_isolates.csv
    - virulence_of_candida_isolates.csv

- Data collection sites and timing
  - Sampling locations: six beaches in Scotland’s central belt (A–F), including marine, estuarine, and freshwater sites; bath-ing water beaches noted.
  - Sampling dates: 27 March 2023; 2 May 2023; 26 May 2023.
  - Analysis window: March–September 2023.

- Data collection and laboratory workflow
  - Sample collection: sterile collection of plastic pieces with forceps; stored in sterile bags.
  - Candida isolation and enrichment:
    - Pre-enrichment in YPD broth with antibiotics; incubation at 30°C for 48 h.
    - Plating on sabouraud glucose agar with chloramphenicol and gentamicin, with fluconazole at 0, 16, 64 mg/L.
    - Subculture onto CHROMagar Candida Plus; incubation results used for presumptive ID.
    - Glycerol stocks prepared and stored.
  - Species identification and confirmation:
    - Colony PCR targeting ITS region to identify major pathogenic Candida species.
    - Sequencing of ITS1 region; confirmation via BLAST against reference sequences.
  - Antifungal susceptibility (MIC):
    - EUCAST broth microdilution method for yeasts.
    - Tested antifungals: amphotericin B, caspofungin, fluconazole, voriconazole across multiple concentrations.
  - Sequencing and verification:
    - ITS1 sequencing with Sanger method for final ID confirmation.
  - Thermotolerance assay:
    - Initial conditioning at 18°C or 38°C for 24 h, then growth at 18, 28, or 38°C.
    - Growth measured by absorbance at 570 nm; temperature monitored with iButton loggers.
  - Galleria mellonella virulence assay:
    - Injections of 10 µL containing 10^5 CFU per larva; groups of 10 larvae; biological triplicates.
    - Survival tracked for 120 h; PBS control for injury/contamination effects.

- Data provenance, responsibility, and quality
  - Responsible data custodian: Rebecca Metcalf.
  - Completeness and QA: data checked for anomalies and bounds; no missing data reported.
  - Data are structured to support cross-table linking via isolate identifiers.

- Data file contents and key variables (overview)
  - candida_isolates.csv
    - Isolate number; sampling location code; plastic type (soft, hard, or polystyrene); PCR-based species ID; BLAST species ID; sequence metrics; GenBank accession; percentage survival at 120 h in Galleria; MIC values for fluconazole, amphotericin B, caspofungin, voriconazole; absorbance readings at 18/18, 18/28, 18/38, 38/18, 38/28, 38/38 for each temperature pairing.
  - mic_of_candida_isolates.csv
    - Links to candida_isolates.csv; antifungal tested; MIC value.
  - thermotolerance_of_candida_isolates.csv
    - Isolate reference; Candida species; absorbance at 570 nm for each temperature pairing (18/18, 18/28, 18/38, 38/18, 38/28, 38/38); dilution; CFU per 20 µL (replicate 1–3); average CFU per mL.
  - virulence_of_candida_isolates.csv
    - Isolate reference; replicate; number of Galleria larvae alive at 24, 48, 72, 96, and 120 h.

- Data governance and reuse considerations
  - Data are provided as CSV files with explicit linkage keys across tables to enable integration and re-use.
  - Metadata includes sampling location codes, plastic type categories, species identifications (PCR and BLAST), GenBank accession numbers, and detailed phenotypic measurements (MICs, thermotolerance, and virulence outcomes).
  - Documentation references standardized methods for species identification (ITS PCR, ITS1 sequencing), EUCAST MIC testing, and Galleria infection assays.
  - Potential reuse in cross-study analyses of environmental microbiomes on plastics, antifungal resistance surveillance, or comparative virulence studies, with attention to harmonization of temperature and exposure conditions across datasets.

- References
  - EUCAST DEFINITIVE DOCUMENT E.DEF 7.3.2 for antifungal MIC testing method.
  - Carvalho et al. (2007) multiplex PCR identification of eight clinically relevant Candida species.
  - Trost et al. (2004) identification of clinically relevant yeasts by PCR/RFLP.