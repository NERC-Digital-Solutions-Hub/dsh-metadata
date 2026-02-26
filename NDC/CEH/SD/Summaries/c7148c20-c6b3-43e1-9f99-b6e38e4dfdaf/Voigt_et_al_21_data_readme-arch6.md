# Past deforestation (2000-2018) and future deforestation probability (2019-2053) for Wallacea

## Overview
- A data package assessing patterns and drivers of forest loss in Wallacea and projecting deforestation to 2053.
- Provides three GeoTIFF data products that enable monitoring and self-serve analysis of deforestation risk.
- Connected to Voigt et al. 2021; funded by Newton Fund/NERC and Indonesian partners.

## Data Files and Content
- A. forest_2014_18_180m.tif
  - Primary forest cover in 2014 (values: 1 for forest; -9999 for non-forest).
  - Used to train the deforestation model.
- B. deforestation_2014_18_180m.tif
  - Primary forest loss between 2014 and 2018 (1 indicates loss; -9999 otherwise).
  - Used to train the deforestation model.
- C. summed_deforestation_probability_20xx_20xx_Wallacea.tif
  - Summed probability of deforestation for 2019–2053.
  - Derived by aggregating 100 binary projection runs; pixel value equals how many runs predicted deforestation (0–100).
- Relationship
  - Files A and B, alongside predictors listed in Table 1 of Voigt et al. 2021, feed the deforestation model to produce File C.

## Purpose and Intended Use
- Establishes a baseline to monitor Wallacea’s development and conservation governance amid policy changes in Indonesia.
- Enables end users to assess deforestation risk across Wallacea and to monitor changes over time.

## Methods and Modelling
- Forest definition
  - Includes mangroves; primary forest defined as mature natural forest >5 ha with high canopy and carbon stock; excludes young regrowth, plantations, agro-forests, and non-vegetated areas.
  - Forest loss derived from Tree Loss dataset (Hansen et al. 2013) with >70% canopy at 30 m resolution; aggregated to 180 m to reduce short-term degradation signals.
- Modelling framework
  - Deforestation probability Ptr loss x,t modeled as a logistic function of predictors.
  - Forward stepwise regression across sub-regions yielded 56–79 candidate models; selection via cross-validation and the model with maximum test likelihood.
  - Parameter estimation with Filzbach (MCMC) to obtain posterior means and credible intervals.
  - Simulation: for seven time steps, parameter values drawn from Gaussian distributions (from the MCMC results); pixel-level loss simulated by comparing Ptr loss to random draws; repeated 100 iterations to capture uncertainty.
  - Outputs aggregated into the summed probability map (File C); predictors treated as static except for neighborhood forest loss, which is updated each time step.

## Data Processing and Technical Details
- Spatial and format details
  - Driver: GTiff/GeoTIFF; 10102 x 10593 pixels; 180 m pixel size.
  - Projection: Asia South Albers Equal Area Conic (with specified parameters); coordinates in meters; NoData value -9999.
  - Band 1, single band per file; Data are stored with DEFLATE compression and band-major interleave.
- Processing workflow
  - All layers reprojected to the same CRS and extent; resampled to 180 m (bilinear for continuous predictors; nearest neighbor for categorical).
  - Tools used: Python, R, ArcGIS Pro.
  - Forest definitions and loss data built from established sources (Giri et al., Hansen et al., Margono et al., etc.).
  - Training and validation steps documented in Voigt et al. 2021 and associated supplementary information.

## Data Coverage and Provenance
- Geographic scope: Wallacea, Indonesia.
- Temporal coverage
  - Observed: 2000–2018 (forest cover and loss for model training).
  - Projected: 2019–2053 (deforestation probability per pixel).
- Data provenance
  - Primary data sources include Hansen/Lee tree loss, national and international forest cover datasets, and ancillary predictors (slope, fire activity, accessibility, population pressure, commodities, transmigrant settlements, mining, and land-use).
  - Detailed predictor descriptions and sources provided in Table 1 of Voigt et al. 2021.

## Data Quality, Uncertainty, and Limitations
- Uncertainty quantified through 100 stochastic simulation runs; results reflect parameter and model uncertainty.
- Spatial resolution is aggregated to 180 m to reduce noise from small-scale degradation.
- Static predictors assumed for the projection period; only neighborhood deforestation is dynamically updated.
- Exclusion criteria biased against plantations, agro-forests, regrowth, and scrublands to focus on primary forest dynamics.
- No multiple versions of the dataset; metadata indicate Sept 2020 data production.

## Access, Documentation, and Reuse
- No versioning beyond the documented package; metadata and readme authored by Maria Voigt (July 2021).
- Primary publication and documentation: Voigt et al. 2021; dataset readme accompanies the data package.
- File-level and methodological details provided to support reproducibility and integration into dashboards or exploratory analyses.

## Contact and Funding
- Contact: Matthew J. Struebig (M.J.Struebig@kent.ac.uk) and Maria Voigt (M.Voigt@kent.ac.uk), University of Kent.
- Funding: Newton Fund Wallacea Programme via NERC and Indonesian partners (various project numbers listed in the metadata).