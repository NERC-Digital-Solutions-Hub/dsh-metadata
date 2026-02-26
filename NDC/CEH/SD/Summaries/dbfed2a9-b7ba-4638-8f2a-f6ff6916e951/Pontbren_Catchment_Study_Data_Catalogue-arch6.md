# Pontbren Database Catalogue

- Purpose and scope
  - Describes the Pontbren Database, including instrumentation, data files, organization, and quality assurance to enable data discovery and reuse.
  - Covers data types from AWS weather data to streamflow, groundwater, tensiometers, neutron probes, rainfall, field diaries, and site manipulation experiments; includes metadata, file structure, and QA documentation.

- Data organization and access
  - Data files are organized into directories using a described framework.
  - Data are provided as text files (mostly .txt), commonly split into six-month blocks (January–June, July–December).
  - Each data point may include a QA code, with QA details in appendices.
  - Appendices provide supplementary information useful to catalogue users (QA coding, borehole logs, neutron probe logs, field notes).

- Database framework and contents
  - Hierarchical folder structure spanning study sites and measurement types.
  - Major data categories (examples of subfolders):
    - AWS (Automatic Weather Station)
    - Bowl study site runoff and soil water tension data
    - Groundwater (boreholes 1–5)
    - Hillslope study site runoff and soil water tension data
    - Llyn Hir study site soil water tension data
    - Land use manipulation plots (four sites with replicates and treatments)
    - Neutron probe soil moisture data
    - Rain gauge data (multiple sites)
    - Field Diaries
    - Streamflow (multiple gauging sites with Starflow and additional methods)

- Data categories: key points
  - AWS
    - Sensors sampled every minute; outputs include daily and 10-minute averages.
    - Post-2009 datasets include improved RH and temperature measurements.
    - Data headings cover incident radiation, wind, soil/air temperature, humidity, and radiation terms.
  - Bowl study site runoff and soil water tension
    - Runoff data from weir boxes and tipping buckets; includes drain and overland flow datasets.
    - Tensiometer data at multiple depths (10, 30, 50 cm); organized by array and logger configuration.
  - Groundwater
    - Five boreholes monitored with Diver pressure transducers and BaroDiver corrections.
    - Height relative to soil surface and temperature provided; sampling frequency evolved over time.
  - Hillslope study site runoff and soil water tension
    - Runoff data from weir boxes (drain and overland flow); tensiometer arrays; tree shelter data.
    - Noted data quality issues (e.g., rodent damage) affecting some datasets.
  - Llyn Hir study site
    - Tensiometer arrays (10, 30, 50 cm) with adjusted sampling frequency over time.
  - Land use manipulation plots
    - Four sites with three replicates each; treatments Ungrazed, Trees, Grazed.
    - Replicates include tensiometers at multiple depths and overland flow measurements.
    - Experimental layout designed to assess land-use impacts on soil moisture and runoff.
  - Neutron probe soil moisture
    - Profiles up to ~120 cm; multiple locations across sites (bowl, hillslope, manipulation plots, tree areas, Llyn Hir).
    - Calibration uses a linear relation with soil and water counts; parameters largely from CEH clay calibration.
  - Rain gauges
    - Data from tipping buckets (mm/day) and storage gauges (mm); site locations correspond to field instruments.
  - Field Diaries
    - Word documents with field notes on monitoring locations and instrumentation issues.
  - Streamflow
    - Sites 1–9 and 13 primarily use Starflow acoustic Doppler meters; some sites use pressure transducers or v-notch weirs.
    - Site-specific calibrations relate Starflow estimates to manual measurements; low-flow data (<50 mm depth) excluded from calibration.

- Quality assurance and documentation
  - Appendix A: Quality assurance coding system
    - Codes categorize data quality (e.g., good, questionable, calibration issues, outages) tailored to data types (tensiometers, rainfall gauges, tipping buckets, groundwater, Starflow, weirs, etc.).
    - Flags recurring issues like logger failures, sensor faults, blockages, calibration errors, and other operational problems.
  - Appendix B: Groundwater borehole logs
    - Detailed borehole equipment, logging logs, water strikes, depths, soils, and casing details.
  - Appendix C: Neutron probe access tube logs
    - Logs documenting access tubes, locations, and site-specific notes.
  - Appendix D: Streamflow gauging sites flow metered spot measurements
    - Practical tabulated measurements of flow metered estimates with start/finish times and values.

- Practical guidance for data use (Data Support perspective)
  - Data integration: Catalogue supports cross-site, cross-technology integration (AWS, runoff, soil tension, groundwater, rainfall, streamflow).
  - Data quality and calibration: Site- and instrument-specific calibrations documented; apply QA codes and calibration parameters during processing.
  - Handling data gaps: Context for gaps is provided via field diaries (e.g., rodent damage, logger issues, access variability).
  - Reproducibility: Consistent file naming, six-month blocks, and QA codes aid traceability and reproducibility of data products.
  - Data products: Outputs such as dashboards, pivot tables, and charts can be built using the self-serve structure; early prototypes may be shared for feedback and iteration.

- Equipment & Methods (borehole logs and site details)
  - Borehole and site information documented with equipment details (hand auger, AQ drill rod, pneumatic hammer, Atlas Copco rigs, etc.).
  - Sites S3, S3 central, and S3 westernmost described with grid references and datum levels.
  - Groundwater monitoring and drilling activities, borehole descriptions (soil types, depths, completion tubes), and sample depths included.
  - Documentation provided by CEH and Groundwater Monitoring and Drilling Ltd; includes multiple sheets and detailed borehole logs.

- Endnotes and caveats
  - Some data sections flagged as questionable or unreliable due to environmental or operational factors (e.g., rodent damage, calibration uncertainties, low-flow measurement challenges).
  - Calibration parameters are site-specific and may vary by site or soil conditions (e.g., peat at Llyn Hir).