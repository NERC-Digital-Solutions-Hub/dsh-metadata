# Network and Substation Characteristics

## Aim and scope
- Builds a database of substations down to the primary level (33/11 kV or 33/6.6 kV) to support generator connections (e.g., solar, wind).
- Data compiled from National Grid and six Distribution Network Operators (DNOs).
- Dataset created in 2018; reflects interpretation by researchers and may not be formally validated by the companies.
- Aims to standardise a common set of attributes and enable analysis of transmission and distribution network assets and constraints.

## The Great Britain electricity network at a glance
- Transmission network: predominantly 400 kV and 275 kV lines and substations (132 kV in Scotland); interconnectors to Ireland and France; new interconnectors to Norway and Belgium under construction.
- Transmission operators: National Grid (England), SSE and Scottish Power (Scotland).
- Distribution networks: 14 licensed DNOs across Britain, owned by six companies (regional breakdown provided for context).
- Voltages by network level:
  - Transmission: 400 kV / 275 kV (and 132 kV in distribution handoff).
  - Distribution: 132 kV, 66 kV, 33 kV, 11 kV, 6.6 kV, and 230/400 V to customers.
- Substation roles span from high-voltage transmission substations to multiple-level distribution sites; switching stations exist without transformers.

## Substation types and roles
- Transmission substations: up to 400 kV/275 kV; many also grid supply points (GSPs) that step down to 132 kV for distribution.
- BSPs (bulk supply points): typically 132 kV to 33 kV (or 66 kV); rural vs urban scale varies.
- Primary substations (PSS): intermediate distribution voltage steps (e.g., 33 kV to 11 kV).
- Distribution substations: commonly 132 kV to 33 kV, or 33 kV to 11 kV; some sites host multiple voltage levels.
- Switching stations: operate at a single voltage level with no transformers; used for collection/distribution or backup switching.

## The Substation Data – structure, units, and quality controls
- Core dataset attributes (per site): SUBST_ID, COMPANY_ID, SUBST_NAME, COMPANY, REGIONAL_SERVICE_AREA, ASSET_TYPE, VOLTAGE_HIGH, VOLTAGE_LOW, CONSTRAINT_STATUS, EASTING, NORTHING.
- Multi-voltage sites: many have two voltages listed; for some, more than two voltages exist; the highest and lowest values are recorded.
- Constraint status: defined variably by DNOs; often a traffic-light (red/amber/green) scheme, but not fully standardised across companies.
- Data organization: by company, with regional service areas; deduplication and site-name matching applied where necessary.

## Data collection and processing methods (2018 dataset)
- National Grid: substations mapped from shapefiles; removed headhouses and very low-voltage sites; finalization yielded 471 sites (313 at 400/275 kV as TRANS; others as GSP).
- SSE (Scottish & Southern Networks): 957 total after additions; 435 North Scotland, 522 Southern England; some gaps for certain 275/400 kV substations in North Scotland identified.
- SP Energy Networks: 1229 total; capacity classified as Green, Amber, or Red (with explicit meaning for each category regarding connection opportunities and potential reinforcement needs).
- Northern Powergrid: 783 total after filtering (269 North East England, 514 Yorkshire).
- Electricity North West: 608 records; later augmented with thermal maps and names; voltage and capacity details added; classifications Green/Amber/Red based on spare capacity.
- Western Power Distribution: 1433 sites; regional breakdown across East Midlands, South Wales, South West England, West Midlands; duplicates removed.
- UK Power Networks (UKPN): 1585 initially; deduplicated to 1327 sites (822 East England, 38 London, 467 South East); FDG (Flexible Distributed Generation) status included; 132 kV and 33 kV mappings standardized; some missing constraint values imputed from LSOA heat maps.
- Data normalization: voltage pairings and constraint statuses mapped to a common framework to enable cross-company comparisons; some status data were blank and supplemented via proxy information (e.g., heat maps, long-term development statements).

## Data quality, gaps, and caveats for analysts
- The dataset reflects 2018 data and may have been updated since; not all company data were uniformly harmonised.
- Constraint status definitions vary by company; standardised interpretation to Green/Amber/Red is approximate.
- Some regions (notably North Scotland) have incomplete coverage of the higher-voltage transmission substations.
- Duplicates existed across sources (e.g., sites with multiple records for combined BSP/PSS on the same site); deduplication exercised to produce a refined site count.
- Some statuses are missing and were inferred using proxies (LSOA heat maps or surrounding site data).

## Relevance for analysis and practical use
- Enables evaluation of distributed generation connections and network constraints at substations down to primary levels.
- Useful for identifying where reinforcement or dedicated studies might be required (Green/Amber/Red capacity classifications).
- Provides geographic coordinates (EASTING/NORTHING) for spatial analyses and integration with GIS-based planning.
- Supports comparison of asset types and voltage levels across the transmission-to-distribution transition.
- Serves as a historical baseline (2018) for tracking changes in capacity, constraints, and substation density over time.

## Key takeaways for analysts
- A comprehensive, multi-source GB substation dataset exists (as of 2018) with standardized attribute fields and a mapped interpretation of capacity constraints.
- Transmission and distribution hierarchies, substation roles, and voltage ladders are clearly defined, enabling layered analyses of where distributed generation can connect and where reinforcement may be needed.
- While rich, the dataset requires careful handling of inconsistent constraint statuses, potential gaps by region (especially North Scotland), and awareness that values reflect a specific point in time with possible updates since.