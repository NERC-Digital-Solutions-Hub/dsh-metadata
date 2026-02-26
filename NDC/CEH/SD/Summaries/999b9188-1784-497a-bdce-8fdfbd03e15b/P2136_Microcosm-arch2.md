# Soil bacterial cell counts and moisture content from a water stress experiment [NERC Soil Biodiversity Programme] -Supporting Information

- Purpose and context
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) assessing soil biota diversity and functional roles in key ecological processes.
  - Focuses on soil bacterial activity and diversity under perturbation (drying and rewetting) in intact soil monoliths from Sourhope field site, Scotland.
  - Data aim to enable understanding of microbial responses to moisture perturbations and allow linkage to broader soil biodiversity studies.

- Study site and experimental design
  - Location: Sourhope field site (Scottish Borders); soils described as organic-rich brown forest soil (pH 4.5–5.0).
  - Setup: Nine microcosms (3 replicates × 3 treatments) created from intact grassland monoliths (~15 cm depth; 45 cm diameter core).
  - Treatments: continual wetting (A), drying (B), and drying followed by rewetting (C).
  - Duration and timing: Experiment ran July–October 2001; 11 sampling events (S1–S11).
  - Weather control: UV-transparent covers installed 14 August to exclude rainfall for experimental manipulation; initial S1–S3 had natural rainfall plus regular watering; after final S3, drying began; rewetting on 18 September (S6).

- Measurements and sampling
  - At each sampling: four 1-cm-diameter cores per pot; combined for analysis; roots and plant material removed.
  - Moisture measurement: oven-dried at 105°C for 24 hours to determine soil moisture content.
  - Bacterial analyses:
    - Culturable cells: soil dispersed in PBS; serial dilutions plated on full-strength TSBA, 1/10-strength TSBA, and PSA with cycloheximide; 10-day incubation at 18°C; colonies counted for culturability on each medium.
    - Biomass from cultured colonies: biomass collected from plates for potential nucleic acid analyses.
    - Total bacterial cells: Nycodenz density gradient extraction from soil, fixation, SYBR Green II staining, and enumeration by flow cytometry (FACS).
  - Sample handling: 0.5 g soil (wet weight) used for analyses; results reported per gram dry soil.

- Data products (two CSV datasets)
  - P2136_Culturable_cells.csv
    - MICROCOSM_ID: microcosm identifier
    - TREATMENT: wet, dry, or rewet
    - SAMPLING_DATE: date of sampling
    - MEDIA_USED: medium type (psa, tsba, or 1/10 tsba)
    - CELL_COUNT: culturable cell count per gram dry weight soil
  - P2136_Microcosm_Soil_Moisture.csv
    - MICROCOSM_ID: microcosm identifier
    - TREATMENT: wet, dry, or rewet
    - SAMPLING_DATE: date of sampling
    - MOISTURE_CONTENT: soil moisture percentage

- Measurement methods and references
  - Culturable cells: plating on media with cycloheximide to suppress fungi; incubation and colony counting.
  - Total cells: flow cytometry after Nycodenz purification and SYBR Green II staining.
  - Related publications for context and methods:
    - Whiteley, Griffiths, and Bailey (2003). Analysis of microbial functional diversity by flow cytometric analysis and CTC+ sorting. J Microbiol Methods.
    - Griffiths, Whiteley, O’Donnell, and Bailey (2003). Physiological and Community Responses of Established Grassland Bacterial Populations to Water Stress. Appl Environ Microbiol.
  - Additional resources:
    - Sourhope Field Data Handbook (2003) and related UK Soil Biodiversity Programme literature.

- Data quality, access, and rights
  - Data are subject to quality assurance procedures; NERC does not warrant accuracy or fitness for a particular use.
  - No liability for any loss or damage arising from use of the data.
  - Data are provided to support analyses of environmental monitoring and microbial responses to moisture perturbations.