# Supporting documentation

- Purpose: describes a dataset of hemispherical canopy photographs used to estimate leaf area index (LAI) at plot level within the Nordeste project, focused on the Caatinga biome in northeast Brazil.
- Context: integrates Brazilian and UK research to address biodiversity and ecosystem-function research gaps in seasonally dry vegetation; aims to inform conservation and future climate-related studies.

## Data Content

- Photographs: hemispherical images (NIKON D100 with Sigma 4.5 mm fisheye lens) used to derive LAI values.
- Coverage: data from 12 plots (sites) with ~36 photos per site, and 14 plots with ~50 photos per site (totaling 1,132 photos and ~2,607.8 MB).
- File details: JPEG (jpg) images; total metadata includes per-site counts, file sizes, and capture dates.
- Per-site metadata (examples): plot name, location (state, country), latitude, longitude, number of photos, file size, and capture date.
- Spatial reference: coordinates provided for each plot; suitable for GIS mapping of plot locations and LAI visualization.

## Methods and Processing

- LAI estimation: derived indirectly from hemispherical photographs; photos processed to yield a representative LAI value for the entire plot (not individual subplots).
- Photography protocol: one photo per intersection of four subplots under overcast conditions; at some sites, one photo at the center of the subplot; camera height ~1 m; top of camera oriented north.
- Data collection window: March 2017 to August 2019.
- Instrument specifics: Nikon D100 with a Sigma 4.5 mm fisheye lens.

## Spatial and Temporal Coverage

- Location: Caatinga biome, northeast Brazil.
- Sites: 12–14 plot sites (two dataset configurations described: 12-site and 14-site arrays); site codes include BTI_01, CGR_01, CJU_01, GBR_01/02, IBD_01/02, JUV_01, PET_01, MCS_01/02, MOR_01/02, PAT_01/02, PSC_01/02/03, SJA_01, SDA_01/02/03, SER_01.
- Temporal notes: photos taken across 2017–2019; some MOR site dates appear to be recorded twice or have inconsistent date metadata (and some JPG dates may be incorrect, reflecting 2017 data).

## Data Quality and Provenance

- Strengths: geolocated plot positions; standardized photography protocol; explicit placeholder for LAI at plot level; detailed per-site metadata.
- Limitations and issues:
  - Some plots (e.g., MOR) have two dates; dating inconsistency in metadata.
  JPG date metadata may be incorrect for certain images.
  Data assembled from multiple sites with varying counts and occasional trigger issues or weather-related gaps.
- Provenance: Nordeste project collaboration (Brazilian and UK researchers) focused on Caatinga biodiversity and ecosystem-function relationships.

## GIS Usage and Integration Considerations

- Potential GIS products:
  - LAI map layer at plot level for the Nordeste Caatinga region.
  - Spatial dataset linking LAI estimates to plot polygons or centroids using provided coordinates.
  - Temporal analyses if date metadata are reconciled and cleaned.
- Data integration:
  - Combine LAI values with soil, climate, and vegetation type layers to model biomass, productivity, or ecosystem function.
  - Harmonize plots with different counts (12-site vs 14-site configurations) for consistent analysis.
- Data standards:
  - Rely on per-site attributes (name, coordinates, date, photo count, file size) to build robust GIS metadata records.
  - Address date inconsistencies and verify image capture dates before time-series analyses.

## Known Issues and Considerations for Use

- Date accuracy: some photos have incorrect capture dates; MOR site dates appear twice, and overall metadata may require cleaning for precise temporal analyses.
- Resolution/scale: LAI is a plot-level representative value, not subplot-level; ensure map scales reflect this when visualizing at finer resolutions.
- Data packaging: large datasets with many photos per site; consider chunking or subsetting for practical GIS processing.

## Summary for GIS Specialists

- This dataset provides geolocated hemispherical photographs and derived plot-level LAI estimates in the Caatinga region, suitable for creating map-based representations of vegetation structure and for integrating with climate and soil data in GIS workflows.
- Key actions for GIS use:
  - Validate and reconcile date metadata; standardize to a common temporal frame.
  - Import per-site coordinates to create plot polygons or centroids and attach LAI values.
  - Use image-derived LAI values as a thematic layer, with attention to plot-level aggregation.
  - Document data provenance and any metadata corrections to maintain traceability in GIS analyses.