# Network and Substation Characteristics

## Overview
- Britain’s electricity network is divided into transmission (400 kV/275 kV, with 132 kV in Scotland) and distribution networks. 
- Transmission is run by National Grid (England) and Scottish Power Energy Networks / Scottish Hydro Electric (Scotland), with interconnectors to Ireland, France, and planned connections to Norway and Belgium.
- There are 14 licensed Distribution Network Operators (DNOs) covering regional service areas, owned by six companies.
- Substations and their voltage levels are described, from high-voltage transmission down to the standard mains 230 V, including intermediate voltages (33 kV, 11 kV, etc.) and various substation types (Transmission, GSP, BSP, PSS, Switching stations).

## The Substation Data - Nature, Units, Quality Control and Data Structure
- A database was created to capture substations down to the primary level (33/11 kV or 33/6.6 kV), aimed at supporting generation connections (e.g., solar/wind) with common attributes.
- Core attributes collected (SUBST_ID, COMPANY_ID, SUBST_NAME, COMPANY, REGIONAL_SERVICE_AREA, ASSET_TYPE, VOLTAGE_HIGH, VOLTAGE_LOW, CONSTRAINT_STATUS, EASTING, NORTHING).
- Most DNOs record two voltages per substation; when more than two voltages exist, the highest and lowest values are retained.
- Substation types include TRANS (transmission), GSP (grid supply point), BSP (bulk supply point), PSS (primary substation), and Switching stations (non-transforming, single voltage level).
- Substations on the same site may host multiple levels (e.g., 132 kV substation with adjacent 33 kV equipment); sites are treated as logically separate substation records.
- Voltage levels and coordinates are standardized using OS grid references (EASTING/NORTHING).

## Data Collection / Generation Methods
- The dataset was created in 2018, aggregating data from National Grid and the six DNOs; processing was done by researchers and not formally validated by the companies.
- National Grid
  - Source: shapefiles of substations and HV lines; polygons converted to central points.
  - Result: 471 sites after filtering (headhouses removed); 313 rated at 400/275 kV (TRANS); others treated as GSP.
- SSE Networks
  - Source: SSE generation-availability Excel files (Aug 2018); included constraint status maps.
  - Regions: 435 in North Scotland; 522 in Southern England; 957 total (with later updates bringing North Scotland to 459 after adding 24 sites).
- SP Energy Networks
  - Source: company pages; locations digitized; site characteristics extracted (June/July 2018).
  - Regions: 476 in South Scotland; 753 in MANWEB; total 1,229 (with later updates adding missing sites to reach about 1,688 after adjustments, including North Scotland additions).
- Northern Powergrid
  - Source: generation-availability map; 2017 data (Ian Foster collaboration).
  - Result: 269 sites in North East England; 514 in Yorkshire; total 783.
- Electricity North West
  - Source: GIS MapInfo data; enhanced with a thermal capacity heat map to assign names, asset type, and capacity.
  - Result: 608 records.
- Western Power Distribution
  - Source: shapefile (1592 records) with key attributes; duplicates and misaligned voltages resolved via site-name inferences; regional overlay for service areas.
  - Result: 1,433 sites (533 East Midlands, 246 South Wales, 379 South West England, 275 West Midlands).
- UK Power Networks
  - Source: DG Mapping Tool; shapefiles for 132 kV, 33 kV, 11 kV substations; heat-map-based constraint statuses to fill gaps.
  - Classification: mapped constraint statuses to GREEN (1–2), AMBER (3–4), RED (5–6); Many records matched to LSOA heat map when site-specific data blank.
  - Data refinement: converted 132 kV substations to 132/33 kV; 33 kV substations to 33/11 kV (where information supported); duplicates removed.
  - Result: 1,327 sites after deduplication (822 East England, 38 London, 467 South East England) from an initial 1,585.

## Data quality, Standardisation, and Limitations
- Variation in data depth and constraint information across companies; standardization to a single attribute set was imperfect.
- Some updates and missing substation records (e.g., certain transmission-network substations in North Scotland) were addressed by cross-referencing multiple sources, but gaps remained.
- Constraint statuses used by DNOs differ; researchers mapped to a common green/amber/red scheme, with additional FDG (Flexible Distributed Generation) context for UK Power Networks.
- Several records had blank or zero constraint data; sites were augmented via LSOA heat maps or adjacent site information.
- The dataset represents a snapshot from 2018 with notes that updates may have occurred since; interpretation and validation were not performed with company approval.

## Output and Intended Use
- Provides a harmonized, cross-operator view of substations suitable for identifying distributed generation connection opportunities and planning network reinforcements.
- Enables cross-operator analysis through a common attribute schema, facilitating data-driven planning and potential self-serve exploration of substation capacity and constraint status.
- Supports mapping of voltage-level transitions and regional service areas, as well as co-located substation configurations (e.g., multiple voltage levels on the same site).