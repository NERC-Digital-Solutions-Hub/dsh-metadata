# Broad Habitat Area Estimates by Land Class for Great Britain

- Purpose and scope
  - National estimates of Broad Habitat stock for 1978, calculated using the 1990 ITE Land Classification; estimates are by Land Class and cover Broad Habitats 1–21, excluding 15 and 20.
  - Aimed at consistent monitoring of environmental health and policy performance over time, with outputs suitable for comparison and scrutiny.
  - Related to measuring habitat change over a 30-year period (as part of the Countryside Survey program and the 1978 data rescue effort).

- Data sources and context
  - Derived from Countryside Survey data (copyright CEH/NERC).
  - Uses the ITE Merlewood Land Classification framework (Bunce et al., 1996; 1981; related publications cited).
  - Publications referenced include: Countryside Survey reports (including 2012 Final Report on 30-year change), CS Technical Reports, and JNCC guidance on Broad Habitat interpretation.

- Data file: CS1978_Estimates_by_LC.csv
  - Purpose: tabular national estimates of Broad Habitat stock by Land Class for 1978.
  - Key columns (with meanings)
    - YEAR: survey year (numeric)
    - LAND_CLASS: ITE Land Class (numeric)
    - BROAD_HABITAT: Broad Habitat code (text)
    - BROAD_HABITAT_NAME: Broad Habitat name (text) from Jackson (2000)
    - LAND_CLASS_AREA: total area of the Land Class (000s hectares)
    - MEAN_ESTIMATE: mean area of Broad Habitat by Land Class (000s ha)
    - LOWER_ESTIMATE: lower 95% confidence interval (000s ha)
    - UPPER_ESTIMATE: upper 95% confidence interval (000s ha)
  - Notes
    - Estimates exclude Broad Habitats 15 and 20.
    - Data are structured to support standardised outputs and downstream analyses.

- Data file: CS78_BH1_17.tif
  - Purpose: raster representation converting Land Class totals for each Broad Habitat into percentages per 1 km pixel.
  - Spatial resolution: 1 km pixels (1000 m).
  - Coordinate system and projection: British National Grid (OSGB36), Transverse Mercator – Great Britain.
  - Coverage and bands
    - Excludes Inland Rock (Band 15) from the dataset.
    - Bands correspond to Broad Habitat classes (16 bands total), including:
      - Band 1: Broadleaved Mixed and Yew Woodland
      - Band 2: Coniferous Woodland
      - Band 3: Boundary and Linear Features
      - Band 4: Arable and Horticulture
      - Band 5: Improved Grassland
      - Band 6: Neutral Grassland
      - Band 7: Calcareous Grassland
      - Band 8: Acid Grassland
      - Band 9: Bracken
      - Band 10: Dwarf Shrub Heath
      - Band 11: Fen, Marsh, Swamp
      - Band 12: Bog
      - Band 13: Standing Open Waters and Canals
      - Band 14: Rivers and Streams
      - Band 15: Inland Rock (excluded)
      - Band 16: Urban
  - Usage note: Each pixel’s value represents the percentage of the Land Class area occupied by the corresponding Broad Habitat category, derived from Land Class totals.

- Spatial and usage details
  - All CS data require acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey ©” rights.
  - Outputs are designed for standardised presentation (e.g., reports, maps, charts) and easy integration into portals/databases to support monitoring programs.
  - The dataset supports cross-year comparisons and aggregation at different geographic scales, aiding assessment of habitat change and policy outcomes.

- How this supports monitoring practice
  - Provides a reproducible, standardised method to quantify Broad Habitat distribution by Land Class for Great Britain.
  - Combines tabular national estimates with a spatial raster representation to facilitate diverse analyses (area summaries, change detection, mapping).
  - Contextualizes 1978 data within the longer Countryside Survey timeline and landscape classification framework, enabling long-term trend assessments.

- References and accompanying information
  - Countryside Survey project overview and methodologies: Countryside Survey website
  - 2012 Final Report: Countryside Survey – Measuring Habitat Change Over 30 Years
  - Technical Reports and field methodologies: CS Technical Report No. 4/07; CS Technical Report No. 1/07 (Field Mapping Handbook)
  - Land Classification framework: ITE Merlewood Land Classification papers (Bunce et al., 1996; 1981)
  - Guidance on Broad Habitat interpretation: Jackson, D.L. (2000)
  - Additional background on data rescue and 30-year change: Wood et al. (2012)

- Access and reuse considerations
  - Data are intended for use within environmental monitoring contexts; ensure proper attribution as outlined above when publishing, presenting, or redistributing outputs.