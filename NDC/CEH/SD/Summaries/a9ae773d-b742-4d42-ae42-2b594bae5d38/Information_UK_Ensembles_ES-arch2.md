# Ensemble maps of UK above-ground carbon stock and water supply

## Overview
- A dataset of ensemble-based environmental service maps for the United Kingdom, combining multiple model outputs to characterise above-ground carbon stock and water supply.
- Includes 14 raster layers (1-band, 32-bit floating) representing 10 different among-model ensemble approaches (with some approaches offering two options) and a shapefile summarising water supply per watershed.
- Designed to enable cross-model comparison, uncertainty assessment, and standardised outputs suitable for policy and monitoring contexts.

## Data content and structure
- 14 raster layers (tiff) with corresponding world-files, representing normalized outputs from ensemble approaches for above-ground carbon stock.
- 1 shapefile (UKWaterEnsembles) containing 14 estimates per watershed polygon (catchments linked to NRFA gauging stations).
- Grid and projection:
  - Carbon rasters: 1,000 m × 1,000 m grid, 1 band, 32-bit float.
  - Projection: British National Grid (EPSG 27700) with 0.9996 scale factor, units in metres.
  - Water shapefile: 519 catchment polygons on mainland GB and Northern Ireland.
- Area coverage:
  - Above-ground carbon stock for Great Britain, Northern Ireland, including Isle of Man, Scilly, Isle of Wight, Orkney, Shetland, Inner/Outer Hebrides.
  - Water supply: 519 selected catchments across GB and NI.
- Units: Relative service delivery, normalised to 0–1; NoData value -999.

## Origin and input model outputs
- Based on ensemble outputs from the EnsemblES project ( Bangor University, UK-CEH, Lactuca), funded by UKRI Landscape Decisions programme.
- Models/ensembles reflect various ecosystem service modelling approaches; not all inputs cover the full UK area.
- Carbon outputs are aggregated to 1 km² resolution; water outputs are mapped to catchments; ensemble weights are derived from validation data and transferred to full-area maps.
- Several input datasets are referenced (e.g., InVest, LPJ-GUESS, LUCI, Copernicus tree cover, DECIPHeR, WaterWorld, etc.) with varying spatial grains and coverages.

## Data processing and normalization
- Individual model outputs were resampled to a common spatial setting (2.5 m grid for most polygon-based predictions; nearest-point resampling within 2.5 × 2.5 m cells).
- For comparability, outputs were area-corrected (per hectare) and normalised across models and validation datasets (Willcock et al., 2019; 2020).
- Normalisation uses a double-sided Winsorising approach (2.5th and 97.5th percentiles) to bound values into [0,1].
- Carbon normalisation reflects mean stock per hectare; water normalisation relates to catchment-based measures per hectare.

## Models and ensemble approaches
- Ten ensemble approaches across multiple model frameworks; weights derived through several strategies (see below) and averaged over jackknife runs (N=50% of polygons per run, 250 runs total).
- Ensemble weighting strategies (Eq. 1 in the document) involve normalised positive weights across models and validation data.
- Ensemble approaches include:
  - a) PCA ensemble: weights based on correlation to the first principal component (consensus axis).
  - b) Correlation coefficient ensemble: weights by mean correlation with other models.
  - c) Regression to the median ensemble: iterative log-likelihood regression against the median ensemble; weights from regression coefficients.
  - d) Leave-one-out cross-validation ensemble: iterative regressions excluding each model in turn; mean coefficients used as weights.
  - e) Grain-size ensemble: penalises coarser-resolution models; relative weights inversely related to grain size.
  - f) Distinct ensembles: attribute-based grouping to balance diversity; weights reflect group distinctiveness.
  - g) Trained/accuracy-weighted ensembles: weights based on model accuracy against a validation subset.
  - h) Log-likelihood regression variant: regression against specific validation data points.
  - i) Trained accuracy ensembles: alternative accuracy-based weighting.
  - j) Additional iterative/training variants as described (e.g., training on partial data with validation on separate subsets).
- All weighting schemes are normalised to sum to 1 before applying to Eq. 1.

## Validation data and calculation polygons
- Carbon validation: 2019 forest estate inventories in England and Scotland (Forest Research), forming 201 forest compartments aggregated into 2,078 forest polygons for mapping, then re-derived to full area.
- Water validation: 519 hydrometric NRFA stations with catchments, selecting catchments >100 km² (plus 41 Welsh catchments to ensure representation); largest station per river used to avoid pseudoreplication.
- Calculation polygons used for both carbon and water validation are described but not exhaustively detailed in the document.

## Analytical workflow and reproducibility
- Calculations conducted within polygons containing validation data; spatial data and validations are described but not fully itemised in this text.
- All ensemble calculations and their comparisons use the same jackknifed data subset per run to ensure consistency.
- Matlab-based workflow (Matlab v7.0.14.739) with statistical and parallel toolboxes; ensemble code available on GitHub (EnsemblesTypes/EnsemblesTypes).

## Quality control
- Internal team review by nine authors and external peer review for Ecosystem Services publication.
- Most input model data derived from peer-reviewed or well-accepted sources.

## Usage notes and caveats
- Potential bias risk: carbon weights concentrated on forests due to model design; non-forested areas may be underrepresented in high-value estimates.
- Some input models do not cover the entire UK area; readers should be aware of coverage limitations per model (see Table 1 in the source).

## Funding
- Funded under the EnsemblES project: Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models (UKRI Landscape Decisions programme, project NE/T00391X/1).

## References
- Key sources spanning ensemble methods, model comparisons, and ecosystem service valuation (e.g., Marmion et al. 2009; Grenouillet et al. 2011; Dormann et al. 2018; Willcock et al. 2019/2020; multiple model datasets and validation studies).