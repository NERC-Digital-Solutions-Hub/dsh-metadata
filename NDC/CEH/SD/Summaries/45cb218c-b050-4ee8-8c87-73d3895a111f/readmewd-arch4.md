# Gridded data of water debt for year 2000

- What it measures
  - WD debt: number of years the hydrological cycle would need to replenish water sources (soil moisture, surface water, groundwater) used to produce annual output of nine major crops (wheat, maize, rice, soybean, sugar cane, sugar beet, cotton, barley, sorghum).
  - Purpose: provides a gridded, global assessment of water demand relative to renewable water availability for crop production around year 2000.

- Methodology highlights
  - Resolution and scope: global coverage at 5 arcmin spatial resolution.
  - Core calculation: WD equals the ratio of the annual water footprint (WF) for a crop s in source l to the average renewable water available in the cell.
  - Renewable water estimate: long-term average from 1987–2013 to smooth out anomalies.
  - Water footprint (WF) per crop per source: WFcr,l = CWFs,cr,l × Pr,l
    - CWFs,cr,l: local crop water footprint (m3 per ton) by crop, source, and location.
    - Pr,l: annual crop production (tons) at location l.
  - Total WD per cell: sum of WD across all nine crops.
  - WD per crop across sources: WDcr,l is the maximum WD value across water sources (GW, SW, SOILMOISTURE) for that crop in the cell.
  - Full methods available via open-access DOI.

- Data details and structure
  - Spatial/temporal metadata
    - Spatial scope: global
    - Spatial resolution: 5 arcminutes
    - Coordinate reference system: WGS 84
    - Temporal scope: 1997–2003 (circa year 2000)
    - Temporal resolution: annual
  - Units and format
    - Units: years
    - Format: txt (text files)
    - Import readiness: can be loaded into MATLAB, Python, or R; or opened directly in GIS by renaming the extension to ".ascii"
  - Crop and source coverage
    - Crops: nine major crops listed (wheat, maize, rice, soybean, sugar cane, sugar beet, cotton, barley, sorghum)
    - Sources: groundwater (GW), surface water (SW), soil moisture (SOILMOISTURE), and an all-sources combined file
  - File naming and organization
    - Each file corresponds to WD for all nine crops for a single source or the combined all-sources file

- Accessibility and practical use
  - Open-access data with a citable methodology reference
  - Suitable for GIS analyses and integration with other datasets to assess crop-water stress, sustainability, and policy implications

- Relevance for Data Leaders
  - Data system thinking: provides a defensible, reproducible global water-debt metric tied to specific crops and water sources.
  - Data quality and governance considerations: includes long-term averaged renewability (1987–2013) to reduce year-specific bias; explicit per-source results enabling cross-comparison and aggregation.
  - Data management actions: can be incorporated into data strategy for water sustainability; requires clear metadata, discoverability, and coordination with data producers due to multi-source inputs.
  - Collaboration opportunities: aligns with sector-wide data communities to standardize water-footprint metrics and support coordination across partners.
  - Practical deployment: supports user-centered applications by enabling mapping of water debt, identifying hotspots, and informing policy or agricultural planning.