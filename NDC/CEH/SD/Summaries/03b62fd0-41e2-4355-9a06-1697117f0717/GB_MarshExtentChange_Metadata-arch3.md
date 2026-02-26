# Change in saltmarsh extent for six regions across Great Britain (1846-2016)

- Purpose: Document and provide data on long-term lateral changes in saltmarsh extent across six regions of Great Britain, derived from historical maps and aerial photographs to analyze large-scale, multi-decadal trends and their drivers.

## Data availability and licensing

- Data location: Data available at https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717
- Licence: Open Government Licence
- Citation requirement: Ladd, C.J.T.; Duggan-Edwards, M.F.; Bouma, T.J.; Pagès, J.F.; Skov, M.W. (2019). Change in saltmarsh extent for six regions across Great Britain (1846-2016). NERC Environmental Information Data Centre. https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717

## Data overview

- Dataset name: GB_MarshExtentChange_Layers_1846-2016
- Content: ESRI shapefile layer containing the areal extent of saltmarshes along 25 estuaries/embayments in 6 regions across Great Britain, digitised from maps and aerial photographs between 1846 and 2016.
- Digitisation details: Marsh edges delineated in ArcGIS 10.6 (1:7,500) with vertices every 5 m; potential errors from basemap georeferencing, georeferencing, digitising, and pre-digitisation map/photo distortions; RMSE calculated for each marsh complex.
- Coverage: Entire estuary/embayment required for a marsh extent record; used to analyse long-term lateral marsh change.
- Temporal design: Change in marsh extent calculated for all 25 estuaries approximately every 30 years between 1846 and 2016. Post-1950 data for Solent and Essex-Kent from prior studies used for rate calculations.
- Data provenance: Collected by C.J.T. Ladd and M.F. Duggan-Edwards; includes maps and aerial photographs from various sources.

## Experimental design

- Spatial scope: 6 regions across Great Britain (Solway, Morecambe, Cardigan, Wash, Essex-Kent, Solent) encompassing 25 estuaries/embayments.
- Temporal scope: Approximately every 30 years from 1846 to 2016; some post-1950 data rely on earlier studies for completeness in specific regions.
- Regional layout: Western GB estuaries along the Irish Sea (Solway, Morecambe, Cardigan) and eastern/southern GB coastlines along the North Sea/English Channel (Wash, Essex-Kent, Solent).

## Methods

- Data sources: Ordnance Survey maps and aerial photographs; dates treated as timestamps.
- Digitisation procedure: Marsh extent delineated at 1:7,500 scale by placing vertices every 5 m along marsh edges; Cardigan region included aerial photographs scanned and georeferenced to OS rasters.
- Accuracy assessment: RMSE components considered:
  - Basemap displacement (RMSE_B)
  - Map/photo distortions (RMSE_G)
  - Interpreter digitising error (RMSE_I)
  - Cartographic presentation errors (RMSE_M)
  - 95th percentile RMSE (RMSE_95)
- Data structure: Six GIS files with a main shapefile GB_MarshExtentChange_Layers_1846-2016; attributes include Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year, RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95, Area_ha.
- Supplementary data: Predictors of marsh extent change available in Table 3 and in GB_MarshChangePredictors_1967-2016.csv; used for analyses in Ladd et al. (in press).

## Data content and variable descriptions

- Table 2 (dataset fields): 
  - Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year
  - RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95
  - Area_ha
- Table 3 (predictors of marsh extent change): for each estuary, includes Latitude, Longitude, LateralRateChange (ha/yr), RSLR (mm/yr), NetSedFlux (m3/yr), BedloadFlux (kg/m2/yr), StormFreq (n/yr), FloodFreq (n/yr), MedianFetch (km), TidalRange (m)
- Table 4 (predictors description and units): clarifies each variable’s meaning and units

## Quality control and validation

- Vector layer accuracy check: Compared the most recent digitised marsh extent against national marsh extent layers to assess general agreement.
- Literature verification: Conducted literature searches to evaluate observed marsh changes and rule out artefacts from surveying; supporting information in Ladd et al. (in press) documents the literature review.

## Miscellaneous and additional analyses

- Predictors dataset: Additional predictors of lateral marsh change (Table 3) and the supplementary predictors file (GB_MarshChangePredictors_1967-2016.csv) were used to analyse drivers of marsh extent change.
- Sediment supply proxy: Net sediment flux per unit marsh area (derived from UVVR, vegetation vs. unvegetated areas) used as a proxy for external sediment supply; its validity supported by significant positive correlation with suspended sediment concentration (SSC).
- Rate computations: Linear rate of marsh change (ha/yr) calculated for 1957-2016; in some regions post-1950 area data sourced from prior studies to enable rate calculation.

## References and related resources

- Foundational data and regional studies cited, including works by Baily & Pearson (2007), Brown & Davies (2010), Cooper et al. (2001), Ganju et al. (2017), Halcrow (2010), Haynes (2016), HR Wallingford (2002), Manning & Whitehouse (2012), NFDC (2017), Oliver (2013), Phelan et al. (2011), Rohweder et al. (2012), Watson et al. (2015), Wernette et al. (2017), and Ladd et al. (in press).