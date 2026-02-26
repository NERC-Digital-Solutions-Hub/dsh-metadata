# Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system

- The dataset is described and analysed in Vercruysse and Grabowski (2021), examining human impacts on river planform in the Himalayan Sutlej-Beas system across centennial, annual, seasonal, and episodic timescales.
- Objectives:
  - Systematically assess changes in river planform characteristics across multiple timescales.
  - Link observed planform changes to human-environment drivers and interactions.
  - Conceptualise geomorphic changes as timescale-dependent evolutionary trajectories.

## Scope and Spatial Extent

- Rivers: Beas and Sutlej.
- Study reach structure:
  - Beas: Pong Dam to confluence with Sutlej; divided into Reach 1 (below the dam) and Reach 2 (plains).
  - Sutlej: Bhakra Dam to confluence with Beas; divided into Reach 1 (below the dam) and Reach 2 (plains).
  - Reach 2 subdivided into four sections for Beas and five sections for Sutlej.
- Coordinate system: WGS84.
- Spatial bounds: West 74.957, East 76.706, North 32.225, South 30.780.

## Data Components (six primary datasets)

- Wet river area (post-monsoon): annually, 1989–2018.
- Active gravel bars: annually, 1989–2018.
- Active channel area: maximum extent 1989–2018.
- Active channel width: annually, 1989–2018.
- Active channel width from historic map: 1847–1850.
- Anabranching index (AI): annually, 1989–2018.

## Data Details and Methods

- Wet river area:
  - Source: Landsat 5–8 imagery (post-monsoon Oct–Dec).
  - Method: mNDWI threshold > 0.15 to separate water from land; manual pixel cleaning; converted to polygon shapefiles.
  - Scope: applied to Reaches 1 and 2 and all sections within Reach 2; annual features exist per year.
- Active gravel bars:
  - Source: Landsat 5–8 reflectance (red channel) for bare gravel bars with reflectance > 0.16 (post-monsoon).
  - Scope: pixels within the wet river area buffer; annual gravel bar features created.
- Active channel area:
  - Derived by aggregating annual wet-area shapefiles (1989–2018) to define the union of wetted areas across years.
- Active channel width:
  - Definition: width of the wet area including gravel bars enclosed by water.
  - Measurement: automatically calculated every 2 km; also derived from the 1847 historic map (The Trans-Sutluj Division, 1847–1852) with widths measured perpendicular to the riverbank.
  - Summary: mean width computed for Reaches 1 and 2 and each section in Reach 2; annual values stored.
- Anabranching Index (AI):
  - Definition: number of active channels separated by bars/islands, measured across at least 10 cross sections (spaced by one braid-plain width).
  - Scope: computed for Reaches 1 and 2 and each Reach 2 section; annual index values recorded.
- Metadata and references:
  - See Vercruysse and Grabowski (2021) for methods and citations (remote sensing, mNDWI, gravel-bar detection, historic map use).

## Data Format and File Organization

- Primary formats:
  - ESRI Shapefiles (with mandatory/optional accompanying files) for spatial data.
  - CSV files for annual metrics (AI, mean active channel width, wet river area).
- Key files:
  - Beas/Sutlej wet river area shapefiles per year.
  - Active gravel bars shapefiles (annual).
  - Beas/Sutlej active channel area shapefiles.
  - Beas/Sutlej width annual shapefiles.
  - Historic width shapefiles (1847 for Beas and Sutlej).
  - Metrics_Annual Beas and Metrics_Annual Sutlej CSVs.
  - Reaches_sections.shp detailing reach and section definitions.

## Quality Control and Validation

- Data sources include Landsat spectral data with QA bands to ensure cloud-free imagery.
- Verification through spot checks against aerial photography.
- Project team at Cranfield University conducted data quality checks at all processing stages.

## Temporal Coverage and Scale

- Time range: 1989–2018 for most datasets; a single historic map period (1847–1850) for comparative width.
- Temporal resolution: annual measurements for most variables; fixed historic map reference for width.

## Usage Notes for Analysts

- The dataset enables analysis of centennial to annual-scale river planform changes and their drivers, supporting correlations with human activities and environmental factors.
- The combination of wet-area, gravel-bar, active channel extent, width metrics, and AI across two major Himalayan rivers allows cross-scale evolutionary trajectory assessments.
- Data are organized to facilitate reproducibility, cross-referencing across reaches, sections, and years; use the Metrics_Annual CSVs for quick cross-year comparisons and shapefiles for spatial analyses.

## References

- Huang et al. (2018) on water detection from space using optical sensors.
- Langat, Kumar, & Koech (2019) on river channel dynamics using remote sensing and GIS.
- Li et al. (2017) on automatic mapping of bare land from Landsat imagery.
- Revenue Survey of India (1852) The Trans-Sutluj Division map (historic width reference).
- Vercruysse & Grabowski (2021) Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system. Geomorphology.