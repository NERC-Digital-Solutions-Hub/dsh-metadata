# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Guidelines for digital field mapping of Countryside Survey 2007 (CS2007) to report land cover change and map Broad Habitats (BH) and Priority Habitats (PH) at country scales.
- Supports time-series analyses and broad community data sharing; marks shift from paper to digital data collection.

## Data system and workflow
- Data model structured around 1 km survey squares edited in GIS (ArcMap) via CS Surveyor extension.
- Mapping comprised of three feature types: Areas (polygons), Lines (linear features), and Points (points); each with components and attributes.
- Standardized workflow enforces data entry, change reporting, and iterative validation (user needs, data quality, update cycles).

## Data model and asset structure
- Core asset types: Broad Habitats (BH) and Priority Habitats (PH); PHs nest within BHs.
- MMU (minimum mapping unit) is 1/25 hectare (400 m2); sub-MMU features may be represented as lines or points.
- Pond mapping is central; each square records ponds via CS2007 Pond Mapping Recording Sheet with one pond selected for detailed sampling.
- Thematic attribute groups cover Inland Physiography, Inland Water, Coastal Features, Agriculture/Natural Vegetation, Forestry, Structures, Recreation, and Transport.
- Woodlands/woody features documented as Areas or Points with attributes (e.g., Belt of Trees, Clump of Trees, etc.); veteran trees have detailed attributes and constraints.

## Data capture tools and procedures
- CS Surveyor (built on ArcMap) used for data capture/editing with dedicated tool panels for Areas, Lines, and Points.
- Line editing includes creating, modifying, cutting, reshaping, and handling shared nodes; strict rules govern event lengths and topology.
- Points and lines require adherence to data integrity rules (e.g., minimum lengths, one-to-one edits, no edits across boundaries without proper procedures).

## Habitat keys and classification
- Vegetation Key assigns primary/secondary BHs and PHs based on vegetation composition.
- Key to woodland types/features classifies woody vegetation to support BH/PH allocation (e.g., Woodland/Forest, Belt of Trees, Clump of Trees).
- PHs nest within BHs; PH extents distinguished post-survey using GIS masks for upland vs. lowland.

## Change management, accuracy, and governance
- Change reporting mandatory; classifications include REAL change, ERROR (correction of earlier misallocations), NEW BASELINE (new subdivision of land cover).
- Unenclosed habitats may require back-correction of 1998 data; integration with CS1990/CS1998 data to enhance detail.
- Attribute consistency checks and mandatory-change fields govern data integrity.

## Pond surveying and sampling
- All ponds in a square identified; one survey pond randomly selected for detailed sampling (or preselected from CS2000 if valid).
- Detailed pond attributes captured on the CS2007 Pond Mapping Recording Sheet (pond ID, area, water presence, reasons for loss/creation, notes).

## Woodlands and woody features
- Woody features documented as Areas or Points; main attributes include Belt of Trees, Belt of Scrub, Clump of Trees, Scattered Trees/Scrub, Patch of Scrub, Dead Wood, etc.
- Veteran trees: up to 10 per square (max 2 per species) with extensive attributes (DBH, health, canopy, epiphytic cover, etc.).
- Buffer zones for woody features can be recorded to reflect land-management practices.

## Data quality, collaboration, and support
- Emphasis on coherent, discoverable data assets with clear provenance, change history, and metadata.
- Encourages cross-partner and cross-sector collaboration to support robust ecosystem-level insights.
- Support channels include a helpdesk, Wiki fault logging, and regular methodological updates.

## Challenges for data leaders
- Fragmented or inconsistent data sources across time and space, especially unenclosed upland BH mapping.
- Need for clear metadata, data standards, and sector coordination to avoid duplication and build strong communities of practice.
- Access and data protection considerations; some data may be gated or restricted requiring governance and data-sharing agreements.
- Transition from paper to digital systems introduces potential field-level bugs; requires proactive support and update mechanisms.

## Implications for data leaders
- Establish robust data governance around habitat classifications, change tracking, and time-series analyses.
- Invest in scalable data models and governance that enable PHs within BHs and post-survey PH mapping.
- Maintain metadata, provenance, and versioning for reproducible analyses and policy-relevant reporting.
- Promote cross-sector collaboration to strengthen data communities and minimize duplicated efforts.

## Additional notes (as context)
- Appendix references and detailed tool-specific procedures (e.g., line editing, shared nodes, and loop data handling) illustrate implementation specifics for data practitioners using the CS Surveyor workflow.