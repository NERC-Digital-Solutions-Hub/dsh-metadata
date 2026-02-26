# Supplementary supporting document for dataset: Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK.

## Summary
- Provides maps of field sites and plot layouts for experimental meadow plantings in two UK urban areas.
- Functions as supplementary to the primary experiment documentation and data files (referenced in F3UES_meadows-expt_supporting-document-for-data.rtf).
- Details how plots are arranged across multiple sites and how treatments map to individual plots, aiding GIS-based visualization and analysis.

## Spatial content
- Contains site-level names and layouts:
  - Bedford – Chiltern Avenue
  - Bedford – Brickhill Heights (additional plots at Robin Hill)
  - Bedford – Robin Hill (additional plots at Brickhill Heights)
  - Bedford – Goldington Green
  - Bedford – Jubilee Park
  - Luton – Bramingham Rd
- For each site, plots are numbered (Plot 1–10) with corresponding treatment codes.
- Some sites include “additional plots” or location annotations (e.g., @Robin Hill), indicating plots in sub-sites or neighboring areas.
- Provides a mapping structure intended for integration into GIS visuals (plots linked to treatments across sites).

## Data organization and contents
- Plot-level layout information is organized by site with explicit plot-to-treatment mappings.
- Treatments are coded (e.g., F, C, B, I, A, G, H, E, D, CONTROL) and linked to specific plots within each site.
- The document uses a consistent plot-numbering scheme per site, though some sites reference multi-location arrangements (e.g., additional plots at Robin Hill or Brickhill Heights).

## Data sources and accessibility
- Primary experiment documentation and data files are located in F3UES_meadows-expt_supporting-document-for-data.rtf.
- This supplementary file focuses on the spatial arrangement and plot layout rather than primary biodiversity measurements.

## GIS considerations and guidance
- Suggested GIS workflow:
  - Create a geospatial layer for sites (polygons or cadastral footprints) and a separate layer for plots (points or centroids) with attributes: site_name, plot_id, and treatment_code.
  - Normalize treatment codes across sites to ensure consistent interpretation (watch for inconsistencies like “@Robin Hill” designations).
  - Link plot records to the main dataset (biodiversity metrics) via plot_id or a composite key.
  - Where coordinates are not provided, extract approximate plot centroids from the included maps or from the primary documentation.
- Data quality and harmonization notes:
  - Data are distributed across multiple locations and sub-sites; verify cross-site treatment mappings.
  - Some plots are described with references to additional locations or hashtags (@), which may require clarification during GIS integration.
  - Ensure resolution and alignment are consistent when merging with other biodiversity or environmental layers.
- Practical outputs:
  - GeoJSON or Shapefile layers for plots and sites.
  - Labeling schemes that show Plot 1–10 and their treatments per site.
  - Metadata documenting data provenance (link to the primary document) and any site-specific notes.