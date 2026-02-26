# Woodlands Survey tree diameter data 1971-2001

- A long-term ecological dataset from 103 broadleaved woodlands across Britain, with detailed information from site-level descriptors and 16 randomly placed 200 m² plots per site.
- Data collection years: 1971 and re-surveys conducted in the early 2000s (referred to as 2001), using the same field methods as the original survey.
- Aims of the underlying research: assess ecological change between 1971 and 2001 and identify drivers of change (e.g., atmospheric deposition of sulfur and nitrogen, climate, canopy structure changes, and woodland management). Key results published in Kirby et al. (2005) and Corney et al. (2004).

- Survey design and methods
  - Stratified sampling across the 103 sites.
  - Standardized field methods (Bunce & Shaw 1973) with a field handbook for documentation.
  - Data collected on canopy and ground flora, soil pH and Soil Organic Matter, habitat management, and other plot/site descriptors.
  - Data re-collected in 2001/2002/2003 using identical procedures to enable temporal comparisons.

- Related datasets and provenance
  - Related: Countryside Survey (and references to other woodland surveys).
  - Originators and contributors include researchers from CEH Lancaster, English Nature, and the University of Liverpool, among others.
  - Supporting documentation and key publications listed (Avery 1973; Corney et al. 2004; Haines-Young et al. 2003; Kirby et al. 2005).

- Data structure and key fields
  - Core components: Site, Plot, BRC_number, BRC_names, Amalgams, Amalgam_names, Status, DBHclass, Count, Final_count, Yr, Woody, Field_sheet.
  - Codes and descriptors:
    - Site: numeric, 1–103.
    - Plot: numeric, 1–16.
    - BRC_number: numeric species code (Biological Record Centre list).
    - BRC_names: scientific name (per BRC list).
    - Amalgams/Amalgam_names: grouped taxa where species were inconsistently recorded.
    - Status: Live or Dead (tree alive or dead).
    - DBHclass: numeric 5 cm interval band (1–32), indicating the DBH class for each tree.
    - Count/Final_count: counts of individuals per species per DBH class within each plot; saplings/shrubs adjusted (multiplied by two due to counting in only two quarters).
    - Yr: 1 = 1971, 2 = 2000s (survey year).
    - Woody: 'w' if woody species.
    - Field_sheet: field data sheet reference (e.g., “Tree sapling shrub”).
  - DBH measurement scheme: 5 cm interval bands with corresponding DBH class codes (ranges span from 0–5 cm up to 156–160 cm), enabling detailed size-structure analysis by species and plot.

- Data usage notes for GIS
  - Enables map-based visualization of species composition and size structure across sites and over time.
  - Suitable for spatial analyses of long-term woodland change, drivers of ecological change, and how these relate to external factors (deposition, climate, management).
  - Can support spatially explicit analyses when site coordinates or shapefiles are available, and can be integrated with external spatial datasets (e.g., Countryside Survey).
  - Requires data cleaning and standardization, particularly around amalgamated taxa and cross-species groupings; careful handling of sapling data (counting adjustments).

- Practical considerations and challenges
  - Data are held in multiple places and require integration for GIS workflows.
  - Some data gaps or inconsistencies may exist due to long-term archival handling and amalgamation of taxa.
  - Consistent data standards are necessary to combine with other datasets; large, multi-year, multi-site data require careful processing to produce usable map-ready layers.

- Access and references
  - DOI/link for the dataset: http://doi.org/10.5285/4d93f9ac-68e3-49cf-8a41-4d02a7ead81a
  - Primary analytical publications to consult for methods and results: Kirby et al. (2005); Corney et al. (2004); Haines-Young et al. (2003); Kirkby et al. (2005).
  - Related literature and acknowledgments list further contextual methodological details and linked datasets.