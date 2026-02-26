# Past deforestation (2000-2018) and future deforestation probability (2019-2053) for Wallacea

- Objective
  - Assess patterns and drivers of forest loss and fragmentation across Wallacea.
  - Use dynamic deforestation models to project future deforestation to 2053.
  - Provide a baseline to monitor Wallacea’s development under policy changes affecting environmental governance and conservation.

- Data products (files)
  - A: forest_2014_18_180m.tif
    - Primary forest cover in 2014 (coded as 1).
    - Forest loss between 2000-2013 coded as 0.
    - Non-forest coded as -9999.
    - Used to train the deforestation model.
  - B: deforestation_2014_18_180m.tif
    - Primary forest cover loss in 2014-2018 (coded as 1).
    - All other pixels coded as -9999.
    - Used to train the deforestation model.
  - C: summed_deforestation_probability_20xx_20xx_Wallacea.tif
    - Summed probability of deforestation for 5-year intervals from 2019 to 2053.
    - Derived by aggregating 100 model iterations: a pixel deforested in 50 of 100 iterations gets a probability of 50%.

- Relationship among files
  - A and B are used with predictor variables (Table 1) from Voigt et al. 2021 to generate the summed probability map C.

- Additional related data
  - See Table 1 for predictors and data sources used in the deforestation modelling.

- Versions
  - No multiple versions of the dataset.

- Methodology (data collection and processing)
  - Projection and resolution
    - All layers converted to Asia South Albers Equal Area Conic projection.
    - Resampled to a common extent at 180 x 180 m pixel size.
    - Continuous predictors: bilinear resampling; categorical predictors: nearest-neighbour.
    - Tools: Python, R, ArcGIS Pro.
  - Forest definitions
    - Forest: annual loss of forest including mangroves.
    - Primary forest: mature natural forest >5 ha, natural composition/structure, >90% canopy cover, high carbon stock.
    - Includes mangroves; excludes regrowth, plantations, agro-forests, etc.
    - Forest cover in 2000 corresponds to the Ministry of Forestry definition with ~90% agreement; mangroves added (880 km²).
    - Forest loss: based on the Tree Loss dataset (Hansen et al. 2013); aims to minimize confusion with plantations and non-forest vegetation; forest pixels defined as >70% canopy cover at 30 m Landsat scale.
  - Temporal scope
    - Training data: 2014-2018 deforestation (and 2000-2013 forest loss) used to calibrate models.

- Modelling framework
  - Probability model
    - Pt_loss,x,t = 1 / (1 + exp(-k_x,t)); k_x,t modeled as a linear combination of predictors.
  - Model fitting
    - Forward stepwise regression with multiple model variants (56-79 models per sub-region).
    - Parameter estimation with Filzbach (MCMC) to obtain posterior means and credible intervals.
    - Log-likelihood defined to assess fit between observed loss and model predictions.
    - Model selection via cross-validation to ensure predictive ability; choose model with maximum test likelihood.
  - Simulation and uncertainty
    - Time-step recalculation with parameter values drawn from Gaussian distributions defined by MCMC results.
    - For each pixel and time-step, compare a random draw to Pt_loss,x,t to determine deforestation.
    - 100 iterations per run; results aggregated into summed_deforestation_probability maps.
    - Predictors treated as static; neighborhood forest loss updated dynamically across time steps.

- Outputs and interpretation
  - Summed deforestation probability maps (C) encode the fraction of simulation runs predicting deforestation per pixel across 2019-2053.
  - Provides a probabilistic forecast of deforestation risk under modeled drivers and parameter uncertainty.

- Geographic and data specifications
  - Data format: GTiff/GeoTIFF
  - File size: 10102 x 10593 pixels
  - Coordinate system: Asia South Albers Equal Area Conic (EPSG:9001 variant)
  - Pixel size: 180 m
  - NoData: -9999
  - Metadata include data origin and processing details; Center coordinates provided.

- Data provenance and sources
  - Predictors and data sources cited (e.g., forest cover/loss datasets from Hansen et al., Giri et al., Margono et al., land-use maps from Indonesian agencies, MODIS/VIIRS fire data, accessibility and population datasets).
  - Related publication: Voigt et al. 2021 (deforestation model and predictors; data in Table 1).

- Funding and contact
  - Funded by the Newton Fund’s Wallacea Programme via NERC (NE/S007067/1) and Indonesian Ministry for Research, Technology & Higher Education.
  - Authors: Matthew J. Struebig and Maria Voigt, University of Kent (contacts provided).