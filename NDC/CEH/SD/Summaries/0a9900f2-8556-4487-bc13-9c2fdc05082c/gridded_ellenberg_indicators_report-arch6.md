# Dataset Documentation for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain 1990 and 2015-2019

- The maps provide integrated gridded estimates of Ellenberg N (nutrient), R (pH), F (moisture), and L (light) indicators for Great Britain.
- Time periods: 1990 (CS data only) and 2015-2019 (integrated from CS, LTMN, NPMS).
- Purpose: produce consistent spatial patterns by combining three vegetation-dataset sources to enable broad-scale analysis and data-driven conservation/restoration work.

Background and rationale
- Datasets combined:
  - Countryside Survey (CS)
  - Natural England Long Term Monitoring Network (LTMN)
  - National Plant Monitoring Scheme (NPMS)
- Goal: generate a representative GB-wide map of Ellenberg indicators by leveraging all available data, while allowing for uneven/spatially biased coverage across schemes.
- Indicators: Ellenberg N, R, F, L (dominant environmental gradients: nutrients, acidity, moisture, light).
- Output: 1) integrated maps for 2015-2019; 2) comparison maps for 1990 using CS data only.
- Accessibility: data available under Open Government Licence; notes on data sources, processing, and citations.

Data collation and processing
- Time periods and plots:
  - 2015-2019: 2,375 unique plots (CS: 445, LTMN: 1,287, NPMS: 643)
  - 1990: 2,282 CS plots
- Plot types by scheme:
  - CS: 2m x 2m random X plots
  - LTMN: 2m x 2m square (VC) plots on a stratified grid
  - NPMS: 5m x 5m plots on grid intersections (Inventory surveys)
- Output variables per plot:
  - Calculated cover-weighted and non-cover weighted Ellenberg scores using vascular plants only
  - Domin scale conversion to standardize cover values; midpoints used for weighting
- Taxon matching: used vegtaxon R package to harmonize taxa across schemes
- Covariates considered:
  - Habitat (Biodiversity Action Plan Broad Habitat classifications)
  - Nitrogen and sulphur deposition (CBED model, 5km square means, preceding 10 years)
  - Climate: annual precipitation, max July temp, min January temp (HadUKGrid, mean over preceding 10 years, 1km squares)
- Data handling note: bryophyte indicators were not included due to inter-scheme recording differences

Modelling
- Model structure:
  - y_i j k l ~ covariates + (1 / scheme / site / plot) + s(East, North) + s(East, North, NPMS only)
  - Cubic regression splines for covariates; spatial smooth terms capture shared patterns; NPMS-specific spatial term accounts for uptake patterns
  - Random effects: α_i j k composed of intercept and random effects for scheme, site, and plot
- Data weighting and uptake:
  - Weights applied to observations to reflect dataset contribution (CS highest weight; LTMN and NPMS down-weighted)
  - NPMS uptake modeled explicitly with a NPMS-only spatial term (dummy variable in the model) to capture complex, dataset-specific spatial patterns
  - LTMN down-weighted due to non-representative GB coverage (primarily nature reserves)
- Practical notes:
  - Time-year effects within 2015-2019 treated as non-estimated; data treated as independent replicates within the period
  - Field protocol differences not explicitly adjusted beyond weighting and model structure

Predictions
- Spatial predictions:
  - 1 km grid cells across GB for both time periods
  - 2015-2019: using 2015 Land Cover Map (dominant target class)
  - 1990: using 1990 Land Cover Map
- Uncertainty:
  - Separate uncertainty (standard error) maps provided for each indicator
  - Higher uncertainty in northern Scotland; advise caution in these regions
- Output scale and use:
  - Broad-scale spatial patterns rather than local, site-specific guidance
  - Suitable for landscape-level planning and trend assessment

Quality control
- Model evaluation:
  - RMSE assessed primarily against CS data (highest weighting, representative GB coverage)
  - Overall RMSE: generally < 1 unit for the non-cover weighted indicators; cover-weighted indicators showed higher RMSE due to cross-dataset recording variation
- Recommendations:
  - Prefer non-cover weighted Ellenberg values for general use
  - Use accompanying uncertainty maps to assess reliability by region
- Limitations acknowledged:
  - Despite integration, residual differences across schemes may persist compared to a single high-coverage unbiased dataset
  - Plans to update maps as new data become available

Data structure
- File set:
  - Three time-period datasets per indicator, each with two bands:
    - [variable]_90.tif: 1990 mean in band 1, standard error in band 2
    - [variable]_15-19.tif: 2015-2019 mean in band 1, standard error in band 2
    - [variable]_difference.tif: Difference 2015-2019 minus 1990 in band 1, SE in band 2
- Variants:
  - _site: non-cover weighted indicator maps
  - _cwt: cover-weighted indicator maps
- Indicators:
  - EBERGN, EBERGR, EBERGF, EBERGL (for each of N, R, F, L)
- Total: 24 files

Calculation of change
- Change metric:
  - Change = predicted 2015-2019 value − predicted 1990 value
  - Uncertainty around change estimated as SE_change = sqrt(SE_1990^2 + SE_2015-2019^2)
  - Note: covariance not accounted for; change SE is a relative uncertainty indicator

Acknowledgements and data availability
- Acknowledgements to NPMS designers and contributors; NERC funding and UK-SCAPE support
- Data availability:
  - Open Government Licence
  - Citation required: Jarvis et al. (2022) Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain, 1990 and 2015-2019
  - Repository and scripts:
    - GitHub: T1.1-indicatormaps (scripts to replicate modelling process; access on request)
  - Input data sources publicly available; CS plot data available on request

Additional references
- References to underlying data sources (CS, LTMN, NPMS, Land Cover Maps, climate and deposition datasets) and methodological prior work are provided in the document.