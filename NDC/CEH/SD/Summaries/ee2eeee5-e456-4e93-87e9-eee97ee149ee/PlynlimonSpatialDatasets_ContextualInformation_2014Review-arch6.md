# Plynlimon Spatial datasets

- Overview and aim
  - The Plynlimon experimental catchments, established in the late 1960s by the Institute of Hydrology (IH, part of NERC) and now part of CEH, were designed to study how upland land use affects catchment water availability, flooding, and low flows.
  - Located at the headwaters of the River Severn and River Wye in mid-Wales, the two catchments represent the dominant upland land uses: coniferous forestry and sheep-grazed grassland.
  - Intensively instrumented; long-term climatic, streamflow, and soil moisture data, plus surveys of topography, soils, vegetation, and land use underpin the datasets.

- Data layers (spatial datasets)
  - Catchment and subcatchments boundaries (PlynlimonCatchments.shp) — British National Grid; defines upland catchments and subcatchments drained by major tributaries.
  - River network (PlynlimonRiverNetwork.shp) — includes stream segments with upstream/downstream orientation, length, catchment, and type (natural vs. artificial).
  - Spot heights (PlynlimonSpotHeight.shp) — elevation points (HEIGHTS in metres).
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp) — 10 and 20 m contour intervals (HEIGHTS).
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp) — 10 m contour intervals (HEIGHTS); derived from HUNTING SURVEY data.
  - Soil Parental Materials (Plynlimon_SoilParentalMaterials) — soil type codes and descriptions.
  - Vegetation map (Plynlimon_VegetationMap2013) — updated vegetation classifications reflecting 2013 field checks and aligning with CEH Land Cover Map 2000 (LCM2000) categories; includes variants to accommodate coniferous woodland vs. felled/new plantation.
  - Hydrologically corrected elevation data
    - Plynlimon DEM (Plyn_DEM) — GRID, 15 m cell size, floating point, British National Grid; hydrologically corrected digital terrain model (DTM) created from a hydrologic flow-aware analysis.
  - Additional context and notes
    - The datasets build on 1:5,000 scale topographic maps (1967–1968) and subsequent digitisation of elevation, boundaries, and networks (late 1990s).
    - A separate Severn contour dataset has provenance tracing to Edinburgh University digitisation efforts; manual editing was undertaken to ensure clean contour lines.

- Data creation and GIS workflow
  - Topography sources
    - 1:5,000 and 1:10,000 scale topographic maps derived from a 1967–1968 Hunting Survey aerial photography project.
    - Photogrammetric processing provided elevation, contours, catchment boundaries, and river networks.
  - Digitising and data capture
    - Most layers digitised at CEH using CALCOMP digitising tablets; ground control points (GCPs) used to register maps; elevation points and contour lines captured at 10 and 20 m intervals and saved as ArcInfo coverages.
    - Severn contour lines captured at Edinburgh University; later converted from irregular point sequences to line features.
  - Hydrologically corrected DEM
    - Integrated 1:5,000 contours, spot heights, stream networks, and catchment boundaries.
    - Generated a TIN, from which a hydrologically corrected DEM (Plyn_DEM) was produced.
  - Vegetation mapping workflow
    - Draft vegetation map created by interpreting 2009 aerial imagery (Next Perspectives) with broad classes.
    - Field checks (2013) refined classes; alignment with LCM2000 categories; updated to accommodate variations in coniferous plantations through a Variants field.
  - Data editions and updates
    - Soil Parental Materials map originally from Bell (1969), IH Report No. 8; CEH published an updated version in 2005.
    - Vegetation map updated in 2013 to reflect ground truthing and 2009 imagery, with 2013 field verification.
  - File formats and projection
    - Shapefiles for vector layers; DEM in GRID format; all data referenced to British National Grid.

- Data sources and provenance
  - Hunting Survey (1967) aerial photography underpins the topographic maps and initial spatial datasets.
  - Soil Hydrology study (Bell, 1969) provides the soil parental materials layer; updated CEH version published in 2005.
  - Vegetation data drawing on CEH Land Cover Map 2000 (LCM2000) as a basis for consistency with CEH models.
  - Appendix A documents the Hunting Survey technical details; film negatives are lost but printed frames have been digitised and rectified.

- Access, usage, and limitations
  - Some datasets are not available due to data rights or loss (e.g., some field surveys historically conducted may be held by other organisations or have not been retained).
  - The LCM2000-based vegetation map was chosen to avoid IP conflicts with newer datasets (LCM2007); LCM2000 classes have been updated to better reflect local vegetation types.
  - Data and related publications are accessible via CEH resources (CEH website and CEH publications pages).

- Applications and context
  - The spatial datasets support hydrological and environmental analyses of land-use effects on rainfall-runoff processes, river networks, and soil-vegetation interactions in upland catchments.
  - The vegetation and soil layers enable geostatistical analyses (e.g., soil carbon studies) in conjunction with SoilTrEC project data.
  - The hydrologically corrected DEM provides a reliable base for hydrological modelling and terrain analysis within the Plynlimon catchments.

- Key references
  - Brandt, C., Robinson, M., Finch, J.W. (2004). Anatomy of a catchment: the relation of physical attributes of the Plynlimon catchments to variation in hydrology and water status. Hydrol. Earth Syst. Sci., 8, 345-354.
  - Bell, J.P. (1969). The Soil Hydrology of the Plynlimon Catchments. Institute of Hydrology Report No. 8.
  - CEH publications on Soil Hydrology and Vegetation datasets; CEH website for dataset access and associated publications.