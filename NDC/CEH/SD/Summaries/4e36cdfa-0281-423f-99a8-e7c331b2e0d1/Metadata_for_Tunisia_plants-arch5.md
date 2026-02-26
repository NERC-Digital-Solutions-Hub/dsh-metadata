# Metadata for Woody species

## Overview
- Provides a large, coded metadata catalogue linking unique codes to woody species names and their functional groups/life forms, plus a parallel section for herbaceous species and a separate block for spatial and environmental data.
- Aims to support data discovery, sharing, and reuse by standardizing taxonomic and ecological metadata and linking to spatial attributes.

## Dataset structure and content
- Woody species metadata
  - Each entry uses a code (e.g., ANAGFOET, ARBUUNED) with a Scientific Name and a Functional group/life form (occasionally blank or labeled as Legume).
  - Some entries include subspecies notes (e.g., "2 subspecies - not differentiated") and occasional qualifiers (e.g., "Coronilla valentina L. (3 subspecies - not differentiated)").
  - Occasional placeholders such as "UNIDENTA" or "UNIDENTB" for unidentified species.
- Herbaceous species metadata
  - Similar code-to-name mappings with a Scientific name and a Functional trait/growth form.
  - Notably, many records present a paired structure labeled "1" and "2" (e.g., AGROPOUR, AGROPOUR) indicating two variant entries per code, potentially representing alternative states or trait definitions.
- Spatial and environmental metadata
  - Geographic coordinates: LATITUDE, LONGITUDE (decimal degrees).
  - Topography and edaphic context: ALTITUDE (m), SLOPE (degrees), Aspect, ROCKCROP (% rock outcropping), SOILPH (soil pH for 50 sites).
  - Biophysical context: Grazing index (1–4), OLIVDIAA/OLIVDIAB/OLIVDIAC/OLIVDIAD and OLIVBREA/OLIVBREE (olive diameter categories at two heights), MEAN30, MEANDBH (mean counts/diameters), FREQ30, FREQDBH (frequency metrics).
  - Olive-related datasets imply applications in agroforestry or olive-dominated systems.

## Metadata quality, gaps, and inconsistencies
- Functional group/life form fields are blank for many woody entries, reducing immediate usability without further curation.
- Taxonomic detail varies; some entries include subspecies notes or indicate undifferentiated subspecies, which may hinder precise taxonomic resolution.
- Presence of unidentified species placeholders (UNIDENTA, UNIDENTB) indicates incompleteness that requires follow-up identifications.
- Herbaceous records use a dual-value (1/2) scheme for many entries, necessitating clear documentation to interpret these paired entries consistently.
- Overall dataset appears to combine taxonomic metadata with ecological/trait data and derived environmental attributes, requiring a well-defined schema and controlled vocabularies for interoperability.

## Data governance, sharing, and interoperability considerations
- The data are intended for uploading to data portals and catalogues, so consistent metadata schemas and data dictionaries are essential.
- Need for governance around taxonomy references, alias management, and updating taxonomic changes (e.g., subspecies differentiation, reclassifications).
- Clear provenance, versioning, and data lineage should be captured, especially for unidentified taxa and subspecies notes.
- Evaluate data sensitivity and access controls for precise location data and ecological traits, particularly in managed landscapes (e.g., olive groves).

## Stewardship actions and recommendations
- Define and enforce controlled vocabularies for Functional group/life form and Functional trait/growth form; document any blanks or ambiguous values.
- Validate and standardize taxonomic nomenclature against authoritative taxonomies; maintain alias mappings and handle synonymy.
- Create and maintain a data dictionary explaining the meaning of codes (e.g., the 1/2 pairings in herbaceous entries) and the interpretation of subspecies notes.
- Implement data quality checks to address incomplete fields, unidentified entries, and non-differentiated subspecies.
- Develop a curation workflow for follow-up identifications to replace UNIDENTA/UNIDENTB entries with resolved taxa where possible.
- Ensure spatial and environmental fields are standardized (units, methods, data collection dates) and aligned with metadata standards for GIS integration.
- Document data provenance and version history; plan for updates as taxonomy and ecological trait knowledge evolves.
- Prepare data products for portal submission, including comprehensive metadata records, data dictionaries, and usage guidelines to facilitate discoverability and reuse.