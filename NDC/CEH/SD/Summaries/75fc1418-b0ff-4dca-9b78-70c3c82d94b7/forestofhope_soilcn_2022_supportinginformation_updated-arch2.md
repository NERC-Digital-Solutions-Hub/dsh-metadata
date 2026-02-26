# Overview

- The Forest of Hope is a native forest creation site on Highlands Rewilding's Beldorney Estate (lat 57.409, lon -2.966).

- Planting details: density of 1600 stems/ha with a species mix of birch 40%, sessile oak 20%, hazel 10%, alder 10%, rowan 10%, willow 5%, hawthorn 5%.

- Planting timeline: began Winter 2022 and planned to be completed in early 2024 after a review of the 2023 planting.

- Experimental plots: 17 unplanted 40 × 40 m plots dispersed throughout the planting area to assess natural regeneration; these natural-regeneration plots are matched to planted plots for comparative monitoring of tree establishment and associated soil and biodiversity metrics.

- Baseline measurements: soil samples collected autumn 2022 to assess soil carbon (C) and nitrogen (N).

- Overall aim for analysts: establish standardized, monitorable baselines for soil C and N and track regeneration and ecosystem development over time, with outputs suitable for reports, maps, and data portals. Explore opportunities to increase data value by linking to other datasets and ensuring broad data accessibility.

## Experimental design and sampling regime

- Baseline soil sampling (Sept 2022): 17 samples on a 100 m grid within the Forest of Hope site prior to mounding and planting. The 100 m grid extends into adjacent grassland to incorporate a control context.

- Control sampling: 8 additional samples extended into the grassland area to serve as a non-planted control.

- Natural regeneration plots: additional soil samples collected in Nov 2022 within the 40 × 40 m unplanted plots to monitor natural regeneration in parallel with planted areas.

- Plot mapping: study plots include planted 40 × 40 m plots and natural regeneration plots; natural regeneration plot centroids are used for sampling.

## Collection methods and measurements

- Soil collection: 1.9 cm diameter auger used at each sampling point.

- Depths: 0–10 cm and 10–30 cm where possible (some locations could not reach 30 cm; depth duly recorded). One unplanted plot (U8) was not sampled due to a pond.

- Sample processing: fresh weight recorded; samples dried at 60°C for at least 48 hours to constant mass; dry weight recorded; samples sieved to <2 mm and weighed for <2 mm and >2 mm fractions.

- Subsampling and analysis: ~5 g of the <2 mm fraction milled; ~10 mg weighed for elemental analysis.

- Analyses: carbon and nitrogen content determined with an elemental analyzer.

- Calculations: absolute total C and N per sample derived from bulk density (based on <2 mm fraction) and %C/%N; outputs include fresh weight, dry weight, bulk density, %C, %N, and total C and N per sample (g/cm3).

## Data quality, management, and structure

- Documentation and tracking: a unique sample ID system used to track samples throughout collection and analysis.

- Quality control: samples handled by experienced lab technicians; high-precision weighing to ensure accurate CN results.

- Data structure: single .csv file named ForestOfHope_SoilCN_Winter2022.csv with fields including:
  - Location_ID, Type, Lat, Long, What3words, Date_collected
  - Top_core_cm, Bottom_core_cm, Core_height_cm, Core_diameter_cm, Core_volume_cm3
  - Fresh_weight_g, Dry_weight_g, More_2mm_g, Less_2mm_g, Bulk_density_gcm3
  - N_percent, C_percent, Total_N_gcm3, Total_C_gcm3
  - Type values denote: 100m grid planted (pre-mounding/planting), 100m grid grassland, natural regeneration plot
  - Each column is described in the dataset documentation.

## Location-specific notes and data interpretation

- Notable site detail: coordinates correspond to Highlands Scotland; baseline sampling was designed to enable comparison between planted and naturally regenerating areas and to inform subsequent monitoring of soil carbon and nitrogen stocks.

- Data considerations: one unplanted plot omission (U8) due to pond; sampling across depth intervals may not be complete in all locations.

## Data management, accessibility, and next steps

- Purpose: establish robust soil C and N baselines to support longitudinal monitoring of planted forest development and natural regeneration, enabling assessment of soil health and carbon stock changes over time.

- Data sharing: dataset to be stored and uploaded to appropriate data portals, enabling broader access for policy analysis and environmental monitoring.

- Timeline context: planting from Winter 2022 with completion targeted for early 2024; ongoing monitoring of tree establishment, soil properties, and biodiversity metrics in both planted and natural regeneration plots.