# Broad Habitat Area Estimates by Land Class for Great Britain

- Overview
  - National estimates of Broad Habitat stock (Habitats 1-21, excluding 15 and 20) for 1978, derived using the 1990 ITE Land Classification.
  - Estimates are provided by Land Class and Broad Habitat, enabling analysis of habitat distribution by land classifications.

- Data Content
  - CS1978_Estimates_by_LC.csv
    - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha)
    - Scope: 1978 national estimates by Land Class (ITE Merlewood classification) for Broad Habitats.
  - CS78_BH1_17.tif
    - Raster dataset created by converting Land Class Broad Habitat totals to percentages per 1 km pixel.
    - Each band corresponds to a Broad Habitat class (except 15); Band mapping includes: 
      - Band 1 Broadleaved Mixed and Yew Woodland
      - Band 2 Coniferous Woodland
      - Band 3 Boundary and Linear Features
      - Band 4 Arable and Horticulture
      - Band 5 Improved Grassland
      - Band 6 Neutral Grassland
      - Band 7 Calcareous Grassland
      - Band 8 Acid Grassland
      - Band 9 Bracken
      - Band 10 Dwarf Shrub Heath
      - Band 11 Fen, Marsh, Swamp
      - Band 12 Bog
      - Band 13 Standing Open Waters and Canals
      - Band 14 Rivers and Streams
      - Band 15 Inland Rock
      - Band 16 Urban
    - Pixel size: 1 km; Coordinate system: British National Grid; Projection: Transverse Mercator Great Britain.

- Formats, Access, and Attribution
  - Data formats: CSV and TIFF (raster).
  - Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©, all rights reserved.
  - Usage notes: Include the specified acknowledgement in all copies, publications, and presentations.

- Spatial Information
  - Coverage: Great Britain.
  - Projection: OSGB1936 (British National Grid); Resolution: 1 km pixels for raster data.

- Provenance, Methodology, and References
  - Data provenance: Based on Countryside Survey 1978 data rescue and analyses described in related reports.
  - Key references:
    - Countryside Survey: Measuring Habitat Change Over 30 Years (2012)
    - Scott, W.A. (2007) CS Technical Report No. 4/07 (Statistical methods for national estimates)
    - Bunce et al. (1996, 1981) ITE Merlewood Land Classification
    - Jackson (2000) Guidance on Broad Habitat Classification
  - Additional CS resources: Countryside Survey website and field mapping methodology reports (1/07).

- Data Quality, Uncertainty, and Limitations
  - 1978 baseline estimates with 95% confidence intervals (lower and upper estimates) provided for MEAN_ESTIMATE.
  - Data are subject to uncertainties inherent in historical surveys and Land Classification mappings (ITE 1990 framework).
  - Certain Broad Habitat types are excluded in the dataset (Habitat 15 and 20 in the raster; 15 omitted in the raster band mapping).

- Practical Considerations for Data Leaders
  - Data discovery: CS datasets are spread across CSV and TIFF formats; ensure proper metadata and lineage are maintained.
  - Data stewardship: Maintain clear attribution, versioning (Versioned: 1), and alignment with ITE Land Classification references.
  - Use cases: National-scale habitat stock estimation by land class; spatial distribution via 1 km raster for visualization and analysis; crosswalks to other habitat classifications via referenced methodologies.
  - Community collaboration: Leverage linked methodological reports to ensure consistent interpretation and re-use across projects.