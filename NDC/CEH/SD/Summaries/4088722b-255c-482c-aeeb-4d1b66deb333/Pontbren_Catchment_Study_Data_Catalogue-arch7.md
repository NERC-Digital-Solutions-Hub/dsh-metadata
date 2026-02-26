# Pontbren Database Catalogue

- Purpose and scope
  - Provides borehole, neutron probe, groundwater, soil moisture, and streamflow data to support map-based GIS analyses across Pontbren study sites.
  - Documents instrumentation, logging methods, site locations, and quality-control context to enable spatial analyses and reproducible GIS workflows.

- Data components and content
  - Borehole logs (NP20–NP23) and N-probe data
    - Multiple sites and plots (e.g., Site S3 manipulation plots 3.1–3.3; central/westernmost plots; edge of wood at Tyn y Fron Trees)
    - Spatial references and layouts included (Location, Grid Reference SJ coordinates)
    - Log details per borehole: Datum level, depth (mBGL), borehole description, soil types and stratigraphy, completion tubing, sample depths, and recorded metadata
    - Information appears as structured logs (Sheet 1 entries) with site-specific notes and cross-referenced to the Centre for Ecology and Hydrology
  - Groundwater and soil moisture context
    - Notes on N-probe placement and soil descriptions aligned with monitoring plots
    - Descriptive soil textures and stratigraphy relevant for GIS-based soil profile mapping
  - Streamflow data (Appendix D)
    - Streamflow gauging sites with flow metered spot measurements
    - Exact start and finish times, and flow estimates (litres per second) across multiple dates and sites (e.g., Site 4–Site 13)
    - Data suitable for hydrograph reconstruction and model calibration

- Spatial references and metadata
  - Grid references provided (British National Grid, e.g., SJ 07360 06833; SJ 07426 06920; SJ 07341 06821; SJ 07323 06807)
  - Datum levels and depths recorded for each borehole interval
  - Instrument locations tied to named plots and landscape features (e.g., edge of wood, manipulation plots, S3 site)
  - Descriptive soil lithology and texture documented within logs for GIS layering (e.g., silty/clay textures, mottling, gravel content)

- Data organization and provenance
  - Equipment & Methods sections compiled by Groundwater Monitoring and Drilling Ltd
  - Logs are presented as sheet-based entries with recurring fields (location, grid reference, datum level, depth, description, completion tubing)
  - Appendices and logs provide context for data provenance and field procedures, aiding spatial data quality and traceability

- GIS relevance and usage guidance
  - Enables creation of georeferenced borehole/soil moisture profiles and co-location with other Pontbren GIS layers (topography, rainfall, runoff, vegetation management)
  - Depth- and site-specific attributes support depth-resolved GIS analyses and plot-scale comparisons
  - Streamflow data supports hydrological modeling and spatially explicit water-budget assessments across multiple sites and time periods
  - The structured, location-tagged logs facilitate data integration, spatial joins, and map-ready datasets for policy, client, or public-facing outputs

- Practical considerations
  - Data formats are logger/log sheet-based text representations; suitable for parsing into GIS-friendly tabular formats
  - Spatial accuracy hinges on precise grid references and datum levels documented in each borehole log
  - Temporal coverage varies by data type (discrete borehole logs vs. continuous streamflow measurements), requiring appropriate GIS-time integration for analyses