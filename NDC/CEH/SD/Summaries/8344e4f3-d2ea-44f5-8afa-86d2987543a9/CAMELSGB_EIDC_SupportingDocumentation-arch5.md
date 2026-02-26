# CAMELS-GB: Catchment attributes and hydro-meteorological timeseries for 671 catchments across Great Britain (CAMELS-GB)

- Purpose and scope
  - Freely available, large-sample dataset of hydro-meteorological time series and catchment attributes for 671 catchments across Great Britain.
  - Daily hydrometeorological timeseries from 1 Oct 1970 to 30 Sep 2015, plus a rich set of catchment attributes describing topography, climate, hydrology, land cover, soils, hydrogeology, hydrometry, and human influences.
  - Designed to support environmental data analysis and modelling with emphasis on accessibility, reproducibility, and cross-study comparability.

- Data contents and structure
  - Hydro-mmeteorological timeseries (671 catchments, 1970-2015)
    - Variables include discharge, rainfall, potential evapotranspiration, temperature, radiation (shortwave and longwave), specific humidity, wind speed, etc.
    - Meteorological inputs sourced from CEH-GEAR (rainfall) and CHESS-met/CHESS-PE (PET and meteorology); PET provided with two estimates (PET and PETI) to account for interception.
    - Daily, catchment-averaged values; 16436 rows per catchment, 11 columns; no missing data in meteorology/pet variables, but flow timeseries may contain NaN.
    - File naming: CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930.txt
  - Catchment attributes (671 catchments, eight attribute classes)
    - Topographic, climatic, hydrologic, land cover, soils, hydrogeology, hydrometry, and human influences.
    - Attributes provided in eight separate text files (e.g., CAMELS_GB_topographic_attributes.txt, CAMELS_GB_climatic_attributes.txt, etc.), each with a gauge_id column identifying the catchment.
    - Examples of attribute types: location, area, elevations; climatic indices (mean precipitation, aridity, seasonality, snow fraction, etc.); hydrologic signatures (mean discharge, runoff ratio, baseflow indices, flow duration curve metrics); land cover shares; soil properties; hydrogeological unit productivity; hydrometric metadata; and human pressures (abstraction, discharges, reservoir attributes).
  - Catchment boundaries
    - Shapefile CAMELS_GB_catchment_boundaries, provided in British National Grid projection; boundaries derived from CEH IHDTM flow direction grids.
  - Data provenance and integration
    - Catchment boundaries and gauge data from UK National River Flow Archive (NRFA).
    - Catchment boundaries from IHDTM; topographic and other attributes derived from CEH datasets and national maps (soil, hydrogeology, land cover, etc.).
    - Additional datasets used for attributes include CEH-GEAR (rainfall), CHESS-met, CHESS-PE, European Soil Database, BGS hydrogeology maps, and reservoir/abstraction datasets.

- Access, documentation, and reuse
  - Intended for broad community use; paper describing CAMELS-GB (CAMELS-GB paper) recommended reading for context and methodology.
  - Data files provided as CSVs and a shapefile; accessible via the project references and data sources (NRFA API, CEH resources, etc.).
  - Acknowledgements and data sources documented; some human-influence and abstraction data have limitations (e.g., England-only coverage for abstractions, time-period caveats, and potential misattribution due to catchment masks).
  - Users should cite CAMELS-GB paper and follow dataset documentation; contact provided for data questions (gemma.coxon@bristol.ac.uk).

- Data quality, limitations, and governance considerations
  - Meteorological datasets are complete; flow data may contain NaN values (noted in the data).
  - Catchment boundary accuracy depends on the IHDTM-based delineation; potential boundary-related errors for small or complex catchments.
  - Land cover attributes use a 2015 snapshot (LCM2015) and may not reflect dynamic land cover changes; soil attributes carry high spatial heterogeneity and pedotransfer function uncertainties; correlations with ground measurements may be weak.
  - Abstraction and discharge attributes are England-specific, with possible NaN values for data-poor catchments and misalignment with topographic catchment masks; abstraction timing and types are not necessarily comprehensive.
  - Discharge uncertainty metrics are based on underlying methods and may not apply uniformly across all stations or time periods.
  - The dataset emphasizes reproducibility but acknowledges that NRFA data are dynamic; CAMELS-GB provides a fixed 1970–2015 window to enable repeatable analyses.

- Practical governance and maintenance notes for stewards
  - The dataset assembles diverse sources with explicit attributions and licensing caveats; ensure proper attribution per dataset sources (NRFA, CEH, BGS, EA, SEPA, etc.).
  - Given the use of external datasets, anticipate updates or changes in source data; document versioning and date of retrieval for reproducibility.
  - Provide guidance to dataset users on caveats (e.g., boundary errors, snapshot nature of land cover, England-only abstraction data) to ensure correct interpretation and comparability.
  - Encourage users to consult the CAMELS-GB paper for methodological details, data processing steps, and attribute definitions to support appropriate use and comparative analyses.

- Endnotes
  - Supplementary materials include extensive tables (Tables 2–9) detailing attribute definitions, data sources, units, and data provenance; appendix lists gauge IDs and collaboration details.
  - Acknowledgements attribute dataset creation to MaRIUS and related UK data initiatives; references provide foundational methods and datasets used.