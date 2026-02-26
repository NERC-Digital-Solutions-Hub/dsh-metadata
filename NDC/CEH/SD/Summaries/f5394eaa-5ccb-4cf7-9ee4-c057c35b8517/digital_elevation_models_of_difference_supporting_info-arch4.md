# Digital elevation models of difference (DoD) for Chamoli avalanche-debris flow landscape change in Uttarakhand, India

- What these data are
  - Digital elevation models of difference (DoD): raster (.tif) datasets that quantify vertical topographic change between two DEM dates.
  - Values: negative = surface lowering (erosion), positive = surface gain (deposition).

- Why these data were collected
  - To support analysis of landscape change after the 7 February 2021 avalanche-debris flow in Chamoli District.
  - To enable numerical modelling with CAESAR-Lisflood (referenced elsewhere in this collection).

- Geographic coverage
  - Area bounded within: approximately WGS 84 / UTM Zone 44 coordinates
    - Top left: 352312 m E, 3385209 m N
    - Bottom right: 384787 m E, 3358896 m N

- Temporal coverage and data generation
  - Base DEMs generated between 10 February 2021 and 27 April 2022.
  - DoDs created on a rolling basis within this window.
  - DoDs produced by subtracting the earlier DEM from the later DEM.

- Data collection and processing methods
  - Software: QGIS (versions 3.18 and 3.24).
  - Procedure: Raster Calculator used to compute DoD for each DEM pair; later DEM minus earlier DEM.
  - Output: DoDs along with interpretation guidance (sign indicates change).

- Provenance and responsibility
  - Project Principal Investigator (PI) created all DoDs and oversaw interpretation.

- Completeness, relevance, and replication
  - Dataset is complete for the DoDs generated as part of this research.
  - Other DoDs could be created from alternative input DEMs within this data collection.
  - Users can replicate the method to estimate significant change thresholds (described in section 5).

- Data quality, units, and significance
  - DoDs are raster/grid data; each pixel holds net elevation change.
  - Data gaps from input DEMs (e.g., cloud cover, photogrammetric reconstruction issues) are reflected in the DoDs.
  - Statistical significance threshold: determined using Pléaides orthoimagery by identifying stable hillside areas and computing a two-sigma DoD uncertainty.
  - Reported two-sigma uncertainty thresholds by period (in meters):
    - 2015-2021 DoD: ±1.11 m
    - 2021-02-10 to 2021-06-06 DoD: ±0.91 m
    - 2021-06-06 to 2021-12-25 DoD: ±0.61 m
    - 2021-02-10 to 2021-12-25 DoD: ±1.14 m
    - 2021-02-10 to 2022-01-27 DoD: ±1.06 m
  - Stable area polygons used for threshold estimation are provided in the data resource.

- Dataset structure and access
  - Included DoD files:
    - 1509_composite_210210_DoD.tif
    - 210210_210606_DoD.tif
    - 210606_211225_DoD.tif
    - 210210_211225_DoD.tif
    - 210210_220127_DoD.tif
  - Stable areas: stable_areas.shp (plus accompanying auxiliary files)
  - Naming convention: YY-MM-DD; the dates indicate the period spanned by each DoD. The 1509 prefix denotes September 2015 (composite) due to the dataset's historical context.
  - File discoverability: DoDs are organized to support replication and further analysis within this data collection.