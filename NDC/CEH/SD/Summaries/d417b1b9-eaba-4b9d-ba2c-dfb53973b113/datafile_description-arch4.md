# Aquatic carbon isotope composition in natural and restoration pools in blanket peatlands in Scotland and Northern Ireland, 2014-2015

- This document outlines the sampling and analytical workflow used to generate the isotopic data in the data repository, which contains a single file: Pools14Cdata.csv.
- It covers three UK regions (northern and southwest Scotland, Northern Ireland) and both natural and restoration pools, detailing site context, collection campaigns, sample types, analytical methods, and data structure.

## Overview of sites and pool types

- Regions and sites
  - Flow Country in northern Scotland: Cross Lochs, Loch Lier, Munsary
  - Blanket peatland in southwest Scotland: Silver Flowe
  - Northern Ireland upland bogs: Slieveanorra and Garron Plateau
- Pool types
  - Natural pools sampled at all sites
  - Restoration pools (drain-blocked and rewetted) sampled at Cross Lochs and Loch Lier
- Historical context
  - Peatland drainage occurred in the 1970s; restoration via rewetting occurred around 1998 (Loch Lier) and 2002 (Cross Lochs)

## Sample collection (2014–2015 campaigns)

- Sampling campaigns
  - Cross Lochs: natural and restoration pools; multiple campaigns in May 2014, November 2014, September 2015; some pools sampled in a single campaign
  - Loch Lier: natural and restoration pools; campaigns in November 2014 and September 2015
- Pool sampling details
  - Natural pools and restoration pools were sampled; ebullition (bubble) samples collected via bubble traps in several pools
  - Additional sample types where possible: dissolved organic carbon (DOC), dissolved CO2, dissolved CH4, ebullition CH4/CO2, particulate organic carbon (POC), pool sediment
- Field sample handling
  - Water collected in 1 L furnaced glass bottles; stored cold and refrigerated; filtered within ~3 days using pre-ashed GF/F filters
  - POC collected from filters; CO2 sampled by headspace equilibration and molecular sieve traps; CH4 separated in the lab
  - Bubble traps deployed for natural and restoration pools; samples stored in N2-flushed bags for CO2/CH4 analysis
  - Sediment core samples collected from top ~20 cm and stored at 4 °C prior to analysis

## Sample processing and data generation (at NERC Radiocarbon Facility, East Kilbride)

- Processing steps
  - DOC samples rotary evaporated to solids; DOC solids and POC filters acid-fumigated to remove inorganic carbon; combusted to CO2
  - Dissolved CO2 recovered from molecular sieve cartridges by heating
  - Ebullition CH4 oxidised to CO2; CO2 separated from CH4 on lab cartridges
  - Sediment samples acid-washed, freeze-dried, homogenised, and combusted to CO2
  - All CO2 produced graphitised for radiocarbon analysis
- Isotope measurements
  - δ13C measured for samples with sufficient CO2 using dual-inlet IRMS (VPDB standard); reported with ±0.1 ‰ uncertainty
  - Radiocarbon (14C) measured by Accelerator Mass Spectrometry (AMS)
  - δ13C-normalisation: 14C results normalised to a δ13C of -25 ‰
  - F14C reported; conventional radiocarbon ages (yBP) calculated for F14C < 1
- QA and QA standards
  - Processed standards alongside samples for quality assurance
  - Radiocarbon-dead standards (bituminous and anthracite coal) used for background correction
  - Reference standards (e.g., barley mash from TIRI and 96H humin) used to verify accuracy and precision
- Data reporting conventions
  - 14C content expressed as fraction modern carbon (F14C)
  - Present defined as 1950 CE for age calculations
  - Uncertainties and notes captured in data

## Data file structure

- Data file: Pools14Cdata.csv
- Key fields
  - Publication/Description codes and material/sample identifiers
  - Site identifiers and location details (latitude, longitude)
  - Pool type (Natural or Restoration)
  - Sampling date
  - Carbon form (e.g., CH4, CH4-ebullition, CO2, CO2-ebullition, DOC, POC, sediment)
  - delta13C (‰, ±0.1)
  - F14C and 1σ uncertainty
  - Radiocarbon age (yBP) and yBP ± 1σ
  - Notes (any additional relevant information)

## Data quality, standards, and provenance

- Provenance
  - Field collection and laboratory analysis are documented; multiple campaigns and diverse sample types captured
  - Analyses conducted at a dedicated radiocarbon facility with standardized procedures
- Quality and comparability
  - Use of background (dead) standards and known-age references to ensure accuracy
  - Detailed metadata and standardized formatting to enable reproducibility and cross-study comparisons
- Reuse and context
  - Data suitable for studies on peatland carbon dynamics, restoration effects, and aquatic carbon cycling
  - Comprehensive metadata supports interpretation of carbon forms, isotopic composition, and age estimates across natural and restored pools

## References and methodological context

- Core methodological sources covering sample processing, CO2/CH4 handling, radiocarbon measurement, and standardization
- Includes foundational work on radiocarbon techniques, headspace sampling, molecular sieves, and delta13C normalization