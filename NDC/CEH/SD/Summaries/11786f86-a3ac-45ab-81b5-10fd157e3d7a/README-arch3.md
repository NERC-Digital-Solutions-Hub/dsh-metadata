# Bank strength measurements in the Amazon River, September to October 2022

## Purpose and scope
- Presents a repository of pre- and postprocessed data collected from field measurements and satellite imagery of the Solimões (Amazon) River, published in the referenced DOI.
- Aims to support environmental health monitoring through bank strength, channel morphology, and erosion/deposition analyses across multiple scales and timeframes.

## Data types and contents
- 1) Bank strength measurements
  - Sep 25–Oct 8, 2022 for a 100 km reach around Tefé (coordinates 64 42'30" W, 3 21' S).
  - Location metadata in Measurement_locations.csv: location IDs, bank type, sediment type, GIS river kilometer.
  - CSM_measurements_test3.csv: location ID, bank type, sediment type, test setting, mean critical shear stress, mean shear strength (kPa).
  - Shear vane measurements saved per location; accompanying Figure2_LSV_CSM_violin.py for violin plots.
- 2) Satellite imagery (Landsat)
  - Postprocessed Landsat data in SHP format; water/land classifications for 1984–1988 and 2019–2023 along three 30–65 km reaches.
  - Data converted to 20 m grid TIFFs; segments defined as 10 km (reach 3) and 20 km (reaches 1–2).
  - Segment shapes include FID/OBJECTID; RiverKM, Depth (m), Width (m), Qrockbank (m), QrockBed (m) as attributes; analyses based on visual observations and FABDEM.
- 3) Corona imagery (1967)
  - USGS-provided Corona image for a 100 km reach around Tefé; stitched into TIFF with RGB bands.
  - Digitized bank and bar lines provided as polylines (SHP) with FID IDs.
- 4) GIS_analysis
  - GWSE-based calculations for ~1,600 km upstream of Manaus.
  - 5-km reaches with separate calculations for right and left banks.
  - Mean annual erosion and deposition distances derived by aggregating 10-km reach polygons over 37 years; results plotted as histograms via Python.
- 5) Multibeam echo sounder data (MBES)
  - Cleaned and postprocessed for a 2 km reach at river kilometer 688 (Manaus region).
  - Outputs include adjusted trajectory files and corrected bathymetric LAZ point clouds.
  - Processing uses GGMatch for strip alignment and BathyQC for final postprocessing; data gridded to 50 cm and 25 cm resolutions; bands are RGB.

## Data formats, access, and documentation
- Formats include CSV, SHP, TIFF, and LAZ; coordinates primarily in WGS 84.
- Includes scripts and tools for visualization (e.g., violin plots) and references methodological sources (e.g., Boothroyd et al., 2020 for Landsat-based classifications).
- Data repositories and file naming conventions provide traceability from raw measurements to postprocessed products.

## Processing and analytical approaches
- Field measurements (CSM) with location- and sediment-based metadata to derive bank strength indicators.
- Landsat-based land-water classification across multiple epochs to assess river channel changes and reach morphology.
- Corona imagery used to complement historical channel delineation and bank lines.
- GWSE-derived erosion/deposition metrics over long timescales to quantify large-scale morphological change.
- MBES data processed to obtain high-resolution bathymetry, with rigorous trajectory corrections to minimize geometric errors.

## Relevance to monitoring frameworks
- Delivers a multi-faceted data package that supports monitoring of environmental health indicators such as bank strength, channel dynamics, and sediment transport.
- Demonstrates end-to-end data management: acquisition, postprocessing, metadata detailing, and visualization-ready outputs.
- Addresses data lineage and reproducibility through explicit file structures, processing steps, and accompanying scripts.

## References and provenance
- Methodological linkage to Boothroyd et al. (2020) for Landsat-based river analysis techniques.
- The repository aggregates field measurements, satellite-derived classifications, historical imagery, and high-resolution bathymetric data to enable integrated monitoring and policy-relevant evaluations.