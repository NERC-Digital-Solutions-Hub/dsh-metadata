# Introduction to the DATABASE Catalogue

- Purpose
  - Describes the Pontbren Database: instrumentation, data structure, QA, and access for data-driven hydrology and land-management analysis.
  - Supports multi-site, multi-dataset analysis of flood risk, sediment/water dynamics, and soil moisture.

- Study sites and data types
  - Bowl site, hillslope, tree shelterbelt, Llyn Hir, and manipulation plots.
  - Data categories include: weather, runoff, soil water tension, groundwater, streamflow, rain gauges, neutron-probe soil moisture, field diaries, and land-use treatments.

- Data organization and access
  - Data stored in structured directories with a defined framework; most data as .txt blocks (often 6-month segments) with QA codes per data point.
  - File names indicate collection dates; appendices provide QA codes, borehole logs, neutron-probe logs, and site notes.
  - Emphasis on metadata, documentation of instrumentation, and making datasets discoverable (portal uploads with metadata).

- Data categories and main datasets
  - Automatic Weather Station (AWS)
    - 1-minute sensor sampling; daily and 10-minute averages; variables include radiation, wind, temperature, humidity, soil temperature.
  - Bowl study site
    - Runoff: weir boxes (drain/overland) and tipping buckets; flow in L/s.
    - Tensiometers: arrays at 10, 30, 50 cm depths (cm H2O).
  - Groundwater monitoring
    - Five boreholes with Diver/barometric-corrected transducers; data as water height and temperature.
  - Hillslope study site
    - Runoff and overland flow; tensiometers; tree shelterbelt overland flow data.
  - Llyn Hir study site
    - Tensio meter measurements at multiple depths (10, 30, 50 cm).
  - Land-use manipulation plots
    - Four plots with replicates; treatments (Grazed, Ungrazed, Trees); tensiometers and overland flow data.
  - Neutron probe soil moisture
    - Profiles from bowl, hillslope, plots, trees, Llyn Hir; typically 10 cm to 120 cm depth; calibration using linear parameters.
  - Rain gauges
    - Tipping-bucket and storage gauges; data in mm/day (tipping) and mm (storage).
  - Field diaries
    - Documentation of data-collection issues and site conditions.
  - Streamflow
    - Starflow acoustic Doppler (ADCP) at most sites with site-specific calibration; some sites use pressure transducers or weirs.

- Calibration, QA, and data quality
  - Calibration
    - Streamflow: site-specific linear calibrations linking Starflow estimates to manual measurements; low-flow data (<50 mm depth) excluded from calibration.
  - QA and codes
    - Appendix A: QA codes for good data, questions, bad data, equipment faults, and site issues; covers tensiometers, rain gauges, overland flow, groundwater, Starflow, etc.
  - Logs and documentation
    - Appendices B and C: borehole and neutron-probe logs with location, depth, soil description, groundwater conditions, and construction details.
  - Data usability and reproducibility
    - Data sources tracked; metadata-rich datasets intended for reproducibility and reuse.

- Practical considerations for analysts
  - Scale and access
    - Local-scale data gaps and patchiness; multiple formats and folder structures; naming conventions vary; expect some gaps.
  - Data quality and interpretation
    - Consult QA codes to assess suitability for calibration, modelling, or trend analysis; field diaries help explain anomalies.
  - Integration and modelling
    - Data are designed for multi-scale modelling (hydrology, soil moisture, flood risk); apply site-specific calibrations for instrument readings.
  - Metadata and reproducibility
    - Emphasis on metadata richness, instrumentation documentation, QA processes to support reproducibility and data reuse.

- Appendices and supporting materials (borehole and method details)
  - Equipment and Methods
    - Borehole drilling equipment and logs (AQ drill rods, pneumatic hammer, rotary drills, access tubing).
    - Site references and grid coordinates; datum levels; soil descriptions; borehole depths and sample intervals.
  - Borehole and soil profiles
    - Logs provide soil types, moisture conditions, depth intervals, and completion details; multiple sites with detailed stratigraphy.
  - Streamflow gauging and flow metering
    - Site-by-site flow metering data, start/finish times, and flow estimates to support calibration and validation.

- Data provenance, discoverability, and reuse
  - Datasets are curated with source tracking and metadata uploads to portals to enhance discoverability and reuse in future analyses.