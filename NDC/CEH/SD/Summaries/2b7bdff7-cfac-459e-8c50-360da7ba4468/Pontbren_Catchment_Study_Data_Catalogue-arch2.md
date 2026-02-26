# Introduction to the Database Catalogue

- Purpose and scope
  - Describes the Pontbren Database, including instrumentation, data structure, QA, and metadata to support monitoring the environment.
  - Aims to provide data in a consistent format to support scrutiny of environmental health and policy performance over time.
  - Designed for reuse and integration with other data sources; includes guidance on data storage and portal upload.

- Data organization and framework
  - Data files are organized into directories with a defined framework; QA codes accompany quality-assured data.
  - Most data are provided as .txt files, typically split into 6-month blocks (Jan–Jun, Jul–Dec); file names indicate collection date ranges.
  - Appendices supply supplementary information useful for data users.
  - Database framework outlines the main data domains and their sub-folders (Quality Assured; AWS; Bowl study site; Groundwater; Hillslope study site; Llyn Hir; Land use manipulation plots; Neutron probe soil moisture; Rain gauge data; Streamflow; Appendices).

- Data streams and instrumentation (high-level)
  - AWS (Automatic Weather Station): sensors sampled every 1 minute; outputs include daily and 10-minute averages; post-2009 sensor updates added Ave Humidity 2 and Ave Air Temp 2.
  - Bowl study site: run-off and soil moisture tension data (weirs, tipping buckets, tensiometers) with site-specific subfolders; weir boxes measure water height and flow; data aggregation evolves from high-frequency to 5-minute means.
  - Groundwater: five locations with Diver pressure transducers (barometric compensation); results as height above soil surface and groundwater temperature; sampling frequency varied over time.
  - Hillslope study site: runoff weirs, tensiometers, tree shelterbelt overland flow; data quality notes include evaporation and data logging issues.
  - Llyn Hir: soil moisture tension arrays at multiple depths with adjusted sampling cadence.
  - Land use manipulation plots: four plots with three replicates each; treatments Ungrazed, Trees, Graze; tensiometers and overland-flow measurements.
  - Neutron probe soil moisture: profiles up to ~120 cm across multiple sites; site-specific calibrations used to convert counts to volumetric moisture content.
  - Rain gauge data: tipping bucket and storage gauge data across sites; reported in mm/day and mm.
  - Field diaries: Word documents documenting site issues and data context.
  - Streamflow: Sites 1–13 monitored with Starflow acoustic Doppler systems (plus some bed-mounted transducers or weirs); Starflow provides multiple parameters at 15-minute intervals; site-specific calibration against spot measurements documented in appendices.
  - Appendices and metadata: comprehensive QA, borehole logs, neutron probe logs, and site-specific details.

- Quality assurance and data usability
  - QA codes accompany data to flag reliability and known issues (Appendix A); covers problems like logger failures, sensor calibration issues, rodent damage, evaporation, and data gaps.
  - Calibration details for Starflow are site-specific (linear models y = alpha x + beta) with associated uncertainties.
  - Rich metadata (field diaries and appendices) supports interpretation and data quality judgments.

- Data access, interoperability and reuse
  - Emphasis on storing and uploading datasets to appropriate portals; standardized naming and directory structure to support cross-site comparisons.
  - Clear documentation on instruments, deployment sites, sampling frequencies, and data processing (block aggregation, quality flags) to aid reproducibility and secondary analyses.

- Practical notes for analysts
  - Expect diverse data formats and sampling cadences; plan for data cleaning and QA code interpretation prior to analysis.
  - Use site-specific calibration parameters for Starflow data; be mindful of limitations at very low flow depths.
  - Anticipate data gaps due to field issues (rodent activity, logger downtime) and annotate accordingly with QA codes.
  - Leverage neutron-probe moisture data with provided conversion equations and site calibrations.
  - When integrating across domains (rainfall, runoff, groundwater, soil moisture), use the table of contents and appendices to map data to instrumentation and site context.

- End-to-end coverage
  - The catalogue encompasses AWS weather data, bowl and hillslope hydrology and soil moisture, groundwater depth and temperature, land-use manipulation experiments, neutron-probe moisture, rainfall, field diaries, and streamflow measurements across Pontbren study sites, with comprehensive metadata and QA guidance to enable robust environmental monitoring and policy-oriented analyses.

- Borehole logging and N-probe data (Equipment & Methods)
  - N-probe borehole logs NP20–NP23 documented for multiple sites (e.g., Llanfair Caereinion); include hand auger drilling, guide tubes, and aluminium access tubing; date of logging (e.g., 14/05/06); depth intervals and soil descriptions (e.g., silty/clayey soils, clay, sandstone/mudstone gravel); site coordinates and datum information; completion details and sampling depths; CEH involvement; detailed borehole log sheets and borehole numbers.

- Appendices reference (Streamflow)
  - Appendix D provides streamflow gauging site flow metered measurements with start/finish times and flow estimates, including multiple sites and repeated measurements, used for validation and calibration of acoustic Doppler flow data.