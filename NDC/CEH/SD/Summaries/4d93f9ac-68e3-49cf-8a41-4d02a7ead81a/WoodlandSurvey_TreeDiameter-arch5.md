# Woodlands Survey tree diameter data 1971-2001

## Overview
- A dataset from a Britain-wide survey of broadleaved woodlands conducted in 1971, with re-surveys in 2000s (2001) using identical methods.
- 103 sites were surveyed, with 16 random plots (200 m² each) per site.
- Data cover species composition (canopy and ground flora), soil pH, Soil Organic Matter, habitat management, and a range of plot- and site-level descriptors.
- Analyses examined ecological change over time and drivers such as atmospheric deposition, climate, canopy structure changes, and woodland management.
- Related publications provide methodological and analytical context (Kirby et al. 2005; Corney et al. 2004); consult these for detailed methods and results.
- Dataset originators and contributors are listed for 1971 and 2001–3, with standardized survey methods (Bunce & Shaw 1973).

## Data Structure and Content
- Site: numeric code (1–103); Plot: numeric (1–16); BRC_number: numeric species code (Biological Record Centre list); BRC_names: text species names.
- Amalgams and Amalgam_names: numeric/text fields for grouped or cross-specific taxa where records were inconsistent.
- Status: numeric indicator; “Live” or “Dead” trees.
- DBHclass: numeric 5 cm interval bands (codes 1–32) indicating diameter at breast height ranges.
- Count and Final_count: numeric counts of individuals in each DBH class per plot; adjustments noted for saplings/shrubs (multiplied by two due to sampling quarters).
- Yr: numeric (1 = 1971; 2 = 2000s).
- Woody: text flag ‘w’ denotes woody species.
- Field_sheet: text reference to the original field sheet (e.g., “Tree sapling shrub”).
- DBH range and class mappings are provided (e.g., 0–5 cm range maps to DBH Class 1; ranges extend up to 156–160 cm in DBH Class 32).

## Provenance and Documentation
- Originators (1971): Bunce & Shaw (Woodland Ecology Section, Nature Conservancy, Merlewood) with later contributors in 2001–3 (CEH Lancaster, English Nature, University of Liverpool).
- Field methods: Re-survey conducted in 2000s using exactly the same field methods as 1971; standardized survey approach per Bunce & Shaw (1973); a field handbook is noted in supporting documentation.
- Related datasets and references:
  - Countryside Survey (related dataset)
  - Steele (1968) National survey of woodlands
  - Core references detailing long-term ecological change and landscape drivers (Corney et al., 2004; Kirby et al., 2005).
- Supporting documentation and publications are provided to guide method interpretation and analytical context.

## Access, Metadata, and Standards
- The dataset is available with a DOI link for access and citation.
- Metadata includes a comprehensive data dictionary (field definitions, code meanings, and data formats) and a field-sheet description, aiding data discovery and reuse.
- Connections to publications provide methodological background and context for analyses of change over the 1971–2001 period.

## Quality, Limitations, and Stewardship Considerations
- Data are derived from a long-term, standardized survey design, enabling temporal analysis but requiring careful handling of legacy coding (e.g., BRC species codes, amalgams).
- Potential issues to note:
  - Inconsistent recording necessitating amalgam groupings for some species (Amalgams).
  - Complex DBH class coding and range mappings; must be interpreted using the provided DBH ranges and class definitions.
  - Large historical dataset with multiple outputs (site, plot, species, counts) and multiple years requiring robust metadata maintenance.
- For governance and reuse, ensure linkage to the original publications (Kirby 2005; Corney 2004) and to the originator details for provenance and update tracking.

## Summary of Key Points for Data Stewards
- This dataset provides a robust, long-term record of woodland structure and composition across 103 sites, with 16 plots per site and repeat sampling in the 2000s using identical methods.
- The data are structured around site/plot-level observations, species codes, and detailed DBH classifications, including counts and live/dead status.
- Provenance and documentation are well documented, with originator details, standard methods, and supporting materials to facilitate proper interpretation and reuse.
- Metadata, data dictionaries, and references are essential for correct interpretation, particularly for species coding (BRC), amalgams, and DBH class mappings.
- When sharing or redistributing, reference the DOI and linking publications to preserve context, methods, and provenance.