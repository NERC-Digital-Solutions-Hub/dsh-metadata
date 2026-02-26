# Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models.

## Aim and context
- Assess yield potential and soil carbon impacts of large-scale Miscanthus bioenergy under a common climate pathway (SSP2-RCP2.6) using three models: MiscanFor (Miscanthus-specific crop model), JULES (Dynamic Global Vegetation Model), and IMAGE (Integrated Assessment Model).
- Explore the role of bioenergy expansion in climate change mitigation, including early scale-up and later use as a sustainable bioenergy feedstock with carbon capture and storage (CCS).
- Provide data outputs (yield and soil carbon) to inform life cycle carbon balance and policy performance under a standardized scenario.

## Data generation and modeling approaches
- Climate driving data:
  - MiscanFor and JULES: HadGEM2-ES under RCP2.6, downscaled to 0.5° and bias-corrected (ISIMIP approach).
  - IMAGE: MAGICC-based RCP2.6 pathway downscaled with HadGEM2-ES data.
- Scenario and focus areas:
  - Tropics (25°N to 25°S) for 2040–2049.
  - Europe (approx. 15°W to 40°E, north of 35°N) for 2090–2099.
  - Bioenergy crop expansion maps generated within IMAGE to define land use for all three models.
- Outputs (primary focuses):
  - Yield (MiscanFor: direct yield; JULES/IMAGE: biomass carbon converted to dry matter at 48% carbon content).
  - Soil carbon change (MiscanFor: per hectare of planted area; JULES/IMAGE: per hectare of entire grid cell, including other land covers).

## Data scope and structure
- Global grid and coverage:
  - 6,858 grid cells selected from a global 0.5° grid where bioenergy land use occurs (about 11% of global land surface excluding Antarctica).
  - Remaining 89% not modeled due to lack of bioenergy land use in the scenario.
- File structure and formats:
  - Files named as {model}_{variable}_{period}.csv (MiscanFor outputs in CSV; JULES and IMAGE in NetCDF).
  - Data merged to a common 0.5° grid, with units standardized across models.
- Data specifics:
  - Each file includes: latitude, longitude, and value (yield or soil carbon change).
  - NaN values denote missing data due to model limitations or regional scope.

## Units and interpretation
- Yield: tonnes dry matter per hectare of planted area per year (MiscanFor), or biomass carbon converted to DM for JULES/IMAGE.
- Soil carbon change: tonnes C per hectare per year (MiscanFor: per planted area; JULES/IMAGE: per grid cell).
- Lat/long refer to the center of each 0.5° grid cell; temporal period indicated in the file name.

## Quality control and provenance
- Models are state-of-the-art, with rigorous testing and validation across multiple sites to ensure numerical stability and accuracy.
- Supporting literature and model versions:
  - MiscanFor (Daioglou et al., 2019; Shepherd et al., 2020)
  - JULES (Littleton et al., 2020)
  - IMAGE (Doelman et al., 2019; Doelman et al., 2018)
  - Related methodological references for ISI-MIP bias correction and SSP land-use dynamics.

## Access, usage, and ties to broader work
- The dataset provides raw model outputs underpinning the publication:
  - Littleton, E.W. et al. (2022). Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models. GCB Bioenergy, 15, 303-318.
- Model code and data availability:
  - JULES code publicly available via the Met Office repository.
  - The dataset supports cross-model comparisons and scenario analyses for monitoring environmental outcomes and policy performance related to bioenergy expansion.
- Referenced materials and context available in the accompanying citations, enabling traceability and reproducibility.

## Implications for environmental monitoring and policy evaluation
- Provides standardized, grid-level outputs (yield and soil carbon) under a common climate pathway, enabling temporal trend analysis and cross-model uncertainty assessment.
- Demonstrates the value and limitations of large-scale Miscanthus bioenergy as a mitigation strategy, informing data-driven monitoring of land-use change, carbon cycling, and policy effectiveness over the 21st century.
- Highlights data accessibility needs and the importance of enabling access to underlying datasets for broader use in environmental monitoring and decision-making.