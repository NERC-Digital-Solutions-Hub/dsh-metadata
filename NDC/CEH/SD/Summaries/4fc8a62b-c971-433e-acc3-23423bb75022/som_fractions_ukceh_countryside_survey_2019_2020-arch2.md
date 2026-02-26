# Soil organic matter fractions

## Overview
- Examines soil organic matter (SOM) pools using density fractionation to understand stability and turnover.
- Focuses on four SOM pools (DOC, LF, OF, MAOM); in this study, DOC and OF were discarded from analysis, with OF derived by mass balance.
- Analyzes light fraction (LF) and mineral-associated organic matter (MAOM) for carbon and nitrogen contents to inform soil health and models of carbon turnover.

## Concepts and Pools
- SOM is heterogeneous with pools that differ in residence time.
- Stability influenced by litter source, aggregation, organo-mineral associations, and soil depth.
- Density fractionation separates:
  - Dissolved organic carbon (DOC)
  - Free light fraction (LF) / particulate organic matter (POM)
  - Occluded fraction (OF)
  - Mineral-associated organic matter (MAOM)

## Methods and Measurements
- Fractionation method:
  - Use sodium polytungstate (SPT) at 1.8 g cm-3 to separate LF and MAOM; discard DOC and OF (OF obtained by mass balance).
  - LF isolated by filtering after centrifugation; MAOM obtained from the remaining pellet after removing LF and OF via sonication and rinsing.
  - Internal controls: two batch standards and 10% replicated samples.
- Sample material:
  - 100 archived soil samples ( sieved to 2 mm) analyzed in spring 2022.
  - Archived soil used for fractionation; LOI, hygroscopic moisture, and CaCO3 measured by thermogravimetric analysis (TGA).
- LOI, hygroscopic moisture, CaCO3 (via TGA):
  - Four heating steps: 105°C (3 h) to determine hygroscopic water; 375°C (15.45 h) for SOM (LOI); 650°C for clay/mineral losses; 1000°C for CaCO3.
  - Calculations convert weight losses to hygroscopic moisture, SOM content, and calcite-C content (with corrections for calcite recovery).
- Carbon and nitrogen analyses:
  - Total C and N measured on LF and MAOM fractions and a subsample of archived soil using an elemental analyzer (SOP3102).
  - SOC calculated as total C minus calcite-C.
  - Fractional C and N contents computed for LF-C, MAOM-C, LF-N, MAOM-N.
  - OF and POM (occluded and particulate) masses and C/N calculated by mass balance; POM-C and POM-N derived from LF and OF.
  - Corrections applied for hygroscopic water; OF and POM corrected for measurement uncertainty (set negative OF values to zero).
- Data processing:
  - Fractions expressed as g per g of oven-dry soil (g g-1) or g per 100 g soil where appropriate.
  - Mass, C, and N values adjusted for inorganic carbon (calcite-C) only for MAOM-C; LF and MAOM fractions not corrected for calcite.
- Data quality and structure:
  - Each batch uses internal standards and replicated samples to ensure accuracy.
  - Dataset structure described (13 columns, 101 rows); includes LF_C, MAOM_C, OF_C, POM_C, LF_N, MAOM_N, OF_N, POM_N, SOC, TN, SOM, Year, SQ_ID.

## Countryside Survey Context and Design
- UKCEH Countryside Survey: ongoing national audit of countryside resources since 1978, with rolling annual monitoring 2019–2023.
- Purpose: track direction and magnitude of soil condition and function changes across Great Britain and how pressures interact spatially and temporally.
- Rolling survey design:
  - 500 x 1-km2 squares across a five-year cycle; 100 squares visited each year.
  - Squares selected randomly within strata defined by Land Classification of Great Britain; urban (>75%) and sea (>90%) areas excluded.
  - Field sampling aims to capture multi-metric, ecosystem-scale data during single visits; current focus on soil and vegetation changes.
- Sampling protocol:
  - Per square, up to 5 X-Plots selected; topsoil samples collected with 15 cm cores concurrent with vegetation surveys.
  - Soil samples for SOM density fractionation analyzed from 100 archived samples collected in 2019–2020 (spring 2022 processing).
- Objectives:
  - Produce data and maps of soil stock and change across GB soils.
  - Co-locate soil measurements with vegetation assessments to understand soil–vegetation interactions.

## Data Outputs and Structure
- Dataset composition:
  - 13 data columns including: LF_C_gperg, MAOM_C_gperg, OF_C_gperg, POM_C_gperg, LF_N_gperg, MAOM_N_gperg, OF_N_gperg, POM_N_gperg, SOC_gperg, TN_gperg, SOM_gperg, Year, SQ_ID.
- Coverage:
  - 101 rows (samples) with some metrics NA where not analysed.
- Purpose of outputs:
  - Provide detailed fraction-specific carbon and nitrogen stocks to support national soil monitoring and models of soil carbon dynamics.

## Funding and References
- Funding: UK-SCAPE national capability programme; Natural Environment Research Council; AI4SoilHealth project.
- Key references: foundational methods on SOM fractionation, UK Countryside Survey design, and related soil carbon research (citations include SPT density fractionation, LOI/TGA methods, and prior Countryside Survey reports).

## Implications for Environmental Monitoring
- Enables monitoring of soil health by tracking stable and labile SOM pools over time, aiding evaluation of soil function and resilience.
- Facilitates data integration by providing standardized, quality-controlled soil carbon and nitrogen fractions for national maps and policy performance assessment.
- Supports cross-data accessibility by structuring outputs for incorporation into monitoring portals and dashboards.