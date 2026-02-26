# Vegetation data from the South Fork McKenzie River in Oregon, USA

- Purpose: Assess vegetation response to wildfire in restored and unrestored sites.
- Collection date: June 2021.
- Size: 88.66 KB, four CSV files totaling the dataset.
- Collected by: Andrès Holz, Krista Farris, Bobette Jones, Upekala Wijayratne.
- Interpreted by: All authors.
- Taxonomic scope: Identified to genus/unclear (40 taxa) and species (29 taxa); total taxonomic units (69).

## Data files and structure

- SFMR_Veg_Coordinates
  - Columns: Transect, Quad, Lat, Long.
- SFMR_Veg_Species
  - Columns: Transect, Site, Quad, Treatment, Initials, Species.name, Cover.Class, Cover.2, Comments, Category, Family, Duration, Growth_Habit, Native_Status.
  - Notes: Species.name; Cover.Class follows Braun-Blanquet scale; Cover.Class.pct converts to % cover.
- SFMR_Veg_Ground
  - Columns: Transect, Quad, Type, Cover_Class, Cover_class_pct.
  - Notes: Ground cover types (e.g., leaf litter, bare ground, moss, log) with Braun-Blanquet scale and % cover.
- SFMR_Veg_Canopy
  - Columns: Transect, Quad, Measurement, Densiom.
  - Notes: Canopy density measured with a densiometer; Measurement encodes cardinal directions (North=1, East=2, South=3, West=4); decimals indicate off-cardinal readings; Densiom is canopy unoccupied by vegetation (%).

## Spatial coverage and sampling design

- Location: Latitude 44.17, Longitude -122.30.
- Transects and quadrats: Data collected along two transects with multiple 1x1 m quadrats.
- Sampling scheme: 20 quadrats in total; includes:
  - 8 quadrats along transects 1 and 2 in restored/burned treatment.
  - 4 quadrats paired with soil data.
  - 4 quadrats paired with soils sampling locations in unrestored/degraded/burned treatment.
  - 3 quadrats in unburned/non-degraded treatment.

## Methods and data standards

- Collection method: Estimated abundance using Braun-Blanquet cover classes, 20 quadrats total.
- Treatments:
  - restored.burned
  - unrestored.burned
  - unrestored.unburned (reference site at Horse Creek to the East)
- Data quality: Collected with standardized procedures by trained fieldworkers; field sheets digitised and double-checked prior to upload.

## Data integration and GIS readiness

- Relational joins: Data can be linked across files via Transect, Site, and Quad.
- Attribute readiness:
  - Species dataset provides taxonomy, growth habit, life duration, native status, and family.
  - Ground dataset adds ground cover types with percent cover.
  - Canopy dataset supplies directional canopy density readings.
- Visualization potential: Map-based representations of species composition, ground cover classes, and canopy density by treatment and location; supports comparisons between restored and unrestored sites and wildfire effects.

## Additional notes

- Dataset explicitly documents taxonomic resolution (genus/species) and total taxa (69).
- The Cover.Class values are accompanied by converted percentages (Cover.Class.pct) for GIS quantification.
- Collected June 2021; structure includes four CSVs named SFMR_Veg_Coordinates, SFMR_Veg_Species, SFMR_Veg_Ground, and SFMR_Veg_Canopy.