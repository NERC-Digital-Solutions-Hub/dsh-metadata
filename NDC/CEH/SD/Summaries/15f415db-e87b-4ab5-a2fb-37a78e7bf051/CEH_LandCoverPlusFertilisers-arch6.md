# CEH Land Cover plus: Fertilisers 2010-2015 (England)

## Data access and citation
- Data accessible from the Environmental Information Data Centre at https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051
- Citation required: Osório, B.; Redhead, J.W.; Jarvis, S.G.; May, L.; Pywell, R.F. (2019). CEH Land Cover plus: Fertilisers 2010-2015 (England). NERC Environmental Information Data Centre. https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051

## Data description
- Maps of predicted average annual application rates (2010-2015) for nitrogen (N), phosphorus (P), and potassium (K) fertilisers in England.
- Resolution: 1 km x 1 km; units: kilograms per square kilometre (kg/km^2); includes accompanying uncertainty estimates.
- Data produced to enable exploration of environmental impacts of agrochemical use and support sustainable farming practices.
- Potential uses include modelling nutrient fate, estimating greenhouse gas emissions from fertiliser use, assessing eutrophication and biodiversity indicators, linking to crop growth models, and informing policy for pollution reduction and water quality improvements.

## Collection methods
- Raw data from Defra’s British Survey of Fertiliser Practice (BSFP), 2010-2015: yearly, georeferenced records of application rates (kg/ha) for N, P, K; about 3,696 farms annually; nationally representative.
- Zeros handling: zero values excluded due to possible missing data, actual zero application, or substitution with organic manures; this aims to preserve spatial predictability at 1 km resolution.
- Crop linkage: fertiliser data linked to crop typology from Land Cover plus: Crops map (England, averaged 2015-2017) at 1 km; total per-cell application calculated by multiplying crop area by crop-specific rates and summing across crops to yield total kg/km^2 per cell.
- Interpolation: Ordinary Kriging (OK) used to generate prediction and a kriging-variance surface (uncertainty); chosen for performance, agricultural data precedent, and ability to produce a variance surface for uncertainty estimation.
- Parameters: variable search radius with 12 input points; ArcGIS default settings used for other parameters; crop-area weighting applied per crop group.

## Analytical methods
- Interpolation approach: OK to estimate predicted rates and derive a corresponding uncertainty surface (kriging variance).
- Crop typology integration: per-crop interpolation surfaces multiplied by crop-area per 1 km cell; aggregated to a total fertiliser application per cell.
- Uncertainty calculation: U = (2 * sqrt(V) / P) × 100, where V is kriging variance and P is predicted rate; yields a percentage uncertainty, representing approximately 95.5% confidence limits.
- Output assembly: per-fertiliser maps of prediction (kg/km^2) and 2-band TIFFs (prediction + uncertainty).

## Data structure
- File format: two-band raster TIFFs at 1 km resolution for each fertiliser, covering all of England.
- File names:
  - fertiliser_n_prediction_uncertainty
  - fertiliser_k_prediction_uncertainty
  - fertiliser_p_prediction_uncertainty
- Band 1: Predicted average annual fertiliser application rate (kg/km^2)
- Band 2: Uncertainty associated with predicted rates (%)

## Acknowledgements and provenance
- Funded by NERC national capability and the ASSIST programme (NE/N018125/1) with CEH and partner institutions.
- BSFP data provided by Defra; individuals acknowledged for data access.