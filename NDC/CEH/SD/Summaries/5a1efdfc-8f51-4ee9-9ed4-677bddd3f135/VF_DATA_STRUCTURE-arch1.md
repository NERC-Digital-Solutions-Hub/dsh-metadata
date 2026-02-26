# UK Environmental Change Network Vegetation: Fine Grain (VF)

- Overview
  - Fine-grain vegetation dataset from the UK Environmental Change Network (ECN), collected and curated by the ECN Data Centre and partners.
  - 12 ECN sites with plots and year-based vegetation data; core survey every three years (some annual plots for extended coverage).
  - Data usage requires acknowledgement and sharing a reprint of publications citing the data.

- Data structure and governance
  - Data stored as site-specific tables within an Oracle database (D1VF_xxx: vegetation plot data; D2VF_xxx: environmental/site-level data; D3VF_xxx: cell features).
  - Core fields include SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE; additional fields cover pedate, land use, slope, aspect, and NVC class.
  - Metadata and reference tables describe codes and field mappings; site metadata include name, coordinates, and date range.

- Code schemes and data content
  - Land Use (Hodgson codes): 1–22 describing land-use categories (e.g., grassland, cereals, woodland types).
  - Slope Form (Hodgson codes): 1 = Convex, 2 = Straight, 3 = Concave.
  - Features (D3VF_xxx): Examples include Path (P), Wall (W), Stream (S), Hedge (H), Ditch (D), Fence (F), Bank (B), Natural boundary (N), No feature (X).
  - Species codes: site- and taxon-specific mappings linking numeric codes to Latin names and common names, with extensive crosswalks to taxonomic concepts.
  - The dataset includes large-scale crosswalks and synonym mappings to harmonize species identifications across codes, sites, and time.

- Species code mappings (highlights)
  - A comprehensive, multi-line mapping between numeric species codes and scientific/common names, including numerous synonym relationships (e.g., Salix aurita variants mapped to related Salix taxa; other plant and moss/liverwort taxa linked to alternative codes or taxon concepts).
  - Cross-references frequently include alternative Vas_ codes and taxonomic updates to support consistent identification across datasets.

- Quality codes and metadata
  - ECN quality codes denote data quality factors (e.g., 100 = no information; 101–160 describe common data issues; 999 = unusual event).
  - Quality notes may accompany data; unusual events are described in accompanying quality text.
  - Quality metadata should be consulted to assess data reliability and to interpret results properly.

- How analysts use the data
  - Purpose: identify correlations and trends in vegetation composition across sites and years; develop predictive insights about responses to environmental change.
  - Data integration: harmonize across sites using core fields (site, year, plot, cell, species code) and standard metadata (NVC types, land use, slope, etc.).
  - Analyses enabled: temporal vegetation change, spatial comparisons by NVC type or site, relationships with environmental variables (pedate, land use, slope, aspect, slope form, management), and presence/absence or abundance patterns at the cell level.
  - Reporting: visualise species distributions over time; ensure data are quality-assured; contextualise findings with site metadata (location, date range).
  - Dissemination: created datasets can be uploaded to data portals with metadata for discoverability and reuse.

- Practical considerations for users
  - Access via site-specific Oracle tables; plan to query across D1VF, D2VF, and D3VF and to join across site tables for multi-site analyses.
  - Be mindful of right-scale limitations and rely on accompanying quality metadata to avoid misinterpretation.
  - When publishing, acknowledge ECN data usage and, if possible, share publications or reprints as requested.

- Data provenance and sponsors
  - Dataset Owner: UK Environmental Change Network (ECN) programme.
  - Sponsors include a range of UK government departments and agencies.
  - Protocol Reference: ECN terrestrial measurements (VF protocol); cite and acknowledge data usage.