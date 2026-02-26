# DATA HEADER information for Understorey_carbon_stock.csv

## Overview
- Records the carbon stock of the herbaceous plants understorey cluster.
- Associated with ESPA Programme and P4GES Project.
- DOI provided: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data provenance and access
- Source programmes: ESPA (http://www.espa.ac.uk/) and P4GES (https://www.p4ges.org)
- Data header documents variable definitions, units, and information fields to support data reuse.
- Acknowledgement requirement noted for products derived from these data.

## Data schema (fields and definitions)
- site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: Not specified
- subplot
  - Information: Subplot where the sample was collected
  - Variable type: Categorical
  - Unit: S1 / S2 / S3 / S4
- Area
  - Information: Size of area sampled (1 m x 1 m)
  - Variable type: Numeric
  - Unit: square metre (m^2)
- Species
  - Information: Species observed in sample
  - Variable type: Not specified
  - Unit: Not specified
- freshweight
  - Information: Total fresh weight
  - Variable type: Numeric
  - Unit: grams
- freshweight_sample
  - Information: Fresh weight of subsample taken from the total understorey collected in the quadrat
  - Variable type: Numeric
  - Unit: grams
- dry_weight_sample
  - Information: Dry weight of subsample taken from the total understorey collected in the quadrat after drying in laboratory
  - Variable type: Numeric
  - Unit: grams
- Biomasse
  - Information: Biomass stock of understorey
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- Stock_C
  - Information: Carbon stock of understorey
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

## Data quality and notes
- Notes: -, NA and blank cells mean no data available.
- Some fields list Variable type as "." (unspecified) in the header, indicating not all fields have a defined variable type in this documentation.
- The dataset includes both raw (fresh weight) and subsample (fresh weight of subsample, dry weight of subsample) measurements alongside derived biomass and carbon stock values.

## How Data Leaders can use this dataset
- Supports carbon stock assessment for understorey herbaceous communities and integration into broader data strategies.
- Clear metadata (sites, subplots, area, species, weights, biomass, carbon) aids discoverability, validation, and interoperability across data products.
- Helps identify data gaps (e.g., missing species details, variable types, or site coverage) and informs prioritization of data gathering and standards development.
- Enables commissioning of supplementary data and cross-project collaboration to strengthen data standards and metadata consistency.
- Useful for designing data products that meet user needs (policy colleagues, researchers) through transparent units, definitions, and provenance.