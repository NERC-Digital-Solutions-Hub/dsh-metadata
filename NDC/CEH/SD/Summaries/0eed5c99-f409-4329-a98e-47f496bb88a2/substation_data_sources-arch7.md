# Network and Substation Characteristics

- Scope and structure
  - Great Britain’s electricity network split into transmission (400 kV, 275 kV; 132 kV in Scotland) and regional distribution networks.
  - Transmission network operated by National Grid in England, and SSE/ScottishPower in Scotland; interconnectors with Ireland, France, and planned lines to Norway and Belgium.
  - 14 licensed Distribution Network Operators (DNOs) cover regional areas; DNO ownership distributed among six companies.

- Substation and voltage framework
  - Transmission substations handle 400 kV/275 kV; many link to 132 kV for handoff to distribution (BSPs often sit between transmission and distribution).
  - Distribution substations operate at 132 kV, 66 kV, 33 kV, 11 kV, and lower voltages (down to 230/400 V for end customers).
  - Typical progression: transmission 400/275 kV → 132 kV (BSPs) → 33 kV/66 kV → 11 kV → 230/400 V.
  - Substations can host multiple voltage levels on the same site; switching stations exist without transformers and operate at a single voltage level.

- The Substation Data set (Nature, Units, Quality Control and Data Structure)
  - A database of substations down to the primary level (33/11 kV or 33/6.6 kV) compiled from National Grid and six DNOs (data created in 2018; may have updates since).
  - Common attribute set includes:
    - SUBST_ID (unique per substation)
    - COMPANY_ID (substation ID within company)
    - SUBST_NAME (name as used by company)
    - COMPANY, REGIONAL_SERVICE_AREA
    - ASSET_TYPE (e.g. TRANS, GSP, BSP, PSS)
    - VOLTAGE_HIGH, VOLTAGE_LOW
    - CONSTRAINT_STATUS (capacity/connection constraints)
    - EASTING, NORTHING (Ordnance Survey grid)
  - Data handling notes:
    - Most records list two voltages; in some cases more than two voltages exist (highest and lowest recorded).
    - Highest value used when only a single voltage is listed.
    - Coordinates are OS grid-based easting/northing in metres.
  - Generation of the dataset emphasizes data harmonisation across sources with varying levels of detail and standardisation.

- Data Collection / Generation Methods (by organization)
  - National Grid
    - Shapefiles for substations and HV lines/cables; polygons converted to central points for comparability.
    - Initial 491 substations; after cleaning, 471 remain (313 at 400/275 kV classified as TRANS; others as GSP).
    - Some headhouses and very low-voltage sites removed; sealing-end/cable junctions kept.
  - SSE (Scottish & Southern Electricity Networks)
    - Data from August 2018 Excel file; 435 sites in North Scotland, 522 in Southern England, 957 total; includes Shetland additions to reflect July 2018 data.
    - Constraint status treated as simply constrained/unconstrained for transmission level.
    - A subset of North Scotland transmission sites (Beauly-Denny area) not captured initially; 24 additional sites identified through other sources.
  - SP Energy Networks
    - Data from SP Energy Networks website; 1,229 total after regional grouping (476 South Scotland, 753 MANWEB); 24 additional sites later identified in North Scotland.
    - Substation capacity classified as Green (available), Amber (near limit), Red (unlikely to connect without reinforcement); some sites use a traffic-light-style coding (capacity constraints).
  - Northern Powergrid
    - Data from generation-availability maps; 269 sites in North East England, 514 in Yorkshire (783 total) after filtering smaller substations (<33/11 kV) and matching by name.
  - Electricity North West
    - MapInfo data (June 2018); name and capacity added using thermal constraint and heat maps; capacity coded as Green/Amber/Red.
    - 608 records in total; adjustments made for unnamed sites and to align with voltage information.
  - Western Power Distribution
    - Shapefile data (1592 records) with key attributes; duplicates removed where multiple records mapped to same site (especially when BSP and primary substation co-located).
    - Final set: 1,433 sites distributed across regions (East Midlands, South Wales, South West England, West Midlands).
    - Used Aggregated Generation Headroom as the constraint indicator when other data were inconsistent.
  - UK Power Networks
    - DG Mapping Tool data; shapefiles for 132/33 kV and 33/11 kV substations; heat-map-based LSOA constraint statuses used to fill gaps.
    - Constraints categorized via mapping (1-6 from source to Green/Amber/Red); includes Flexible Distributed Generation (FDG) concept and SoW (Statement of Work) requirements.
    - After de-duplication, 1,327 sites remained (822 East England, 38 London, 467 South East England).
    - Substation voltage codings projected to 132/33 kV or 33/11 kV unless named differently (e.g., 33/6.6 kV).

- Data quality, gaps and harmonisation considerations for GIS work
  - Substantial variation in data completeness, terminology, and constraint classifications across DNOs.
  - Differences in voltage level definitions and site duplication (multiple assets on a single site) require careful deduplication and on-site validation.
  - Some regions/substations are missing from certain datasets (notably North Scotland for certain high-voltage sites).
  - Dataset reflects 2018 snapshot; ongoing updates and validation by individual companies are not reflected here.

- GIS-ready outcomes and practical uses
  - A harmonised, multi-source database of substations with coordinates, voltage ranges, asset types, and constraint indicators.
  - Enables map-based visualisations of transmission vs distribution assets, capacity constraints, and planned reinforcement needs.
  - Supports analysis of clustering of substations by region, voltage level, and potential feeding points for distributed generation connections.
  - Provides a framework for integrating future updates from the 2018 baseline, with explicit fields to capture source, regional area, and constraint status.