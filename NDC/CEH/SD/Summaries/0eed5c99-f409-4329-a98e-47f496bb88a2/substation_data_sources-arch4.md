# Network and Substation Characteristics

## Overview
- GB electricity network comprises two tiers: transmission (high voltage) and distribution (lower voltage).
- Transmission: 400 kV and 275 kV lines with interconnectors to Ireland and France (and planned to Norway and Belgium).
- Distribution: 14 licensed distribution network operators (DNOs) delivering from transmission to industrial, commercial, and domestic users.
- Transmission and distribution are operated by different entities across England, Scotland, and Northern Ireland (with six main company groups owning the 14 DNOs).

## Network Structure and Stakeholders
- Transmission network operators:
  - National Grid (England)
  - Scottish Hydro Electric and Scottish Power (Scotland)
- Distribution network operators (DNOs) managed by six companies:
  - UK Power Networks
  - Western Power Distribution
  - Scottish Power Energy Networks
  - SSE (Scottish and Southern Electric)
  - Northern Powergrid
  - Electricity North West
- Substations and related assets are organized by voltage level and service area, with sites often housing multiple administrative and technical entities.

## Voltage Levels and Substation Typology
- Transmission voltages: 400 kV and 275 kV (with 132 kV in Scotland as part of the transmission/distribution boundary).
- Distribution voltages include 132 kV, 66 kV, 33 kV, 11 kV, 6.6 kV, and 230/400 V, with various use cases (e.g., 132 kV for higher-level distribution, 33 kV intermediate steps, and 11 kV/6.6 kV for local distribution).
- Substation types:
  - Transmission substations (TRANS): 400 kV or 275 kV, often connected to major generation sources.
  - Bulk Supply Points (BSPs): intermediate substations stepping down from transmission levels.
  - Primary Substations (PSS): step-down points closer to the distribution network.
  - Distribution substations (e.g., 132 kV, 33 kV, 11 kV levels) delivering to local networks.
  - GSPs (grid supply points) and switching stations (no transformers, single voltage level, used for collection/distribution or back-up switching).

## The Substation Data - Nature, Units, Quality Control and Data Structure
- A database of substations down to the primary level (33/11 kV or 33/6.6 kV) was created, focusing on sites large enough to serve generators like solar farms or wind turbines.
- Core attributes captured for each site:
  - SUBST_ID (unique substation identifier)
  - COMPANY_ID (substation in company database)
  - SUBST_NAME, COMPANY
  - REGIONAL_SERVICE_AREA
  - ASSET_TYPE (e.g., TRANS, GSP, BSP, PSS)
  - VOLTAGE_HIGH, VOLTAGE_LOW
  - CONSTRAINT_STATUS (extent of generation connection constraints)
  - EASTING, NORTHING (Ordnance Survey coordinates)
- Many DNOs list two voltages per site (high/low); when more than two voltages exist (e.g., combined facilities), the highest and lowest are recorded.
- Constraint status is a simplified traffic-light system (red/amber/green) where possible, with variability in standardisation across utilities.

## Collection / Generation Methods
- Data compiled from multiple sources, with the dataset created in 2018 and potentially updated since. Key contributors include:
  - National Grid: shapefiles for substations and HV lines; substations converted to central points; initial 471 sites after cleaning (313 at 400/275 kV as TRANS; others as GSP).
  - SSE Networks: generation availability data (August 2018) used to determine constraint status (constrained/unconstrained) and site counts (North Scotland, Southern England, total 957–459 sites after updates).
  - SP Energy Networks: 1,229 total records (South Scotland and MANWEB regions) with capacity classifications Green/Amber/Red indicating connection suitability and reinforcement needs.
  - Northern Powergrid: ~783 sites after filtering for ≥33/11 kV.
  - Electricity North West: 608 records; enhanced with names and capacity classification (Green/Amber/Red) using thermal maps and other sources.
  - Western Power Distribution: 1,592 records; duplicates removed; final list 1,433 sites across regions; various constraint and capacity attributes.
  - UK Power Networks (UKPN): DG Mapping Tool data for 132 kV/33 kV/11 kV substations plus heat maps; constraint status mapped to orderings (GREEN/AMBER/RED); status codes supplemented with LSOA-based classification when site data were incomplete.
- Data integration and standardisation steps:
  - Substations from multiple sources were harmonised into a single dataset, including conversion to comparable point geometries and alignment of voltage classifications.
  - Where possible, constraint and capacity information were standardised (e.g., FDG status, SoW requirements).
  - Duplicates and inconsistent entries were identified and removed; voltage levels and site associations adjusted to maintain coherent mappings.

## Data Quality, Gaps and Limitations (Implied)
- Incomplete constraint information for some regions and sites; some regions (e.g., North Scotland) lacked full coverage in certain sources.
- Substations with limited or missing voltage or constraint data required inference or mapping from related sources, potentially introducing inconsistencies.
- Duplicates existed across datasets (e.g., multiple records for the same site); de-duplication was necessary to achieve a clean final dataset.
- The 2018 dataset reflects the state of data at that time; updates and changes since may not be captured uniformly across all sources.
- Interpretations of constraint status varied between companies, requiring careful normalization to a common scheme (e.g., GREEN/AMBER/RED), with some edge cases remaining ambiguous.

## Implications for Data Leaders
- This consolidated substation dataset provides a foundational asset for assessing network capacity, planning connections for distributed generation, and informing policy and operational decisions.
- Emphasises the importance of:
  - A unified data model with clear fields, units, and coding (e.g., VOLTAGE_HIGH/LOW, ASSET_TYPE, CONSTRAINT_STATUS).
  - Robust data provenance and version control, given multiple sources and update cycles.
  - Metadata and standardisation practices to reduce ambiguity across utilities and over time.
  - Continuous data quality improvement, including filling gaps in constraint information, reducing duplicates, and reconciling voltage classifications.
- Encourages collaboration across the wider data community (utilities, regulators, and planners) to maintain an accurate, up-to-date view of substations and their connectivity constraints.