# Background

## Overview
- Describes the NERC Soil Biodiversity Thematic Programme (established 1999) and its focus on soil biodiversity, ecological processes, and the roles of soil organisms.
- Aimed to understand both soil biota diversity and functional roles in key ecological processes through multiple projects, centred on a field experiment at Sourhope (Scottish Borders).

## Study site and aims
- Location: Sourhope field site at the Macaulay Institute (now James Hutton Institute) farm, Sourhope, Scottish Borders (Grid reference: NT8545019630).
- Primary aims: simultaneous understanding of soil biota diversity and functional roles in ecological processes; investigation across 24 projects covering soil structure, carbon and nitrogen cycles, micro-fauna/flora, meso-fauna, and macro-fauna.

## Sampling design and methods

### Baseline vegetation (1998)
- Timing: baseline survey between 27 July and 7 August 1998.
- Method: 50 x 50 cm point quadrats; 25 points per quadrat.
- Subplot sampling: five randomly selected subplots within each main plot (out of fifteen total per main plot).
- Data captured: presence/absence (with potential abundance) of species at each point; records reflect actual counts of species observations.
- Outputs: baseline vegetation data by sub-plot using a standardized sampling framework.

### Point analysis surveys (2000–2002)
- Timing: annual surveys in July/August for years 2000, 2001, 2002.
- Sampling cell: within each sub-plot S, T, U, V, a separate 0.5 m^2 cell.
- Frame: 100-hole point-quadrat, with a large pin dropped through 25 designated holes per sampling occasion; records species touched by the pin along the vegetation profile.
- Species data: counts of species observed in each sub-plot; bryophyte identification enhanced in 2002 to species level (vs. earlier broader categories).
- Participants/records: survey team noted as S. Buckland, W. Walker, and G. Burt-Smith.

### Bryophyte and data notes
- Bryophyte identification refined in 2002 to species level; earlier years grouped bryophytes more broadly (Rhytidiadelphus squarrosus, other mosses, liverworts).

## Data structure and files

### Baseline vegetation data (1998)
- File: P2109_BOTANICAL_SURVEY_BASELINE_1998.csv
- Key fields:
  - MEAS_LOC_ID: concatenated block, plot, sub-plot codes
  - BLOCK: block number (1-5)
  - MAIN_PLOT: main plot letter (A-F)
  - SUB_PLOT: sub-plot identifier
  - BASE_DATE: date of baseline sampling
  - SPECIES_CODE: vegetation species code
  - SPECIES_NAME: species name (Stace, 1997)
  - ABUNDANCE: total hits of each species at sub-plot level

### Point quadrat data (2000–2002)
- File: P2109_BOTANICAL_SURVEY_2000_2002.csv
- Key fields:
  - YEAR: sampling year
  - SAMPLE_DATE: date of sampling
  - BLOCK: block number (1-5)
  - MAIN_PLOT: main plot letter (A-F)
  - SUB_PLOT: sub-plot identifier
  - TREATMENT_NO: treatment code
  - TREATMENT: treatment description applied to soil
  - SPECIES: species name (Stace, 1997)
  - SPECIES_COUNT: total hits of each species at sub-plot level

## Data quality and limitations

- Quality controls: numeric range checks, formatting conformity, and logical integrity checks implemented.
- Liability disclaimer: NERC provides data without warranty of accuracy; no responsibility for fitness for a particular use; no liability for loss or damage arising from use of the data.

## References and provenance
- Scott, R.; Bell, J.; Kenny, C.; Jeffers, J.; Buckland, S.; Burt-Smith, G. (2003). Sourhope Field Data Handbook 2003 (Supporting Information via EIDC catalogue record).
- Stace, C. (1997). New flora of the British Isles. Cambridge University Press.