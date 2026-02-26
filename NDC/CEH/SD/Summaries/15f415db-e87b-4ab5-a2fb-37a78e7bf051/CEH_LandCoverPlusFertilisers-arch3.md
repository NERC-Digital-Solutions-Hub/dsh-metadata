# CEH Land Cover plus: Fertilisers 2010-2015 (England)

## Data access and citation
- Data are available from the Environmental Information Data Centre.
- Citation: Osório, B.; Redhead, J.W.; Jarvis, S.G.; May, L.; Pywell, R.F. (2019). CEH Land Cover plus: Fertilisers 2010-2015 (England). NERC Environmental Information Data Centre. https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051

## What the data are
- Maps of predicted average annual application rates (2010-2015) of three inorganic fertilisers—nitrogen (N), phosphorus (P), and potassium (K)—in England, at 1 km x 1 km resolution.
- Each map also includes corresponding uncertainty estimates.
- Generated under the ASSIST project to explore impacts of agrochemical usage and support sustainable farming practices.
- Applications include nutrient fate modelling, greenhouse gas emissions estimation, eutrophication indicators, linking to crop growth models, and informing policies to mitigate fertiliser impacts.

## Data content and structure
- Two-band raster TIFFs (1 km resolution) covering England for each fertiliser:
  - Band 1: Predicted average annual fertiliser application rate (kg/km^2).
  - Band 2: Uncertainty associated with the predicted rate (percent).
- File names:
  - fertiliser_n_prediction_uncertainty
  - fertiliser_p_prediction_uncertainty
  - fertiliser_k_prediction_uncertainty

## How the data were collected
- Raw data come from Defra’s British Survey of Fertiliser Practice (BSFP), 2010–2015.
- Surveys are voluntary, nationally representative, and based on a stratified random sample of farmers. Average of ~3,696 georeferenced farms per year.
- Each record includes year, application rates (kg/ha), location (British National Grid), crop typology (66 classes), soil type, farm size indicators, and IDs.
- Zero-rate records were excluded from the analysis due to ambiguity (missing data, use of organic manure, or actual zero application), so maps show only areas where fertilisers were applied (>0 kg/ha).

## Analytical methods
- Interpolation method: Ordinary kriging (OK), chosen for performance, agricultural data precedent, and ability to generate a variance surface for uncertainty.
- Crop context: Interpolations tied to crop typology from CEH Land Cover plus: Crops (averaged 2015–2017) at 1 km resolution; crop-area weighting applied to produce total application per 1 km cell.
- Base data: BSFP fertiliser rates (kg/ha) per crop, linked to crop area to derive total application per cell (kg/km^2) for each fertiliser.
- Use of satellite-derived Crops map (Sentinel-based) to reflect cropping patterns.

## Modelling and uncertainty assessment
- Semivariogram and kriging parameters set within ArcGIS; a variable search radius of 12 input points used to interpolate each cell.
- Uncertainty calculation: Kriging variance per crop-type multiplied/aggregated to produce a per-fertiliser uncertainty surface; final uncertainty per cell calculated as:
  U = (2 * sqrt(V)) / P * 100
  where V is kriging variance and P is the predicted rate for that cell.
- Resulting uncertainty represents approximately 95.5% confidence (double the standard deviation) and can be scaled relative to predicted values.

## Data quality and limitations
- Zeros in BSFP data are excluded, which may introduce gaps in spatial predictability for certain areas or crops.
- Uncertainty guidance is based on kriging variance aggregated across crops; correlations between crops are ignored in the simple aggregation approach.

## Data provenance and processing workflow
- Raw fertiliser data linked to crop typology; interpolation performed per fertiliser and per crop; results scaled by crop-area, then aggregated across crops to final per-cell fertiliser totals.
- All processing performed using ArcGIS with default settings for transparency and reproducibility.

## Acknowledgements
- Supported by NERC national capability funding to CEH and NERC/BBSRC under NE/N018125/1 LTS-M ASSIST.
- Defra BSFP acknowledged for data access; special thanks to David Fernall and Alison Wray.