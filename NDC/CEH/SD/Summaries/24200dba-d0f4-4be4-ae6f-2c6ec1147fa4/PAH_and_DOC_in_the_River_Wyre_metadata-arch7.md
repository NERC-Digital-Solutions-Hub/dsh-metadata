# PAHs and DOC concentrations across sites and seasons

## Overview
- Dataset of PAH concentrations and dissolved organic carbon (DOC) measurements across five sites, collected in four seasons.
- Includes total dissolved PAHs, freely dissolved PAHs, PAHs bound to DOC, DOC concentration, and a derived log K_DOC (water-DOC partition coefficient).
- Designed to support map-based visualisations of spatial and temporal PAH distribution and their partitioning with DOC.

## Data fields
- Site: 1 = Marshaw Wyre; 2 = Abbeystead; 3 = Dolphinholm; 4 = Six Arches; 5 = Garstang.
- Season: 1 = 19 Aug 2010; 2 = 6 Dec 2010; 3 = 6 Mar 2011; 4 = 6 Jun 2011.
- total dissolved [ng L-1]: concentration of total dissolved PAHs.
- freely dissolved [ng L-1]: concentration of freely dissolved PAHs.
- DOC-bound [ng L-1]: concentration of PAHs bound to DOC.
- DOC [mg L-1]: concentration of DOC.
- log K_DOC: logarithmised water-DOC partition coefficient, derived from PAH and DOC concentrations.
- Definitions for derivation: c_total = total dissolved PAHs (ng L-1); c_free = freely dissolved PAHs (ng L-1); c_DOC = DOC concentration (mg L-1).

## Derived metric
- log K_DOC is computed from the PAH concentrations (c_total, c_free) and DOC concentration (c_DOC) to characterise the partitioning between water and DOC.

## GIS usage guidance
- Use Site as the spatial key to join to corresponding geographic features (points/polygons).
- Use Season as a temporal dimension for time-enabled maps or animations.
- Map each variable (total dissolved PAHs, freely dissolved PAHs, DOC-bound PAHs, DOC) and the derived log K_DOC to examine spatial patterns and seasonal changes.
- Validate and maintain consistent units across joins; manage missing data and note any assumptions in the derived log K_DOC calculation.

## Considerations and challenges
- Data may reside in multiple sources; ensure consistent data standards and integration.
- Potential data gaps at certain sites or seasons; plan for cautious interpretation or imputation if appropriate.
- Cleaning and transformation may be required to prepare data for GIS workflows and meaningful visualization.