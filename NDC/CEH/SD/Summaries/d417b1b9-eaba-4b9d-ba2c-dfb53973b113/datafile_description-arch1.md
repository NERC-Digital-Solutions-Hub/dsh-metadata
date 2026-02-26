# Aquatic carbon isotope composition in natural and restoration pools in blanket peatlands in Scotland and Northern Ireland, 2014-2015

## Overview
- Data repository file: Pools14Cdata.csv, containing all radiocarbon (14C) and stable carbon isotope (δ13C) data, plus site details and uncertainties.
- Study scope: natural and restoration peatland pools across northern/southwestern Scotland and Northern Ireland, focusing on dissolved and ebullition carbon forms, with restoration pools created by drain blocking.

## Study sites and sampling design
- Regions and locations:
  - Cross Lochs, Loch Lier, Munsary in the Flow Country (northern Scotland)
  - Silver Flowe in Galloway (southwest Scotland)
  - Slieveanorra and Garron Plateau in County Antrim, Northern Ireland
- Pool types:
  - Natural pools sampled at all locations
  - Restoration pools (drain-blocked) sampled at Cross Lochs and Loch Lier
- Restoration history:
  - Ditch construction in the 1970s (dates not precisely known)
  - Rewetting/restoration via water-table rise: Loch Lier in 1998; Cross Lochs in 2002
- Sampling campaigns:
  - May 2014, November 2014, September 2015 (primary campaigns)
  - Additional pools at Cross Lochs surveyed in a single campaign
  - Loch Lier sampled in November 2014 and September 2015
- Sample identifiers and pool coverage detailed in the data file

## Field sampling methods and sample types
- Water samples:
  - Focus on dissolved organic carbon (DOC) and dissolved CO2
  - Collection in 1 L glass bottles, pre-furnaced, stored at 4 °C
  - Filtration using pre-ashed GF/F filters (0.7 μm)
  - POC samples collected by combusting filters where material permitted
- Ebullition (bubble) sampling:
  - Bubble traps deployed on natural and restoration pools at Cross Lochs
  - Traps: inverted glass funnels with float, deployed 21 May 2014, checked until 5 November 2014
  - Gas samples collected in N2-flushed bags; CO2 separated from CH4 in the lab
- Sediment sampling:
  - Top ~20 cm of pool sediment collected with a corer; stored at 4 °C

## Laboratory analysis and data generation
- Processing location: Natural Environment Research Council Radiocarbon Facility, East Kilbride
- Processing steps:
  - DOC: rotary evaporated to solids
  - DOC solids and POC filters: acid fumigated to remove inorganic C, then combusted to CO2
  - Dissolved CO2: recovered from headspace via degassing and molecular sieve cartridges
  - Ebullition CH4: filtered to remove CO2, CH4 oxidised to CO2
  - Sediments: cold acid wash, homogenised, freeze-dried, combusted to CO2
  - All CO2 for 14C graphitised via Fe-Zn reduction
  - δ13C analysis: aliquots (<2 mL CO2) analysed by dual-inlet IRMS
- Radiocarbon dating:
  - 14C content expressed as fraction modern carbon (F14C), normalised to δ13C = -25 ‰
  - Ages reported as conventional radiocarbon ages (yBP) when F14C < 1
  - Standards and QA:
    - 14C-dead standards for background corrections (Donahue et al. 1990)
    - TIRI barley mash and 96H humin as radiocarbon reference standards
- Laboratories and facilities:
  - 14C measurements: NERC AMS facility (East Kilbride)
  - Additional measurements (when needed): Keck Carbon Cycle AMS (UC Irvine)
- Data quality and reporting:
  - Uncertainties provided as 1σ
  - δ13C reported relative to VPDB
  - Sample metadata and measurement codes included in the data file

## Data file structure and key variables
- File: Pools14Cdata.csv
- Core columns:
  - Publication code, Description: unique radiocarbon analysis identifier
  - Material ID, Description: sample identifier
  - Site ID, Description: site identifier
  - Location, Description: peatland complex of collection
  - Pool type, Description: Natural or Restoration
  - Sampling date, Description: date of collection
  - Latitude, Longitude: coordinates
  - Carbon form, Description: CH4, CH4-ebullition, CO2, CO2-ebullition, DOC, POC, sediment
  - delta13C (‰ ± 0.1): stable carbon isotopic composition
  - F14C, Description: radiocarbon content with ±1σ
  - Radiocarbon age (yBP), yBP ± 1σ: conventional radiocarbon ages where applicable
  - Notes, Description: additional relevant information
- Purpose:
  - Enables analysis of relationships between pool type, carbon form, isotopic signatures, and radiocarbon ages
  - Supports age dating, carbon sourcing, and restoration impact assessments

## References and context
- Key methodological and contextual references for sampling, processing, and interpretation of radiocarbon and δ13C data include:
  - Methods for combustion and isotope analysis (e.g., Boutton et al. 1983)
  - Radiocarbon facility protocols and advancements (Garnett et al. 2019; Garnett et al. 2016)
  - Standards and QA procedures (Donahue et al. 1990; Stuiver & Polach 1977)
  - Previous related peatland carbon studies and regional variability (Turner et al. 2016; Holden et al. 2018; Chapman et al. 2022)
  - Supporting methodological work on dissolved methane and carbon dioxide analyses (Garnett et al. 2011; Gulliver et al. 2010)

## Key considerations for analysts
- Data at specific scales: site- and pool-level data enable local-scale analyses of restoration effects and carbon sources.
- Data accessibility: single comprehensive CSV with extensive metadata; check notes for sample-specific caveats and campaign details.
- Cross-dataset integration: ensure compatibility of units and standards when combining with other isotopic or age data.
- Quality assurance: reliance on multiple standards and laboratories; pay attention to reported uncertainties and normalization conventions.