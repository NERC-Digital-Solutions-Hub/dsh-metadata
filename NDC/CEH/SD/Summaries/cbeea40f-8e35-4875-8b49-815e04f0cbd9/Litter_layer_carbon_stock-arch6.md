# DATA HEADER information for Litter_layer_carbon_stock.csv

## Overview
- Describes the carbon stock of the litter layer on each site.
- Related to ESPA Programme and P4GES Project; includes a DOI for the dataset.
- Acknowledgement required for work derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- References to additional documentation: Manual 1_Classical_Survey.

## Data content and purpose
- Provides the structure and metadata for the Litter_layer_carbon_stock dataset, enabling understanding, verification, and reuse.
- Designed to support data discovery, integration with other datasets, and the creation of data products (e.g., dashboards, reports) for end users to explore litter carbon stock data.

## Data schema (key variables)
- site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: .
  - Field materials/resources: .
- Subplot
  - Information: subplot where the sample was collected
  - Variable Type: Categorical
  - Unit: S1 / S2 / S3 / S4
  - Field materials/resources: botanist
- Area
  - Information: Area of the quadrat in which the samples were taken
  - Variable Type: Numeric
  - Unit: square metre (m2)
  - Field materials/resources: botanist
- Litter_thickness
  - Information: Thickness of the litter layer measured before sampling in the field
  - Variable Type: Numeric
  - Unit: Centimeter (cm)
  - Field materials/resources: ruler
- Matt_root_thickness
  - Information: Thickness of the root matt layer measured before sampling in the field
  - Variable Type: Numeric
  - Unit: Centimeter (cm)
  - Field materials/resources: ruler
- Biomass
  - Information: Biomass stock of litter
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field materials/resources: .
- Stock_C
  - Information: Carbon stock of litter
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field materials/resources: .

## Provenance and usage
- Source/programme: ESPA (Environmental Surveillance Programme) and Project P4GES
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Included documentation: Manual 1_Classical_Survey

## How this supports data work (Data Support archetype alignment)
- Provides a clear data header that facilitates data understanding, quality checks, and transformation for end-user self-service dashboards or reports.
- Enables data integration by listing data types, units, and collection context (subplots, quadrat area, field measurements).
- Highlights data provenance and acknowledgement requirements to maintain proper citation and reuse.
- Supports communication of data content to non-specialists by explicitly describing what each field represents and how it was collected.

## Notes and potential caveats
- Some fields (Field materials/resources) may be empty for certain variables.
- There is a minor inconsistency in the Biomass unit notation (listed as milligrams per hectare with Mg.ha-1), so users should verify the correct unit in the dataset documentation.
- The header references an external Manual for additional context; refer to Manual 1_Classical_Survey for methodological details.