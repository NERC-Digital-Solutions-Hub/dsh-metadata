# Change in saltmarsh extent for six regions across Great Britain (1846-2016)

## Data availability and licensing
- Data accessible at https://doi.org/10.5285/03b62fd0-41e2-4355-9a06-1697117f0717
- Licensed under the Open Government Licence; citation required: Ladd, C.J.T.; Duggan-Edwards, M.F.; Bouma, T.J.; Pagès, J.F.; Skov, M.W. (2019). Change in saltmarsh extent for six regions across Great Britain (1846-2016). NERC Environmental Information Data Centre.
- Dataset name: GB_MarshExtentChange_Layers_1846-2016 (ESRI shapefile layer) with 12 attribute fields. Six GIS files in total.

## Data content and structure
- Purpose: Areal extent of saltmarshes along 25 estuaries/embayments in 6 GB regions, measured from 1846 to 2016 using maps and aerial photographs.
- Delineation: Marsh edges traced in ArcGIS 10.6 at 1:7,500, placing vertices every 5 m; RMSE estimated from basemap accuracy, georeferencing, digitising, and pre-digitisation distortions.
- Coverage: Only marsh extents available for entire estuary/embayment were recorded.
- Estuaries and regions: 25 estuaries across six regions (Solway, Morecambe, Cardigan, Wash, Essex-Kent, Solent).
- Data structure: The dataset comprises 6 GIS files with a shapefileGB_MarshExtentChange_Layers_1846-2016. Attribute table contains 12 fields: Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year, RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95, Area_ha.
- Table 2 (field descriptions) and Table 4 (predictors) define values, units, and meanings (e.g., RMSE components, Area_ha in hectares).

## Experimental design and methods
- Temporal design: Change in marsh extent calculated for the entire 25 estuaries across six regions at ~30-year intervals between 1846 and 2016.
- Regions and locations: Western GB (Solway, Morecambe, Cardigan) and eastern/southeastern GB (Wash, Essex-Kent, Solent) with specific estuaries listed in the dataset.
- Data sources: Ordnance Survey maps and aerial photographs; timestamps aligned with survey dates; for Cardigan, aerial photographs from the Royal Commission on Ancient Historical Monuments Wales.
- Post-1950 data: For Solent and Essex-Kent, post-1950 extents drawn from Bailey & Pearson (2007) and Cooper et al. (2001) respectively.
- Additional measurements: For 1957–2016, linear rates of marsh change calculated; in some regions, alternative approaches used where data were non-linear (e.g., Wash).
- Predictor data (miscellaneous): Tables of predictors (Table 3) and a separate CSV (GB_MarshChangePredictors_1967-2016.csv) for 25 estuaries, including:
  - LateralRateChange, RSLR (relative sea level rise), NetSedFlux, BedloadFlux
  - StormFreq, FloodFreq, MedianFetch, TidalRange
  - Derived metrics like UVVR (unvegetated/vegetated ratio) and sediment flux equations
- Supporting data and validation: UVVR-SSC correlation used to validate net sediment flux as a proxy for external sediment supply; qualitative checks against national marsh extents (Phelan et al., Haynes 2016) and literature searches.

## Data quality and validation
- Quality control: Vector layer qualitatively checked against national marsh extent layers; literature searches to assess plausibility and potential map-surveyor errors.
- RMSE accounting: Four RMSE components (basemap displacement, georeferencing distortions, interpreter digitising error, and map/photo distortions prior to digitisation) quantified to estimate uncertainty (RMSE_B, RMSE_G, RMSE_I, RMSE_M; RMSE_95 for 95% error bound).

## Use and context
- Original analyses: Data used in Ladd et al. (in press) to examine long-term, large-scale patterns in saltmarsh lateral expansion and erosion; contributors included C.J.T. Ladd and M.F. Duggan-Edwards.
- Data products: Marsh extent layers enable self-service analysis (e.g., regional change, rates, and predictors) and support further research into sediment supply and coastal marsh dynamics.
- Related outputs: Ancillary datasets (e.g., predictors) and publications cited in the metadata (e.g., 1967–2016 predictors, coastal processes references).

## References and related material
- Primary dataset and methods references listed in the metadata (e.g., Oliver 2013; Phelan et al. 2011; Haynes 2016; Ganju et al. 2017; Manning & Whitehouse 2012; various sediment transport and coastal studies).