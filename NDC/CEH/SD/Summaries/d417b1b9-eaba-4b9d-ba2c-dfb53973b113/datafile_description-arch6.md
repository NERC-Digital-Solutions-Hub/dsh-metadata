# Aquatic carbon isotope composition in natural and restoration pools in blanket peatlands in Scotland and Northern Ireland, 2014-2015

- Purpose: Describes the sample collection and analysis needed to generate the isotopic data in the repository file Pools14Cdata.csv, including radiocarbon (14C) and stable carbon (δ13C) data, site details, and uncertainties.
- Scope: Three main geographic regions in the UK (northern and southwest Scotland, Northern Ireland) with both natural pools and restoration pools (where drain blocking/restoration occurred).

## Sites and pool types

- Locations:
  - Cross Lochs, Loch Lier, Munsary (Flow Country, northern Scotland)
  - Silver Flowe ( blanket peatland, southwest Scotland)
  - Slieveanorra (upland raised bog, Northern Ireland)
  - Garron Plateau (near-natural upland blanket bog, Northern Ireland)
- Pool types:
  - Natural pools at all locations
  - Restoration pools at Cross Lochs and Loch Lier (restored by rewetting; ditching occurred earlier in the 1970s)
- Ditching/restoration context: Drainage in the 1970s; restoration via water-level rewetting in 1998 (Loch Lier) and 2002 (Cross Lochs).

## Sampling campaigns and design

- Campaigns:
  - May 2014, November 2014, September 2015 (Cross Lochs; P01, P04, P06, P07, P09, P10)
  - Additional pools at Cross Lochs (P03, P05, P11, P12) sampled once
  - November 2014: Loch Lier natural and restoration pools
  - September 2015: all locations except Loch Lier
- Sample types targeted:
  - Water for DOC and dissolved CO2
  - Particulate Organic Carbon (POC)
  - Ebullition (bubbles) CH4 and CO2
  - Dissolved CH4
  - Pool sediments

## Field sampling and sample handling

- Water collection: 1 L glass bottles, pre-ashed at 450°C, cooled promptly, stored at 4°C.
- Transport: Kept cool, delivered to NERC Radiocarbon Facility (East Kilbride) within ~1 day.
- Filtration and processing: Water filtered within ~3 days using pre-ashed GF/F filters (0.7 μm); POC from filters when material available.
- Ebullition sampling: Bubble traps deployed on pool surface; bubbles collected into N2-flushed bags; CO2 separated from CH4 in-lab using molecular sieve cartridges.
- Sediments: Top ~20 cm collected with corer, refrigerated at 4°C prior to analyses.

## Sample processing and isotopic analysis

- Processing at NERC Radiocarbon Facility (East Kilbride):
  - DOC solids: rotary evaporated to solids
  - POC filters: acid fumigated to remove inorganic C, then combusted to CO2
  - Dissolved CO2: recovered from molecular sieves by heating
  - Ebullition CH4/CO2: CH4 oxidized to CO2 after removing CO2
  - Sediments: acid-washed, homogenised, freeze-dried, combusted to CO2
- Isotopic measurements:
  - δ13C: measured when ≥1 mL CO2 available; dual-inlet IRMS (VPDB standard)
  - 14C: determined by Accelerator Mass Spectrometry (AMS)
  - Normalization: 14C values normalized to δ13C = -25‰ VPDB; reported as F14C
  - Age conversion: conventional radiocarbon ages (yBP) for F14C < 1
- Alternate lab access: If sample size < 0.5 mL CO2, analyzed at UC Irvine (Keck AMS)

## Data file and structure

- Data file: Pools14Cdata.csv
- Content:
  - Radiocarbon (14C) and stable carbon (δ13C) data
  - Site details, pool type, sampling date, location (latitude/longitude)
  - Carbon form (e.g., CH4, CH4-ebullition, CO2, CO2-ebullition, DOC, POC, sediment)
  - δ13C with ±0.1 ‰ uncertainty
  - F14C with 1σ uncertainty
  - Radiocarbon age (yBP) with 1σ uncertainty
  - Notes: Additional relevant information
  - Metadata fields: Publication code, Material ID, Site ID, Location description

## Data quality, standards, and QA

- Standards and background corrections:
  - 14C-dead standards (bituminous and anthracite coal) for background correction (Donahue et al. 1990)
  - Radiocarbon reference standards: barley mash from TIRI intercomparison and internal 96H humin standard
- Method references and provenance:
  - Methodological supports and instrument advances cited (Garnett et al. 2011, 2016, 2019; Gulliksen & Scott 1995; Xu et al. 2004; Donahue et al. 1990)
- Data provenance:
  - Data generated at the NERC Radiocarbon Facility (East Kilbride) with some samples analyzed at UC Irvine
  - Links to related regional studies (Turner et al. 2016; Holden et al. 2018; Chapman et al. 2022)

## Usage and potential data products

- Data can be used to:
  - Compare natural vs. restoration pool isotopic signatures
  - Examine carbon cycling processes in blanket peatland pools
  - Integrate with other peatland hydrology and carbon concentration studies
  - Support self-contained data exploration dashboards or reports that require site- and pool-level isotopic data with uncertainty estimates
- Reusability and sourcing:
  - All measurements and metadata are compiled in Pools14Cdata.csv with explicit sample identifiers, site details, carbon forms, and uncertainties
  - Proper citation to underlying methodological references and associated regional studies recommended when using the data