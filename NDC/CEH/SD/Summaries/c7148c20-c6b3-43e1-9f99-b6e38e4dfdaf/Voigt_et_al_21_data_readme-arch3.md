# Past deforestation (2000-2018) and future deforestation probability (2019-2053) for Wallacea

## Overview
- Dataset documenting historical deforestation (2000-2018) and projected deforestation probability (2019-2053) for Wallacea, Indonesia.
- Aims to understand patterns and drivers of forest loss, project future deforestation, and provide a baseline to monitor governance and conservation outcomes amid policy changes in Indonesia.
- Funded by the Newton Fund's Wallacea Programme via UK NERC and the Indonesian Ministry of Research, Technology & Higher Education.

## Data Content
- A. forest_2014_18_180m.tif: Primary forest cover in 2014 (1 = forest; -9999 = non-forest). Used to train the deforestation model.
- B. deforestation_2014_18_180m.tif: Primary forest loss between 2014 and 2018 (1 = loss; -9999 = other). Used to train the deforestation model.
- C. summed_deforestation_probability_20xx_20xx_Wallacea.tif: Summed probability of deforestation for 5-year intervals from 2019 to 2053. Values represent the fraction of 100 model iterations in which deforestation occurred for a pixel (0–100).
- Relationship: A and B, together with predictors described in Voigt et al. 2021 (Table 1), feed into the deforestation model to generate C.
- Geographic scope: Wallacea, Indonesia.
- Data versions: No multiple versions of this dataset.

## Methods
- Data processing and projections:
  - All layers converted to Asia South Albers Equal Area Conic projection; resampled to a common extent and origin at 180 x 180 m.
  - Resampling: continuous predictors use bilinear; categorical predictors use nearest-neighbour.
  - Tools: Python, R, and ArcGIS Pro.
- Forest definitions:
  - Deforestation: annual loss of forest including mangroves.
  - Primary forest: mature natural forest >5 ha, with high canopy cover (>90%), natural composition/structure, and not cleared recently.
  - Mangroves included; plantations/regrowth excluded.
  - Forest cover defined using Landsat-based data with >70% canopy, aggregated to 180 m resolution.
- Modelling framework:
  - Based on a logistic model for each pixel x and time t: P(deforestation) = 1 / (1 + exp(-k_x,t)).
  - k_x,t modeled as a function of predictors via forward stepwise regression; 56–79 models tested per sub-region.
  - Parameter estimation with Filzbach (MCMC) to obtain posterior means and credible intervals.
  - Model selection via cross-validation: evaluated predictive power on held-out data; choosing the model with the highest test likelihood.
- Simulations and uncertainty:
  - Time-step–by–time-step recalculation with parameter values drawn from the MCMC-derived Gaussian distributions to propagate uncertainty.
  - At each step, pixels are classified as deforested by comparing a random draw to P(deforestation).
  - 100 iterations per run; results aggregated into summed_deforestation_probability maps.
  - Predictors are treated as static; only neighborhood forest loss is dynamically updated across time steps.
- References and predictors:
  - Predictors include forest cover and loss (2000–2013, 2014–2018), slope, fire activity, accessibility, population pressure, main commodity, transmigrant settlements, mining, and land-use (as described in Voigt et al. 2021).

## Outputs and Format
- Output file types: GTiff/GeoTIFF (three main outputs: two inputs and one aggregated projection).
- Spatial resolution: 180 m pixels.
- Coordinate reference: Albers Equal Area projection (specific parameters described in the metadata).
- Data characteristics:
  - Data type: Int32 per pixel; NoData value = -9999.
  - Metadata includes projection, origin, pixel size, corner coordinates, and file structure details.
- All three files share identical geographic characteristics and are provided with accompanying readme metadata.

## Data Provenance and Funding
- Principal investigators: Matthew J. Struebig and Maria Voigt, University of Kent.
- Funding: Newton Fund’s Wallacea Programme via UK NERC and Indonesian partners.
- Related methodological framework and predictor descriptions published in Voigt et al. 2021.

## Relevance for Monitoring Frameworks
- Provides a scalable approach to monitor deforestation risk and its drivers over time, aligning with the aim of identifying environmental health measures to scrutinize policy and inform future decisions.
- Delivers:
  - Historical baseline (2000–2018) of forest cover and loss.
  - Probabilistic future scenarios (2019–2053) to evaluate policy impacts and governance needs.
  - Transparent, reproducible modelling workflow with uncertainty quantification to support decision-making and data governance.

## Access, Metadata, and Governance Considerations
- Data are produced with explicit methodological detail, transparent assumptions (forest definitions, predictors, and modeling approach), and explicit metadata (projection, resolution, extents, and data structure).
- As with many monitoring datasets, challenges include ensuring metadata completeness, data accessibility, and consistent updates to maintain timeliness and usefulness for governance purposes.
- The dataset emphasizes openness of model inputs/outputs and clear documentation to facilitate reuse in monitoring and policy evaluation contexts.

## Limitations and Considerations for Use
- Spatial resolution is 180 m, which may limit detection of very fine-scale deforestation and smallholder activities.
- Predictors are largely static, with only neighborhood deforestation updating across time steps, which may affect capture of dynamic drivers.
- Model uncertainty is communicated via multiple iterations and posterior parameter distributions, but users should still consider residual uncertainties in policy evaluations.
- Mangrove and primary forest definitions are explicitly incorporated, but definitions can influence comparability with other datasets.

## Contact and Source Reference
- Dataset produced by Struebig and Voigt (University of Kent); data and methodology described in Voigt et al. 2021; readme and data package provide detailed file specifications and processing steps.