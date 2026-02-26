# Aquatic carbon isotope composition in natural and restoration pools in blanket peatlands in Scotland and Northern Ireland, 2014-2015

## Overview
- Describes sample collection and analysis used to generate isotopic data available in the data repository (Pools14Cdata.csv).
- Focuses on natural and restoration pools across three UK regions: northern and southwest Scotland and Northern Ireland.
- Restoration pools were created by drain blocking (Cross Lochs and Loch Lier); ditching occurred in the 1970s with restoration rewetting in 1998 (Loch Lier) and 2002 (Cross Lochs).

## Study sites and sampling design
- Regions and locations:
  - Flow Country in northern Scotland: Cross Lochs, Loch Lier, Munsary.
  - Blanket peatland in southwest Scotland: Silver Flowe.
  - Northern Ireland upland bogs: Slieveanorra (County Antrim) and Garron Plateau (County Antrim).
- Pool types:
  - Natural pools sampled at all locations.
  - Restoration pools sampled at Cross Lochs and Loch Lier.
- Sampling campaigns:
  - May 2014, November 2014, September 2015 (Cross Lochs and Loch Lier and others); some additional pools sampled once.
- Sample types collected (where possible):
  - Water: DOC and dissolved CO2.
  - Particulate organic carbon (POC), ebullition CH4, ebullition CO2, dissolved CH4, pool sediment.
- Site metadata captured (location coordinates, pool type, sampling date).

## Field sampling methods
- Water collection:
  - 1 L glass bottles pre-ashed, stored at 4 °C, transported to the lab within 1 day.
  - Filtration: pre-ashed GF/F filters (0.7 μm) within three days of arrival.
  - POC collected by combusting filtered material when present.
- Gas sampling:
  - CO2 sampled by headspace method (3 L water with 1 L headspace) for 3 minutes; CO2 captured on molecular sieve cartridges in the field.
  - Ebullition samples collected with bubble traps deployed on pool surfaces; traps purged and gas collected in inert gas-flushed bags; CO2 separated from CH4 in the lab.
  - Sediment and other solid samples collected where possible.

## Sample processing and laboratory analysis
- Processing location: Natural Environment Research Council Radiocarbon Facility, East Kilbride.
- Procedures:
  - DOC solids concentrated by rotary evaporation; DOC/POC inorganic carbon removed via acid fumigation; combusted to CO2.
  - Dissolved CO2 recovered from sieves by heating to 425 °C.
  - Ebullition CH4 oxidized to CO2 after filtering CO2; CH4/CO2 separated in lab.
  - Sediment samples: top ~20 cm collected, washed, freeze-dried, combusted to CO2 using sealed quartz tube method.
  - Glassware cleaned by high-temperature combustion.
- Isotope measurements:
  - 14C in CO2 graphitised via Fe-Zn reduction.
  - For samples with >1 mL CO2, a fraction was analysed for δ13C using dual-inlet IRMS (VPDB standard).
  - δ13C values reported as per VPDB; F14C used for radiocarbon content; yBP ages derived when F14C < 1.
- Standards and QA:
  - Radiocarbon-dead standards used to quantify background; radiocarbon reference standards (barley mash from TIRI and 96H humin) used to verify accuracy and precision.
  - Background corrections applied as described in Donahue et al. 1990.

## Data management and file structure
- Data repository file: Pools14Cdata.csv
- Data included:
  - Radiocarbon (14C) and stable carbon isotope (δ13C) data, site details, and uncertainties.
  - Publication code: unique identifier for each radiocarbon analysis.
  - Material ID: sample submission identifier.
  - Site ID and Location: site identifiers and peatland complex.
  - Pool type: Natural or Restoration.
  - Sampling date and coordinates (latitude, longitude).
  - Carbon form: dissolved CH4, ebullition CH4, dissolved CO2, ebullition CO2, DOC, POC, sediment.
  - δ13C (‰ VPDB) with ±0.1 ‰ uncertainty.
  - F14C and 1σ uncertainty; radiocarbon age (yBP) with uncertainty.
  - Notes: additional relevant information.
- Data structure supports traceability from field collection through lab analysis to final dataset.

## Data governance and stewardship considerations
- Coverage and context:
  - Detailed site and pool-type metadata to support discovery and reuse for researchers studying peatland carbon dynamics.
  - Context on restoration history and ditching provides critical interpretation for data users.
- Standards and interoperability:
  - Use of established radiocarbon conventions (F14C, yBP) and δ13C measured against VPDB; alignment with published protocols and QA standards.
  - Multiple labs/facilities referenced for analysis and cross-checking results when necessary.
- Quality assurance:
  - Inclusion of known standards and background corrections to ensure measurement reliability.
  - Documentation of sample sizes, types, and processing steps to facilitate reproducibility.
- Access and reuse:
  - Data presented in a single, well-documented CSV with comprehensive metadata fields, enabling reuse across publications and comparative studies.
- Potential limitations and considerations:
  - Various pool types and carbon forms require careful interpretation due to differences in carbon sources and preservation; contextual notes in the dataset aid interpretation.
  - The restoration vs. natural pool comparisons depend on accurate dating and consistent sampling across campaigns.

## References and methodological grounding
- References covering sampling methods, radiocarbon calibration, QA procedures, and prior related studies (e.g., Gulliver et al., Garnett et al., Donahue et al., Turner et al., Holden et al., etc.) are provided to support data integrity and methodological choices.