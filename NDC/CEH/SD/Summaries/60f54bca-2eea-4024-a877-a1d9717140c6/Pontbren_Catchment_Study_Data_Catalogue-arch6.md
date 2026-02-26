# Introduction to the DATABASE Catalogue

- Describes the Pontbren Database, including instrumentation, data files, directory structure, and quality assurance (QA) procedures to enable data discovery, verification, and reuse across topics.
- Documents multiple study sites and data types (weather, hydrology, soil moisture, groundwater, land-use experiments, neutron probe data, rain gauges, field diaries, streamflow) to support analysis and data products.

## Data organization and structure

- Data files are stored in directories organized into six-month blocks (January–June, July–December) in .txt format; file names reflect collection dates.
- Appendices provide metadata and QA guidance to support interpretation and reuse.
- Hierarchical database framework includes categories such as AWS, Bowl, Groundwater, Hillslope, Llyn Hir, Land use plots, Neutron probe, Rain gauges, Field diaries, and Streamflow, with further sub-division by instrument or site.

## Data quality, metadata and documentation

- QA codes describe data quality (good, questionable, calibration issues, sensor faults, gaps, etc.); Appendix A outlines the coding system.
- Borehole logs (Appendix B) and Neutron probe logs (Appendix C) provide site-specific metadata for instrumentation, lithology, water levels, and calibration context.
- Documentation and metadata accompany data tables and figures to aid interpretation (Table of Tables and Figures referenced).

## Key data categories

- Automatic Weather Station (AWS)
  - Location: Bowl; 1-minute sensor sampling; daily and 10-minute averages available.
  - Variables include incident radiation, wind, temperatures, humidity, net radiation; RH and temperature sensor updates implemented after 2009.
- Bowl study site
  - Runoff: Weir boxes and tipping buckets; data in litres/second; evaporation effects may cause negative readings.
  - Tensiometers: Arrays at multiple depths; data stored as soil water tension (cm H2O); logging arrangements updated in 2008.
- Groundwater
  - Five boreholes with Diver pressure transducers and barometric compensation.
  - Variables: water height (cm) relative to soil surface, temperature; sampling frequency shifted from 10 to 30 minutes in Oct 2006.
- Hillslope study site
  - Runoff from overland flow traps, drain flow, tensiometers; tree shelterbelt overland flow data included.
  - Runoff: 1-minute or 5-minute sampling; evaporation impacts considered.
  - Tensiometers and plots: Arrays across depths; some arrays removed over time; centralized logging.
- Llyn Hir study site
  - Tensiometers at 10, 30, 50 cm; sampling intervals adjusted (e.g., Sep 2009 changes).
- Land use manipulation plots
  - Four sites (Rhos1, Rhos2, Tyn Fron, Penllwyn) with 3 replicates and four treatments (Grazed, Ungrazed, Trees); replicated layout randomized.
  - Data: Tensiometer readings and overland flow by replicate plot.
- Neutron probe soil moisture
  - Coverage across Bowl site, hillslope, manipulation plots, tree areas, Llyn Hir.
  - Data: Raw counts with calibration to volumetric moisture content; site-specific notes and tube locations recorded.
- Rain gauges
  - Sites include Bowl, Hirrhos Uchaf, Llyn Hir, Penllwyn, Quarry, Rhos1.
  - Data: Tipping bucket and storage gauge readings; height above ground documented; coverage varies by site.
- Field diaries
  - Word documents with field notes to aid interpretation of site conditions and data issues.
- Streamflow
  - Sites 1–9 and 13 use Starflow (acoustic Doppler); Sites 10–12 use alternative methods.
  - Data: Stage height, velocity, cross-sectional area, water depth, temperature, battery status, flow rate; low-flow calibration uses site-specific linear relations (y = αx + β).
  - Calibration parameters are site-specific (Table 3); data quality limited when water depth is very low (e.g., < 50 mm).

## Calibration and data processing

- Streamflow calibration
  - Starflow estimates are adjusted to manual measurements using site-specific parameters (α, β); low-flow data with water depth < 50 mm are not used for calibration.
- Neutron probe calibration
  - Counts-to-moisture conversion uses a linear relation derived from calibration data; adjustments may be required for peat or organic-rich layers.
- Metadata and site-specific notes
  - Calibrations and interpretations depend on borehole logs, neutron logs, and site lithology.

## Practical use and data integration

- Data are patchy in places (e.g., rodent damage to tree shelterbelt plots; evaporation affecting runoff measurements); QA codes should be consulted before modelling.
- Temporal coverage is frequent (1-minute AWS, several minutes for other sensors) with block-based file organization; consistent site naming supports cross-dataset integration.
- End users should:
  - Filter data by QA codes for quality control.
  - Cross-check borehole logs and neutron logs for calibration and lithology context.
  - Apply site-specific streamflow calibration for Starflow estimates, especially in low-flow periods.
- Integration across datasets is enabled by consistent site naming and a structured hierarchy, facilitating hydrological modelling and flood-risk analysis across AWS, runoff, soil moisture, groundwater, and streamflow data.

## Notable limitations and considerations

- Outputs can be underutilized or under-shared; emphasis on promoting outputs and incorporating feedback recommended.
- Some data are informationally complex and require careful interpretation of field notes and QA metadata before use in analyses or models.
- Documentation, QA guidance, and site-specific appendices are essential for correct calibration, especially for streamflow and neutron-probe measurements.

## Appendices and supplementary materials

- Appendix A: QA coding system for data quality across instruments.
- Appendix B: Borehole logs (instrumentation, lithology, water levels, etc.).
- Appendix C: Neutron probe logs (location and soil profiling details).
- Appendix D: Streamflow gauging sites flow metered spot measurements (manual metered flow data with time stamps and site references).