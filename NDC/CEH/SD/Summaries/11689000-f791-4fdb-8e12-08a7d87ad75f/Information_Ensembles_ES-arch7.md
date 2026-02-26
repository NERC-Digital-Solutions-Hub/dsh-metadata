# Details of data-structure

- 12 TIFF raster layers (with world-files) representing Mean, Median, and Standard Error of Mean (SEM) for ensemble outputs of Ecosystem Service models across Stored Carbon, Grazing use, and Non-Timber Forest Products (Firewood and Charcoal); outputs are normalised.
- Two shapefiles for water supply ensembles (Mean, Median, SEM) for catchments with weirs, delineated by:
  - South Africa Department of Water and Sanitation (DWS)
  - Global Runoff Data Centre (GRDC)
  - Overlapping polygons separate layers by delineation origin.
- One shapefile for per-country water use per capita ensembles (Mean, Median, SEM).

- Grid and resolution:
  - Raster grid: 1000 m × 1000 m (1 km² cells), 1-band, 32-bit floating point.
  - Area of interest: continental Africa (36 countries, primarily Sub-Saharan), including Madagascar; excludes islands not connected to the continent; catchments crossing outside this area may be partially included.

- Projection and units:
  - Projection: WGS-1984 Lambert with Azimuthal Equal Area (EPSG 9820).
  - Units: metres; all inputs projected to this CRS prior to calculations.
  - Area-coverage units: Relative Service delivery, normalised to 0–1.
  - No Data value: -999 (outside area or LCM mask per service).

- Origin and data lineage:
  - Original model outputs come from the WISER project (NE/L001322/1) under ESPA funding.
  - Validation and model descriptions in Willcock et al. 2019 (Ecosystems 22:1902-1917); six ecosystem services considered and six modelling frameworks used (InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes models).

- Normalisation and transformation:
  - Value transformations include log10 for most services (except Stored Carbon).
  - Values are normalised to 0–1 using the 95th percentile to reduce effects of extreme values (winsorising).
  - These normalisations enable cross-model comparability across different units and scales.

- Ensemble construction (Analytical methods):
  - Ensembles per ecosystem service combine outputs from multiple models to produce:
    - Emn(x): mean across available models for grid-cell x
    - Emd(x): median across available models for grid-cell x
    - SEMx: standard error of the mean across models for grid-cell x
  - Model availability per grid-cell is tracked; only grid-cells with at least 3 models are used; others are set to No Data (-999).
  - Large-scale rasters and polygons are clipped to a standard area shape, re-sampled to ensure identical dimensions, and processed in ArcGIS 10.x and MATLAB.
  - Mean and Median ensembles are re-normalised to 0–1 after calculation.
  - Code and workflow are available at https://github.com/dhooftman72/ES_Ensembles.

- Model frameworks included (per service):
  - Available water supply: InVEST, Co$ting Nature (not publicly available), WaterWorld, Benefits transfer, LPJ-GUESS, Scholes Growth days model (note some outputs restricted by rights).
  - Water usage: InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes Growth days model.
  - Stored carbon: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS.
  - Non-Timber Forest Product – Firewood: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes firewood model.
  - Non-Timber Forest Product – Charcoal: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS.
  - Grazing: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes (global and local parametrised models).

- Processing workflow:
  - Central workflow involved clipping to standard area, exporting to ASCII, importing into MATLAB for mean/median/SEM calculations, re-normalising, and exporting back to ArcGIS as TIFFs.
  - All results are presented as 0–1 relative service delivery and are available as rasters (1 km²) and polygons (catchments / countries).

- Data packaging and limitations:
  - Not all models cover the entire study area; a minimum of 3 model outputs required per cell; otherwise No Data.
  - Underlying model outputs cannot be published publicly; rights belong to project partners/third parties.
  - Some model outputs (e.g., from Co$ting Nature) are not publicly available.

- Funding Information
  - WISER project (ESPA, NE/L001322/1) and EnsemblES project (NE/T00391X/1) funded the work.

- References used (selected)
  - Willcock et al. 2019: continental-scale validation of ecosystem service models.
  - Araújo & New (ensemble forecasting), Costanza et al. (changes in global value of ecosystem services), and related methodological sources on ensemble approaches and ecosystem service modelling frameworks.