# Introduction to the DATABASE Catalogue

- Purpose and scope
  - Describes the Pontbren Database, its instrumentation, data organization, and how data are provided.
  - Data stored in directories, with QA codes attached to data points and details in Appendices.
  - Most data are in .txt format, typically in six-month blocks; file names indicate collection dates.
  - Appendices provide metadata to aid users and support data interpretation.

- Database framework and organization
  - Data are structured into top-level folders with subfolders for each data stream:
    - AWS (Automatic Weather Station)
    - Bowl study site runoff and soil water tension data
    - Groundwater
    - Hillslope study site runoff and soil water tension data
    - Llyn Hir study site soil water tension data
    - Land use manipulation plots
    - Neutron probe soil moisture data
    - Rain gauge data
    - Field Diaries
    - Streamflow
  - Each dataset includes instrumentation locations and description images/figures (instrument locations shown in site maps).

- Equipment, methods, and data collection (focused on boreholes and probes)
  - Borehole logging and drilling methods described (hand auger, AQ drill rod/guide tube, pneumatic hammer, Atlas Copco RAB/Leopard air-flush drills).
  - N-probe installations detailed for various plots/sites (e.g., Site S3 and manipulation plots 3.1–3.3).
  - Borehole data include grid references, datum levels, soil descriptions, depths, completion tubing, and sample intervals.
  - Specific boreholes (e.g., NP20–NP23) documented with location, date, soil stratigraphy, and installation notes.
  - Logs contain detailed soil descriptions (color, texture, mottling, moisture-related notes) and material records (e.g., gravelly CLAY, sandstone/mudstone fragments).

- Site references and spatial context
  - Instrument locations and sites are documented with grid references and site names (e.g., PEN-TAL-Y-CEIN LLANFAIR CAEREINION; COED CWM-Y-LLWYNOG LLANFAIR CAEREINION; Edge of wood).
  - Site-specific pages provide grid references and datum levels to support GIS placement and spatial analyses.

- Data quality, calibration, and QA
  - Quality Assurance (QA) codes cover data quality status, calibration, logger faults, data gaps, and sensor/de-installation issues (detailed in Appendix A).
  - QA notes include site-specific calibration concerns and field notes (e.g., issues with calibration or environmental effects).
  - Data assembly and calibration considerations are included (e.g., site-specific calibration notes and standard deviations).

- Appendices and supplementary material
  - Appendix A: QA coding system (codes and descriptions across measurement types).
  - Appendix B: Groundwater monitoring borehole logs (equipment, drilling methods, logs per borehole).
  - Appendix C: Neutron probe access tube logs (locations and installation details).
  - Appendix D: Streamflow gauging sites flow metered spot measurements (calibration and spot readings).

- Practical notes for GIS and data use
  - Data are designed to support map-based GIS visualizations, with explicit instrument locations and site layouts aiding spatial analyses.
  - Time-series data span multiple sites and instruments; joining by site, location, and timestamp is essential for coherent GIS layers.
  - File naming conventions and appendices provide metadata to support data integration, quality control, and calibration in GIS workflows.

- End-user guidance and limitations
  - Emphasizes iterative testing and user feedback; users should review QA codes and field diaries to assess data reliability and context.
  - Acknowledges variability in data quality across sites and instruments, including calibration status and environmental influences impacting data.