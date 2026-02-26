# Lepidoptera species catalog with codes and common names

## Overview
- A large, line-by-line dataset listing moth species with multiple identifiers and names.
- Entries mix internal Lep codes (e.g., Lep_7792) with scientific names and common names (e.g., Buff Arches, Peach Blossom).
- Catalog-like codes (e.g., 73.190, 74.002) and taxon references are interwoven with names.
- The data landscape spans many species across families, with numerous duplicates, truncations, and inconsistent field presence.
- Some records include partial fields, corrupted values, or missing data denoted by placeholders (e.g., dots).

## GIS relevance and potential uses
- Acts as a taxonomy backbone to link occurrence data to both scientific and common names for map labeling and filtering.
- Enables joins between spatial occurrence datasets and the species catalog via codes (e.g., BF_NUMBER/ABH_NUMBER) or Lep codes.
- Supports map visualization by species or taxonomic group (e.g., choropleth, hotspots, or symbol-based maps).
- Facilitates audience-friendly outputs by labeling maps with common names while enabling rigorous analyses with scientific names.
- Useful for creating searchable map apps and faceted maps by family, genus, or common name.

## Data structure, fields, and typical content
- Core elements observed:
  - Lep codes (e.g., Lep_7792) serving as internal identifiers.
  - Scientific names (e.g., Agrochola macilenta) and common names (e.g., Yellow-line Bricky).
  - Catalog-like codes (e.g., 73.190, 73.192; 74.002; 71.009) that may reference taxonomy or catalog entries.
  - Repeated or overlapping values, sometimes with truncations or partial fields.
- Inconsistencies:
  - Missing values (denoted by dots), incomplete records, and repetition across lines.
  - Mixed formatting and occasional corrupted segments, suggesting extraction from a larger database or export with irregularities.
- Implication:
  - Requires normalization to a fixed schema before GIS use (e.g., stable IDs, complete names, and canonical codes).

## Data quality, limitations, and preparation needs
- Quality issues:
  - Numerous missing or placeholder values.
  - Apparent corruption or truncation in several records.
  - Duplicates and inconsistent field presence.
- Preparation steps:
  - Define a fixed schema: Lep_code, scientific_name, common_name, catalog_code, alternate_name(s), taxon_rank (if available).
  - Remove or correct corrupted records; flag uncertain entries for manual review.
  - Normalize taxon names and unify synonyms across records.
  - Create a robust lookup table mapping Lep_code and catalog_code to standardized species IDs.
  - Validate against external taxonomic references and, where possible, attach distribution or habitat context.
- GIS readiness:
  - Standardized fields and clean data are essential for reliable joins to spatial data and for stable map labeling.

## GIS integration guidance
- Recommended schema for GIS workflows:
  - Fields: Lep_code, catalog_code, scientific_name, common_name, alternate_names, brc_concept (if present), brc_species_name (if present), taxon_rank.
- Key usage patterns:
  - Join occurrence or sighting data to the taxonomy backbone on Lep_code or catalog_code for labeling and filtering.
  - Use scientific_name for rigorous analyses; use common_name for user-facing maps and UI.
  - Group by taxonomic categories to create faceted maps for policy briefs or dashboards.
- Data augmentation opportunities:
  - Attach habitat suitability or distribution layers to build spatially explicit taxon dashboards.
  - Develop an interactive atlas with search by common or scientific name and species detail panels.

## End-to-end workflow implications for GIS specialists
- Data ingestion: Import cleaned records; apply a stable schema; address missing or corrupted fields.
- Data hygiene: Normalize field names, reconcile synonyms, ensure unique identifiers (prefer Lep_code or canonical species ID).
- Spatial integration: Join to occurrence data and spatial layers; ensure cross-source code alignment.
- Visualization and product delivery:
  - Create map templates that support both scientific and common names.
  - Implement user-friendly filters (by common name, Lep_code, or taxonomic group) for diverse audiences.
- Quality assurance: Validate mappings with prototype visualizations; iterate based on end-user feedback to ensure clarity and usefulness.

## Next steps
- Validate and clean the dataset to produce a GIS-ready taxonomy backbone.
- Establish a standardized schema and a stable lookup table for species identifiers.
- Integrate with spatial datasets to produce map-based data products for audiences such as policy teams, clients, and the public.