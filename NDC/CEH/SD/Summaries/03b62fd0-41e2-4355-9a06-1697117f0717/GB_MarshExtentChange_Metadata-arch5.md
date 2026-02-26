# Change in saltmarsh extent for six regions across Great Britain (1846-2016)

## Data availability and citation
- Data can be accessed via the provided DOI links and is licensed under the Open Government Licence.
- Citing requirement: Ladd, C.J.T.; Duggan-Edwards, M.F.; Bouma, T.J.; Pagès, J.F.; Skov, M.W. (2019). Change in saltmarsh extent for six regions across Great Britain (1846-2016). NERC Environmental Information Data Centre.
- Authors and dataset origin: C.J.T. Ladd, M.F. Duggan-Edwards, T.J. Bouma, J.F. Pagès, M.W. Skov; data collection and processing credited to Ladd and Duggan-Edwards.
- Data are part of a study on long-term, large-scale lateral saltmarsh change; associated publication in press (Ladd et al.).

## Data overview
- Dataset: GB_MarshExtentChange_Layers_1846-2016, an ESRI shapefile layer detailing saltmarsh areal extent for 25 estuaries/embayments across 6 GB regions (1846–2016).
- Delineation: Marsh extents mapped in ArcGIS 10.6 (scale 1:7,500) by plotting vertices every 5 m along marsh edges.
- Uncertainty: RMSE components include basemap georeferencing inaccuracies, georeferencing procedure, interpreter edge digitising, and pre-digitisation map/photo distortions.
- Coverage criteria: Marsh extent recorded only where maps/photos covered the entire estuary/embayment.
- Context: Data gathered for a study on large-scale, long-term lateral marsh change; used in Ladd et al. (in press).
- Data collectors: C.J.T. Ladd and M.F. Duggan-Edwards.

## Experimental design
- Scope: Change in saltmarsh extent calculated for 25 estuaries/embayments in 6 GB regions approximately every 30 years from 1846 to 2016.
- Regional layout: Western GB (Solway, Morecambe, Cardigan) along Irish Sea; Eastern/Southern GB (Wash, Essex-Kent, Solent) along North Sea/English Channel.
- Data gaps: Post-1950 aerial photographs unavailable for Solent and Essex-Kent regions.

## Methods
- Data sources: Ordnance Survey maps and aerial photographs; maps from EDINA Digimap; Cardigan aerials from Royal Commission on Ancient Historical Monuments Wales.
- Timestamping: Survey dates extracted from Oliver (2013) and used as timestamps.
- Processing: Aerial photographs scanned and georeferenced to OS rasters in British National Grid; marsh edges digitised in ArcGIS 10.6 (1:7,500), vertices every 5 m.
- RMSE assessment: Four contributing factors to spatial error (basemap displacement, georeferencing distortions, digitising interpreter error, pre-digitisation map distortions); RMSE calculated per marsh complex.
- Region/estuary coordinates: Table 1 provides decimal-degree coordinates for study regions and estuaries.

## Data structure
- Files: 6 GIS files, with one primary shapefile named GB_MarshExtentChange_Layers_1846-2016.
- Attribute table: 12 fields including Region, Estuary, Marsh, Edition, Surv_Year, Pub_Year, RMSE_B, RMSE_G, RMSE_I, RMSE_M, RMSE_95, and Area_ha.
- Field descriptions and units: Detailed in Table 2 (Region/Estuary/Marsh names; Edition source; Surv_Year and Pub_Year timing; RMSE components in meters; Area_ha in hectares).

## Quality control
- Qualitative accuracy check: The most recent digitised marsh extent was compared against national marsh extent layers (Phelan et al., 2011; Haynes, 2016) for general agreement.
- Supporting evidence: Literature searches to assess reliability of observed marsh changes and to identify potential mapping/surveyor errors (further details in Ladd et al., in press).

## Miscellaneous
- Predictors of marsh change: Data on predictors (Table 3) are provided and also in the CSV file GB_MarshChangePredictors_1967-2016.csv; used in the Ladd et al. analysis.
- Data collation: Ladd compiled and processed predictor data; includes rates of lateral marsh expansion/erosion and key predictors for 25 estuaries/embayments across six regions (1967–2016).
- Rate calculations: Linear rate of marsh change (ha/yr) between 1957 and 2016; some regions post-1950 data sourced from other studies (e.g., Solent, Essex-Kent). Wash region rates treated as non-linear due to reclamation phases, with averaged rates after each phase.
- Environmental predictors: Flood and wind-storm event frequencies; relative sea-level rise (RSLR); median wind-wave fetch; bedload sediment flux; UVVR (unvegetated vs. vegetated area ratio) as a proxy for external sediment supply; SSC for validation.
- Data quality checks for predictors: Correlation between UVVR and SSC used to validate UVVR as an indicator of sediment supply.

## References
- Baily, B., & Pearson, A. W. (2007)
- Brown, J. M., & Davies, A. G. (2010)
- Cooper, N. J., Cooper, T., & Burd, F. (2001)
- Ganju, N. K. et al. (2017)
- Halcrow (2010)
- Haynes, T. (2016)
- HR Wallingford (2002)
- Ladd, C.J.T. et al. (in press)
- Manning, A. J., & Whitehouse, R. S. J. (2012)
- NFDC (2017)
- Oliver, R.R. (2013)
- Phelan, N. et al. (2011)
- Rohweder, J. et al. (2012)
- Watson, S.J. et al. (2015)
- Wernette, P. et al. (2017)