# Ensembles of Ecosystem Service Models for Sub-Saharan Africa

- Overview: A descriptive data package detailing ensemble ecosystem service models across continental Sub-Saharan Africa, including carbon storage, grazing, non-timber forest products (firewood and charcoal), and water-related services (available water supply and per-capita water use). The data are prepared for cross-model comparison and potential prioritisation of areas for policy or management actions.

## Data structure and formats

- Raster data
  - 12 TIFF rasters (1,000 m x 1,000 m grid, 1-band, 32-bit float) with mean, median, and standard error of the mean (SEM) for ensemble outputs.
  - Services covered: Stored Carbon, Grazing, Firewood, Charcoal, Available Water Supply (per catchment), and water use (per capita per country).
- Vector data
  - Three shapefiles (mean, median, SEM) for:
    - Water supply in delineated catchments (weirs) from two delineation origins:
      - South Africa Department of Water and Sanitation (DWS)
      - Global Runoff Data Centre (GRDC)
    - Per-country water use per capita
- Grid and projection
  - Grid: 1,000 m x 1,000 m
  - Projection: WGS-1984 Lambert Azimuthal Equal Area (EPSG 9820); units in metres; central meridian 20°E, latitude 5°N
- Area and coverage
  - All continental territory of 36 African countries (primarily Sub-Saharan), including Madagascar; offshore/island areas not connected to the continent are omitted
  - Catchments crossing outside the continental area may be partially represented
- Data values
  - Relative service delivery values normalised to 0–1
  - No Data value: -999 (outside area or outside land cover mask per service)

## Data provenance and origin

- Origin: Derived from the multi-partner WISER project (Which Ecosystem Service Models Best Capture the Needs of the Rural Poor?), with funding from ESPA.
- Ecosystem services validated in Willcock et al. 2019:
  - Stored carbon, Available water supply, Water use (including beneficiaries), Firewood (including beneficiaries), Charcoal (including beneficiaries), Grazing (including beneficiaries)
- Modelling frameworks used (per service):
  - InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes models (with variations for some services)
  - Some outputs are not publicly available and rights belong to project partners or third parties
- Data transformation and normalisation
  - Values transformed with log10 (except stored carbon)
  - Normalised to 0–1 using 95th percentile (winsorisation) to reduce effects of extreme values
  - Ensemble surfaces (mean and median) are renormalised to 0–1

## Ensemble construction and analytics

- Ensemble definitions (per grid cell or polygon)
  - Emn(x): Mean of all available models for a grid cell x
  - Emd(x): Median of all available models for a grid cell x
  - SEMx: Standard Error of the Mean across available models for grid cell x
- Model coverage and data inclusion
  - Not all models cover the entire study area; calculations use only grid cells with at least 3 valid model estimates
  - Cells with fewer than 3 models are set to No Data (-999)
- Data processing workflow
  - All Willcock et al. (2019) layers clipped to a standard area shape
  - Data converted to ASCII, imported into Matlab for mean/median/SEM calculations
  - Results re-exported to ArcGIS and as TIFFs
  - Reproducible workflow available at GitHub: dhooftman72/ES_Ensembles
- Practical applications
  - The ensembles provide relative service levels across the area and can inform optimization or prioritisation of sensitive areas
  - Useful for cross-model comparisons and assessing uncertainty through SEM

## Data access, governance, and limitations

- Data accessibility
  - Raster and vector layers are prepared for GIS use (ArcGIS) and can be reinterpreted in standard ETL workflows
  - ASCII grid data and Matlab-based processing support reproducibility
- Rights and publication notes
  - Individual model outputs cannot be published publicly; rights held by project partners and/or third parties
  - Ensemble outputs are intended for internal analysis, policy support, and planning, with proper attribution
- Data coverage and quality considerations for Data Leaders
  - Coverage varies by service and model; a minimum of 3 model estimates per cell is required
  - Some modelling outputs are not publicly available; cross-model comparability relies on normalisation and consistent processing
  - Spatial extent is continental Africa with specific catchment delineations; edge areas may have data gaps
- Metadata and discoverability
  - Detailed descriptions of each service and modelling framework are provided, along with methodological references
  - Code and methods are documented and publicly linked for reproducibility and auditing

## Funding and references

- Funding
  - ESPA (Environmental Services for Poverty Alleviation) programme
  - EnsemblES project (Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models)
- Key references
  - Willcock et al. 2019: Continental-scale validation of ecosystem service models
  - Foundational works on ensemble forecasting, ecosystem service valuation, and modeling frameworks (Costanza, Kareiva, Marmion, Mulligan, Scholes, Smith et al., Verhagen et al., etc.)

## Implications for data strategy and governance

- Aligns with Data Leader aims to understand the data system, assess user needs, and manage data assets with attention to quality, metadata, and discoverability.
- Demonstrates a multi-model, ensemble-based approach to estimate ecosystem services, with emphasis on standardisation, transparency, and reproducibility.
- Highlights governance considerations around data access rights, model provenance, and the balance between public dissemination and partner-controlled outputs.
- Provides a structured, scalable model for assembling and comparing complex data assets across partners and networks, potentially informing policy, planning, and collaborative data practices.