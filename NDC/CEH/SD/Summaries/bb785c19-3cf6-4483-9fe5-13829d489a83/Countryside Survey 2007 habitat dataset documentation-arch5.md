# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 2007 using the 2007 ITE Land Classification; freshwater habitats analyzed with a different statistical model.
- Two data products:
  - CS007_Broad_Habitat_Stock.csv: national estimates of Broad Habitat area by Land Class, in 000s of hectares, with mean and 95% confidence intervals (lower/upper). Negative mean values should be treated as 0.
  - CS2007_Stock.tif: 1 km resolution raster where each 1 km pixel contains the mean percentage estimate of habitat within that square, with bands corresponding to Broad Habitat classes.
- Datasets are associated with Countryside Survey data and are to be acknowledged accordingly.

## Datasets and Structure

- CS007_Broad_Habitat_Stock.csv
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha) [may be negative; treat as 0]
    - LOWER_ESTIMATE: Lower bound of 95% CI (000s ha)
    - UPPER_ESTIMATE: Upper bound of 95% CI (000s ha)
  - Note: freshwater habitats use a distinct statistical model.

- CS2007_Stock.tif
  - 1 km pixel size; British National Grid (OSGB36), Transverse Mercator projection.
  - Each band corresponds to a Broad Habitat class (17 bands total). Band mapping is defined so that:
    - Broad Habitat 1/2 combinations map to specific bands (e.g., Coniferous Woodland, Broadleaved Mixed and Yew Woodland, etc.).
  - Pixel values represent mean percentage of habitat in each 1 km square, derived from 1 km survey squares within each Land Class strata.

## Data Quality, Interpretation, and Use

- Data provenance and standards:
  - Based on Countryside Survey methodologies; referenced in accompanying publications and technical reports.
  - MEAN_ESTIMATE values are areas in 000s ha; interpret negative values as 0.
- Freshwater vs terrestrial:
  - Freshwater Broad Habitats were modeled differently from other habitats; consider this in cross-habitat comparisons.
- Metadata and attribution:
  - All CS data require explicit acknowledgment: "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and copyright notes.

## Access, Usage, and Attribution

- Access and dissemination:
  - Datasets are uploaded to relevant portals and catalogues; appropriate citations to the CS UK 2007 results and methodological reports are expected in publications.
- Citations and references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No. 4/07 – Statistical Report
  - Bunce et al. (1996, 1981) ITE Merlewood Land Classification
  - Jackson (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification
  - Countryside Survey Technical reports and Field Mapping Handbook (No. 1/07)

## Governance and Stewardship Considerations

- Data governance aligned with Data Stewards responsibilities:
  - Ensure data meet standards for accuracy, consistency, metadata richness, and supported formats (CSV and TIFF).
  - Maintain provenance: document the 2007 survey methods, ITE Land Classification basis, and the different freshwater modeling approach.
  - Metadata and documentation: preserve definitions of fields, units (000s ha for CS007; 1 km² cells for CS2007_Stock.tif), and the link to Land Class descriptions.
  - Update and versioning: track survey cycles (e.g., 2007) and note any future revisions or methodological changes.
  - Interoperability: handle both tabular (CSV) and raster (TIFF) formats; ensure consistent Land Class mapping across products.
  - Usage constraints: respect disclosure risks and any dataset-specific limitations; ensure proper acknowledgment in all outputs.
  - Embargoes and access controls: not specified for this dataset, but governance should consider any future embargoes or proprietary considerations.

## Challenges to Consider

- Incomplete understanding of user needs and priorities for broad habitat stock data.
- Timeliness of data delivery and updates following new surveys.
- Ensuring data creators meet metadata and format standards across multiple files and formats.
- Handling multiple systems and formats (CSV vs. raster TIFF) and large spatial datasets.
- Integrating with older or archival databases that may require bespoke interoperability solutions.

## References and Related Publications

- Countryside Survey website and UK results from 2007 ( Carey et al., 2008 )
- CS Technical Report No. 4/07 – Statistical Report (Scott, 2007)
- ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996; Bunce et al., 1981)
- Guidance on Broad Habitat Classification interpretations (Jackson, 2000)
- Countryside Survey Field Mapping Handbook (CS Technical Report No. 1/07)