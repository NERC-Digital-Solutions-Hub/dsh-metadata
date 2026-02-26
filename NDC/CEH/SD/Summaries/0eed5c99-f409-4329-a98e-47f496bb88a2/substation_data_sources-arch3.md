# Network and Substation Characteristics

- Overview of Britain’s electricity network
  - Two-tier system: transmission network (400 kV and 275 kV; 132 kV in Scotland) and regional distribution networks.
  - Transmission operated by National Grid in England, SSE Scottish Power/Scottish Hydro Electric in Scotland.
  - Interconnectors move power to Ireland, France; new links under construction to Norway and Belgium.
  - 14 licensed Distribution Network Operators (DNOs) cover regional service areas; ownership split among six companies.

- Substation roles and voltage levels
  - Transmission substations: up to 400 kV/275 kV; many also act as Grid Supply Points (GSPs) stepping down to 132 kV.
  - Distribution substations: operate at 132 kV down to 33 kV, 11 kV, 6.6 kV, and lower to 230 V for end customers.
  - Key substation types:
    - BSPs (bulk supply points) and PSS (primary substations)
    - Switching stations: operate at a single voltage level, no transformers, used for collector/distribution or redundancy
  - Typical flow: 132 kV -> 33 kV (or 66 kV) -> 11 kV (or 6.6 kV) -> 230 V (domestic)

- The Substation Data - Nature, Units, Quality Control and Data Structure
  - Dataset compiled from National Grid and six DNOs to a common primary-level dataset (33/11 kV or 33/6.6 kV).
  - Core attributes (SUBST_ID, COMPANY_ID, SUBST_NAME, COMPANY, REGIONAL_SERVICE_AREA, ASSET_TYPE, VOLTAGE_HIGH, VOLTAGE_LOW, CONSTRAINT_STATUS, EASTING, NORTHING).
  - Variables reflect two-voltage records; some sites have more than two voltages (highest/lowest values recorded).
  - Generation constraint statuses typically use a traffic-light scheme (red/amber/green), though standardization across companies is limited.
  - Substations organized by company and regional area; duplicates and multi-site configurations commonly encountered.

- Collection / Generation Methods
  - Data set created in 2018 with varying data updates since; interpretations are the researchers’ and not formally validated by individual companies.
  - Data sources and processing differ by company, with some sites’ details supplemented or inferred from related maps or portals.
  - General approach:
    - Convert network shapefiles or polygons to comparable point locations (central coordinates).
    - Interpret single-voltage entries as the highest voltage when possible.
    - Classify constraint status where available (kV-specific constraints noted).
  - Data quality and completeness vary between providers; metadata quality and standardization are ongoing concerns.

- Company-specific data collection and site counts
  - National Grid
    - Substations derived from May 2018 shapefiles; 471 sites after filtering (headhouses removed; cables/sealing ends retained).
    - 313 sites classified as TRANS (400/275 kV); remaining as GSP; 132 kV often linked to distribution.
  - SSE (Scottish & Southern Electricity Networks)
    - Data from generation-availability Excel; 957 total (435 North Scotland, 522 Southern England).
    - Transmission status used as constraint indicator (constrained/unconstrained); Shetland sites added to dataset.
    - Not all Beauly-Denny 400/275 kV substations captured; additional sites identified from multiple sources bringing total to 459 in North Scotland (adjusted to 459+).
  - SP Energy Networks
    - 1,229 total sites (476 South Scotland, 753 MANWEB region); capacity status categorized as Green/Amber/Red.
    - Some network areas updated by third-party sources; 33 sites identified as missing from final total (post-filter).
  - Northern Powergrid
    - Data from generation-availability map; 783 total sites (269 North East England, 514 Yorkshire).
  - Electricity North West
    - 1,433 sites after cleaning (608 initial records); use of thermal capacity heat maps to infer constraint status.
    - Decommissioned sites and duplicates (same substation with multiple records) removed; issues with unnamed sites and mixed voltages resolved by deduplication.
  - Western Power Distribution
    - 1,592 initial records; final cleaned list of 1,433 sites (East Midlands 533, South Wales 246, South West 379, West Midlands 275).
    - Substation data from shapefile download; handling of duplicate multi-site entries (e.g., BSP + Primary on same site).
  - UK Power Networks (UKPN)
    - Substations, lines, and a 132 kV/33 kV mapping approach with heat-map-based constraint statuses.
    - Status categories derived from FDG (Flexible Distributed Generation) modeling; major portion of data had blank or 0 constraint statuses.
    - After processing, 1,327 sites remained (East England 822, London 38, South East 467); large number of duplicates removed.
    - 132 kV substations mapped to 132/33 kV; 33 kV substations mapped to 33/11 kV unless specified otherwise.
    - Notable data gaps: blank statuses and duplicated records across some regions.

- Data quality, standardization, and governance implications for monitoring
  - Widespread challenges include lack of complete constraint data, inconsistent voltage representation, and recurring duplicates.
  - Metadata gaps hinder rapid verification of data suitability for policy monitoring and decision-making.
  - Substantial transformation and normalization efforts required to produce comparable, up-to-date datasets across all operators.
  - Data sharing and governance concerns (quality, timeliness, openness) are central considerations for ensuring usable outputs in monitoring frameworks.

- End note
  - The document outlines a comprehensive, multi-source effort to standardize substation data for generation capacity and network monitoring, while highlighting ongoing data quality and standardization barriers that monitoring framework authors must address in future policy evaluation and decision-making.