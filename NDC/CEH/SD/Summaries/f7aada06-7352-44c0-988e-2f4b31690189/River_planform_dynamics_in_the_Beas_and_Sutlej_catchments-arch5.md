# Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system

- Overview
  - Dataset described and analyzed in Vercruysse and Grabowski (2021) to evaluate human impacts on river planform across centennial, annual, seasonal, and episodic timescales.
  - Case study: Himalayan Sutlej-Beas River system.
  - Aims: (i) quantify changes in planform characteristics over multiple timescales; (ii) link planform changes to human-environment drivers; (iii) conceptualize geomorphic changes in terms of timescale-dependent evolutionary trajectories.

- Scope and Spatial Extent
  - Beas River: Pong Dam to confluence with Sutlej; Reach 1 (below dams) and Reach 2 (Punjab plains); Reach 2 subdivided into 4 sections (Beas) and 5 sections (Sutlej).
  - Sutlej River: Bhakra Dam to confluence with Beas.
  - Coordinate System: WGS84.
  - Spatial bounding: West 74.957, East 76.706, North 32.225, South 30.780.

- Data products ( What’s in the dataset )
  - Wet river area, post-monsoon, annually 1989-2018.
  - Active gravel bars, annually 1989-2018.
  - Active channel area (maximum extent 1989-2018).
  - Active channel width, annually 1989-2018.
  - Active channel width from historic map (1847-1850).
  - Anabranching index, annually 1989-2018.

- Data generation methods (Key technical details)
  - Wet river area:
    - Derived from Landsat 5-8 imagery (1989-2018) using post-monsoon mNDWI (>0.15) to separate water/land.
    - Manual edits to remove stray water pixels; converted to polygon shapefiles; annual per reach/section.
  - Active gravel bars:
    - Identified via high red reflectance (>0.16) from Landsat data (1989-2018) within the wet-area buffer; shapefiles created per year.
  - Active channel area:
    - Aggregated yearly wet-area shapefiles (1989-2018) to form a multi-year active-channel polygon.
  - Active channel width:
    - Width measured from the wet-area extent every 2 km; also derived from historic 1847 map; width perpendicular to riverbank.
    - Mean width calculated for Reaches 1 and 2 and for each Reach-Section; annual series.
  - Anabranching index (AI):
    - Calculated from cross sections (minimum 10) showing active channels separated by bars/islands; annual values for each reach/section.
  - Documentation notes: See Vercruysse & Grabowski (2021) for methodological details.

- Data formats and file listing
  - Primary formats: ESRI Shapefiles (with mandatory/optional ancillary files) and CSVs.
  - Shapefile-based data:
    - Post monsoon season wet river area, 1989-2018: Beas_PM_Wetted_annual.shp; Sutlej_PM_Wetted_annual.shp
    - Post monsoon season active gravel bars, 1989-2018: Active_Gravel_Bars_Annual.shp
    - Active channel area (1989-2018): Beas_ActiveChannel_BelowDam.shp; Sutlej_ActiveChannel_BelowDam.shp
    - Active channel width (1989-2018): Beas_Width_Annual.shp; Sutlej_Width_Annual.shp
    - Active channel width from historic map (1847): Beas_Width_1847.shp; Sutlej_Width_1847.shp
    - Reaches/Sections definitions: Reaches_sections.shp
  - CSV data:
    - Metrics_Annual_Beas.csv
    - Metrics_Annual_Sutlej.csv
  - Additional notes: Year of measurement and corresponding attributes (e.g., Year, Width) are included in the datasets.

- Quality control and provenance
  - Landsat-derived data incorporate quality assessment bands to ensure cloud-free imagery selection.
  - Processing performed by project team with spot validation against aerial photography.
  - Data checked for errors at all stages by Cranfield University team.

- Metadata, governance, and reuse
  - Data described with clear spatial-temporal scope, geospatial definitions, and measurement methods.
  - Formats chosen for interoperability (ESRI Shapefiles, CSVs) to support GIS-based data stewardship.
  - Potential considerations for reuse include threshold choices (e.g., mNDWI, red reflectance) and historic-map-derived metrics; dataset accompanied by methodological references.

- Documentation and references
  - Core references guiding methods and interpretation:
    - Huang et al. 2018 on water detection from space.
    - Langat et al. 2019 on river-channel dynamics monitoring.
    - Li et al. 2017 on automatic bare land mapping thresholds.
    - Revenue Survey of India (1852) map source.
    - Vercruysse & Grabowski 2021 (Geomorphology) describing the associated study and context.

- Contact
  - Dr Robert Grabowski
  - Cranfield University
  - Email: r.c.grabowski@cranfield.ac.uk
  - Tel: +44 (0) 1234 758360

- Relevance for data stewardship
  - Provides multi-temporal, multi-scale river planform data suitable for governance, planning, and management of river systems.
  - Demonstrates end-to-end data pipeline from remote sensing to curated geospatial products, with quality checks and provenance documentation suitable for data catalogs and discovery systems.
  - Enables tracking of data lineage, versioning, and potential updates to reflect new imagery or revised methods.