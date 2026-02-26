# UK Environmental Change Network (http://www.ecn.ac.uk) Frogs (BF) Dataset

- A phenology-based frog spawning dataset collected by the UK Environmental Change Network (ECN) with accompanying water quality analyses.
- Data are organized into two primary data streams per site: core observational data and laboratory analysis data.
- Data originator: ECN Data Centre; Dataset Owners: ECN programme sponsors (UK government departments and agencies).

## What the dataset covers

- Focus: Spawning of the Common Frog as an indicator of population health, using the count of frog egg masses and supported by laboratory water analyses.
- Protocol: Phenology-based methodology; includes observation of spawning and associated water chemistry analyses.
- Access and attribution: ECN requests acknowledgement of data use and one reprint of any publication citing the data.

## Data structure and organization

- Core data (D1BF_xxx): Ten tables (one per site) in an Oracle database, with site-specific codes (xxx) and schema including SITECODE, LCODE, FROMDATE, SDATE, FIELDNAME, VALUE, and related metadata references.
- Laboratory data (D2BF_xxx): Ten tables (one per site) in an Oracle database, with fields such as SDATE, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE, and VALUE, among others.
- Metadata and reference tables: Core metadata tables are linked to standard reference tables (e.g., M_DESC, M_REFFIELD); additional quality information accompanies the dataset.
- Site codes and date ranges: 11 sites (T01–T11) with site names, precise coordinates, and date ranges in the dataset (e.g., Drayton, Glensaugh, Hillsborough, Moor House – Upper Teesdale, North Wyke, Rothamsted, Wytham, Alice Holt, Porton Down, Snowdon). Date ranges vary by site (approximately 1994–2012 for many sites).

## Site details (highlights)

- T01 Drayton
- T02 Glensaugh
- T03 Hillsborough
- T04 Moor House – Upper Teesdale
- T05 North Wyke
- T06 Rothamsted
- T08 Wytham
- T09 Alice Holt
- T10 Porton Down
- T11 Snowdon (Y Wyddfa)
- Each site entry includes location coordinates and the dataset’s date range for that site.

## Field names and data content

- Core variables (examples): 
  - Alkalinity (ALKY), Aluminium (ALUMINIUM), Calcium (CALCIUM), Chloride (CHLORIDE), Conductivity (CONDY), Colour (COLOUR), Depth (DEPTH), Dissolved Organic Carbon (DOC), pH measurements, Phosphate (PO4P), Potassium (POTASSIUM), Nitrate/Nitrogen (NO3N), Ammonium (NH4N), Sulphate (SO4S), Sodium (SODIUM), and related water chemistry metrics.
  - Biological/phenology metrics: CONGDATE (first frog congregation date), NEWMASS (new spawn masses), SPAWNDATE (first spawning date), HATCHDATE (first hatch date), PERCDEAD (percentage dead/diseased eggs), SPAWN-related measurements (e.g., SPawn area, Spawn counts).
  - Environmental and physical measurements: MAXTMP (max temperature), MINTMP (min temperature), SURFAREA (spawn surface area), DEPTH (spawn area depth), VOLUME (sample volume), and associated quality codes.
- Quality and data confidence:
  - Quality codes are assigned by ECN site managers from a standardized list; 999 indicates an unusual event with accompanying text available in the quality metadata.
  - Quality codes cover a wide range of data integrity and sampling conditions (e.g., equipment issues, sample contamination, weather effects, laboratory handling, and data edits).

## Data governance and usage guidance

- Ownership and sponsorship: ECN program and its consortium of government departments and agencies fund and oversee the dataset.
- Acknowledgement and publication: Users must acknowledge ECN data and provide one reprint of any publication citing the dataset.
- Protocol reference: Measurements follow ECN’s terrestrial protocol for frogs (BF); accompanying quality information should be used when analyzing data.
- Metadata availability: Detailed core metadata documentation exists (structure and definitions referenced by M_DESC, M_REFFIELD); use the accompanying metadata to interpret fields and units accurately.
- Access considerations: The dataset is documented with data structure specifics (site tables, field names, and data types); maintainers encourage engagement with the quality metadata to ensure appropriate use and interpretation.

## Practical notes for data leadership and system integration

- Whole-system view: The dataset spans multiple sites with centralized core and lab data streams, requiring cross-site metadata alignment and consistent data harmonization practices.
- Data discoverability: Core and lab data are organized by site-specific tables (D1BF_xxx and D2BF_xxx) in an Oracle database; metadata documentation is essential for discovery and correct use.
- Data quality management: Leverage the ECN quality codes to assess data reliability and to guide data cleaning and weighting in analyses.
- Data update and governance: Loosely time-bounded by site date ranges; be mindful of varying date coverage per site when aggregating across the network.
- Collaboration and reuse: When integrating with wider networks, ensure the dataset’s attribution, protocol adherence, and accompanying quality documentation are preserved.

- Protocol and contact: Protocol reference available at ECN measurements page; for data access and permissions, contact ECN Data Centre (ecn@ceh.ac.uk).