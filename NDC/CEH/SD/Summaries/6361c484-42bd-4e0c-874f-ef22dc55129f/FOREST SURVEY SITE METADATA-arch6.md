# Forest Stand Data

- Overview
  - A large, multi-record dataset of forest stands identified by codes (e.g., A1, A2, A7, B3, C17, D32, etc.).
  - Each record includes geospatial coordinates (Easting, Northing), planting history, tree species, soil type, and harvest information.
  - Temporal data cover initial planting dates (First planting year), potential second planting (Year of second planting, Second planting species), and harvest status (Year felled or Standing crop).
  - Start date and End date fields appear as day/month/year components, indicating operational time windows; some entries use ambiguous or partial year representations (e.g., Start date = 7, Start date = 9, Start date = 95).

- Data Structure
  - Core fields per record:
    - Location: Easting, Northing
    - Planting history: First planting year, Year felled, Year of second planting, Second planting species
    - Species: Tree species (predominantly Sitka spruce; others include Norway spruce, Western hemlock, Japanese larch, Scots pine, Douglas fir, Noble fir, Lodgepole pine, etc.)
    - Soil type: Various classifications (Gley, Podzol, Brown earth, Bog)
    - Temporal markers: Start date components and End date components
  - Records are grouped with prefixes/labels (A, B, C, D) and numeric identifiers (e.g., A1, A2, B3, C17, D32).

- Key Content Themes
  - Species distribution: Sitka spruce is the most common species; numerous other species appear across stands (Norway spruce, Western hemlock, Japanese larch, Scots pine, Douglas fir, Noble fir, etc.).
  - Timber status: Many records indicate felled years around the 1990s; several entries show "Standing crop" as the harvest status, indicating ongoing stands.
  - Second planting: Where present, second planting years cluster around mid-1990s (e.g., 1994–1996); second planting species vary (e.g., Sitka Spruce, Japanese Larch, Silver Birch).
  - Soil diversity: A mix of Gley, Podzol, Brown earth, and Bog soils, with subtypes noted (e.g., Gley (PG), Podzol (PIP), etc.).
  - Spatial scope: Coordinates suggest a mapped dataset covering numerous locations, with repeated or nearby Easting/Northing pairs across multiple stands.

- Data Quality & Gaps
  - Missing data: Many fields list NA for Year of second planting or Second planting species.
  - Inconsistent formatting: Start date and End date fields appear as separate line items in some records, which may require normalization for analysis.
  - Ambiguities: Some records use non-numeric or textual harvest statuses (e.g., Standing crop) instead of numeric year values.

- Potential Data Products and Uses for Data Support
  - Self-serve analytics dashboards by stand to explore planting histories, species mixtures, and harvest status.
  - Geospatial visualizations: maps of stands colored by species, soil type, or harvest status.
  - Aggregations and summaries: counts and distributions by species, soil type, or year of felled; analysis of second planting incidence.
  - Data quality reports: identify missing Year of second planting, Second planting species, or inconsistent Start/End date formats.
  - Data integration workflows: link with external silviculture datasets to enrich species mappings, soil classifications, or historical climate data.