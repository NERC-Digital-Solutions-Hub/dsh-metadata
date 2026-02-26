# Broad Habitat Area Estimates by Land Class for Great Britain

- Purpose and scope
  - Provides national estimates of Broad Habitat stock by Land Class for 1978, using the 1990 ITE Land Classification.
  - Estimates are by Land Class and Broad Habitat, enabling assessment of habitat distribution across Great Britain for historical comparison.

- Data assets included
  - CS1978_Estimates_by_LC.csv
    - Contains Year, Land Class, Broad Habitat code and name, Land Class Area (000s ha), Mean Est, Lower and Upper 95% CI estimates.
    - Notes: Broad Habitat codes exclude certain classes (11, 15, 20 mentioned in context); estimates derived from Countryside Survey data and the 1990 ITE Land Classification.
  - CS78_BH1_17.tif
    - Raster representation converting Land Class totals into percentages per 1 km pixel.
    - Each band corresponds to a Broad Habitat class (bands 1–17 excluding 15); pixel size 1 km; British National Grid coordinates (OSGB36).

- Data structure and key fields
  - CSV fields include: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE (000s ha).
  - TIFF bands provide per-pixel percentage allocations for Broad Habitat classes across the raster.

- Spatial and temporal coverage
  - Temporal: Year 1978 data (historical baseline).
  - Spatial: Great Britain; data aligned to British National Grid (OSGB1936) with 1 km pixel resolution.

- Methodology and provenance
  - Data derived from Countryside Survey 1978 with estimates grounded in the 1990 ITE Merlewood Land Classification framework.
  - References provide methodological context for generation of national estimates from 1 km survey squares (e.g., Scott 2007; Bunce et al. 1996/1981; Jackson 2000).

- Practical notes for Data Leaders (alignment with aims)
  - Useful for building a holistic view of habitat stocks across land classes, informing data strategy and governance around land use and biodiversity.
  - Supports co-ownership and collaborative use of a historical habitat dataset; helps identify data availability and gaps (e.g., 1978 baseline, excluded land classes).
  - Provides both tabular (estimates with uncertainty) and spatial (per-pixel percentage) formats for flexible analysis, visualization, and dissemination.
  - Helps prioritise data improvements: data quality, metadata completeness, and harmonization with other datasets; track provenance and ensure traceability.

- Data quality, metadata and limitations
  - Uncertainty expressed via 95% confidence intervals in the CSV.
  - Exclusion noted for certain land classes (e.g., Land Class numbers 15 and 20 in some contexts); 1978 baseline only, which may limit longitudinal analyses without additional years.
  - Raster data requires GIS tools for use; accuracy depends on alignment between Land Class totals and raster bands.

- Access, attribution and licensing
  - Acknowledgement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey ©”
  - All rights reserved; attribution must accompany copies, publications, reports, and presentations.

- Relevant references and resources
  - Countryside Survey website and project reports for methodology and background.
  - Key technical reports: Scott (2007) CS Technical Report No. 4/07; Bunce et al. (1996, 1981) ITE Merlewood Land Classification; Jackson (2000) guidance on Biodiversity Broad Habitat Classification.
  - Data formats and field descriptions provided within the CSV and TIFF documentation.

- Potential use cases for data leaders
  - Baseline for historical habitat change analyses and trend assessment when combined with other years.
  - Informing policy discussions on land management by providing quantified Broad Habitat stocks by Land Class.
  - Supporting data discovery and governance by mapping data lineage, access patterns, and attribution requirements.
  - Planning data integration efforts: aligning this dataset with current land cover datasets, interoperability standards, and metadata schemas.