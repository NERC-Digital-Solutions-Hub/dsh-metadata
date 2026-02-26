# Broad Habitat Area Estimates by Land Class for Great Britain

- Version and provenance: Version 1 (1-2-2012); Countryside Survey data © NERC - Centre for Ecology and Hydrology. CS1978_Estimates_by_LC.csv and CS78_BH1_17.tif are provided as data products.

## Data assets

- CS1978_Estimates_by_LC.csv
  - National estimates of Broad Habitat stock (Habitat codes 1-21, excluding 15 and 20) for 1978, calculated using the 1990 ITE Land Classification (per Scott, 2007). Estimates are given by Land Class.
  - Columns include: YEAR; LAND_CLASS (ITE Land Class); BROAD_HABITAT (code); BROAD_HABITAT_NAME; LAND_CLASS_AREA (000s ha); MEAN_ESTIMATE (000s ha); LOWER_ESTIMATE (000s ha; 95% CI); UPPER_ESTIMATE (000s ha; 95% CI).

- CS78_BH1_17.tif
  - Raster data created by converting Land Class totals for each Broad Habitat (1-17, excluding 15) to percentages per 1 km pixel (band per Broad Habitat class).
  - Bands correspond to: 1 Broadleaved Mixed and Yew Woodlands; 2 Coniferous Woodland; 3 Boundary and Linear Features; 4 Arable and Horticulture; 5 Improved Grassland; 6 Neutral Grassland; 7 Calcareous Grassland; 8 Acid Grassland; 9 Bracken; 10 Dwarf Shrub Heath; 11 Fen/Marsh/Swamp; 12 Bog; 13 Standing Open Waters and Canals; 14 Rivers and Streams; 15 Inland Rock; 16 Urban. Pixel size: 1 km; Coordinate system: British National Grid; Projection: Transverse Mercator Great Britain; Extent: Great Britain.

## Spatial, classification and technical details

- Pixel size and projection: 1 km pixels; British National Grid (OSGB1936) / Transverse Mercator GB.
- Coverage: Great Britain; historical dataset based on 1978 Countryside Survey data.
- Data formats: CSV (tabular estimates by Land Class) and TIFF (raster habitat proportions by 1 km pixel).
- Metadata implications: to use or share, follow the stated acknowledgement and copyright requirements (see Rights and Acknowledgments).

## Metadata, provenance, and references

- Classification frameworks:
  - ITE Merlewood Land Classification (Bunce et al. 1996; 1981) used for Land Class definitions.
  - Broad Habitat classifications (Jackson 2000) and related JNCC guidance for interpretation.
  - 1990 ITE Land Classification used for the 1978 estimates (Scott 2007).
- Key publications and sources:
  - Countryside Survey: Measuring Habitat Change Over 30 Years; 1978 Data Rescue Final Report (CEH NEC03689).
  - CS Technical Reports and field mapping methodologies referenced for data generation and interpretation.
- Acknowledgments and copyright:
  - All CS data usage must include acknowledgement: "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Usage rights, sharing, and governance

- Data stewardship obligations:
  - Acknowledge Countryside Survey data ownership and copyright in all copies, publications, and presentations.
  - Ensure metadata remains intact and references are preserved when sharing or redistributing.
- Access and sharing limitations:
  - Data are governed by the Countryside Survey copyright; follow the explicit acknowledgment language in all outputs.
- Potential for reuse:
  - Suitable for historical habitat change analysis, national-scale habitat stock estimation by land class, and spatial portrayal of Broad Habitat distribution as percentages per 1 km pixel.

## Data quality, limitations, and caveats

- Temporal scope: 1978 estimates based on the 1990 Land Classification framework; suitable for retrospective analyses but not current state without reclassification.
- Exclusions: CSV excludes Broad Habitats 15 and 20; TIFF bands include 1-17 excluding 15, so users must account for this in interpretation.
- Uncertainty: MEAN_ESTIMATE with LOWER_ESTIMATE and UPPER_ESTIMATE (95% CI) provided in CSV, enabling uncertainty assessment.
- Data rescue context: part of a 30-year change measurement project; interpret with awareness of methodological specifics documented in cited reports.

## Governance considerations for Data Stewards

- Data mapping and interoperability:
  - Maintain alignment with ITE Land Classification and Broad Habitat nomenclature for compatibility with related datasets.
  - Preserve projection (OSGB36) and unit conventions (000s ha for area; percentages for raster).
- Documentation and traceability:
  - Link data to the referenced publications and the Countryside Survey website for methodological context.
  - Document any transformations or re-projecting steps performed during ingestion or analysis.
- Update and lifecycle planning:
  - The dataset covers 1978; any updates or new releases should maintain consistent classification standards or clearly document changes.
- User needs and discoverability:
  - Provide clear metadata and usage notes to ensure datasets meet user needs for national-scale habitat assessment and historical trend analyses.
  - Ensure license and acknowledgment requirements are visible in data portals and metadata records.

## Appendix: Key references

- Countryside Survey website: http://www.countrysidesurvey.org.uk/
- 2012 Countryside Survey: Measuring Habitat Change Over 30 Years; 1978 Data Rescue – Final Report (CEH NEC03689)
- Scott, W.A. (2007) CS Technical Report No.4/07 – Statistical methods for deriving national estimates from 1 km survey squares
- Bunce, R.G.H. et al. (1996, 1981) – ITE Merlewood Land Classification and related user notes
- Jackson, D.L. (2000) – Guidance on interpretation of the Biodiversity Broad Habitat Classification
- CS Technical Reports No.1/07 – Field Mapping Handbook