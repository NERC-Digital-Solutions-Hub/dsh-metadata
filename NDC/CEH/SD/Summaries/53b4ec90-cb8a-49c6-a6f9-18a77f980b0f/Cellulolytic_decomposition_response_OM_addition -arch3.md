# Cellulolytic decomposition of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates how leaf litter (oak, birch, alder) input affects cellulolytic decomposition in Welsh upland streams.
- Employs a BACI (before-after-control-impact) design to compare upstream reference zones with downstream experimental zones.
- Uses a measurable proxy for decomposition: tensile strength (breaking strain) of calico (cotton) strips exposed in stream reaches.

## Experimental design and manipulations
- Each stream section is split into:
  - Upstream reference (control) zone
  - Downstream experimental zone
  - 20–50 m separation to ensure independence
- Time periods:
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation
  - After period (T2): 57–62 days (early Jan to Mar 2013); leaf litter manipulation in the experimental zone
- Leaf litter addition:
  - One tonne bags of deciduous leaves (oak, birch, alder) added to the experimental zone proportional to area
  - Vegetable nets maintained a minimum wet weight of 1.7 kg m^-2 in the experimental zone
  - Additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after two storm events
- Experimental units:
  - Six calico strips placed randomly in each reach before and after manipulation
  - Strips recovered, frozen at -20°C, then analyzed in the lab

## Measurement methods and laboratory analysis
- Tensile strength testing:
  - Conducted using a Hounsfield machine (25 kN load cell, 40 mm gap)
  - One breaking strain estimate per strip
  - Three untreated control strips used to account for losses during transport and washing
- Collection and processing:
  - Strips collected in the field, then rinsed, dried to constant mass, and tested
- Contextual references:
  - Related literature cited for methodological background (e.g., Jenkins et al. 2013; Hladyz et al. 2011)

## Data and metadata
- Data structure:
  - Flatbed CSV with 10 columns:
    - site_code, region, date, time (Before/After), landuse, reach (Experimental/Control), replicate, exposure (days), breaking_strain (Newtons), %_loss
- Supporting metadata:
  - Site description CSV with fields:
    - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment
- Documentation and links:
  - References and URLs provided; some links referenced through CEH Data Catalogue
  - Note: external links may change over time; data are organized for reproducibility

## Quality, limitations, and data governance
- Quality control:
  - No explicit calibration steps documented
  - No formal quality control procedures described within the dataset
- Data availability and governance considerations:
  - Data and site metadata are organized for sharing, but provenance of some references relies on external catalogues (potential link rot)
  - Clear metadata enhances transparency and potential reuse in monitoring frameworks, though standardization and interoperability considerations should be addressed for policy use

## Relevance for monitoring frameworks and policy evaluation
- Demonstrates a structured approach to linking environmental inputs (organic matter) with a quantifiable ecological response (cellulolytic decay proxy)
- BACI design provides a clear framework for attributing observed changes to the manipulation, aiding policy evaluation of nutrient/organic matter inputs on stream decomposition processes
- Metadata-rich dataset supports traceability and potential integration into monitoring dashboards or reports, while highlighting areas for improvement in data quality assurance and governance (calibration, QC, and metadata completeness) for routine monitoring programs