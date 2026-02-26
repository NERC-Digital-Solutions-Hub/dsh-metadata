# Change in saltmarsh extent for six regions across Great Britain (1846-2016)

- Data availability and citation
  - Access: https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717
  - Licence: Open Government Licence
  - Citation should be: Ladd, C.J.T.; Duggan-Edwards, M.F.; Bouma, T.J.; Pagès, J.F.; Skov, M.W. (2019). Change in saltmarsh extent for six regions across Great Britain (1846-2016). NERC Environmental Information Data Centre. https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717

- Data overview
  - Dataset name: GB_MarshExtentChange_Layers_1846-2016
  - Content: ESRI shapefile layer depicting the areal extent of saltmarshes along 25 estuaries/embayments in 6 regions of Great Britain, across 1846–2016 (maps and aerial photographs)
  - Delineation: Marsh edges traced in ArcGIS 10.6 at 1:7,500 by placing vertices every 5 m
  - Uncertainty: RMSE components include basemap georeferencing, georeferencing procedure, interpreter digitising, and pre-digitisation map/photo distortions
  - Coverage caveat: Marsh extent measures were recorded only where maps/aerial photographs covered the entire estuary/embayment
  - Context: Part of a study on long-term lateral saltmarsh change; used in Ladd et al. (in press)
  - Data creators: C.J.T. Ladd and M.F. Duggan-Edwards (processing)

- Experimental design
  - Spatial scope: 25 estuaries/embayments across 6 GB regions (Solway, Morecambe, Cardigan, Wash, Essex-Kent, Solent)
  - Temporal resolution: Approximately every 30 years from 1846 to 2016
  - Regional notes: Western GB (Solway, Morecambe, Cardigan) along the Irish Sea; eastern/southeastern GB (Wash, Essex-Kent, Solent) along the North Sea and English Channel
  - Data gaps: Post-1950 aerial photographs not available for Solent and Essex-Kent regions

- Methods and data sources
  - Primary sources: Ordnance Survey maps and aerial photographs
  - Access to sources: OS maps via EDINA Digimap; survey dates used as timestamps; Cardigan aerials from the Royal Commission on Ancient Historical Monuments Wales
  - Digitisation: Marsh extent delineated in ArcGIS 10.6 at 1:7,500 with 5 m vertices; pixel field details ~0.25 × 0.25 m for Cardigan
  - Quality assessment: RMSE per marsh complex calculated from basemap inaccuracies, georeferencing, interpreter digitising, and pre-digitisation distortions
  - Regional listings: Table 1 provides study region and estuary names with geographic coordinates

- Data structure
  - Files: 6 GIS files, including 1 shapefile named GB_MarshExtentChange_Layers_1846-2016
  - Attribute table fields (12): Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year, RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95, Area_ha
  - Value descriptions and units are provided in Table 2 (e.g., RMSE components in meters, Area_ha in hectares)

- Quality control
  - Vector layer validation: Compared the most recent digitised marsh extent against national marsh extent layers (Phelan et al. 2011; Haynes 2016) to check general agreement
  - Literature validation: Additional literature searches to assess reliability of observed marsh change and to identify potential artefacts from map surveyors

- Miscellaneous: predictors of saltmarsh extent change (Table 3 and related data)
  - Supporting predictors dataset: GB_MarshChangePredictors_1967-2016.csv
  - Purpose: Used in Ladd et al. (in press) to analyse drivers of lateral marsh change
  - Contents: Rates of lateral marsh expansion/erosion and predictor variables for 25 estuaries/embayments across 6 regions (1967–2016)
  - Rate calculations: Linear rates of marsh change (ha/yr) between 1957 and 2016 derived from GB_MarshExtentChange_Layers_1846-2016; post-1950 data for Solent and Essex-Kent drawn from other sources
  - Predictors included (Table 4):
    - Latitude, Longitude
    - LateralRateChange (ha/yr)
    - Relative Sea Level Rise (RSLR, mm/yr)
    - NetSedFlux (m3/yr per unit marsh area)
    - BedloadFlux (kg/m2/yr; direction of sediment movement)
    - StormFreq (n/yr)
    - FloodFreq (n/yr)
    - MedianFetch (km)
    - TidalRange (m)
  - Data processing and quality checks: Wind-speed data quality-controlled; UVVR (unvegetated/vegetated area ratio) used as a proxy for sediment supply; UVVR validated against SSC (suspended sediment concentration) data

- References and context
  - Foundational sources and related datasets for validation and methodology, including:
    - Phelan et al. (2011); Haynes (2016) national marsh extent layers
    - HR Wallingford (sediment transport studies)
    - Ladd et al. (in press) on sediment supply and saltmarsh dynamics
    - Related methodological papers on fetch, wind and storm data, tidal ranges, and sediment flux proxies

- Summary for monitoring use
  - Provides a long-term, geo-spatially explicit record of saltmarsh extent change across six regions of Great Britain with quantified uncertainties
  - Enables analysis of decadal to multi-decadal trends and their potential drivers (sediment supply, hydrology, storm/tide regimes)
  - Includes predictors and a derived dataset to support exploratory and hypothesis-driven monitoring of marsh dynamics and coastal resilience
  - Suitable for integration into environmental health assessments, coastal policy evaluation, and scenario planning where standardized, quality-controlled marsh extent data are needed over time