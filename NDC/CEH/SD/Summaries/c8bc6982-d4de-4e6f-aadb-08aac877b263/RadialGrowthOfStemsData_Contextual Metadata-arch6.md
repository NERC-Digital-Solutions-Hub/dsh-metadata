# Radial growth in stems in human-modified forests of Eastern Amazonia

## Overview
- A dataset (RadialGrowthOfStemsData.csv) containing monthly radial growth measurements (in mm) of stems from 20 Amazonian forest plots arranged along a gradient of prior human disturbance (undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests).
- Timeframe: December 2014 to September 2018, collected under the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).
- Each plot hosts at least 50 dendrometer bands across five DBH size classes, plus bands on all lianas ≥10 cm DBH.
- Note: The overview mentions litterfall, but the dataset records radial growth of stems measured with dendrometers.

## Data collection and structure
- Plot design: 20 plots, each 250 x 10 m, distributed across the disturbance gradient; canopy disturbance classified via satellite chronosequence (1988–2010) and field assessments (fire scars, charcoal, logging debris).
- Measurement protocol:
  - Dendrometer bands installed 10 cm above DBH; waited one month to mark the no-growth line; first measurement taken ~5 months after marking, then monthly thereafter.
  - If a band was damaged, it was replaced and installation repeated; if a stem died, the band was moved to a new tree in the same size class.
  - Negative growth values may occur due to trunk water loss; negative values are not corrected.
- Data scope includes both individual trees and lianas/palms, with growth data tied to individual identifiers and plot metadata.
- Coordinates are provided for each plot/catchment (microcatchments ~5,000 ha), enabling spatial analysis.

## Data fields and measurements
- Core identifiers and location:
  - Catchment, Transect, Plot (unique plot code combining bacia and transect numbers), Rainfor
  - Forest (disturbance class before the 2015–16 El Niño)
  - Fire_ElNino (whether the plot burned during the 2015–16 El Niño)
- Individual-level data:
  - Tree_tag (individual identifier with dendrometer band)
  - Tree_code (unique code for the individual)
  - DBH (diameter at breast height; measured in 2014; units: cm)
  - Life form (A = tree, C = liana, P = palm)
  - Re-installed (whether a dendrometer was re-installed during the collection)
- Monthly measurement data (Data-Dec14 onward):
  - Data-Dec14, mm-Dec14, OBS-Dec14 (and similarly for subsequent months: Jan15, Feb15, etc.)
  - mm-<Month> fields represent radial growth in millimeters for that month
  - OBS-<Month> fields contain field notes for that month
- File format: Comma-separated values (CSV) with a structured schema for monthly radial growth data across all individuals and plots

## Temporal and spatial scope
- Temporal coverage: December 2014 through September 2018 (monthly measurements after the initial marking period)
- Spatial coverage: 20 plots across a gradient of disturbance inside Eastern Amazonian forests; coordinates for each plot are provided

## Data quality, caveats, and provenance
- Data collected under a formal programme (HMTF) and accompanied by plot-specific disturbance classifications
- Data handling includes band maintenance and re-installations; growth values may be negative due to water loss in bark and are not corrected
- Some months may have notes or missing values where re-installation or field conditions affected measurements

## Potential uses and data products
- Assess effects of disturbance type and El Niño-related fire on stem radial growth
- Compare growth dynamics across life forms (trees, lianas, palms) and DBH size classes
- Temporal analyses of monthly growth trends and growth responses to disturbances
- Combine with forest disturbance and canopy data for integrative analyses; suitable for dashboards or self-serve analyses by researchers or policy teams

## Access, references, and relationships
- Related data collection and provenance: NERC HMTF Programme; Grant NE/K016431/1
- Data can be integrated with the ForestPlots database (Rainfor) and other plot-level metadata for enriched analyses