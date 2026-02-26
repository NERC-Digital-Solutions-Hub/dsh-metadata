# Past deforestation (2000-2018) and future deforestation probability (2019-2053) for Wallacea

## Overview
- A geospatial data package assessing forest loss and fragmentation in Wallacea, Indonesia, and projecting future deforestation probability to 2053.
- Funded by the Newton Fund Wallacea Programme via NERC and Indonesian government partners.
- Purpose: establish a baseline to monitor environmental governance and conservation amid Indonesia’s development policies.

## Datasets and structure
- Three main GeoTIFF files:
  - forest_2014_18_180m.tif: primary forest cover in 2014 (1 = primary forest; 0 = forest loss 2000-2013; -9999 = non-forest). Used to train the deforestation model.
  - deforestation_2014_18_180m.tif: primary forest loss from 2014 to 2018 (1 = loss; -9999 = other).
  - summed_deforestation_probability_20xx_20xx_Wallacea.tif: summed probability of deforestation for 5-year intervals 2019-2053 (aggregate across 100 model iterations; a pixel deforested in 50 of 100 runs yields 50%).
- All files share the same geographic characteristics and projection (Albers equal-area), resolution (180 m), and data structure (GeoTIFF, no-data value -9999).

## Data relationships
- Datasets A and B (forest cover and recent loss) were used with predictor information (Table 1) from Voigt et al. 2021 to produce Dataset C (summed deforestation probability).
- The predictors include variables describing forest cover/loss history, environmental factors, accessibility, human pressure, economic drivers, and land-use.

## Predictors and data sources
- Forest cover and loss (2000, 2001-2013, 2014-2018): Giri et al. 2011; Hansen et al. 2013; Margono et al. 2014.
- Slope: Farr et al. 2007.
- Fire activity: MODIS and VIIRS data (2000-2018; 2012-2018).
- Accessibility: combinations including roads, settlements, slope; sources include Deere et al. 2020, Weiss et al. 2018, World Resources Institute data.
- Human population pressure: Rose et al. 2018; related population datasets.
- Main commodity, transmigrant settlements, mining, and land-use: Indonesian statistics and WRI data; 2010-2018 references.
- All predictors are treated as static inputs for the modelling, except for neighbourhood forest loss which is updated across time steps.

## Methodology
- Data processing:
  - Reprojected to Asia South Albers Equal Area; resampled to a common 180 m grid (bilinear for continuous, nearest-neighbour for categorical).
  - Forest defined as mature natural forest (primary forest) including mangroves; non-forest includes agriculture and degraded/other land uses.
  - Forest loss derived from the Tree Loss dataset (Hansen et al. 2013); care taken to minimize misclassification of plantations and regrowth.
- Modelling framework:
  - Logistic model for deforestation probability P_loss,x,t with forward stepwise regression to select predictors.
  - Many models (56–79 per sub-region) evaluated using Filzbach (MCMC) to obtain posterior means and credible intervals.
  - Model selection via cross-validation on held-out data (50% split) to retain predictors with predictive power.
- Simulations and uncertainty:
  - Parameter values drawn from Gaussian distributions based on MCMC results; per-iteration probabilities recalculated for each pixel over 7 time steps.
  - Spatially explicit deforestation simulated across time; each iteration yields a deforestation outcome. 100 iterations per region produce the summed_deforestation_probability product.
  - Neighborhood deforestation is updated each time step; all other predictors are static.
- Outputs:
  - 7 time steps simulated with aggregated results into summed deforestation probability rasters.

## Technical specifications
- File format: GTiff/GeoTIFF; compression: DEFLATE.
- Coordinate reference system: Albers Equal Area (detailed parameters provided); origin and standard parallels specified.
- Image characteristics: 10102 x 10593 pixels; pixel size 180 m; data type Int32; NoData -9999.
- Metadata includes area/point designation, axis mapping, and corner coordinates.

## Data quality, governance, and versioning
- Data version: no multiple versions noted in the record.
- Data quality measures include cross-validation during model selection and uncertainty quantification via Monte Carlo iterations.
- Documentation references accompanying publications for methodological details (Voigt et al. 2021).

## Provenance, funding, and references
- Principal investigators: Matthew J. Struebig and Maria Voigt, University of Kent.
- Funding: Newton Fund Wallacea Programme via UK NERC and Indonesian partners (grant numbers provided in the document).
- Key references for data sources and methods include Hansen et al. (2013), Giri et al. (2011), Margono et al. (2014), and the Voigt et al. 2021 publication linking predictors to the modelling framework.

## Usage and intended audience
- Designed as a baseline data asset for monitoring development trajectories and environmental governance in Wallacea.
- Useful for data leaders seeking to understand data provenance, modelling approach, uncertainty handling, and how combined predictor sets translate into future deforestation probabilities.