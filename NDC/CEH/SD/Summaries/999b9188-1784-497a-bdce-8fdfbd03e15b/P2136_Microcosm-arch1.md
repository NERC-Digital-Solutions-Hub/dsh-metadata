# Soil bacterial cell counts and moisture content from a water stress experiment [NERC Soil Biodiversity Programme] -Supporting Information Griffiths, R. I., Whiteley, A. S., O'Donnell, A. G., Bailey, M. J., Mayoux, D. and Burt-Smith, G.

- Context and aims
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biota diversity and their functional roles in key ecological processes.
  - 24 research projects examined soil structure, processes (carbon and nitrogen cycles), and roles of microfauna and flora across soils.
  - This data subset targets soil bacteria: their activity and diversity in response to drying and rewetting, using intact soil monoliths from Sourhope (Scotland) to study culture-dependent and culture-independent measures.

- Experimental design and site
  - Location: Sourhope field site, Macaulay/JH Institute, Scottish Borders; soil: organic-rich brown forest soil, pH ~4.5–5.0.
  - Monoliths: nine microcosms (approx. 15 cm depth; 45 cm diameter) assembled into three replicates of three treatments.
  - Treatments (July–October 2001; 11 sampling times S1–S11): 
    - A: continual wetting
    - B: drying
    - C: drying and rewetting
  - Rainfall manipulation: initial natural rainfall with regular distilled-water watering, then UV covers to exclude rainfall; rewetting occurred after about 1 month of drying.
  - Sampling: regular weekly sampling; cores taken from each pot, composited, then analyzed.
  - Standardization: plants trimmed and soils prepared to minimize edge effects; leachate drainage and soil moisture maintained per treatment.

- Measurements and methods
  - Culturability and total cell counts
    - Soil sample processing: 0.5 g wet soil dispersed in PBS with glass beads, serial dilutions prepared.
    - Culturing: plated on full-strength TSBA, 1/10-strength TSBA, and PSA media, with cycloheximide to suppress fungi; incubation at 18°C for 10 days; colonies counted.
    - Biomass extraction: biomass from plates pooled, suspended in PBS, stored for nucleic acid analyses.
    - Total bacterial cells: density gradient separation (Nycodenz), fixation, and SYBR Green II staining; enumeration by flow cytometry.
  - Soil moisture
    - Moisture determined by oven-drying soil at 105°C for 24 hours.

- Data structure and files
  - Two CSV data files:
    - P2136_Culturable_cells.csv: microcosm culturable cell counts across media (psa, tsba, 1/10 tsba), by microcosm, treatment, sampling date; cell counts per gram of dry soil.
    - P2136_Microcosm_Soil_Moisture.csv: soil moisture measurements across microcosms and sampling dates; moisture content in percent.
  - Key columns (shared): 
    - MICROCOSM_ID (numeric): microcosm identifier
    - TREATMENT (text): wet, dry, or rewet
    - SAMPLING_DATE (date): date of sampling
  - Additional columns:
    - For culturability file: MEDIA_USED (text), CELL_COUNT (numeric)
    - For moisture file: MOISTURE_CONTENT (numeric)

- Data quality, use, and scope notes
  - Data are subject to quality assurance; NERC does not warrant accuracy or fitness for any particular use and disclaims liability for any loss or damage arising from use.
  - The dataset provides both culture-dependent and culture-independent measurements of soil bacterial abundance, alongside precise moisture data, enabling analysis of responses to drying and rewetting.
  - Useful references for broader context and related analyses include:
    - Whiteley et al. 2003; J. Microbiol. Methods
    - Griffiths et al. 2003; Applied and Environmental Microbiology
  - Auxiliary materials and related documentation include the Sourhope Field Data Handbook and related UK soil biodiversity literature.

- Practical relevance for analysis
  - Enables correlations between soil moisture dynamics and bacterial abundance (culturable and total counts) under different moisture regimes.
  - Supports modeling of microbial community response to water stress and recovery, including comparisons across media and treatments.
  - Provides standardized metadata and a clear temporal sampling framework suitable for time-series analyses and cross-dataset integration (e.g., linking moisture content to microbial activity).