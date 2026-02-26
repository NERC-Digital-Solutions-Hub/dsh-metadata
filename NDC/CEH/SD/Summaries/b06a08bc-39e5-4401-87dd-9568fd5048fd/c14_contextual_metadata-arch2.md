# Radiocarbon dating of charcoal pieces collected from soil in the Amazon Basin

## Overview
- Radiocarbon dating of macrocharcoal pieces (≥1 mm) collected from soils in terra-firme, non-seasonally flooded sites across Guyana, Peru, and Brazil.
- Part of the RAINFOR network; total of 60 dated macrocharcoal samples.
- Field campaigns conducted in 2015, 2017, 2018, and 2019.
- Funded by Natural Environment Research Council (NERC) grant NE/N011570/1 and CAPES (Brazil) PVE177-2012.
- Dataset has been used in and referenced by published studies on Amazon fire history and charcoal chronology.

## Dataset and Scope
- Data file: C14.csv (comma-separated values).
- Samples: 60 macrocharcoal pieces collected from soil profiles near 1 ha permanent plots; soils sampled in 3 replicate pits per site, spaced ~100 m apart.
- Sites: Guyana, Peru, and Brazil, within the Amazon forest.
- Field collection details: charcoal extracted from soil in 1 cm depth increments up to 70 cm; 4 pieces per pit selected for dating, prioritizing the surface sample from each pit and deeper increments to balance depth representation. Northern Peru site includes an additional date at 46 cm depth (a fourth pit) to harmonize sample numbers.

## Sampling Methods
- Charcoal collection: from soil profiles adjacent to each plot, separating charcoal from soil, air-drying, and storage in plastic containers.
- Pit strategy: three replicate pits per site, 100 m apart; 1 cm depth increments up to 70 cm.
- Selection criteria for dating: (i) sample nearest the surface of each pit; (ii) select the next three samples from progressively deeper depth intervals.

## Data Analysis and Dating Process
- Sample preparation: surface charcoal scraped; pre-treatment with standard acid-base-acid sequence (0.5 M HCl at 80°C for 2 h, 0.5 M KOH at 80°C for 2 h, then 0.5 M HCl at 80°C for 2 h).
- Combustion and purification: samples combusted to CO2 in sealed quartz tubes, cryogenic purification, and conversion to graphite via Fe/Zn reduction (Slota et al., 1987).
- Dating: Accelerator Mass Spectrometry (AMS) radiocarbon dating conducted at the NERC Radiocarbon Facility (UK) and the Physics Institute of Universidade Federal Fluminense (Brazil).
- Result unit: radiocarbon age in years before present (BP).
- Quality control: failed runs or non-convergent runs discarded.

## Data Structure and Quality
- File structure: C14.csv with columns:
  - Location, Plot, Latitude, Longitude
  - Soil_Pit, Depth
  - C-14_age_yr_BP, C-14_age_Uncertainty
  - Lab_ID
- Missing data indicated as 'NA' (not recorded or no longer accessible).
- All data values are age determinations in years BP with associated uncertainties.

## Data Use and Relevance for Environmental Monitoring
- Provides a historical record of fire activity and charcoal deposition in Amazonia, contributing to understanding carbon dynamics and fire regimes over time.
- Supports broader monitoring of environmental health and forest carbon dynamics by supplying standardized radiocarbon dating data aligned with field plots in the RAINFOR network.
- Data and associated publications underpin assessments of past fires and their impact on biodiversity and soil carbon storage.

## Funding, Collaborations, and References
- Funding: NERC grant NE/N011570/1; CAPES (PVE177-2012).
- Related publications utilizing the dataset:
  - Feldpausch et al. (2022). Forest Fire History in Amazonia Inferred From Intensive Soil Charcoal Sampling and Radiocarbon Dating. Frontiers in Forests and Global Change, 5.
  - Goulart et al. (2017). Charcoal chronology of the Amazon forest: A record of biodiversity preserved by ancient fires. Quaternary Geochronology, 41, 180-186.
- Methodological reference: Slota et al. (1987). Preparation of small samples for 14C accelerator targets by catalytic reduction of CO. Radiocarbon, 29, 303-306.