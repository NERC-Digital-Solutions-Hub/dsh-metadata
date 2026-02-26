# Details of data-structure

- 12 tiff-file raster layers (with world-files) containing Mean, Median, and Standard Error of Mean (SEM) of Ecosystem Service model ensembles for:
  - Stored Carbon
  - Grazing use
  - Non-Timber Forest Product: Firewood and Charcoal
  - Outputs are normalised
- Two shapefiles with Mean, Median, and SEM Ecosystem Service model ensembles for water supply in catchments delineated for weirs stored at:
  - South Africa, Department of Water and Sanitation (DWS)
  - Global Runoff Data Centre (GRDC)
  - Layers are separated due to overlapping polygons
- One shapefile layer with Mean, Median, and SEM Ecosystem Service model ensembles for per-country water use per capita
- Spatial grid and units:
  - Raster grid: 1000 m x 1000 m, 1-band, 32-bit floating point
  - Projection: WGS-1984 Lambert with Azimuthal Equal Area (EPSG 9820); units in metres; central meridian 20°E, latitude 5°N
- Area covered:
  - All continental Africa (36 countries) including Madagascar; islands and non-contiguous areas omitted
  - Catchments crossing country boundaries may extend outside the continental area
- Data values:
  - Relative Service delivery, 0–1 scale
  - No Data value: -999 (outside area or LCM mask)

## Origin of model outputs

- Derived from the WISER project “Which Ecosystem Service Models Best Capture the Needs of the Rural Poor?” (NE/L001322/1), ESPA funding
- Willcock et al. (2019) continental-scale validation of ecosystem service models used to calibrate/validate six services across six modelling frameworks:
  - Services: Stored carbon; Available water supply; Water use (including beneficiaries); Firewood; Charcoal; Grazing
  - Frameworks: InVEST; Co$ting Nature; WaterWorld; Benefits transfer (Costanza-based); LPJ-GUESS; Scholes models
- Methodological notes:
  - Service values defined per hectare (water per catchment hectare)
  - Bespoke developments for carbon, grazing, firewood, charcoal
  - Relative rural population density used to translate model outputs to beneficiaries
  - Land cover masks (LCM) define where services apply (e.g., forest for carbon, woodland for firewood/charcoal, grassland/savanna for grazing)
  - Log10 transformation applied to all values except stored carbon; then 0–1 normalisation using the 95th percentile (winsorising) to reduce impact of extreme values
  - Details on model approaches and validation available in Willcock et al. (2019) Supplementary Information
  - Original model outputs cannot be published in full due to rights held by project partners

## Analytical methods for Ensemble Models

- Ensembles combine normalised outputs from Willcock et al. (2019) per Ecosystem Service
- Metrics:
  - Mean (Emn) across available models for each 1 km² grid cell
  - Median (Emd) across available models for each grid cell
  - Standard Error of the Mean (SEMx) per grid cell
- Coverage rules:
  - Only grid cells with at least 3 models providing valid values are included; others are No Data (-999)
  - Grids and polygons are treated consistently, with alignment to a standard area
- Processing workflow:
  - Clip Willcock et al. layers to the standard area; homogenise extent
  - Export to ASCII, read into Matlab for mean/median/SEM calculations
  - Re-normalise mean/median to 0–1 scale using the same method as above
  - Outputs re-exported to ArcGIS and saved as TIFFs
  - Code for ensemble generation available at: https://github.com/dhooftman72/ES_Ensembles

## Modelling frameworks included (per service)

- Available water supply: 6 frameworks (InVEST, Co$ting Nature†, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes Growth days)
- Water usage: 6 frameworks (InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes Growth days)
- Stored carbon: 4 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS)
- Non-Timber Forest Product – Firewood: 5 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes firewood)
- Non-Timber Forest Product – Charcoal: 4 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS)
- Grazing: 6 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes globally, Scholes locally parameterised)
- Notes:
  - Some outputs (Co$ting Nature) are not publicly available
  - Scholes models include both global and local parameterisations
  - Some frameworks are based on carbon outputs or specific biophysical models

## Data processing and provenance

- Raster and polygon layers are standardized to a single extent and grid, ensuring consistent dimensions
- Mean and Median ensembles are re-normalised to the 0–1 scale in the same manner as the underlying data
- All processing steps and code are documented and made available (GitHub) to facilitate reproducibility
- Results are exported back to GIS format for mapping and further analysis

## Usage, interpretation, and potential applications

- Ensembles provide relative, comparable levels of service across Africa
- Useful for optimization, prioritisation, and targeting of conservation or development interventions
- Serves to integrate differences among multiple models, reducing reliance on a single framework

## Limitations and caveats

- Not all models cover the entire study area; a minimum of 3 models is required per cell to compute ensembles
- Some outputs are restricted by data rights or not publicly available
- Masking and administrative boundaries can limit spatial completeness; some areas may be No Data
- Scale differences: raster cells are uniform (1 km²) while catchments and country polygons vary in size

## Funding

- WISER project: Which Ecosystem Service Models Best Capture the Needs of the Rural Poor? (NE/L001322/1)
- ESPA funding (UK Ecosystem Services for Poverty Alleviation)
- EnsemblES project: Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models (NE/T00391X/1)

## References used

- Araújo, M.B., New, M. (2007). Ensemble forecasting of species distributions. Trends Ecol. Evol.
- Costanza, R. et al. (2014). Changes in the global value of ecosystem services. Global Environmental Change.
- Kareiva, P.M. (2011). Natural capital: mapping ecosystem services. Oxford University Press.
- Marmion, M. et al. (2009). Evaluation of consensus methods in predictive species distribution modelling. Divers. Distrib.
- McKenzie, E. et al. (2012). InVEST guidance and case studies.
- Mulligan, M. (2013, 2015). WaterWorld; trading off agriculture with nature’s benefits.
- Scholes, R.J. (1998). Grazing potential mapping (CSIR).
- Smith, B. et al. (2001, 2014). Vegetation dynamics and N cycling in models.
- Verhagen, W. et al. (2017). Using ecosystem service demand to identify priority areas.
- Willcock, S. et al. (2019). A Continental-Scale Validation of Ecosystem Service Models. Ecosystems.