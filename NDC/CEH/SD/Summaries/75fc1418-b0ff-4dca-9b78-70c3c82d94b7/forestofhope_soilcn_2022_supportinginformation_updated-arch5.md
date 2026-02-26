# Forest of Hope – Soil CN Baseline Winter 2022

## Overview and purpose
- Describes soil carbon (C) and nitrogen (N) baseline measurements at the Forest of Hope, Highlands Rewilding, Beldorney Estate.
- Supports comparison between planted forest plots and natural regeneration plots, with a grassland control for reference.
- Baseline data collected to monitor soil C and N changes as the woodland establishes.

## Study site and design
- Location: Forest of Hope within the Beldorney Estate (lat 57.409, lon -2.966).
- Planting: 1600 stems/ha across mixed native species; planting began Winter 2022 and to complete by early 2024.
- Plots: 17 planted plots and 17 natural regeneration plots (40 m x 40 m each); plots matched between planted and natural regeneration areas.
- Natural regeneration assessment plots are distributed along a distance gradient from seed sources and an eastern semi-natural native woodland.
- Baseline soil samples collected autumn 2022 to establish initial C and N metrics.
- Additional sampling extended into surrounding grassland to create a control dataset.

## Experimental sampling regime
- 17 soil samples on a 100 m grid within the planting area (pre-mounding and planting in Sept 2022).
- 8 additional samples collected in grassland to monitor a control area extending the 100 m grid.
- In November 2022, extra sampling occurred in the 40 × 40 m unplanted plots for spatial monitoring of natural regeneration.
- One unplanted plot (U8) was not sampled due to a pond being present.

## Collection methods and depths
- Equipment: soil sampling using a 1.9 cm diameter auger.
- Depths: 0–10 cm and 10–30 cm (depths recorded where sampling did not reach 30 cm).
- Sample processing: fresh weight measured, samples dried at 60°C for at least 48 hours to constant mass, then weighed.
- Fractionation: samples sieved to <2 mm; weights for <2 mm and >2 mm fractions recorded.
- Subsampling for chemical analysis: 5 g of <2 mm fraction ball milled; ~10 mg transferred to tin capsule for elemental analysis.

## Analytical measurements and data products
- Analyzed using an elemental analyzer to determine carbon and nitrogen content.
- Reported values include:
  - Fresh weight, dry weight (g)
  - Bulk density (g/cm3) based on <2 mm fraction
  - %C and %N
  - Total C and Total N (g/cm3) calculated from bulk density and %C/%N
- Data record includes core dimensions, sample volumes, and precise weight measurements.

## Data structure and metadata
- Primary dataset: ForestOfHope_SoilCN_Winter2022.csv
- Key fields include:
  - Location_ID and Description (sample location identifiers and type: planted grid, grassland grid, natural regeneration plot)
  - Lat/Long and What3words for geolocation
  - Date_collected
  - Top_core_cm, Bottom_core_cm, Core_height_cm, Core_diameter_cm, Core_volume_cm3
  - Fresh_weight_g, Dry_weight_g
  - More_2mm_g, Less_2mm_g
  - Bulk_density_gcm3, N_percent, C_percent
  - Total_N_gcm3, Total_C_gcm3
- Clear traceability and documentation of sampling locations, depths, and analytical methods for reproducibility.

## Quality control and data governance
- Pre-collection numbering system implemented to track samples.
- Lab processing conducted by experienced technicians to ensure precision in elemental analysis.
- Exact weights recorded to high precision (0.001 mg for subsamples) to ensure data accuracy.
- Data lineage: from field collection to lab analysis, with detailed methodological notes and unit definitions.

## Relevance for data stewardship
- Demonstrates end-to-end data lifecycle: planning, collection across multiple plot types, lab analysis, and structured data file with comprehensive metadata.
- Highlights the importance of harmonizing spatially distributed sampling data (planted vs. natural regeneration vs. control grassland) with consistent units and depth records.
- Provides a single dataset ready for integration into broader site data portals, enabling comparative analyses of soil C and N dynamics during woodland establishment.
- Enables versioning and updates (e.g., incorporation of 2023 planting review outcomes) while preserving baseline winter 2022 data.

## Limitations and notes
- One unplanted plot (U8) excluded due to pond formation.
- Some locations could not be sampled to the full 30 cm depth, and the exact depth achieved is recorded.
- Sampling achieved across multiple grids and plot types, which may require careful metadata alignment when integrating with other site datasets.