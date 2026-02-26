# DATA HEADER INFORMATION for Braun_Blanquet_vegetation_and_indicator species.csv

## Overview
- Provides header information and a data dictionary for the Braun-Blanquet vegetation and indicator species dataset.
- Part of the Classical Survey documentation; references Manual 1_Classical_Survey.
- Associated with ESPA Programme and P4GES project.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data Schema and Variables
- site_id
  - Information: P4GES WP4 site code
  - Variable Type: Text String
  - Unit: None specified
  - Field materials/resource s: Not specified
- Scientific_name
  - Information: Scientific name of the inventoried species
  - Variable Type: Text String
  - Unit: None specified
  - Field materials/resource s: botanist
- Local_name
  - Information: Vernacular/local name of the inventoried species
  - Variable Type: Text String
  - Unit: None specified
  - Field materials/resource s: botanist
- Family
  - Information: Scientific family of the inventoried species
  - Variable Type: Text String
  - Unit: None specified
  - Field materials/resource s: botanist
- Life_form
  - Information: Life form category/class
  - Variable Type: Categorical
  - Unit: Fern/Shrub/Herb/Grass/Vine/Tree
  - Field materials/resource s: botanist
- Percent_cover
  - Information: Degree of dominance of the inventoried species
  - Variable Type: Numeric
  - Unit: %
  - Field materials/resource s: numeric scale
- Indicator_species
  - Information: Whether the inventoried species is a specific indicator of a land use
  - Variable Type: Binomial
  - Unit: Yes/No
  - Field materials/resource s: NA (values indicate not yet known as indicator)
- B_B_scale
  - Information: Braun-Blanquet scale value
  - Variable Type: Categorical
  - Unit: Categories 0, 1, 2, 3, 4, 5, 6
  - Field materials/resource s: (not specified)
  - Scale mapping:
    - 0: Not present
    - 1: 1-5% cover
    - 2: 5-25% cover
    - 3: 25-50% cover
    - 4: 50-75% cover
    - 5: 75-95% cover
    - 6: >95% cover

## Provenance, Access and Attribution
- DOI: https://doi.org/10.5285/b31330cc-743c-431e-95cd-68b316efed0b
- Programme: ESPA
- Project: P4GES
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo

## Standards and Metadata
- Data uses the Braun-Blanquet scale for percent cover interpretation.
- Explicit field definitions for each variable, including type and unit, to aid data discoverability and reuse.
- Indicates data contributors (e.g., botanist) for several fields, supporting data provenance.

## Usage and Data Leader Considerations
- Ensures data assets are discoverable and properly attributed via DOI and project metadata.
- Supports data quality and standardization through explicit variable types, units, and scale mappings.
- Highlights the need to maintain metadata completeness (e.g., field materials/resource s for some fields) and clear documentation of data collection methods (Classical Survey context).
- Encourages coordination with data communities and clear indicators of which species serve as land-use indicators.