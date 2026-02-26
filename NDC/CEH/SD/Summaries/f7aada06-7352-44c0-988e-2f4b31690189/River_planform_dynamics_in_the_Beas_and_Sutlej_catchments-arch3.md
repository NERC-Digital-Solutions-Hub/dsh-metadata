# Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system

## Overview
- Evaluates human impacts on river planform through multi-timescale lens (centennial, annual, seasonal, episodic).
- Case study: Himalayan Sutlej-Beas River system.
- Aims:
  - Systematically assess changes in river planform characteristics across multiple timescales.
  - Link observed planform changes to human-environment drivers.
  - Conceptualise geomorphic changes as timescale-dependent evolutionary trajectories.
- Dataset supports these aims with multi-year, multi-section river measurements.

## Study area and temporal coverage
- Rivers: Beas and Sutlej.
- Spatial scope: Beas from Pong Dam to confluence with Sutlej; Sutlej from Bhakra Dam to confluence with Beas.
- Reach structure: Reach 1 (below dams) and Reach 2 (wide plains); Reach 2 subdivided into 4 Beas sections and 5 Sutlej sections.
- Coordinate system: WGS84.
- Extent: West 74.957, East 76.706, North 32.225, South 30.780.
- Temporal span: 1989–2018 for most metrics; historic width from 1847–1850 for comparative context.

## Data components and key variables
- Wet river area (post-monsoon): annually, 1989–2018.
- Active gravel bars: annual, 1989–2018.
- Active channel area: maximum extent 1989–2018.
- Active channel width: annually, 1989–2018.
- Active channel width (historic map): 1847–1850.
- Anabranching index (AI): annually, 1989–2018.

## Methods and data processing
- Wet river area:
  - Derived from Landsat 5–8 imagery (1989–2018) using post-monsoon mNDWI (>0.15).
  - Manual editing to remove stray water pixels; raster-to-polygon conversion to shapefiles; year-by-year features.
  - Calculated for Reaches 1 and 2 and Reach 2 sections.
- Active gravel bars:
  - Red reflectance threshold (>0.16) on post-monsoon imagery used to identify bare gravel bars.
  - Buffers defined by maximum wet river extent; year-by-year shapefiles.
- Active channel area:
  - Aggregation of annual wet river areas to define the multi-year active channel extent.
- Active channel width:
  - Width of the wet area including enclosed gravel bars; calculated every 2 km.
  - Also computed for the 1847 historic map scenario; width measured perpendicular to banks.
  - Mean width computed for Reaches 1 and 2 and Reach 2 sections.
- Anabranching Index (AI):
  - Measures number of active channels separated by bars/islands, using at least 10 cross sections spaced across braid plains.
  - Calculated for Reaches 1 and 2 and Reach 2 sections.

## Data formats and file structure
- Primary formats: ESRI Shapefiles (plus mandatory/optional ancillary files) and CSVs.
- Width data: point features indicating measurement locations with Year and Width attributes.
- Metrics: annual CSVs for Beas and Sutlej (anabranching index, mean width, wet area).
- Topology and definitions: Reaches_sections.shp defines reach/section geometry.

## Quality assurance and validation
- Data derived from landsat spectral data with QA bands to ensure cloud-free imagery.
- Processing conducted by the Cranfield University project team.
- Spot validation against aerial photography to verify results.

## Implications for monitoring frameworks
- Demonstrates a multi-timescale, GIS-based monitoring approach linking physical planform metrics to governance-relevant questions.
- Provides a reproducible workflow for deriving:
  - Wet area, active channel extent, and width across years.
  - Gravel bar dynamics and anabranching structure.
- Emphasizes the need for:
  - Standardized metadata and data-sharing practices.
  - Clear data governance, provenance, and quality checks.
  - Handling data gaps and ensuring timely data access for policy decision-making.

## Limitations and considerations
- Scope constrained to two Himalayan rivers and specific reaches; may affect generalisability.
- Relies on optical remote sensing (cloud-free Landsat data) with potential data gaps due to imagery availability.
- Requires careful metadata management to support future reuse and cross-study comparability.
- Data governance and public sharing considerations noted as potential barriers in broader monitoring contexts.

## References (key context)
- Huang et al. (2018) on surface water detection from space.
- Langat, Kumar, & Koech (2019) on monitoring river channel dynamics with remote sensing and GIS.
- Li et al. (2017) on identifying bare land from Landsat imagery.
- Revenue Survey of India (1852) historic mapping context.
- Vercruysse & Grabowski (2021) foundational study guiding the dataset and its multi-timescale interpretation.