# Forest inventory and lightning strikes data from the Ngel Nyaki forest, Nigeria, from 2018-2021

## Overview
- Two CSV datasets describing tree inventory and lightning-strike events in a 40-hectare plot at Ngel Nyaki Forest Dynamic Plot, south-eastern Nigeria.
- Timeframe: June 2018 – July 2021.
- Sample: 2,552 individual trees measured for diameter and living status; 23 lightning-strike events documented.
- Location context: Ngel Nyaki is a submontane, phylogenetically diverse forest within the ForestGEO network. The work contributed to the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Data content
- Forest_inventory_NgelNyaki_Nigeria_2018_2021.csv
  - Per-tree measurements and status across the census periods.
  - Key fields: Tree_id, census_date, POM (point of measurement in cm), D (diameter in cm at POM), Tree_status (coded alive/dead with subcategories).
  - Diameter and status data used to assess mortality and condition (e.g., alive, dead, hollow, broken, uprooted, etc. with multi-letter codes).
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Subset of trees from the inventory that were struck by lightning.
  - Key fields: Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_strike, Fuse_status, Observations_strikes, Tree_status_after, Observations_after.
  - Includes 23 lightning strike records, with pre-strike and post-strike statuses and fuse condition.

## Data collection methods
- Field census in the 40-ha plot: tagged and measured all trees and lianas with stem diameter at 1.3 m (or above buttresses) ≥25 cm; recorded living status and mode of death.
- Measurements:
  - POM (point of measurement) typically 130 cm; adjusted if buttress/deformity required.
  - D (diameter) at current POM; missing D recorded as 0 when dead and not measured.
- Lightning detection:
  - Each measured tree equipped with a Rogowski Coil sensor to detect lightning strikes without harming the tree.
  - Quick visual check of fuse condition to confirm strike; documented damage to tree and surroundings.
- Quality control:
  - Unit checks, flagging ambiguous values for review against field notes; resurvey when possible; unresolved issues flagged for future surveys.
  - Missing values exist where field records were ambiguous or incomplete.

## Data structure and key fields

- Forest_inventory_NgelNyaki_Nigeria_2018_2021.csv
  - Tree_id: unique tag number for each stem.
  - census_date: date of census measurement.
  - POM: point of measurement (cm), typically 130 cm; adjusted to avoid buttress/deformity.
  - D: diameter (cm) at the POM; if dead and not measured, D = 0.
  - Tree_status: coded living/dead status, with multi-letter codes (examples):
    - A = alive; D = dead.
    - Second-letter combinations indicate conditions (e.g., AN = Alive Normal, AB = Alive Broken, AH = Alive hollow, DL = Dead by lightning, etc.).
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Country, Site, Plot: site identifiers.
  - Tree_id: link to inventory tag.
  - Species: taxonomic identification.
  - census_strike_date: date (month/year) of census when strike was recorded.
  - POM_strike: diameter measurement at strike date (cm).
  - D_strike: diameter at POM_strike (cm); 0 if not measured due to death.
  - Tree_status_strike: status at the census prior to strike (same coding as Tree_status).
  - Fuse_status: fuse condition at census_strike_date (notes on electrical fuse health).
  - Observations_strikes: qualitative notes from the pre-strike census.
  - Tree_status_after: status at the latest census after the strike (same coding as Tree_status).
  - Observations_after: notes about the tree after strike.

## Codes and interpretation (examples)
- Tree_status (and Tree_status_strike/Tree_status_after): A = Alive; D = Dead. Second-letter combinations provide finer states (e.g., AN = Alive Normal, AB = Alive Broken, AH = Alive hollow, DL = Dead by lightning, DS = Dead standing, DU = Dead, unknown location, etc.).
- D_strike and D (where applicable) reflect diameters at the relevant measurement points; D = 0 when not measured due to death.

## Potential uses for data support and analysis
- Assess the role of lightning in tree mortality by comparing pre- and post-strike statuses and fuse outcomes.
- Link diameter and species to susceptibility to lightning damage.
- Explore spatial and species-wide patterns of mortality within the 40-ha plot.
- Integrate with ForestGEO data to compare mortality drivers across sites.
- Develop self-serve data products (dashboards, pivotable views) enabling end users to investigate mortality risks and disease indicators related to lightning events.
- Promote data reuse and sharing to improve understanding of tropical forest disturbance and mortality processes.

## Provenance and access
- Data collected under the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).
- Data are provided as two CSV attachments with documented field definitions and coding.