# Vegetation data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Monitoring dataset collected to assess vegetation response to wildfire in restored and unrestored sites.
- Collected and interpreted by a team led by Andrès Holz, Krista Farris, Bobette Jones, and Upekala Wijayratne.
- Location includes transects around restored/burned, unrestored/burned, and unrestored/unburned reference sites (Horse Creek to the East).
- Collection date: June 2021.
- Dataset size: 88.66 KB; comprises four separate CSV files.

## Purpose and scope
- Aimed at evaluating how vegetation communities respond to wildfire under different restoration treatments.
- Data supports comparisons across treatment categories: restored.burned, unrestored.burned, unrestored.unburned (and reference context).

## Datasets and structure
- SFMR_Veg_Coordinates.csv
  - Columns: Transect, Quad, Lat, Long.
  - Provides spatial locations of sampling quadrats.

- SFMR_Veg_Species.csv
  - Columns: Transect, Site, Quad, Treatment, Initials, Species.name, Cover.Class, Cover.2, Comments, Category, Family, Duration, Growth_Habit, Native_Status.
  - Species-level data with identification to genus/species (69 total taxa), abundance using Braun-Blanquet cover classes (0.1–5) and conversion to percent cover (Cover.Class.pct).
  - Includes metadata on plant category (dicot, monocot, gymnosperm, etc.), growth habit, duration, and native status.
  - Initials denote data collectors; Comments capture field notes.

- SFMR_Veg_Ground.csv
  - Columns: Transect, Quad, Type, Cover_Class, Cover_class_pct.
  - Ground cover data (e.g., leaf litter, bare ground, moss, log) with Braun-Blanquet classes and percent cover conversions.

- SFMR_Veg_Canopy.csv
  - Columns: Transect, Quad, Measurement, Densiom.
  - Canopy cover measurements by cardinal directions (North=1, East=2, South=3, West=4; decimals used for off-cardinal points).
  - Densiometer readings indicate canopy openness (% unoccupied by vegetation).

## Sampling design and intensity
- Total quadrats: 20 (1x1 units).
- Restored/burned treatment: 8 quadrats.
- Unrestored/degraded/burned: 4 quadrats (paired with soil data locations).
- Unrestored/unburned (reference context): 4 quadrats (paired with soils sampling locations).
- Unburned/non-degraded treatment: 3 quadrats.
- Quadrats distributed along two transects for each treatment group, with paired soil sampling in select treatments.

## Collection methodology and quality control
- Abundance estimated using Braun-Blanquet cover class method.
- Standardized field procedures implemented by trained fieldworkers.
- Data digitized from field sheets and double-checked prior to upload.
- Metadata and data transformations (e.g., Cover.Class to percent cover) documented within datasets.

## Notes for use
- Species data includes a mix of identification levels (40 genus/unclear, 29 species; total taxa = 69).
- Data is organized to enable cross-treatment comparisons of species composition, ground cover, and canopy structure.
- The dataset supports analyses of vegetation response to wildfire under restoration scenarios and comparison with an unburned reference site.