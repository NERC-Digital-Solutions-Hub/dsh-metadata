# Rigg Foot topographical survey data, Sourhope Field Experiment Site, Scotland [Soil Biodiversity Programme]

- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on linking soil biodiversity with ecological processes at Sourhope, Scottish Borders. The Sourhope site hosted a large field experiment with 24 projects studying soil structure, processes (e.g., carbon and nitrogen cycles), and flora/fauna across micro- to macro-fauna.
- A topographic survey was conducted at Sourhope in April–May 2000 (with a follow-up in May 2000) by Mick Whelan and Stuart Bradley (University of Stirling) to map site topography for data integration with biomass, diversity, and other soil studies.
- Purpose of the survey: provide raw and gridded topographic data to support matching with other site data, analysis, and comparative mapping.

## Data files

- Rigg_foot_Topographic.csv
  - Contains original survey data: x, y, z coordinates in metres with an arbitrary altitude datum.
  - Coordinate system notes: x-y origin set so the bottom-left corner of plot 1A is at (1000, 1000); y axis aligned upslope along plot boundaries.
  - Units: metres; z is altitude relative to the arbitrary datum.
  - Includes notes on survey point locations and approximate OSGB 1936 coordinates (Easting/Northing).

- Rigg_foot_Topographic_newgrdxyz.csv
  - Regular grid across the site at 25 cm intervals with interpolated altitude values.
  - Data represent x-y-z coordinates on a regular grid (cell size ~0.25 m).
  - Grid construction: interpolations from a Triangulated Irregular Network (TIN) of survey points; ASCII grid exported via ArcInfo GRID (ESRI) and saved as CSV.
  - Units: metres; origin and orientation consistent with the raw data.

## Site Level Maps

- Two draft contour maps provide an overall view of the Sourhope site topography.
- Interim results; higher-quality maps with sub-plot boundaries within each treatment are available in Rigg_Foot_Topo_maps.pdf.

## Data quality, usage, and liability

- Data have undergone quality assurance procedures; however, NERC cannot warrant the accuracy of the data.
- NERC disclaims responsibility for determining fitness for a user’s purpose; no liability for loss, damage, or use consequences.
- Data can be matched with other site data (e.g., biomass, diversity), or analysed in more detail with the raw and gridded coordinates, but users should verify suitability for their specific needs.

## Access, provenance, and metadata

- Original survey conducted using a Leica Geosystems Total Station EDM; initial processing and re-orientation performed with LISCAD.
- Provides detailed descriptions of coordinate definitions, datum, and axis orientation to aid discoverability and reuse.
- Authors and institution: Mick Whelan and Stuart Bradley, Department of Environmental Science, University of Stirling; Sourhope Field Experiment Site, Scottish Borders.
- Data availability includes both raw coordinates and a regularly gridded dataset, plus preliminary maps; more refined outputs are available in accompanying PDFs.