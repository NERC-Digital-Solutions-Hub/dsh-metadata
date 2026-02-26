# Countryside Survey Environmental Zones 2007

- Purpose and scope
  - Datasets were created to report Countryside Survey results at a sub-GB level, higher than the 45 ITE Land Classes, using aggregations of ITE Land Classes determined from environmental data across 1km squares in Great Britain.
  - The Environmental Zones (EZ) are used to summarize nationwide survey results and support analysis at finer detail than ITE classes, while maintaining a consistent, repeatable methodology.

- Data specifics
  - File contains 8 areas of Great Britain, created by aggregating ITE Land Classes (ITE Land Classification 2007) for Countryside Survey reporting.
  - Columns: Envzone (zone number, numeric) and Description (zone description, text).
  - Resolution: 1 km.
  - Spatial reference: coordinate system British National Grid; projection OSGB36 (Transverse Mercator).
  - Extent: Great Britain (excluding Northern Ireland for this dataset).

- Background and methodology
  - Environmental Zones were developed to report Countryside Survey results at a sub-GB level, derived from repeatable multivariate analyses of environmental data for each 1km square.
  - Zones are aggregations of multiple ITE Land Classes, based on combinations of environmental characteristics.
  - Detailed aggregations are documented in accompanying tables linking ITE Land Class Numbers (2007) to Environmental Zones (EZ1–EZ9).

- Zone naming and geographic coverage
  - EZs are not named from a single parameter; they are hierarchical across Scotland, England, and Wales.
  - Names and zone coverage:
    - EZ1: Easterly Lowlands, England
    - EZ2: Westerly Lowlands, England
    - EZ3: Uplands, England
    - EZ4: Lowlands, Scotland
    - EZ5: Intermediate Uplands and Islands, Scotland
    - EZ6: True Uplands, Scotland
    - EZ7: Northern Ireland (not included in this dataset)
    - EZ8: Lowlands, Wales
    - EZ9: Uplands, Wales

- Associated datasets and provenance
  - ITE Land Classification (2007) (associated dataset)
  - Countryside Survey (overall) (website: www.countrysidesurvey.org.uk)
  - Core references and background materials include:
    - Barr (1998) on the sampling strategy
    - Bunce et al. (1996) on ITE Merlewood Land Classification
    - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Data © NERC - Centre for Ecology & Hydrology (CEH)

- Access, usage, and publishing considerations
  - Data are prepared for reporting survey results and may be published in conjunction with the Countryside Survey outputs.
  - Metadata and provenance are important for reuse, including the ITE class-to-zone mappings and the 1km resolution grid.
  - Citations and licensing should acknowledge CEH/NERC and the Countryside Survey project.

- Data governance considerations for Data Stewards
  - Metadata completeness: ensure clear documentation of the zone-to-ITE-class mappings and the exact version of the ITE Land Classification used.
  - Data lineage and provenance: maintain traceability to Carey et al. (2008) and the ITE classification methodology (Bunce et al. 1996; Barr 1998).
  - Interoperability: ensure consistent coordinate system and projection (OSGB36, British National Grid) across related datasets; preserve the 1km resolution semantics.
  - Versioning and updates: the Zones are based on 2007 data; plan for updates or new editions (e.g., subsequent Countryside Survey rounds) with clear crosswalks.
  - Access and licensing: data are credited to NERC-CEH; ensure proper attribution and compliance with data-sharing policies.
  - Data quality and standardization: validate the zone mappings against published tables; maintain consistency in zone naming and descriptions to avoid ambiguous interpretation.
  - Potential challenges to address
    - Incomplete understanding of all user needs across diverse stakeholder groups.
    - Timely access to updated ITE classifications and zone mappings.
    - Handling multiple systems and formats when integrating with other Countryside Survey datasets.
    - Managing scale and performance considerations when working with nationwide 1km-resolution data.
    - Keeping legacy zone definitions coherent if future surveys re-derive classifications.