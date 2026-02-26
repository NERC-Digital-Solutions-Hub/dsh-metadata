# Macroinvertebrate composition of Welsh upland rivers in response to organic matter addition

## Summary at a glance
- BACI experimental design with upstream reference and downstream experimental zones across multiple streams.
- Before period (T1) followed by after period (T2) during which leaf litter was added to the experimental zone to simulate natural organic matter inputs.
- Leaf litter (oak, birch, alder) totalized 1 tonne per stream with additional periodic supplementation after storm events.
- Six Surber net samples collected per reach on five occasions (Jan–May 2013), preserved on-site and processed in the lab.
- Taxonomic identification to species level where possible; body measurements recorded (Size1 and Size2 in mm).
- Data stored as flat CSV files; includes a site description dataset with geographic and catchment information.
- Notable gaps: no explicit quality control steps documented; taxonomic resolution may vary; metadata completeness and data provenance require careful curation for reuse.

## Experimental design and sampling regime
- Design: Before-after-control-impact (BACI) with:
  - Upstream reference zone (control) and downstream experimental zone (manipulated).
  - 20–50 m separation to ensure independence.
- Periods:
  - Before (T1): 61–65 days (early Nov 2012 – early Jan 2013); no manipulation.
  - After (T2): 57–62 days (early Jan – Mar 2013); leaf litter addition in the experimental zone during the entire T2 period.
- Treatment details:
  - One tonne bags of deciduous leaves (oak, birch, alder) distributed proportional to experimental zone area.
  - Vegetable nets maintained to keep a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after storm events.
- Sampling: six random macroinvertebrate samples per stream reach, collected in five sessions (January–May 2013).

## Data collection, processing, and structure
- Collection method:
  - Surber net sampler: area 0.1 m^2, mesh 330 µm, depth 10 cm.
  - Samples preserved on-site in 70% IMS; laboratory processing included rinsing and sorting.
- Taxonomy and measurements:
  - Identification to species level where possible; otherwise to genus, family, or coarser level.
  - Body measurements recorded as Size1 and Size2 in millimeters with a corresponding body part note.
- Data formats:
  - Primary Surber data stored as flatbed CSV with 11 columns:
    - site_code, region, month, time (Before/After), landuse, reach (Experimental/Control), replicate, taxon_name, Size1, Size2, measurement_key, Comment
  - Miscellaneous supporting data: site_description.csv with 10 columns including site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.
- Documentation and provenance:
  - Site description file provides geographic and survey context.
  - Calibration steps and detailed quality controls are not documented.

## Data quality, provenance, and limitations
- Quality control:
  - No explicit quality control procedures described.
  - No calibration steps recorded.
- Taxonomic and measurement constraints:
  - Taxonomic resolution varies (species when possible; otherwise genus/family/coarse levels).
  - No documented validation of identifications or measurement repeatability.
- Metadata completeness:
  - Core metadata included (locations, timing, treatment, sampling method, and measurement units), but explicit data quality flags or lineage/versioning are not described.
- Reproducibility considerations:
  - Clear description of BACI design, leaf litter treatment, sampling schedule, and data fields enables replication, yet the absence of QC documentation should be addressed for robust reuse.

## Data availability and sharing considerations
- Data format:
  - CSV-based datasets (Surber data and site descriptions) suitable for ingestion into standard ecological analysis pipelines.
- Documentation:
  - Supporting site description data enhances geospatial interpretation and context.
- Sharing considerations for data stewards:
  - Ensure persistent IDs for sites and consistent naming conventions across datasets.
  - Provide or reference a data dictionary clarifying column meanings (some column names imply specific semantics, e.g., time, reach, replicate).
  - Consider publishing to a data portal with clear access rights and versioning; attach data quality notes and provenance details.

## Practical guidance for reuse and data governance
- Metadata alignment:
  - Maintain consistent taxon_name fields and ensure resolution options are documented.
  - Standardize units (mm for Size1/Size2) and clearly define measurement methods.
- Temporal and spatial clarity:
  - Preserve explicit Before/After labeling and map experimental vs. control reaches to ensure correct downstream analyses.
  - Use site_description to link macroinvertebrate data to precise geographic coordinates and catchment context.
- Data quality and curation:
  - Implement QC steps (taxonomic validation, measurement repeatability checks) and document them within the data package.
  - Add data quality flags or confidence levels where identifications are uncertain.
- Future governance:
  - Establish data versioning and an update mechanism if datasets are expanded or revised.
  - Create a concise data usage note describing limitations, potential biases (e.g., seasonal sampling, BACI design assumptions), and recommended analyses.

## Key considerations and challenges for Data Stewards
- Potential gaps in user needs and data applicability; ensure metadata captures intended analyses and limitations.
- Timely data availability and coordination with data creators to maintain up-to-date records.
- Heterogeneous data from multiple streams and potential format inconsistencies; plan for standardization.
- Handling large volumes of biological census data alongside environmental context (site descriptions) and ensuring interoperability.
- Ongoing maintenance of embedded documentation (e.g., site_description) to reflect any changes in survey sites or methods.