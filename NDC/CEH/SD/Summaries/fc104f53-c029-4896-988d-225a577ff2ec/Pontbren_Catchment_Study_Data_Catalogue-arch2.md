# Introduction to the Database Catalogue

- Describes the Pontbren Database, detailing instrumentation, data organisation, and quality-assurance framework used to monitor environmental conditions.
- Aims to provide standardized data to support assessment of environmental health and policy performance over time, enabling scrutiny and cross-site comparisons.

## Data Organization and Access

- Data stored in clearly structured directories; each data point labeled with a quality-assurance code.
- Time-series primarily in .txt files, typically organized in six-month blocks (Jan–Jun, Jul–Dec); dates embedded in file names.
- Appendices supply supplementary guidance and site descriptions to aid navigation and use.

## Main Data Domains and Contents

- AWS (Automatic Weather Station)
  - Location: bowl on instrumented hillslope; sensors sampled every 1 minute; daily and 10-minute averages; includes daily max/min and wind-direction SD.
  - 2009 updates added RH and air temperature sensors.

- Bowl study site runoff and soil water tension data
  - Subfolders for bowl runoff, weir boxes (drain/overland), tipping buckets, tensiometers.
  - Runoff as flow (litres/second); weir-box height-based flow; tipping buckets for alternate estimates.
  - Tensiometer arrays at multiple depths; data organized by array/chronology; logging changes documented.

- Groundwater monitoring
  - Five boreholes with Diver/barometric compensation; data as height above ground and temperature.
  - Sampling cadence evolved from 10-minute to 30-minute intervals; borehole logs describe equipment and stratigraphy.

- Hillslope study site runoff and soil water tension
  - Runs via hillslope runoff (drain/overland), tensiometers, and tree shelterbelt overland flow.
  - Weir-box flow derived from water-height changes; evaporative loss can yield negative readings.
  - Tree shelterbelt area includes overland-flow traps and tensiometers; data quality affected by rodent damage in some systems.

- Llyn Hir study site soil water tension
  - Tensiometers at 10, 30, 50 cm with sampling frequency adjustments.

- Land use manipulation plots
  - Four sites with three replicates each; treatments include Grazed, Ungrazed, Trees.
  - Replicates host tensiometers (10/30/50 cm) and overland-flow measurements; plot layouts described; treatment locations recorded.

- Neutron probe soil moisture
  - Profiles across bowl, hillslope, manipulation plots, tree areas, and Llyn Hir; moisture derived from calibrated neutron counts.
  - Soil-type dependent calibration (e.g., alpha, beta) to convert counts to volumetric moisture.

- Rain gauges
  - Tipping-bucket and storage gauges across multiple locations; data in mm/day or mm per file type.

- Field Diaries
  - Word docs detailing field observations relevant to data quality and interpretation.

- Streamflow
  - Bed-mounted Starflow systems at multiple sites; others use pressure transducers or weir plates.
  - Starflow outputs include stage height, velocity, water depth, temperature; calibration against spot measurements documented.

- Equipment & Methods (Boreholes and N-probes)
  - detailed borehole deployment at multiple N-probe manipulation plots (Sites S3, central/westernmost, etc.).
  - equipment: hand auger, AQ drill rod, pneumatic hammer, Atlas Copco drills; logging of borehole depth, soil description, lithology, and completion tubing (16 gauge aluminium).
  - site references and grid coordinates (e.g., SJ 07360 06833; SJ 07341 06821; SJ 07323 06807) and CEH involvement; dates around 14/05/06; borehole logs include depth, soil type, moisture-related notes, and sampling intervals.

- Groundwork and data provenance
  - Drilling and borehole work conducted by CEH and Groundwater Monitoring and Drilling Ltd; logs include detailed lithology and installation details.
  - N-probe manipulation plots linked to specific field sites (e.g., PEN-TAL-Y-CEIN LLANFAIR CAEREINION, Site S3).

- Appendix D: Streamflow gauging sites flow metered spot measurements
  - Contains metered flow measurements with start/finish times and flow estimates from various sites and dates.

## Data Characteristics, Calibration, and Quality

- Calibration and site-specific relationships
  - Streamflow calibration uses site-specific linear relationships between Starflow estimates and manual measurements; site-specific alpha* and beta* parameters provided with standard deviations.

- Data quality and gaps
  - QA codes annotate data as good, questionable, calibration issues, or faults; common issues include sensor degradation, equipment removal, logger faults, and animal damage.
  - Appendices define QA codes and how to interpret them.

- Data frequency and practical considerations
  - High-frequency data (often 1-minute) with derived summaries; irregular sampling occurs due to logger limits or field incidents; metadata and diaries document variations.

## Appendices and Reference Material

- Appendix A: Quality assurance coding system
  - Defines QA codes for cross-dataset data quality.
- Appendix B: Groundwater monitoring borehole logs
  - Detailed borehole methodology, drilling apparatus, depths, lithology, and well construction.
- Appendix C: Neutron probe access tube logs
  - Logs describing neutron-probe installation and locations.
- Appendix D: Field Diaries and related notes
  - Field notes linked to instrumentation and data interpretation.

## Practical Implications for Analysts

- Enables consistent cross-site environmental monitoring and long-term trend analysis.
- Supports data quality assessment, calibration across streams and data streams, and data integration.
- Facilitates data transparency and access rights to maximise value beyond single-use analyses.

## Endnotes and Considerations

- Emphasises data provenance, instrument positions, and site-specific configurations.
- Documents known quality caveats (e.g., rodent damage, gas-logging issues) requiring careful handling during analysis.