# DATA HEADER information for Litter_layer_carbon_stock.csv

## Overview
- Describes the carbon stock of the litter layer at each site.
- Associated with ESPA programme and P4GES project.
- DOI provided for data citation.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Cross-referenced with Manual 1_Classical_Survey for additional context.

## Data provenance and structure
- Primary dataset: Litter layer carbon stock (carbon stock of litter).
- Site identifier: site_ID (P4GES site code; type Text String; unit not specified).
- Subplot: Subplot where the sample was collected (categorical; values S1, S2, S3, S4).
- Area: Quadrat area where samples were taken (numeric; unit m2; description: 1m x 1m = 1 m2).
- Litter_thickness: Thickness of the litter layer before sampling (numeric; unit cm; field method: measured with ruler).
- Matt_root_thickness: Thickness of the root mat layer before sampling (numeric; unit cm; field method: ruler).
- Biomass: Biomass stock of litter (numeric; unit “milligrams per hectare (Mg.ha-1)”).
- Stock_C: Carbon stock of litter (numeric; unit “milligrams per hectare (Mg.ha-1)”).
- Field materials/resources for several fields listed (e.g., Subplot measured by botanist; Litter_thickness and Matt_root_thickness measured with ruler); some fields show unspecified resources.

## Variables and data types (highlights)
- site_ID: Text String.
- Subplot: Categorical (S1/S2/S3/S4).
- Area: Numeric (square metres, m2).
- Litter_thickness: Numeric (cm).
- Matt_root_thickness: Numeric (cm).
- Biomass: Numeric (unit possibly Mg.ha-1; described as milligrams per hectare).
- Stock_C: Numeric (unit Mg.ha-1).

## Provenance, usage, and attribution
- Data stem from ESPA and P4GES projects; DOI provided for citation.
- Acknowledgement requirement explicitly stated for products derived from these data.
- Related documentation: Manual 1_Classical_Survey.

## Data quality, gaps, and considerations for Data Leaders
- Metadata largely present, but some fields (e.g., Field resources for Stock_C) are incomplete in the header.
- Unit clarity: Biomass unit appears potentially inconsistent (milligrams per hectare vs. Mg.ha-1); verify and standardize units for consistency.
- Data discoverability: Key identifiers (site_ID, Subplot, Area) are defined; ensure consistent formats across datasets.
- Cross-referencing with related manuals recommended to ensure proper interpretation of sampling context.

## Access, governance, and next steps
- DOI and project affiliations provided to support proper attribution and access.
- Follow-up action: consult Manual 1_Classical_Survey for full methodological context; ensure metadata completeness and unit standardization before integration into broader data system.