# Aquatic carbon isotope composition in natural and restoration pools in blanket peatlands in Scotland and Northern Ireland, 2014-2015

- This document describes the sample collection and analysis required to generate the isotopic data provided in a data repository containing a single file: Pools14Cdata.csv.

## Study context and sites

- Geographic scope: three regions of the UK — northern and southwest Scotland and Northern Ireland.
- Key sites:
  - Cross Lochs, Loch Lier, Munsary (Flow Country, northern Scotland)
  - Silver Flowe ( blanket peatland in Galloway, southwest Scotland)
  - Slieveanorra (upland raised bog, County Antrim, Northern Ireland)
  - Garron Plateau (near-natural upland blanket bog, County Antrim)
- Pool types:
  - Natural pools sampled at all locations
  - Restoration pools (drain blocking to rewet) sampled at Cross Lochs and Loch Lier
- Landscape context: ditching to drain peatlands in the 1970s; restoration via rewetting occurred around 1998 (Loch Lier) and 2002 (Cross Lochs).

## Sampling campaigns

- Cross Lochs: three natural and three restoration pools sampled in May 2014, November 2014, and September 2015 (P01, P04, P06, P07, P09, P10); additional pools sampled once (P03, P05, P11, P12).
- Loch Lier: two natural and two restoration pools sampled in November 2014; in September 2015, all locations except Loch Lier were sampled.
- Sampling cadence aimed for consistency across campaigns.

## Sample types and collection

- Water sampling focus: dissolved organic carbon (DOC), dissolved CO2; additional measurements where possible include particulate organic carbon (POC), ebullition CH4, ebullition CO2, dissolved CH4, and pool sediment.
- Collection and handling:
  - Water collected in 1 L glass bottles pre-fired at 450°C
  - Samples kept cool (4°C) and transported promptly; storage up to three days
  - Transport to NERC Radiocarbon Facility (East Kilbride)
  - Filtration with pre-ashed GF/F filters (0.7 μm); POC sampled by combusting filters when material allowed
  - CO2 samples obtained via headspace method (3 L water to 1 L headspace) and later processed on-site with molecular sieves
  - Ebullition traps deployed in six natural pools and five restoration pools to collect gas bubbles; samples combined per pool when multiple traps used
  - Sediment grabs from selected pools (top ~20 cm), refrigerated for analysis

## Sample analysis and data generation

- Location of analysis: United Kingdom National Environment Research Council (NERC) Radiocarbon Facility, East Kilbride
- Processing steps:
  - DOC solids rotary evaporated; inorganic C removed from DOC solids and POC filters by acid fumigation; combusted to CO2
  - Dissolved CO2 recovered from molecular sieves by heating; ebullition CH4 oxidized to CO2
  - Sediment samples acid-washed, homogenised, freeze-dried, combusted to CO2
  - All CO2 converted to graphite via Fe-Zn reduction for 14C analysis
  - δ13C analysis performed on samples with sufficient CO2 using dual-inlet IRMS (Thermo Fisher Delta V), reported relative to VPDB
  - 14C content measured by Accelerator Mass Spectrometry (AMS); presented as fraction modern carbon (F14C)
  - Traditional radiocarbon ages (yBP) provided for F14C < 1
- Standards and QA:
  - Radiocarbon-dead standards (bituminous and anthracite coal) to quantify processing background and background-correct results
  - Reference standards include barley mash from TIRI intercomparison and an internal 96H humin standard for accuracy and precision checks
- Isotopic details:
  - δ13C reported in ‰ VPDB with ±0.1 ‰ uncertainty
  - F14C and radiocarbon ages include 1σ uncertainties
  - Normalization and age calculations follow established radiocarbon conventions

## Data file structure and content

- Data file: Pools14Cdata.csv (single CSV file) containing all radiocarbon (14C) and stable carbon isotope (δ13C) data, site details, and uncertainties
- Key fields:
  - Publication code and Description (unique radiocarbon analysis identifier)
  - Material ID and Description (sample identifiers used in submission)
  - Site ID and Location (peatland complex)
  - Pool type (Natural or Restoration)
  - Sampling date (collection date)
  - Latitude and Longitude
  - Carbon form (e.g., dissolved CH4, CH4-ebullition, dissolved CO2, CO2-ebullition, DOC, POC, sediment)
  - delta13C (‰, ±0.1)
  - F14C (radiocarbon content, with 1σ uncertainty)
  - Radiocarbon age (yBP) and yBP ±1σ
  - Notes (additional context)
- Purpose: centralised, standardized dataset with associated uncertainties and metadata to support interpretation of aquatic carbon cycling and restoration impacts in blanket peatlands

## Data governance, openness and applicability

- Metadata and data provenance are embedded through explicit field definitions and references
- Data generated with standardized QA, QA procedures, and use of established reference standards
- Data accessibility supports reuse in monitoring and assessment of environmental health and restoration outcomes in peatland ecosystems
- The document provides extensive methodological references to enable reproducibility and comparability with other studies

## References

- Comprehensive references accompanying sampling and analytical methods, including radiocarbon standards, headspace sampling approaches, and prior peatland carbon studies (e.g., Gulliver et al. 2010; Garnett et al. 2019; Turner et al. 2016; Holden et al. 2018; Chapman et al. 2022; and others)