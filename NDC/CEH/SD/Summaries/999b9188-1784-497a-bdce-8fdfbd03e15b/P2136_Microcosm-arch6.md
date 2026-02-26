# Soil bacterial cell counts and moisture content from a water stress experiment [NERC Soil Biodiversity Programme] -Supporting Information

## Background
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) investigating soil biota diversity and functional roles in key ecological processes.
- Field site: Sourhope, Scottish Borders; organics-rich brown forest soil; grassland monoliths used to study responses to drying and rewetting.
- Objectives for the soil bacteria study: monitor molecular diversity and physiological status of bacterial communities under water stress and recovery; compare total cell counts with culture-based counts using flow cytometry of SYBR II-stained cells.

## Experimental set-up and sampling
- Sample origin: intact grassland monoliths excavated to ~15 cm depth; transported to laboratory and placed in pots to minimize edge effects.
- Experimental design: 9 microcosms (3 replicates of 3 treatments) with three regimens:
  - A: continual wetting
  - B: drying
  - C: drying followed by rewetting
- Duration: 3 months (July–October 2001); 11 sampling events (S1–S11).
- Treatment timeline: S1–S3 natural rainfall with regular watering; rainfall exclusion introduced on 14 Aug; drying from ~20 Aug; rewetting initiated ~18 Sep and continued like treatment A.
- Sampling method: four 1-cm-diameter cores per pot to ~7 cm depth; samples homogenized; 0.5 g soil used for analyses.
- Environment: open-air maintenance at Oxford; soil moisture and microbial activity tracked throughout.

## Culturability and total cell count of bacterial community
- Cultural assays:
  - Soil dispersed in PBS with glass beads, decimally diluted, plated on full-strength TSBA, 1/10-strength TSBA, and PSA, all with cycloheximide to suppress fungi.
  - Incubation: 10 days at 18°C; colonies counted for culturability; biomass from plates used for nucleic acid extraction.
- Total cell counts:
  - 0.5 g soil dispersed in PBS; density gradient separation using Nycodenz; cells fixed with paraformaldehyde; stained with SYBR Green II.
  - Enumeration performed by flow cytometry (FACSCalibur) after preparation.

## Data structure
Two CSV files provided:
- Drought experiment. Microcosm culturable cell counts (P2136_Culturable_cells.csv)
  - MICROCOSM_ID (numeric): microcosm identifier
  - TREATMENT (text): water treatment (wet, dry, rewet)
  - SAMPLING_DATE (date): sampling date
  - MEDIA_USED (text): media type (psa, tsba, 1/10 tsba)
  - CELL_COUNT (numeric): culturable cell count per gram dry weight soil
- Drought experiment. Microcosm moisture contents of soil samples (P2136_Microcosm_Soil_Moisture.csv)
  - MICROCOSM_ID (numeric): microcosm identifier
  - TREATMENT (text): water treatment (wet, dry, rewet)
  - SAMPLING_DATE (date): sampling date
  - MOISTURE_CONTENT (numeric): soil water content (%)
Notes:
- Data were quality-assured per project procedures; NERC does not warrant accuracy or imply fitness for a particular use; no liability for data use.

## Usage and references
- Key related publications:
  - Whiteley, Griffiths, and Bailey (2003). Analysis of microbial functional diversity in water-stressed soils by flow cytometry and CTC+ sorting.
  - Griffiths et al. (2003). Physiological and community responses of established grassland bacteria to water stress.
- Useful accompanying resources:
  - Sourhope Field Data Handbook (2003).
  - Understanding biological diversity in soil (UK Soil Biodiversity Programme) sources.
- Note: These data may be used for reanalysis of bacterial abundance under moisture perturbations and for comparative studies with other soil microbial datasets.