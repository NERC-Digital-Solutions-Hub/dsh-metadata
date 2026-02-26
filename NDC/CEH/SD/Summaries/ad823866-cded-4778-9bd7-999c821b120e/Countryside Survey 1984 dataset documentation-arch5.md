# Broad Habitat Area Estimates by Land Class for Great Britain 1984

- National estimates of Broad Habitat stock (Habitats 1-17) for 1984 calculated using the 1998 ITE Land Classification, with results provided as total area in thousands of hectares per Broad Habitat per Land Class, including 95% confidence intervals (lower and upper estimates).
- Two data artifacts accompany the dataset:
  - CS1984_Broad_Habitat_Stock.csv: contains tabular stock estimates with the following columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
    - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)
  - cs1984_stock.tif: a 1 km resolution raster where each band represents a Broad Habitat class, and each 1 km pixel contains a mean percentage estimate of habitat cover for that square, derived from 1 km survey squares within each Land Class strata.
- Band-to-habitat mapping information is provided (e.g., Band 2 corresponds to Broad Habitat 2 for certain Habitat combinations; detailed mapping lines are included in the file description).

- Spatial information:
  - Pixel size: 1 km (1000 m)
  - Coordinate system: British National Grid (OSGB36), Projection: Transverse Mercator
  - Extent: Great Britain

- Data provenance and classification:
  - Estimates are grounded in the Countryside Survey 1984 and based on the 1998 ITE Land Classification (Bunce et al.; Scott 2007).
  - Land Class definitions and Broad Habitat classifications are drawn from established sources (ITE Land Classification, JNCC guidance, and related publications listed in the references).

- Usage and attribution:
  - All CS data must be acknowledged; Countryside Survey data are owned by NERC - Centre for Ecology & Hydrology, with copyright and database rights retained.
  - Acknowledgement and copyright notice must accompany all copies, publications, and presentations.

- References and methodological context:
  - Publications and methodological reports related to Countryside Survey methods and classifications are provided (e.g., Scott 2007; Bunce et al. 1996, 1998; Jackson 2000), with links and DOIs included in the dataset documentation.
  - The dataset is a historical snapshot (1984) using the then-current land classification framework and methodologies.

- Data quality and limitations:
  - Estimates include 95% confidence intervals to reflect uncertainty.
  - The raster represents mean percent habitat per 1 km square within Land Class strata, which may mask finer-grained variability.
  - The 1984 data reflect legacy classifications and survey practices; users should consider temporal and classificatory differences when integrating with more recent datasets.

- Governance and stewardship considerations:
  - Metadata and data structure are designed to support discovery and reuse (csv stock file and geospatial tif).
  - The dataset is intended for appropriate governance, with clear provenance, usage rights, and citation requirements.
  - Data sharing and reuse should maintain the classification lineage (ITE Land Classification) and acknowledge the Countryside Survey provenance.