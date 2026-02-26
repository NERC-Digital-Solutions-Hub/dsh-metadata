# Landscape area data 1978 [Countryside Survey], Great Britain

- Dataset describes areas of Broad and Priority Habitats from 256 1km squares across Great Britain, surveyed in 1978.
- Data owner: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology (CEH); all rights reserved.
- File format: LANDSCAPE_AREA_FEATURE_HAB_1978.csv; content supports historical habitat mapping and landscape classification analysis.

## Data content and structure

- Columns and meanings:
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of survey (number)
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad or Priority Habitat (Jackson, 2000)
  - AREA: Area of habitat within 1km polygon (square metres)
  - LAND_CLASS90: ITE Land Class 1990 (Bunce et al. 1996; 1981, 1990)
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY: County or Council (Sco) for the square
  - EZ_DESC_07: Countryside Survey Environmental Zone description (reference linked)
- Scope: 1978 data used to measure habitat distribution within 1km squares across GB.

## Provenance, classifications, and references

- Source framework: Countryside Survey data; classifications include ITE Land Classification (1990) and Biodiversity Broad Habitat classifications.
- Related references and links (examples):
  - Countryside Survey project overview and methodologies
  - 1978 Data Rescue Final Report (Wood et al., 2012)
  - Statistical treatment of UK estimates (Scott, 2007)
  - ITE Land Classification publications (Bunce et al., 1990; Bunce et al., 1981)
  - Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)
- Environmental Zone documentation available via CEH catalogue linkage.

## Access, usage rights and licensing

- Usage acknowledgement: All use of Countryside Survey data must be acknowledged.
- Required wording:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Citations: Include the referenced CS publications and CEH links when using the data (publication list provided in the doc).

## Metadata and governance for data stewards

- Governance notes:
  - Data is part of a larger Countryside Survey data portfolio; ensure consistency with other CS datasets.
  - Documentation references for classification schemes and methodologies should accompany the dataset (e.g., ITE Land Classification, Broad Habitat Guidance).
- Metadata considerations:
  - Ensure clear metadata for SQUARE coding, year, unique ID semantics, and the relationship between BROAD_HABITAT codes and names.
  - Include the EZ_DESC_07 documentation link and any provenance details (survey year, methods).
- Catalogue and accessibility:
  - Record in data catalogues with a stable identifier; reference CEH/NERC as rights holder and link to publications.

## Quality, limitations, and caveats

- Temporal context: Data from 1978; may require careful interpretation alongside modern datasets due to legacy classifications.
- Interoperability: Legacy codes (BROAD_HABITAT, LAND_CLASS90) may differ from newer schemes; harmonisation may be needed for integrated analyses.
- Data completeness: Acknowledge potential gaps typical of historical surveys; ensure metadata captures collection methods and any known limitations.

## References and publications

- Countryside Survey Website and methodologies
- 2012 CS 1978 Data Rescue Final Report (Wood et al., NEC03689)
- 2007 CS Technical Report No.4/07 (Scott)
- Publications detailing the ITE Land Classification and habitat classifications (Bunce et al. 1981, 1990; Jackson 2000)
- Links to DOIs and PDFs provided in the original dataset documentation for deeper methodological context.