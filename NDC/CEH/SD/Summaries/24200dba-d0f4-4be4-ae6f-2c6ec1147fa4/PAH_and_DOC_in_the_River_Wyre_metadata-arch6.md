# PAH concentrations and DOC partitioning across sites and seasons

## Overview
- A dataset capturing PAH concentrations in water across five sites and four seasons, including total dissolved PAHs, freely dissolved PAHs, and PAHs bound to dissolved organic carbon (DOC).
- Includes DOC concentration and a derived log water-DOC partition coefficient (log K_DOC) based on PAH and DOC measurements.
- Intended to enable analysis of how PAHs partition between dissolved phases and DOC, supporting environmental assessment and data-driven insights.

## Data fields and meanings
- Site
  - 1 = Marshaw Wyre
  - 2 = Abbeystead
  - 3 = Dolphinholm
  - 4 = Six Arches
  - 5 = Garstang
- Season
  - 1 = 19th August 2010
  - 2 = 6th December 2010
  - 3 = 6th March 2011
  - 4 = 6th June 2011
- total dissolved [ng L-1]
  - Concentration of total dissolved PAHs
- freely dissolved [ng L-1]
  - Concentration of freely dissolved PAHs
- DOC-bound [ng L-1]
  - Concentration of PAHs bound to DOC
- DOC [mg L-1]
  - Concentration of DOC
- log K_DOC
  - Logarithmised water-DOC partition coefficient, derived from PAH and DOC concentrations
  - Based on c_total (total dissolved PAHs, ng L-1), c_free (freely dissolved PAHs, ng L-1), and c_DOC (DOC concentration, mg L-1)

## Calculation note
- log K_DOC is a computed metric using PAH concentrations and DOC:
  - c_total: total dissolved PAHs (ng L-1)
  - c_free: freely dissolved PAHs (ng L-1)
  - c_DOC: DOC concentration (mg L-1)
- The exact formula is derived from these values to quantify the PAH partitioning between the water phase and DOC.

## Scope and structure
- Spatial: 5 sites with assigned names
- Temporal: 4 seasons (specific dates)
- Data points: up to 20 site-season combinations
- Use cases: compare PAH partitioning across sites and seasons; explore relationships between DOC levels and PAH speciation; support environmental risk assessment

## How this supports data use (Data Support perspective)
- Facilitates building self-serve analyses (tables and dashboards) by providing consistent fields and units.
- Enables data quality workflows: verify site-season mappings, ensure unit consistency (ng L-1 for PAHs, mg L-1 for DOC), and compute log K_DOC uniformly.
- Supports data integration with related datasets (e.g., additional water chemistry or site characteristics) to drive deeper insights.
- Encourages sharing outputs and iterating on dashboards or reports to promote broader data use and understanding.

## Potential challenges and considerations
- Patchy data or variations in data formats across fields or seasons.
- Ensuring consistent units and naming conventions across datasets or future updates.
- Communicating the interpretation of log K_DOC and its dependence on c_total, c_free, and c_DOC to non-technical stakeholders.

## Suggested data products and next steps
- Create a dashboard showing PAH concentrations (total, freely dissolved, DOC-bound) by site and season, with log K_DOC as an additional metric.
- Develop pivot tables to compare DOC concentrations with PAH partitioning across sites.
- Document data provenance and quality checks to support future reuse and expansion of the dataset.