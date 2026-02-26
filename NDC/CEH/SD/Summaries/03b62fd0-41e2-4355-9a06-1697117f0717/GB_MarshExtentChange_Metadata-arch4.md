# Change in saltmarsh extent for six regions across Great Britain (1846-2016)

## Data availability and citation
- Data access: GB_MarshExtentChange_Layers_1846-2016 dataset and related materials available at the provided DOI and data portal.
- License: Open Government Licence.
- Citation: Ladd, C.J.T.; Duggan-Edwards, M.F.; Bouma, T.J.; Pagès, J.F.; Skov, M.W. (2019). Change in saltmarsh extent for six regions across Great Britain (1846-2016). NERC Environmental Information Data Centre. https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717

## Data overview
- Dataset: ESRI shapefile layer GB_MarshExtentChange_Layers_1846-2016 containing areal extent of saltmarshes for 25 estuaries/embayments across 6 regions of Great Britain, mapped 1846–2016.
- Delineation method: Marsh edges digitized in ArcGIS 10.6 at 1:7,500 scale with vertices every 5 m.
- Accuracy considerations: RMSE components from basemap georeferencing, georeferencing procedure, interpreter digitizing, and pre-digitisation distortions; RMSE estimates provided per marsh complex.
- Coverage: Marsh extent recorded only where maps/air photos were available for the entire estuary/embayment.
- Purpose: Data collected for examining long-term, large-scale lateral saltmarsh change; used in Ladd et al. (in press).
- Lead data collection: C.J.T. Ladd and M.F. Duggan-Edwards.

## Experimental design
- Spatial scope: 25 estuaries/embayments in 6 Great Britain regions.
- Temporal scope: Approximately every 30 years between 1846 and 2016.
- Regional distribution: Western GB (Solway, Morecambe, Cardigan) and eastern/southeastern GB (Wash, Essex-Kent, Solent regions).
- Post-1950 data caveat: No aerial photograph data for Solent and Essex-Kent post-1950.

## Methods
- Data sources: Ordnance Survey maps and aerial photographs; timestamps from Oliver (2013); Cardigan regional data from Welsh monuments archives.
- Digitization workflow: Aerial photographs scanned and georeferenced to OS rasters; marsh edges digitized at 1:7,500 with 5 m vertex spacing.
- Georeferencing accuracy: RMSE estimates account for basemap displacement, georeferencing distortions, interpreter variability, and historical map/photo distortions.
- Software and scale: ArcGIS 10.6; 1:7,500 map scale; field pixel size ≈ 0.25 × 0.25 m.
- Data processing: Marsh extent calculations and RMSE per marsh complex; timestamps tied to survey events.

## Data structure
- Files: 6 GIS files, including 1 shapefile named GB_MarshExtentChange_Layers_1846-2016.
- Attribute fields (12): Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year, RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95, Area_ha.
- Value descriptors: Each field has defined meanings (region and estuary names, marsh identifier, data edition source, survey and publication years, multiple RMSE components, and marsh area in hectares).

## Quality control
- Qualitative accuracy check: Recent vector layer compared with national marsh extent layers to ensure general agreement.
- Literature validation: Additional checks to assess whether observed changes are reliable or explainable by mapping/surveyor error.
- Supporting information: Detailed literature search and QA discussions available in Ladd et al. (in press).

## Miscellaneous
- Predictors of lateral marsh change: Table 3 and a companion file GB_MarshChangePredictors_1967-2016.csv provide predictor data used in related analyses.
- Predictor data authorship: Ladd et al. compiled and processed predictor data.
- Additional data sources: Post-1950 area data for some regions drawn from Baily & Pearson (2007) and Cooper et al. (2001) for rate calculations.
- Sediment and environmental proxies: UVVR (unvegetated/vegetated area ratio) used as a proxy for external sediment supply; cross-validated with SSC (suspended sediment concentration).

## Predictors (Table 3 and Table 4)
- Predictor variables include:
  - Latitude, Longitude (locations of estuaries)
  - LateralRateChange (ha/yr)
  - RSLR (mm/yr; relative sea level rise)
  - NetSedFlux (m3/yr)
  - BedloadFlux (kg/m2/yr)
  - StormFreq and FloodFreq (n/yr)
  - MedianFetch (km)
  - TidalRange (m)
- Notes: Details and units provided for each predictor; some regions have NA values where data are unavailable.

## References
- Key sources for data, methods, and validation cited, including works on saltmarsh mapping, sediment transport, sea-level rise, wind/fetch models, and prior national/regional marsh datasets.