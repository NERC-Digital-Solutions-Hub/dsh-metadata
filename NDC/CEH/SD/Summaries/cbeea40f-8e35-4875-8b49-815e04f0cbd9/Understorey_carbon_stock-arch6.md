# DATA HEADER information for Understorey_carbon_stock.csv

## Overview
- The dataset records the carbon stock of the herbaceous plants cluster in the understorey.
- Associated with ESPA Programme and Project P4GES; includes P4GES site code (site_ID) and sampling details.
- Acknowledgement is required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Related documentation: Manual 1_Classical_Survey, page 10, Section 2.3.2; DOI provided in the header.

## Provenance and usage rights
- Programme: ESPA
- Project: P4GES
- DOI for data reference: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required for derived products.
- Source notes: The dataset includes a header describing each field and its units; note that -, NA, and blank cells indicate no data available.

## Data schema and units
- site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: (none)
- Subplot
  - Information: subplot where the sample was collected
  - Variable type: Categorical
  - Unit: S1 / S2 / S3 / S4
- Area
  - Information: Size of area sampled = 1m x 1m
  - Variable type: Numeric
  - Unit: square metre (m²)
- Species
  - Information: Species observed in sample
  - Variable type: (unspecified)
  - Unit: (none)
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

## Data quality and missing data
- Notes: -, NA and blank cells mean no data available.