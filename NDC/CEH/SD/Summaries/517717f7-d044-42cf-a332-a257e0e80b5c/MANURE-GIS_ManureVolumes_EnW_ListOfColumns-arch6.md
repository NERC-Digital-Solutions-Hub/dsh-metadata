# DATA STRUCTURE

## Overview
- Manure volumes by livestock type and land use for England and Wales are stored in a shapefile named MANURE-GIS_ManureVolumes_EnW.shp.

## Dataset and Format
- The data are organized as a geospatial shapefile with attributes describing the source livestock sector, manure type, and destination land-use type, plus units.
- Covers multiple livestock sectors: Beef, Dairy, Layers, Pigs, Sheep, and Broilers (poultry).
- Attributes follow a structured coding scheme that links livestock, manure type, and land-use destination.

## Naming conventions
- Prefix indicates livestock sector:
  - B_ = Beef, D_ = Dairy, L_ = Layers, P_ = Pigs, S_ = Sheep, Bro_ = Broilers (poultry)
- Middle segment indicates manure type:
  - FYM = Farmyard manure, Slu = Slurry, Direct excreta, etc.
- Suffix indicates Destination Land Use Type:
  - Gras = Grass, AraW = Arable Winter, AraS = Arable Spring, and other codes; some entries use - for unspecified.
- Units column shows measurement units.

## Examples
- B_FYM_Gras: Beef, Farmyard manure, Grass, kilograms
- D_FYM_AraW: Dairy, Farmyard manure, Arable Winter, kilograms
- S_Grazing: Sheep, Direct excreta, Grass (managed), kilograms
- P_Slu_AraS: Pigs, Slurry, Arable Spring, litres
- L_FrRngGra: Layers (Free Range), Direct excreta, Grass (managed), kilograms

## Units and data coverage
- Units include kilograms (solid manure) and litres (slurry).
- Data pertains to England and Wales.

## Notable caveats
- Sheep grazing data: only the proportion of excreta deposited on managed grass is included; excreta on rough grazing is not counted.

## Data use implications for data support
- Enables detailed, self-serve analyses and mapping of manure volumes by sector, manure type, and land-use destination.
- Useful for integrating with other geospatial datasets to inform policy, planning, and agricultural management.
- Requires filtering by sector, manure type, and land-use code to create targeted data products or dashboards.