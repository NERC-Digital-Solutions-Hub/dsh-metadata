# GB_MarshExtentChange_Layers_1846-2016

## Data overview
- ESRI shapefile layer named GB_MarshExtentChange_Layers_1846-2016 containing the areal extent of saltmarshes for 25 estuaries/embayments across 6 Great Britain regions (1846–2016), derived from maps and aerial photos.
- Marsh edges delineated in ArcGIS 10.6 at 1:7,500 with vertices placed every 5 m; RMSE terms quantify uncertainty from basemap, georeferencing, interpretation, and pre-digitisation distortions.
- Data recorded only where maps/imagery were available for the entire estuary/embayment.
- Used to analyze long-term, large-scale lateral saltmarsh change; associated with Ladd et al. (in press).

## Experimental design
- Change in marsh extent calculated for 25 estuaries/embayments in 6 GB regions at roughly 30-year intervals (1846–2016).
- Regions span western GB (Solway, Morecambe, Cardigan) and eastern/southern coasts (Wash, Essex-Kent, Solent).
- Post-1950 data gaps in Solent and Essex-Kent regions.

## Methods and data generation
- Primary data sources: Ordnance Survey maps and aerial photographs (Digitised via Digimap; Cardigan region used Royal Commission imagery).
- Timestamps and survey years recorded; pixel size ~0.25 m on field rasters for Cardigan.
- Marsh extent delineation, RMSE components, and 95% RMSE (RMSE_95) calculations described.
- Post-1950 marsh areal extent references for rate calculations sourced from additional studies (e.g., Bailey & Pearson; Cooper et al.).
- Predictor data assembled for later analysis (see Miscellaneous).

## Data structure
- Six GIS files total; the main shapefile is GB_MarshExtentChange_Layers_1846-2016.
- Attribute table includes 12 fields: Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year, RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95, Area_ha.
- Table 2 defines field descriptions/units (e.g., RMSE terms in meters, Area_ha in hectares).

## Quality control and validation
- Qualitative accuracy assessed by comparing the vectorised marsh layer with national marsh extent layers (Phelan et al. 2011; Haynes 2016).
- Literature reviews conducted to assess likelihood of observed changes and to identify potential map-surveyor errors.
- Supporting information available in Ladd et al. (in press) for transparency.

## Miscellaneous and related data
- Additional dataset: predictors of lateral marsh extent change (Table 3) and file GB_MarshChangePredictors_1967-2016.csv.
- Predictors include: latitude/longitude, LateralRateChange, RSLR, NetSedFlux, BedloadFlux, StormFreq, FloodFreq, MedianFetch, TidalRange.
- Rate calculations: linear marsh change (ha/yr) 1957–2016; post-1950 data used where available; Wash region treated with non-linear changes and segmented rates.
- Predictors validated by correlating UVVR (unvegetated/vegetated area ratio) with estuarine sediment concentration indicators.

## Access, licensing, and citation
- Data access URL: https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717
- Licence: Open Government Licence
- Required citation: Ladd, C.J.T.; Duggan-Edwards, M.F.; Bouma, T.J.; Pagès, J.F.; Skov, M.W. (2019). Change in saltmarsh extent for six regions across Great Britain (1846-2016). NERC Environmental Information Data Centre. (DOI provided in data entry)

## Practical notes for GIS specialists
- Use in ArcGIS-compatible workflows; data are in British National Grid projection; suitable for spatial analysis, time-series mapping, and uncertainty visualization using RMSE fields.
- RMSE_B, RMSE_G, RMSE_I, RMSE_M, and RMSE_95 provide edge-position uncertainty for error-aware mapping.
- The predictor dataset enables regression-based analyses of drivers of marsh change (e.g., UVVR-related sediment supply, fetch, wind/storm/flood metrics, and relative sea-level rise).
- When sharing or repurposing, cite the dataset and consider referencing the related Ladd et al. (in press) study for interpretation context.