# Past deforestation (2000-2018) and future deforestation probability (2019-2053) for Wallacea

- Aims and scope: Assess patterns and drivers of forest loss and fragmentation in Wallacea and project deforestation to 2053 using dynamic models; establish a baseline to monitor governance and conservation amidst policy changes in Indonesia.

## Data products (files)

- A. forest_2014_18_180m.tif
  - Primary forest cover in Wallacea in 2014 (coded as 1); forest loss between 2000 and 2013 (coded as 0); non-forest as -9999.
  - Used to train the deforestation model.

- B. deforestation_2014_18_180m.tif
  - Primary forest loss in Wallacea between 2014 and 2018 (coded as 1); all other pixels -9999.
  - Used to train the deforestation model.

- C. summed_deforestation_probability_20xx_20xx_Wallacea.tif
  - Summed probability of deforestation for 5-year intervals from 2019 to 2053.
  - Derived by aggregating 100 binary model iterations; value equals the number of iterations predicting deforestation for a pixel.

## Relationship to related work

- Files A and B are used with data described in Voigt et al. 2021 to produce the summed probability map (File C).
- The modelling framework and predictor variables are detailed in Voigt et al. 2021 (including a table of predictors).

## Methods and modelling approach

- Forest definition
  - Deforestation: annual loss of forest including mangroves.
  - Primary forest: mature natural forest >5 ha with undisturbed history; canopy >90% and high carbon stock; mangroves included to extend coverage.
  - Excludes regrowth, agro-forests, plantations, scrub, non-vegetated areas.

- Data processing
  - All layers reprojected to Asia South Albers Equal Area Conic; resampled to 180 x 180 m grid (bilinear for continuous, nearest-neighbour for categorical).
  - Processing performed in Python; analyses and visualization in Python, R, and ArcGIS Pro.

- Modelling framework
  - Probabilistic deforestation model: Ptrloss_x,t = 1 / (1 + exp(-k_x,t)); k_x,t modeled as a function of predictors.
  - Forward stepwise regression to assemble models per province/state; 56–79 models tested depending on predictor availability.
  - Model fitting via Filzbach (MCMC) to obtain posterior parameter distributions; cross-validation using a 50% holdout to assess predictive power.
  - Selection: best model is the one with the maximum test likelihood across the candidate set.

- Simulations and uncertainty
  - Simulations recalculate Ptrloss with parameters drawn from posterior distributions; at each time step, pixels are classified as deforested based on Ptrloss.
  - 100 iterations per scenario; results aggregated into summed_deforestation_probability files.
  - Static predictors; only neighbourhood deforestation is updated dynamically at each time step.

## Data specifics

- Geographic extent: Wallacea, Indonesia.
- File format: GeoTIFF (GTiff); 10102 x 10593 pixels.
- Coordinate reference system: Asia South Albers Equal Area Conic (specified parameters and EPSG codes in metadata).
- Pixel size: 180 meters; NoData value: -9999.
- Band/values: Integer; 1 = primary forest / deforestation signal as defined, 0 = forest loss (for training), -9999 = NoData.
- Shared grid: Files A, B, and C share identical grid, extent, and projection.
- Metadata notes: Includes origin, pixel size, corner coordinates, and projection details; readme prepared July 2021.

## Temporal scope and outputs

- Training period: 2000–2018 (forest cover and loss data used for model calibration).
- Projection period: 2019–2053 (5-year intervals); 100 stochastic iterations per interval to generate summed probabilities.

## Data quality, limitations, and notes

- Predictor variables treated as static; only local deforestation neighbourhood changes are dynamic across time steps.
- Cross-validation helps ensure predictive usefulness, but model performance depends on predictor availability and data quality across provinces.
- Data not versioned; a single dataset release (no multiple versions).

## Access, provenance, and funding

- Data produced: September 2020; authors: Matthew J. Struebig and Maria Voigt, University of Kent.
- Funding: Newton Fund Wallacea Programme via NERC and Indonesian Ristekdikti.
- Related publication: Voigt et al. 2021; data readme and methodology described therein.

## How this aids GIS work

- Provides a spatially explicit baseline and future deforestation probabilistic surfaces suitable for map-based visualization and policy/research communications.
- Facilitates scenario monitoring and integration with other spatial datasets to explore drivers and spatial patterns of deforestation in Wallacea.