# Taxonomy for macroinvertebrates in Welsh upland rivers

## Aim and scope
- Describes macroinvertebrate taxonomy across the Welsh Acid Water Survey (WAWS) network (66 sites) and the Wye catchment (44 sites).
- WAWS aims to understand biological responses to acidity gradients (geology and acidic episodes); Wye aims to sample a gradient of land-use intensification.
- Data intended to support comparative analyses of community composition across sites and conditions.

## Sampling design and collection methods
- Timeframe: spring 2012 for WAWS; spring 2013 for Wye.
- Sampling: 2-minute semiquantitative kick samples collected in riffles, covering major habitats; designed to detect site differences.
- Preservation: on-site with 100% industrial methylated spirit (IMS); in the laboratory, samples preserved in 70% IMS.
- Identification: major groups identified and counts obtained to species or genus where possible, or to family or higher where taxonomy is difficult or development incomplete.
- Documentation references: Bradley & Ormerod (2002); Weatherley & Ormerod (1987). Links to these references may be provided in the CEH Data Catalogue but may not be persistent.

## Taxonomy, data content, and data structure
- Taxonomic levels recorded: class, order, family, genus, and taxon_name (finest level available).
- Abundance recorded for each taxon; some taxa identified at coarse levels (e.g., Oligochaeta, Tricladida).
- Data file schema (nine columns): dataset, site_code, year, class, order, family, genus, taxon_name, abundance.
- If the finest identification is at the family level, the genus field is populated with the family name to align with trait-level data often available at genus/family level.
- Some records have NA for family and genus when identification was not resolved to those levels.
- Trait-level information is typically extractable at genus or family level, enabling trait-based analyses across taxa.

## Metadata and supporting documents
- Main data: flatbed CSV with the nine taxonomic/abundance columns.
- Supporting site description: DURESS_CU_site_description.csv, including:
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey (WAWS or Wye), Catchment.
- Geographic and survey metadata enable spatial discovery and contextual interpretation.
- Data provenance references included; external links to literature may not be permanently stable.

## Data quality, governance, and stewardship considerations
- Quality control: no explicit quality control steps documented in the dataset.
- Metadata completeness: robust taxonomic fields and site metadata available, but with some coarse identifications and NA values requiring careful handling during analysis.
- Interoperability: some taxa identified only to family or genus; ensure standardized taxonomy mappings if integrating with other data sources.
- Updates and provenance: clear source surveys (WAWS and Wye) and time points; ensure mechanisms exist to update identifications or add new sites.
- Accessibility and persistence: dataset described in CEH Data Catalogue; be aware of potential link rot for referenced literature.

## Accessibility, availability, and caveats
- Data accessible via CEH Data Catalogue; external references may disappear over time.
- Users should account for potential non-interoperable identifiers due to coarse taxonomic resolution and missing metadata for certain records.
- When sharing or reusing data, document the identification resolution level and any NA fields, and reference the underlying WAWS and Wye survey contexts.