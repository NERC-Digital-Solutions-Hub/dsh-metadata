# Network and Substation Characteristics

## Overview
- GB electricity network is divided into transmission (high voltage) and distribution (lower voltage) networks.
- Transmission is operated by National Grid (England) and Scottish Hydro Electric/Scottish Power (Scotland), with interconnectors to Ireland and France; new interconnectors to Norway and Belgium under construction.
- There are 14 licensed distribution network operators (DNOs) responsible for regional areas, owned by six companies; they manage the flow from transmission to end users.

## Substations and Voltage Levels
- Key voltage tiers:
  - 400 kV and 275 kV: Transmission substations; often connected to large generation (e.g., nuclear).
  - 132 kV: Distribution side; many substations step down from transmission to 33 kV for further distribution.
  - 33 kV/66 kV: Intermediate distribution voltages; 132 kV substations may output 33 kV (or rarely 66 kV).
  - 11 kV and 6.6 kV: Final distribution levels prior to local substations.
  - 230/400 V: Standard mains for customer supply.
- Substation types:
  - Transmission substations (TRANS) and Grid Supply Points (GSPs) that interface with distribution.
  - Bulk Supply Points (BSPs) and Primary Substations (PSSs) on the distribution side.
  - Switching stations: operate at a single voltage level without transformers; used for collection/distribution or backup switching.
- Sites can host multiple levels on the same site but are administratively and technically separate entities.

## The Substation Data Dataset
- Purpose: compile a database of substations down to the primary level (33/11 kV or 33/6.6 kV) to support generation connection assessments and network understanding.
- Common attributes (schema): 
  - SUBST_ID (unique site identifier), COMPANY_ID (substation in company context), SUBST_NAME, COMPANY, REGIONAL_SERVICE_AREA
  - ASSET_TYPE (TRANS, GSP, BSP, PSS), VOLTAGE_HIGH, VOLTAGE_LOW
  - CONSTRAINT_STATUS (generation connection constraints), EASTING, NORTHING (Ordnance Survey grid coordinates)
- Multi-voltages: many sites list two voltages; where more than two voltages exist, highest and lowest are recorded. If a single voltage is listed, it is treated as the highest value with the lower left blank.
- Constraint status: varied (traffic-light-like classifications); interpretive standardisation was limited by source data.

## Data Collection and Processing (2018)
- Data compiled from National Grid plus six DNOs; dataset created in 2018 with researcher interpretation (not formally endorsed by each company).
- National Grid
  - Substations from shapefiles of substations and HV lines; polygons converted to central points; about 471 sites after cleaning; 313 at 400/275 kV classified as TRANS; others as GSP.
- SSE (Scottish & Southern Electricity Networks)
  - Excel data (Aug 2018) including 957 total records (435 in North Scotland, 522 in Southern England); 11 Shetland additions; constraint status recorded as constrained/unconstrained; some North Scotland gaps (Beauly-Denny line areas identified separately).
- SP Energy Networks
  - 1,229 total records (476 in South Scotland, 753 in MANWEB); capacity status classified as Green/Amber/Red; 33 sites added through supplementary sources.
- Northern Powergrid
  - Data (Dec 2017) from generation-availability map; 783 total after filtering (269 NE England, 514 Yorkshire); substantial data cleaning to remove sub-33/11 kV sites and duplicates.
- Electricity North West
  - GIS data (MapInfo); 608 records; site names added via thermal/priority maps when missing; voltage and capacity statuses assigned.
- Western Power Distribution
  - Shapefile with 1,592 records; duplicates resolved; final dataset by region; capacity/constraint data incorporated via available maps; 1,433 sites after deduplication; duplicates often arose from co-located BSP and PSS.
- UK Power Networks
  - DG Mapping Tool data; shapefiles for 132/33 and 33/11; integrated with LSOA-based constraint heat maps; statuses normalized to GREEN/AMBER/RED; 1,585 initial records reduced to 1,327 sites (822 East England, 38 London, 467 South East) after deduplication; 503 records lacked site-specific statuses and were assigned LSOA-based codes.
  - Substations were allocated 132/33 kV or 33/11 kV codes based on available documentation; some duplicates remained, particularly in East England.

## Data Quality, Provenance and Governance
- Data created in 2018; methods reflect researchers’ interpretation and may not capture all updates from individual companies.
- Inconsistencies across sources:
  - Missing or non-standard constraint information.
  - Different representations of voltages and capacities.
  - Duplicates when multiple asset types are on a single site (e.g., BSP + PSS).
  - Some sites with blank or 0 statuses, later inferred via heat maps or related maps.
- Coordinate data (Easting/Northing) from OS grid; some sites lacked full attribute sets.
- Data were organized by company and regional service area, with deduplication and cross-referencing across multiple sources to build a cohesive dataset.

## Practical Implications for Data Stewards
- Useful for assessing generation-connection opportunities and understanding network constraints at the primary substation level.
- Can support planning studies, capacity assessments, and integration analyses for distributed generation (DG) with clearly defined asset types and voltage relationships.
- Requires careful governance:
  - Standardize constraint status semantics (e.g., GREEN/AMBER/RED) across sources.
  - Establish a robust updating process to reflect changes in the network, new substations, or retired assets.
  - Validate coordinates and asset-type classifications with primary operators where possible.
  - Manage duplicates and multi-asset sites with clear ownership and maintenance of combined records.
  - Document data provenance, versioning, and any interpretation rules used during harmonisation.

## Challenges for Data Stewards
- Incomplete picture of user needs and priorities for substation data.
- Timeliness: data reflect 2018 sources and may be out-of-date.
- Acquiring data that meets consistent metadata standards across many operating companies.
- Handling multiple systems and formats (shapefiles, Excel, MapInfo, online tools).
- Managing large datasets with site-level detail and various voltage schemes.
- Dealing with outdated databases that require bespoke, non-interoperable solutions.