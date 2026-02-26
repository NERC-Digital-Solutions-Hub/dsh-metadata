# Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011

## Data access and reuse
- Data are accessible via DOI: https://doi.org/10.5285/29ced467-8e03-4132-83b9-dc2aa50537cd
- Licence: Open Government Licence v3
- Required citation in reports/publications describing research using the data:
  Perry, A.; Beaton, J.K.; Stockan, J.A.; Cottrell, J.E.; Iason, G.R.; Cavers, S. (2022). Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/29ced4678e03-4132-83b9-dc2aa50537cd
- Attribution statement to acknowledge source: "Contains data supplied by UK Centre for Ecology & Hydrology."
- Must include any copyright notice identified in the metadata record for the Data in all copies and publications
- Data reuse requires appropriate sharing of underlying data and adherence to data governance processes

## Data description
- Study design: seed collected in March 2007 from 21 native Scottish Scots pine populations (10 families per population; total 210 families; 24 half-sibling progeny per family; total 5,040 individuals)
- Sampling and provenance: populations chosen to cover native range in Scotland; three populations from each of seven Scots pine seed zones
- Propagation and growing conditions: seeds germinated in controlled conditions, transplanted to pots (8 cm x 8 cm x 9 cm); three nurseries:
  - NW: outdoors at Inverewe Gardens, western Scotland
  - NE: outdoors in a fruit cage at James Hutton Institute, Aberdeen
  - NG: unheated glasshouse at James Hutton Institute
- Experimental design: 40 randomized trays per nursery (blocks), two trees per population per block (total 42 trees per block)
- Transplant and repotting: seedlings moved outdoors in 2010; all plants repotted in 2010 to larger pots
- Traits measured (2007–2011) in three categories:
  - Phenology: budburst timing and growth cessation (2008; weekly assessments)
  - Form: total number of buds (2008); needle length (2007–2009)
  - Cumulative growth: height (2007–2011); stem diameter (2008–2011); canopy width (2007–2009)
- Mortality: recorded annually (2007–2010)
- Data quality and handling:
  - Height increments < 0 mm treated as missing (NA) due to measurement error or damage
  - Stem diameter increments between 0 and -2 mm adjusted to 0
  - Increments < -2 mm set to NA along with most recent diameter measurements
- Data collection timeline and scope: measurements taken annually post-growing season; phenology assessed in spring and autumn of 2008

## File information
- Data file: NurseryTraits.txt
- Key variable categories and examples:
  - Identifiers: PopulationCode, Family, Seedling
  - Site and design: Nursery (NE; NG; NW), Block07to10, Block10to12
  - Transplant status: FieldCode
  - Phenology and growth: HA07–HA11 (height), DA08–DA11 (diameter), CW07_1, CW07_2, CW08_1, CW08_2, CW09_1, CW09_2 (canopy width)
  - Needle measurements: NL07_1, NL07_2, NL08_1, NL08_2, NL08_3, NL09_1, NL09_2, NL09_3
  - Buds and growth events: Bu08 (bud count), BB08 (budburst days), GC08 (growth cessation days), HI08–HI11 (height increments), DI09–DI11 (diameter increments)
  - Status: STATUS07–STATUS11 (ALIVE; DEAD years)
- Notes: One dataset file contains all measurements and derived fields

## Version history
- 2022-05-04: First version
- 2022-08-11: Metadata correction ( Seedling variable description corrected from numeric to alphanumeric ); Data access and reuse section added

## Implications for monitoring frameworks
- Provides longitudinal, multi-site phenotypic data suitable for evaluating environmental health indicators related to tree growth, phenology, and stress responses under controlled nursery conditions
- Demonstrates comprehensive metadata and provenance, including coordinates, site details, assay methods, and data cleaning rules, aiding transparency and reproducibility
- Licensing and attribution are clearly specified, supporting open data practices and governance
- Potential limitations for monitoring in policy contexts include site-specific conditions (nursery environments), missing years for some variables, and need for careful interpretation when extrapolating to natural forests
- Useful as a benchmark dataset for testing data management pipelines, standardization of trait measurements, and cross-site integration in environmental monitoring frameworks