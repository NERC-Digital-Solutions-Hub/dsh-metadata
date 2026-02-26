# Past deforestation (2000-2018) and future deforestation probability (2019-2053) for Wallacea

## Overview
- Study to assess patterns and drivers of forest loss and fragmentation across Wallacea and project future deforestation to 2053.
- Provides a baseline for monitoring policy and governance changes affecting environmental conservation in Indonesia.
- Data produced in September 2020 by researchers at the University of Kent; funded by Newton Fund’s Wallacea Programme via NERC and the Indonesian Ministry.

## Data files and relationships
- A. forest_2014_18_180m.tif: Primary forest cover in 2014 (coded 1); forest loss between 2000-2013 (coded 0); non-forest as -9999. Used to train the deforestation model.
- B. deforestation_2014_18_180m.tif: Primary forest loss between 2014-2018 (coded 1); all other pixels -9999. Used to train the deforestation model.
- C. summed_deforestation_probability_20xx_20xx_Wallacea.tif: Summed probability of deforestation for 5-year intervals from 2019 to 2053. Pixel-level deforestation probability across 100 model iterations; value equals the number of iterations in which the pixel was deforested (0–100).
- A and B were used with predictors described in Table 1 of Voigt et al. 2021 to produce C (deforestation probability).
- No multiple versions of the dataset; table of predictors (Table 1) includes variables such as forest cover/loss, slope, fire activity, accessibility, population pressure, commodities, transmigrant settlements, mining, and land-use.

## Data provenance and governance
- Geographic scope: Wallacea, Indonesia.
- Files share the same projection and grid characteristics (Albers Equal Area Conic; 180 m pixel size; 10102 x 10593 grid; NoData = -9999).
- Data processing and modelling built on established datasets and methods (e.g., Hansen et al. for tree cover loss; various land-use and accessibility layers referenced in Voigt et al. 2021).
- Model framework uses logistic probability of deforestation with forward stepwise regression; parameter uncertainty captured via MCMC (Filzbach) and cross-validation to select predictive predictors.
- Simulations run 100 iterations to propagate parameter uncertainty; neighbor (neighbourhood) deforestation updated dynamically each time-step.
- Related publication: Voigt et al. 2021 (data and methods described; link provided in accompanying documentation).

## Methods and modelling details
- Data preparation: all layers re-projected to Asia South Albers Equal Area Conic, resampled to 180 m (continuous predictors: bilinear; categorical: nearest-neighbour).
- Forest definition: primary forest includes mature natural forest (>5 ha, high canopy cover, high carbon stock); mangroves included; exclusions applied for regrowth, plantations, agro-forestry, etc.
- Forest loss base: Tree Loss dataset ( Landsat time-series ) with >70% canopy cover threshold; processed to 180 m resolution to reduce short-term degradation bias.
- Modelling: probability of loss in pixel x, t defined by a logistic function with k_x,t as a linear combination of predictors; forward selection yielded 56–79 models per region; models evaluated via cross-validation and likelihood; best model per province selected.
- Simulations: predictions updated each time-step with parameter values drawn from MCMC posterior; binary deforestation decisions sampled against P_subset; results aggregated into summed_deforestation_probability outputs.
- Temporal scope: predictors treated as static; only deforestation in the immediate neighbourhood updated over time steps.

## Technical specifications and metadata
- Data format: GeoTIFF (GTiff) with single band per file.
- Spatial resolution: 180 m; extent and origin aligned across A, B, and C.
- Coordinate reference: Albers Equal Area Conic (specific parameters provided); origin and corner coordinates included in metadata.
- Pixel dimensions: 10102 (width) x 10593 (height).
- NoData value: -9999.
- File characteristics: area-based metadata; projection and CRS mapping information included in the data readme.
- Data axis mapping: consistent with two-dimensional projected coordinate system.

## Usage, limitations, and governance considerations
- Purpose-built for monitoring deforestation patterns and testing governance-related futures under policy changes in Indonesia.
- When reusing, note that the summed probability outputs (C) reflect model-run aggregations across 100 iterations and are not direct observed deforestation but model-based projections with parameter uncertainty.
- Dataset relies on multiple external sources (e.g., Hansen et al. 2013; regional land-use data) and a defined forest concept that includes mangroves and excludes certain degraded/non-forest categories.
- Data owners emphasize documentation of work and alignment with the publishing publication (Voigt et al. 2021) for methodological reference and reproducibility.

## Contact and access
- Primary contacts: Matthew J. Struebig (University of Kent) and Maria Voigt (University of Kent).
- Data produced by Voigt et al.; readme generated by Maria Voigt (28.07.21) with methodological and technical details.
- Related publication and methods accessible via the provided Voigt et al. 2021 link in the dataset documentation.