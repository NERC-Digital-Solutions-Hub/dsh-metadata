# Rigg Foot topographical survey data, Sourhope Field Experiment Site, Scotland [Soil Biodiversity Programme] Mick Whelan and Stuart Bradley (University of Stirling)

## Overview
- Context: Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope, focusing on soil biodiversity and ecological processes within a large field experiment.
- Purpose for data stewards: Provide topographic data to support linking soil biodiversity studies with site topography; raw data and maps are available for integration with other datasets.

## Data Collected and Study Site
- Site: Sourhope Field Experiment Site, Scottish Borders (Grid NT8545019630).
- Survey period: April 4–6, 2000 and May 11–12, 2000.
- Methods: Topographic survey using Leica Geosystems Total Station EDM; initial processing and re-orientation with LISCAD.
- Primary investigators: Mick Whelan and Stuart Bradley, Department of Environmental Science, University of Stirling.

## Data Files and Content
- Rigg_foot_Topographic.csv
  - Content: Original x-y-z coordinates (metres) with an arbitrary altitude datum.
  - Coordinate orientation: Bottom-left corner of plot 1A at 1000,1000; y-axis aligned upslope.
  - Descriptions and units included for x, y, z; Easting/Northing approximate OSGB 1936 references.
  - Includes location notes for survey points.
- Rigg_foot_Topographic_newgrdxyz.csv
  - Content: Regular grid across the site at 25 cm intervals with interpolated altitude values.
  - Format: x-y-z coordinates on a 25 cm cell grid, interpolated from a TIN; ASCII grid exported via ArcInfo GRID, saved as CSV.
  - Descriptions and units similar to original coordinates; oriented to the same bottom-left reference.
- Documentation notes
  - Two site level maps (drafts) showing overall topography; sub-plot boundaries within each treatment appear in the later Rigg_Foot_Topo_maps.pdf.

## Documentation and Provenance
- Authorship: Mick Whelan and Stuart Bradley (University of Stirling).
- Background context: Part of the NERC Soil Biodiversity Programme; fields and plots used to study soil biota, including microbes, microfauna, meso-/macro-fauna, and related ecological processes.
- Related materials: Interim contour maps available; higher quality maps with sub-plot boundaries available in Rigg_Foot_Topo_maps.pdf.

## Quality, Limitations, and Usage Notes
- Quality assurance: Data have undergone QA procedures; however, NERC cannot warrant the accuracy of the data or determine fitness for any particular use.
- Liability: NERC Soil Biodiversity Programme cannot be held responsible for inaccuracies, losses, or any outcomes from data use.
- Datum and coordinates: Altitude datum is arbitrary; coordinate references include OSGB 1936 approximations for Easting/Northing and a defined 1000,1000 origin for plot alignment.

## Access, Formats, and Preservation
- Access: Data are provided as downloadable CSV files (raw and gridded/topographic grid).
- Formats: CSV for both raw and gridded data; ArcInfo GRID-derived interpolation used in preparation of the gridded dataset.
- Map availability: Draft site maps available; final/maps with sub-plot boundaries in Rigg_Foot_Topo_maps.pdf.
- Reproducibility: Original processing used Leica Total Station data and LISCAD; gridding involved ArcView 3.1 and ArcInfo GRID utilities.

## Data Stewardship Considerations and Recommendations
- Metadata completeness: Ensure metadata includes site reference, survey dates, instrument, processing software, coordinate system, datum, grid cell size, and provenance.
- Data quality notes: Maintain clear QA history and caveats regarding accuracy; include the liability disclaimer with data portals.
- Formats and longevity: Preserve raw CSV and gridded CSV alongside original survey files; include migration plans for obsolete software (ArcView 3.1, ArcInfo GRID) to current GIS formats.
- Licensing and access: Document usage rights and any restrictions; link to related publications and maps (Rigg_Foot_Topo_maps.pdf).
- Linkage and interoperability: Maintain cross-references to site maps and associated biodiversity datasets to support integrated analyses of soil biota vs. topography.
- Versioning and updates: Establish version control and update mechanisms for revised topographic data or improved maps, ensuring users can access both raw and processed datasets.