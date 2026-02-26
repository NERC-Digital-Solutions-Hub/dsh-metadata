# Topsoil nutrient model estimates [Countryside Survey]

## Overview
- Dataset of topsoil nutrient estimates for Great Britain (GB) focusing on the 0–15 cm soil depth.
- Core variables: total nitrogen concentration (%), C:N ratio, and Olsen-Phosphorus (mg/kg).
- Data derived from samples collected in 2007 (with reference to 1998 data) across 256 one-kilometre squares, enabling habitat/parent material–level modelling.
- Models produce mean estimates for habitat and parent material combinations, based on dominant habitat and parent material characteristics.

## Data scope and key variables
- Total nitrogen concentration: modeled means across habitat/parent material combinations; N concentration also used to derive C:N ratio.
- Olsen-Phosphorus (P): modeled mean concentrations across the same strata.
- Parent material characteristic: Dominant grain (DOM_GRAIN) used for modelling N, C:N, and Olsen-P.
- Habitat and land cover linked via Land Cover Map 2007 (LCM2007) and related classifications.
- Table of dataset attributes includes: LCM_CLASS, LCM_NUMBER, DOM_GRAIN, SOIL_GROUP, CACO3_RANK, NCONC_98/07, CN_98/07, TOTN_07, OLSEN_98/07, SE values, and related standard errors.

## Sampling design and collection
- Sampling frames:
  - Total N: 1024 plots in 2007; 1110 plots in 1998 (75% overlap between years).
  - Olsen-P: 1068 plots in 2007; 65% of these also sampled in 1998.
- Plots are drawn from the Main Plots within the 256 original 1 km × 1 km squares.
- Some habitat/parent material combinations could not be estimated due to insufficient sample sizes, and urban or littoral rock areas were not sampled by Countryside Survey.

## Collection methods and analytical procedures
- Sampling method: soil cores (15 cm long, 5 cm diameter) collected following the Emmett et al. field protocol.
- Total nitrogen and C:N ratio: measured via a CEH Lancaster UKAS-accredited elemental analyzer (SOP3102).
- Olsen-P: extracted from air-dried, sieved soil (5 g, 0.5 M NaHCO3, pH 8.5); phosphorus quantified colorimetrically using molybdenum blue at 880 nm with a dialysis step to mitigate reagent interference.
- Calibration and analytical details: further information available in Emmett et al. 2008 and 2010.

## Modelling, data attributes, and references
- Modelling approach: mixed-model estimates of mean values by habitat/parent material combinations; dominant habitat and parent material characteristics are derived from LCM2007 and the Soil Parent Material Model (DOM_GRAIN).
- Data attributes include numeric codes and descriptive labels for habitat, land cover, soil texture, carbonate content, and nutrient measurements with corresponding 1998 and 2007 values and associated standard errors (e.g., NCONC_98, NCONC_07, TOTN_07SE, CN_98, CN_07, Olsen_07, Olsen_98, etc.).
- Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700).
- Data quality and governance: adherence to Defra/NERC Joint Codes of Practice throughout the project.
- Supporting documents and references:
  - Emmett et al. 2008: Soils Manual (Countryside Survey Technical Report No. 03/07)
  - Scott 2008: Statistical Report (CS Technical Report No. 4/07)
  - Emmett et al. 2010: Soils Report from 2007 (CS Technical Report No. 9/07)
  - Morton et al. 2011: Land Cover Map 2007 (GB)
  - Additional related works and datasets cited for methodology and context.

## Data governance, access, and limitations
- Public sharing of underlying data is subject to governance and metadata availability; some habitat/parent material combinations may lack estimates due to insufficient sampling.
- Some areas (urban and littoral rock) are not sampled within Countryside Survey.
- Transformation and alignment to hierarchical habitat/parent material classifications depend on the dominant characteristics from LCM2007 and DOM_GRAIN models.
- Data quality ensured through standardized protocols and QA practices; references provide detailed methodological validation.

## Practical relevance for monitoring frameworks
- Provides time-series-like insight by comparing 1998 and 2007 data for key soil nutrients across GB habitats, enabling trend analysis and policy evaluation.
- Delivers standardized, model-based estimates that can feed dashboards, reports, and governance processes for environmental health monitoring.
- Clear metadata structure (attributes, units, sampling design, and analytical methods) supports data discovery, provenance tracking, and reproducibility in monitoring frameworks.