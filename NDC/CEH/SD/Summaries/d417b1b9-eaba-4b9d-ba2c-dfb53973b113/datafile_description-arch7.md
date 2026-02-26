# Aquatic carbon isotope composition in natural and restoration pools in blanket peatlands in Scotland and Northern Ireland, 2014-2015

## Overview
- Describes the sample collection and analysis used to generate the isotopic data in the data repository, which consists of a single CSV file: Pools14Cdata.csv.
- Focuses on aquatic carbon isotopes (14C and δ13C) from peatland pools across three UK regions, including both natural pools and restoration (drain-blocked) pools.

## Study sites and sampling design
- Regions: northern and southwest Scotland and Northern Ireland.
- Sites include Cross Lochs, Loch Lier, Munsary (Flow Country, northern Scotland), Silver Flowe (Galloway, southwest Scotland), Slieveanorra (County Antrim, Northern Ireland), Garron Plateau (County Antrim, Northern Ireland).
- Pool types: natural pools at all sites; restoration pools sampled at Cross Lochs and Loch Lier.
- Restoration context: drainage occurred in the 1970s; rewetting/restoration by water-table raising implemented in 1998 (Loch Lier) and 2002 (Cross Lochs), prior to sampling campaigns.

## Sampling campaigns and sample types
- Campaigns at Cross Lochs: May 2014, November 2014, September 2015 (six pools sampled across campaigns; some pools sampled once).
- Loch Lier: November 2014 (two natural and two restoration pools).
- Additional sampling: all locations (except Loch Lier) in September 2015.
- Sample types collected where possible:
  - Dissolved organic carbon (DOC)
  - Dissolved inorganic carbon forms: dissolved CO2
  - Particulate organic carbon (POC)
  - Ebullition samples: CH4 and CO2 (from bubble traps)
  - Sediment samples from the pool floor
  - Dissolved CH4 and, where present, dissolved CO2 from headspace methods

## Sample collection and handling (field)
- Water samples stored in 1 L glass bottles, pre-fired, cooled, and refrigerated; transported to facility promptly.
- Filtration: field-filtered using pre-ashed GF/F filters (0.7 μm).
- POC: where material allowed, collected by combusting the filters.
- Ebullition sampling: bubble traps deployed on surface; samples collected via gas-tight methods and separated into CH4 and CO2 in the lab.

## Sample processing and isotopic analysis (lab)
- Location: Natural Environment Research Council Radiocarbon Facility, East Kilbride.
- DOC: rotary evaporated to solids; inorganic C removed; combusted to CO2.
- POC: combusted post-filtration; for δ13C analysis, aliquots taken from >1 mL CO2 when possible.
- Ebullition CH4/CO2: CH4 oxidized to CO2; CO2 separated in the lab.
- Sediments: top ~20 cm; acid-washed, homogenized, freeze-dried, combusted to CO2.
- Isotopic measurements:
  - δ13C: measured on a dual-inlet IRMS (VPDB standard) for samples with sufficient CO2.
  - 14C: measured by Accelerator Mass Spectrometry (AMS); results normalized to δ13C = -25 ‰ VPDB; reported as F14C (fraction modern) and, when applicable, conventional radiocarbon ages (yBP).
- Standards and QA:
  - Radiocarbon-dead standards and known-age standards processed alongside samples to quantify background and verify accuracy.
  - Internal standards used include TIRI barley mash and a 96H humin standard to verify accuracy and precision.

## Data file structure and contents
- Data file: Pools14Cdata.csv
- Contents:
  - Radiocarbon (14C) and stable carbon isotope (δ13C) data
  - Site details and associated uncertainties
- Key columns and descriptions:
  - Publication code, Description: unique code for each radiocarbon analysis
  - Material ID code, Description: unique sample identifier
  - Site ID, Description: site identifier
  - Location, Description: peatland complex of sample origin
  - Pool type, Description: Natural or Restoration
  - Sampling date, Description: date of sample collection
  - Latitude, Description: geographic latitude
  - Longitude, Description: geographic longitude
  - Carbon form, Description: sampled carbon form (e.g., CH4, CH4-ebullition, CO2, CO2-ebullition, DOC, POC, sediment)
  - delta13C (‰ ± 0.1), Description: δ13C value with ±0.1 ‰ uncertainty
  - F14C, Description: radiocarbon content as fraction modern carbon with ±1σ
  - Radiocarbon age (yBP), Description: traditional radiocarbon age
  - yBP ± 1 sd, Description: uncertainty for the radiocarbon age
  - Notes, Description: additional relevant information

## Uncertainty and reporting
- δ13C uncertainty: ±0.1 ‰
- F14C uncertainty: ±1 standard deviation
- Radiocarbon ages: reported with associated uncertainties (yBP ± 1 sd)
- Standardization and background corrections align with established radiocarbon protocols and references

## Data relevance for GIS specialists
- Provided coordinates (latitude and longitude) enable precise mapping of pool locations.
- Includes pool type (natural vs restoration) and location identifiers to support thematic mapping and comparative analyses.
- Rich metadata (sampling dates, carbon forms, and isotopic values with uncertainties) supports spatial-temporal analyses of carbon cycling in blanket peatlands.
- Data provenance and lab methods are documented to assist data quality assessment and reproducibility in GIS-enabled analyses.

## References and context
- The dataset builds on methodology and interpretation frameworks cited in multiple studies related to peatland hydrology, radiocarbon analysis, and stable carbon isotopes, including processes for sample collection, processing, and QA.