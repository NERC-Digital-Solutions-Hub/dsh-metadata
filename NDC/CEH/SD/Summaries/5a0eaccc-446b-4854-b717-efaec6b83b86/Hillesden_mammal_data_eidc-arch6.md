# Live-trapping surveys of small mammals on arable field margins on the Hillesden estate in Buckinghamshire (England) during 2005-2011

## Overview
- Longitudinal live-trapping study of small mammals on grassy field margins across three farming-management regimes (Cross Compliance CC, Entry Level Scheme ELS, Entry Level Scheme Extra ELSX) on the Hillesden estate, Buckinghamshire, 2005–2011.
- Part of a wider experiment assessing environmental stewardship options and their effects on biodiversity, with habitat-management contrasts designed to create varying semi-natural habitats.
- Data underpin published analyses on mammal abundance/diversity and habitat effects; includes detailed capture and mark-recapture records suitable for integration with GIS and other datasets.

## Study design and treatments
- Location and setup:
  - 1000 ha farming estate with lowland arable crops (wheat, oil-seed rape, beans) bordered by ditches and hedgerows.
  - Five replicate blocks; each block contains CC, ELS, and ELSX treatment areas/margins.
- Treatments:
  - CC (Cross Compliance): control; 2 m wide field margins from hedgerow centers or 1 m from ditch tops; hedgerows cut annually.
  - ELS: ~1% of cultivated land converted to 6-m margins with grass mix; occasional field patches for food resources; hedgerows cut biennially.
  - ELSX: larger area and greater habitat diversity; ~5% converted to 6-m margins with grasses/wildflowers; multiple field patches sown; hedgerows cut biennially.
- Margin management:
  - CC margins mowed (flailed) annually to limit shrub growth.
  - ELS/ELSX margins mown in the first year after installation, then left to develop grassy habitat.
- Sampling framework:
  - Autumn surveys in 2005, 2006, 2008, 2010; spring surveys in subsequent May.
  - Two 100-m trap lines per replicate; each line with 11 Longworth traps (total 22 traps per treatment replicate).
  - Traps pre-baited for four days, then set for three nights; monitoring occurred morning and afternoon across five trapping sessions per season.
- Trapping and marking:
  - Species, body mass, sex, and breeding condition recorded on first autumn capture.
  - PIT tagging (12 mm) for wood mice, bank voles, and field voles; fur clipping for other captures (then moulted before following season).
  - Trapping not typically limiting (high trap occupancy observed, ~70% of traps active on only a minority of sessions).

## Data collected and dataset structure
- Dataset size and scope:
  - 3172 trapping records, representing at least 1881 individual animals.
  - Records include captures, recaptures, and occasional non-capture trap activations.
- Core data fields (representative list):
  - Year, Season (Spring or Autumn), Date, Trap_Check_Time (Morning/Afternoon)
  - Farming_Regime (ELs or CC), Habitat (margin type; 6-m ELS/ELSX vs 1-2 m CC)
  - Sampling_Block (1–5), Location (field name), x_coordinate, y_coordinate (start of 100 m trap line)
  - Trap_Number (1–11 per line)
  - Fur_Clip_or_PIT (mark type), PIT_Tag_Code (unique ID for PIT-tagged animals)
  - Capture_Type (new vs recapture; trap activation without capture)
  - Species_English, Species_Scientific
  - Sex, Body_Condition, Weight_g (0.5 g precision)
  - Notes (additional relevant information)
- Data quality and cleaning:
  - Records were checked and cleaned; missing values labeled as No_data.
  - Appendix-related observations document data interference issues (see below).

## Data quality, validation, and caveats
- Quality control:
  - Systematic cleaning to remove errors; standardized tagging and recording procedures.
- Potential biases and caveats:
  - Trap interference by corvids (crows/magpies) observed, particularly from 2008 onward, affecting a subset of transects and visits.
  - Interference included disturbance, disassembly or removal of bedding, and bait consumption without capture.
  - Evidence suggests corvids were primarily attracted to bait and may have disrupted monitoring efforts; some disturbances observed during middle of the day.
  - In 2011, direct observations linked carrion crows and magpies to trap disturbance, with multiple individuals likely contributing to interference.
  - Mitigation attempts (pinning traps, partly burying, or covering with litter) had limited success.
- Implications:
  - Data on capture rates and abundance in affected transects/periods may be biased; analyses should account for potential trap-disturbance bias and consider sensitivity analyses or exclusion of heavily affected transects/timeframes if necessary.
- Related outputs:
  - The full analysis of habitat-management effects on small mammal populations is reported in Broughton et al. (2014).

## Data usage and potential products
- Data integration and analysis opportunities:
  - Time-series analyses of capture rates by treatment, margin type, or block.
  - Species-specific abundance, diversity metrics, and recapture rates across management regimes.
  - Spatial analyses using coordinates to map distribution relative to hedgerows and margins.
  - Habitat association analyses comparing CC, ELS, and ELSX treatments.
  - Data fusion with hedgerow metrics and GIS-derived habitat features for broader landscape-scale insights.
- Data products for end users:
  - Dashboards and pivot-table style summaries for self-service exploration (by treatment, year, season, or species).
  - Recapture datasets and tag-tracking outputs to examine movement and habitat use.
  - Documentation of data collection methods and quality notes to support transparent reuse.
- Considerations for re-use:
  - Acknowledge potential trap-disturbance bias in corvid-rich transects and incorporate correction or exclusion where appropriate.
  - Use the unique PIT tag codes to longitudinally track individuals across seasons when applicable.

## Appendices and notes
- Appendix: Corvids exploiting Longworth mammal traps
  - Describes observations of corvid interference (Carrion Crows, Magpies) with Longworth traps on the Hillesden estate.
  - Details the pattern and timing of disturbances (not limited to early morning; some disturbances mid-day).
  - Discusses attempts to limit interference and the likelihood that corvids learned to associate traps with bait, potentially affecting monitoring data.
- References (selected):
  - Gurnell & Flowerdew (2006) Practical Guide for live trapping small mammals.
  - Broughton et al. (2014) Agri-environment scheme effects on biodiversity at the farm scale.
  - Heard et al. (2012) Quantifying ELS effects on biodiversity (unpublished report).
  - Hinsley et al. (2010) Hillesden experiment in Ibis.