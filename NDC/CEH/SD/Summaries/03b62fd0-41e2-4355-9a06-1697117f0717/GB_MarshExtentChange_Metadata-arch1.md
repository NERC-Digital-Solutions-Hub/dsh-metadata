# GB_MarshExtentChange_Layers_1846-2016

## Data availability and licensing
- Data can be accessed at: https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717
- Licence: Open Government Licence
- Citation to use: Ladd, C.J.T.; Duggan-Edwards, M.F.; Bouma, T.J.; Pagès, J.F.; Skov, M.W. (2019). Change in saltmarsh extent for six regions across Great Britain (1846-2016). NERC Environmental Information Data Centre. https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717

## Data overview
- Dataset: GB_MarshExtentChange_Layers_1846-2016 (ESRI shapefile layer)
- Spatial scope: 25 estuaries/embayments across 6 regions in Great Britain
- Temporal scope: 1846–2016 (approximately every 30 years)
- Delineation method: ArcGIS 10.6, scale 1:7,500; marsh edge vertices every 5 m
- Uncertainty sources (RMSE components): basemap georeferencing, georeferencing process, digitising interpreter, map/photo distortions
- Inclusion criterion: marsh extent recorded only where maps/aerials exist for the entire estuary/embayment
- Purpose: study large-scale, long-term lateral saltmarsh change; data underpin Ladd et al. (in press)
- Lead data collectors/processors: C.J.T. Ladd and M.F. Duggan-Edwards

## Experimental design
- 25 estuaries/embayments in 6 regions across GB
- Temporal cadence: ~1846, ~1870, ~1900, ~1930, ~1967, ~2016 (approximate)
- Regions by coast: western GB (Solway, Morecambe, Cardigan) and eastern/southern GB (Wash, Essex-Kent, Solent)
- Note: post-1950 marsh data gaps for Solent and Essex-Kent

## Methods
- Data sources: Ordnance Survey maps and aerial photographs
- Timestamps: survey dates from Oliver (2013)
- Cardigan region: aerial photos scanned and georeferenced to OS rasters
- Pixel resolution: ~0.25 m
- Marsh extent digitising: 1:7,500; 5 m edge vertices
- RMSE estimation: four sources of error (basemap displacement, georeferencing distortions, interpreter digitising, pre-digitisation map/photo distortions)
- Supporting data: Table 1 lists study regions/estuaries with coordinates

## Data structure
- File composition: 6 GIS files; 1 shapefile named GB_MarshExtentChange_Layers_1846-2016
- Attribute fields: Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year, RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95, Area_ha
- Field descriptions and units provided in Table 2 (e.g., RMSE components in meters; Area_ha in hectares)

## Quality control
- Qualitative accuracy check: digitised marsh extent compared with national marsh extent layers (Phelan et al. 2011; Haynes 2016)
- Literature verification: assessed reliability of observed marsh changes and potential map-surveyor errors
- Supporting materials: additional literature review in Ladd et al. (in press)

## Miscellaneous
- Predictors of marsh extent change: Table 3 and the file GB_MarshChangePredictors_1967-2016.csv
- Rate calculations: linear marsh-change rates (ha/yr) for 1957–2016; some regions use post-1950 data from other studies
- Environmental predictors included:
  - Flood and wind-storm event frequencies (Counts per year)
  - Relative sea level rise (RSLR) from tide gauges
  - Median wave fetch length
  - Net sediment flux per unit marsh area (derived from UVVR)
  - Bedload sediment flux (positive/negative indicating in/outflow)
- Validation: UVVR-derived net sediment flux correlates positively with estimated suspended sediment concentration (SSC)
- Data processing and quality checks described in relation to UK datasets and cited sources

## Predictors and data for modelling
- Predictors of lateral marsh change (per estuary): Latitude, Longitude; LateralRateChange (ha/yr); RSLR (mm/yr); NetSedFlux (m3/yr); BedloadFlux (kg/m2/yr); StormFreq (n/yr); FloodFreq (n/yr); MedianFetch (km); TidalRange (m)
- These predictors underpin analyses of drivers behind long-term marsh expansion or erosion across the six GB regions

## Use and limitations
- Suitable for analysing long-term spatial patterns of saltmarsh change and their predictors
- Limitations: incomplete post-1950 data in Solent and Essex-Kent; RMSE components quantify uncertainty; edge delineation at 1:7,500 scale; potential georeferencing and interpretation biases
- Data provenance and metadata are provided to enable reproducibility and data discovery

## References
- Ladd et al. (in press): Sediment supply explains long-term and large-scale patterns in saltmarsh lateral expansion and erosion (GRL)
- Supporting methodological and data references: Baily & Pearson (2007); Brown & Davies (2010); Cooper et al. (2001); Ganju et al. (2017); Halcrow (2010); Manning & Whitehouse (2012); Phelan et al. (2011); Haynes (2016); HR Wallingford (2002); Oliver (2013); RSL and wind/sea datasets; Waves Toolbox; NOAA tide data; etc.