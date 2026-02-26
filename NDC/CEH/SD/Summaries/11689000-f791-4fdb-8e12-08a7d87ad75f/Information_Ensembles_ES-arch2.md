# Ensemble Models of Ecosystem Services for Sub-Saharan Africa

- Purpose: Present ensemble ecosystem service (ES) outputs by integrating multiple modelling frameworks to enable monitoring of environmental health and policy performance over time in Africa.

## Details of data-structure

- Data comprise:
  - 12 TIFF raster layers (Mean, Median, SEM) of ES model ensembles for Stored Carbon, Grazing use, and Non-Timber Forest Products (Firewood and Charcoal) with normalised outputs.
  - Two shapefile layers for water supply ensembles in catchments delineated for weirs, sourced from:
    - South Africa Department of Water and Sanitation (DWS)
    - Global Runoff Data Centre (GRDC)
  - One shapefile layer for per-country water use per capita ensembles.
- Grid and projection:
  - Raster grid: 1000 m x 1000 m, 1-band, 32-bit floating point.
  - Projection: WGS-84 with an azimuthal equal-area (EPSG 9820), central meridian 20°E, latitude 5°N.
- Coverage and units:
  - Area: All continental Africa (36 countries, Sub-Saharan majority); offshore areas and non-contiguous regions excluded.
  - Units: Relative service delivery, 0–1 scale (normalised); No Data value: -999.
- Origin of delineation:
  - Separate layers due to overlapping polygons by origin of delineation.
- Naming conventions:
  - Rasters: <Ensemble_type_Service>
  - Shapefiles: <Ensembles_delineation_source>

## Origin of individual model outputs (Willcock et al. 2019)

- Source project: WISER—Which Ecosystem Service Models Best Capture the Needs of the Rural Poor? (NE/L001322/1), funded by ESPA.
- Validation basis: Willcock et al. 2019 provides continental-scale validation of ES models for six services.
- Services covered:
  - Stored carbon, Available water supply, Water use (including beneficiaries), Firewood (including beneficiaries), Charcoal (including beneficiaries), Grazing (including beneficiaries).
- Modelling frameworks included (per service; note varying coverage):
  - InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes models (multiple grazing and rainfall surplus models).
- Key modelling points:
  - Service delivery per hectare (water per catchment hectare).
  - Bespoke carbon-based developments for grazing and NTFP (firewood/charcoal).
  - Use of population density to translate supply to beneficiaries.
  - Masking: LCM-based masks define service occurrence (e.g., forested, wooded, grassland) with zeros outside masks.
  - Data transformation: log10 for all values except stored carbon; then 0–1 normalisation using 95th percentile (winsorising) to reduce outlier effects.
- Data rights: Individual model outputs remain with project partners/third parties and are not published.

## Analytical methods for generating Ensemble Models

- Ensemble construction:
  - Combines available normalised model outputs per ES, producing mean (Emn) and median (Emd) ensembles per 1 km2 grid cell, catchment, or country polygon.
  - Standard Error of the Mean (SEM) computed to reflect inter-model uncertainty.
- Calculation details:
  - Emn(x) = mean of all models i for grid-cell x.
  - Emd(x) = median of all models i for grid-cell x.
  - SEMx = standard deviation of model values at x divided by sqrt(n), where n is the number of valid models.
- Data validity requirements:
  - An ensemble is computed only for grid cells with at least 3 valid model estimates; otherwise No Data (-999).
- Processing workflow:
  - All Willcock et al. (2019) rasters clipped to a standard area, aligned to identical grid/extent.
  - Exported as ASCII, processed in MATLAB to generate mean, median, and SEM matrices.
  - Re-normalised to a 0–1 scale; results re-drawn in ArcGIS and exported as TIFFs.
  - Code for ensemble generation available at GitHub: dhooftman72/ES_Ensembles.
- Frameworks per service (illustrative; not all models cover entire area):
  - Available water supply: InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes Growth days model.
  - Water use: InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes Growth days model.
  - Stored carbon: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS.
  - Firewood: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes firewood model.
  - Charcoal: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS.
  - Grazing: InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes models.
- Outputs:
  - Ensemble layers (mean, median) and SEM per ES, mapped to 1 km2 cells, catchments, or countries.
- Accessibility and storage:
  - Raster and shapefile layers prepared for GIS use; underlying inputs and outputs stored in project portals as appropriate.

## Funding Information

- Supported by:
  - WISER project (ESPA) – NE/L001322/1
  - EnsemblES project – NE/T00391X/1

## References Used

- Key foundational works on ensemble forecasting and ES modelling, including:
  - Araújo & New (2007)
  - Costanza et al. (2014)
  - Kareiva (2011)
  - Marmion et al. (2009)
  - McKenzie et al. (2012)
  - Mulligan (2013, 2015)
  - Mulligan et al. (2010)
  - Scholes (1998)
  - Smith et al. (2001, 2014)
  - Verhagen et al. (2017)
  - Willcock et al. (2019) – continental-scale validation of ES models

## Practical Implications for Analysts Monitoring the Environment

- Data products enable spatial comparison and prioritisation of ES across Africa, supporting policy and management decisions.
- Ensemble approach helps mitigate model-specific biases by combining multiple frameworks and reporting uncertainty via SEM.
- Normalisation to a common 0–1 scale and requirement of multiple model supports robust cross-service comparability.
- Availability constraints: not all models cover the entire study area; plan analyses around cells with sufficient model coverage (≥3 models).
- Data integration potential: opportunities to combine with other environmental datasets for enhanced monitoring and decision-making.
- Data governance note: some underlying model outputs are not publicly published; ensure proper data access permissions and refer to project portals for data availability.