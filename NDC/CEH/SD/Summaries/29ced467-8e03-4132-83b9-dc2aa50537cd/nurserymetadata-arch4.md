# Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011

## Overview
- A long-term study of Scots pine nursery phenotypes across three sites to understand phenology, form, and growth.
- Sample: 210 families (10 families from each of 21 native Scottish populations), comprising 5,040 individuals (24 half-sibling progeny per family).
- Experimental design: seeds collected in 2007, germinated and grown in three nurseries (NW, NE, NG) across Scotland in randomized blocks (40 blocks per nursery; 2 trees per population per block; 3 nurseries total).
- Transplanting and growth: NG plants moved outdoors in 2010; all plants repotted in 2010 into larger pots; no artificial light used.
- Traits measured (2007–2011): phenology (budburst, growth cessation), form (total buds, needle length), and cumulative growth (height, stem diameter, canopy width). Mortality recorded annually (2007–2010).
- Data structure: a single data file (NurseryTraits.txt) with detailed trait measurements, provenance, and experimental design metadata.

## Data Access, Licensing, and Citation
- Data access: available at https://doi.org/10.5285/29ced467-8e03-4132-83b9-dc2aa50537cd
- Licence: Open Government Licence v3 (OGPLv3)
- Attribution and citation requirements:
  - Always cite: Perry, A.; Beaton, J.K.; Stockan, J.A.; Cottrell, J.E.; Iason, G.R.; Cavers, S. (2022). Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/29ced4678e03-4132-83b9-dc2aa50537cd
  - Include the attribution statement: "Contains data supplied by UK Centre for Ecology & Hydrology."
  - Include any copyright notices identified in the metadata record for the Data in all copies and publications.

## Data Description and Contents
- Population and seed origin: seeds from 21 native Scottish Scots pine populations, representing the species’ native range with three populations per seed zone.
- Propagation and nursery setup:
  - Initial sowing and dormancy break procedures documented.
  - Seedlings allocated to three nurseries: NW (western Scotland outdoor), NE (Aberdeen fruit cage), NG (Aberdeen unheated glasshouse).
  - Plants arranged in 40 randomized blocks per nursery; 2 trees per population per block.
  - Transplant management and repotting details provided; eventual outdoor relocation of NG stock to Glensaugh in 2010.
- Traits and timing:
  - Phenology: budburst (days from 31 March 2008 to green needles observed) and growth cessation (days from 10 Sept 2008 to end of growth).
  - Form: total number of buds; needle length (mm).
  - Growth metrics: height (mm), stem diameter (mm), canopy width (mm).
  - Annual mortality (2007–2010); trait measurements collected 2007–2011.
- Data quality and cleaning:
  - Missing values treated as NA when height increments were invalid (<0) or due to measurement issues.
  - Stem diameter increments adjusted: 0 to -2 mm treated as 0; increments < -2 mm set to NA along with the most recent diameter.
- Data file and schema:
  - File: NurseryTraits.txt
  - Key fields include: PopulationCode, Family, Seedling, Nursery (NE, NG, NW), Block07to10, Block10to12, FieldCode, HA07–HA11 (height), DA08–DA11 (diameter), CW07_1/2, CW08_1/2, CW09_1/2 (canopy width), NL07_1/2–NL09_3 (needle length), Bu08 (buds counted), BB08 (budburst days), GC08 (growth cessation days), HI08–HI11 (height increment), DI09–DI11 (diameter increment), STATUS07–STATUS10 (survival status).
- Population and family structure:
  - 210 families (10 per population); 24 half-siblings per family; transplantation and tracking across three nurseries.
- Location coordinates:
  - Aberdeen (approximately latitude 57.133214, longitude -2.158764); NW and NE nursery sites referenced with coordinates.

## Metadata, Provenance, and Documentation
- Provenance: dataset derived from a controlled, multi-site nursery experiment spanning 2007–2011.
- Ownership/curation: CEH (Centre for Ecology & Hydrology) and James Hutton Institute (Aberdeen).
- Version history:
  - 2022-05-04: First version released.
  - 2022-08-11: Corrected description of the Seedling variable (numeric → alphanumeric) and added Data access and reuse section.

## Accessibility and Reuse Considerations for Data Leaders
- Openness and licensing: OGPLv3 supports broad reuse with attribution.
- Reuse requirements: must include the specified citation and attribution text in publications and presentations.
- Data discoverability and metadata quality: dataset is well-described with a clear schema and provenance, though users should consult the file's column definitions for exact variable meanings.
- Potential limitations to consider:
  - Data collected in controlled nursery environments; external validity to field conditions may be limited.
  - Missing data handling guidelines are described; users should account for NA values and measurement corrections in analyses.
  - Geographic and temporal scope is limited to Scottish populations and the 2007–2011 window, with a specific experimental design (three nurseries, replicated blocks).
- Data standards and interoperability:
  - A comprehensive column naming convention and unit annotations are provided, facilitating integration with related datasets and meta-analyses.
  - Explicit units (mm, days, counts) and status indicators enhance consistency across analyses.