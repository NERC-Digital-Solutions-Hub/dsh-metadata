# Flower density values of common British plant species [AgriLand]

## Overview
- Data format: .csv, three spreadsheets
- Project: UK IPI AgriLand grant BB/H014934/1
- Data collection period: 2011–2012; dataset creation: 2015
- Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott (contact emails provided)
- Field survey window: February–October 2011–2012; majority sites in southern England (Bristol, UK)

## Data structure and content
- Spreadsheet 1: AgriLand_FlowerDensity_herbs.csv
  - 1380 observations, 169 species, 22 columns
  - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency, counts for buds/opened/fruited floral units, cross points, vegetative area, opened/total flowers per floral unit, per m2 metrics
- Spreadsheet 2: AgriLand_FlowerDensity_trees.csv
  - 85 observations, 10 species, 27 columns
  - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency, height-related measurements, flower distribution, counts of floral units, vegetative area, per m2 metrics
- Spreadsheet 3: AgriLand_FlowerDensity_perspecies.csv
  - 179 species, 15 columns
  - Key fields: species, FU.category, per-species statistics (mean, variance, and sample size) for opened flowers per floral unit, total flowers per floral unit, flowers per m2 of vegetative cover, and peak-season estimates

## Field surveys and sampling regime
- Field period: February–October 2011–2012
- Locations: predominantly in southern England (e.g., Bristol area)
- Sampling per species:
  - 5 quadrats per population; 2 populations per species when possible
  - Median total quadrats per species: 10 (range 1–20)
  - Flowers counted per floral unit to estimate density
- Species list selection:
  - Based on Countryside Survey 2007; 270 target species (insect-pollinated plants plus some other important taxa)
  - 50 locally important species added; total initial target list of 270 species

## Data collection, transformation and analysis
- Herbs and shrubs (0.5m x 0.5m quadrats):
  - Vegetative cover estimated via cross points (max 36 points for 0.25 m²)
  - Outputs include: nb. of floral units in buds/opened/fruited; nb. of buds/opened/fruiting flowers per floral unit; vegetative area; flowers per m² (opened and total)
- Trees (3D sampling in 0.5m³ cube at tree outer foliage):
  - Height estimation using inclinometer values (top, upper trunk, bottom) and distance
  - Flower distribution within foliage recorded; extrapolated to whole tree using height and distribution class
  - Outputs include: nb. of floral units in buds/opened/fruited; total floral units; opened/total flowers per m² of vegetative cover; total flowers per tree column
- Calculations:
  - Vegetative cover area = cross points × 0.25 / 36
  - Total flowers per opened floral unit = buds + opened + fruited
  - Total floral units = buds + opened floral units + fruited floral units
  - Flowers per m² = flowers / vegetative surface
  - Tree height: derived from inclinometer measurements and distance
  - Whole-column flower estimates: based on counts in the 0.5 m height cube, tree height, and distribution percentage
  - Statistics: mean, variance, and sample size of flower density (flowers per m²) per species

## Species list and project context
- Species were selected from UK Countryside Survey 2007 results, prioritizing pollinator-rewarding species
- Final scope included 270 plant species (with 50 additional locally important species)

## Access, responsibilities and references
- Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott
- Project grant: BB/H014934/1
- Key references:
  - Baude et al. 2015 (Britain in bloom: national-scale changes in nectar resources for pollinators, in revision)
  - Carey et al. 2008 (Countryside Survey: UK Results from 2007)
- Data availability and metadata are provided within the three spreadsheets, including detailed variable descriptions and units
- Field data locations and sample sizes summarized in the row data appendix