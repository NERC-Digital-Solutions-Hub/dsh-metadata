# Plynlimon experimental/research catchments

## Aim and context
- Established in the late 1960s by the Institute of Hydrology (NERC) to study how land use affects catchment water availability, flooding, and low flows downstream.
- Located in mid-Wales as adjacent catchments representing two main upland land uses: coniferous forestry and sheep-grazed grassland.
- Feature long-term, intensive instrumentation and climatic, hydrological, and soil moisture records from the late 1960s.
- Datasets support understanding evaporation differences, hydrology, and land-use impacts across the Severn and Wye headwaters.

## Data and datasets
- Spatial layers included:
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye and Severn catchment contour lines
  - Soil parental materials
  - Vegetation map
- Hydrologically corrected elevation grid (DTM/DEM)
  - Plyn_DEM: 15 m grid, British National Grid, floating-point cells
- Data status and provenance:
  - Some datasets are unavailable or owned by other organisations; some have been lost.
  - Key soil hydrology work: Bell, J.P. 1969 (IH Report No. 8); revised/updated CEH 2005 version available.
- Vegetation mapping (2013 update)
  - Based on CEH Land Cover Map 2000 (LCM2000) with updates to include heath, bracken, and improved grassland.
  - Derived from 2009 aerial photography with 2013 field verification; mapped in ArcGIS 10.1.
  - Classes aligned with LCM2000; included a Variants field to reflect conifer plantation statuses (coniferous woodland, felled, new plantations).

## Source maps and digitising
- Initial topographic maps produced from the Hunting Survey aerial photography (1967).
- In the late 1990s, maps digitised into GIS:
  - Elevation, catchment boundaries, river networks, and related layers created from 1:5000/1:10000 maps.
- Data capture and registration:
  - Ground control points (GCPs) used during digitising; Arcinfo (coverage) formats used for most datasets.
  - Severn catchment contour lines digitised at Edinburgh University from 1:5000 maps; converted to lines from point data.

## Creation of the hydrologically corrected elevation model
- Integration of:
  - 1:5,000 contour maps (photogrammetric origin)
  - Spot heights
  - Stream maps
  - Catchment boundaries
- Processed in Arcinfo to create a TIN and a hydrologically corrected DEM (Plyn_DEM):
  - DEM: 15 m cells, British National Grid, hydrologically corrected for catchment analysis.

## Datasets and their attributes (highlights)
- Catchment boundaries: PlynlimonCatchments.shp
  - Attributes: Catchment, Subcatch (names)
- River network: PlynlimonRiverNetwork.shp
  - Attributes include FNODE_, TNODE_, LENGTH, Catchment, Type (natural or artificial)
- Spot heights: PlynlimonSpotHeight.shp
  - Attribute: HEIGHTS (elevation in metres)
- Wye elevation contours: Plynlimon_WyeElevationContours.shp
  - Attribute: HEIGHTS (metres)
- Soil parental materials: Plynlimon_SoilParentalMaterials
  - Attributes: SOIL (code), Descript (description)
- Vegetation map: Plynlimon_VegetationMap2013
  - Attributes: id, VegClass (description), Varients (subclass description)
- Severn elevation contours: Plynlimon_SevernElevationContours.shp
  - Attribute: HEIGHTS (metres)

## Vegetation mapping methodology and purpose
- Rationale: Update LCM2000 to better reflect heath, bracken, improved grassland, etc., for SoilTrEC soil carbon work.
- workflow:
  - Draft class map from 2009 Next Perspectives aerials
  - On-screen digitising in ArcGIS 10.1 with aerial backdrop
  - Field verification during 2013 surveys; differences documented
  - Refinement to align with LCM2000 classes; conifer plantations reclassified or distinguished via Variants
- Final product supports geostatistical analyses and model inputs requiring updated vegetation boundaries.

## Appendix A: Hunting Survey
- Aerial photography conducted by Hunting Survey Ltd in June 1967.
- Film negatives are lost; digitised copies of prints exist with footprints shown.
- Provides historical context for the base topographic data and frame references.

## Data governance, openness, and monitoring implications
- Data quality and usability depend on metadata completeness, data ownership, and openness.
- Some datasets are not readily accessible or openly shared due to provenance or rights, potentially limiting rapid reuse.
- Ensuring data standards, provenance, and up-to-date maintenance is critical for monitoring frameworks evaluating environmental health and informing policy decisions.