# Supporting documentation to dataset: Anthropogenic litter data collected from the Portoviejo River, Ecuador, 2021-2022

- Purpose and context
  - Documents a dataset of weekly litter weights (kg) by category, collected Feb 2021–Dec 2022, to monitor riverine transport of anthropogenic litter from the Portoviejo River toward the ocean.
  - Part of a NERC-funded project aiming to reduce plastic leakage in the Eastern Pacific and support sustainable, circular plastics resource flows.

- Experimental design and sampling regime
  - Location: Portoviejo River, Ecuador (1° 01' 23.9" S, 80° 29' 35.6" W).
  - Sampling period: February 2021 to December 2022.
  - Frequency: daily on weekdays (excluding bank holidays); generally even coverage, with interruptions on days of high river flow (>4.5 m), mainly March–April.
  - Exact interruption dates not always recorded.

- Collection methods
  - Barrier system: Azure System (Ichthion Limited) traps floating litter and channels it to a shoreline sorting area.
  - Classification: litter categorized by material type according to OSPAR Guidelines (Edition 1.0, 2010) for marine litter on beaches.
  - Measurement: weights recorded in kilograms using a hand scale and logged in field spreadsheets, then compiled into digital spreadsheets as weekly weights per category.

- Data quality control
  - Oversight by expert lead engineer during data collection.
  - Data assembled, revised, and reported by lead field engineer Desiree G. Hidalgo (Ichthion).
  - Data interpretation and analysis by Dr. Lara Pinheiro, University of Exeter.

- Data structure and metadata
  - File: LitterData_PortoviejoRiver.csv.
  - 39 columns: includes Site, Year, Month, Week, Latitude, Longitude, Sample_Depth, followed by litter categories (e.g., Aerosol_and_spray_cans, Animal_waste, Bags_shopping_empty, Bags_shopping_filled, Bottles_glass, Caps_and_lids, Cardboard, Clothing, Cosmetics_bottles, Cups, Cutlery_trays_straws, Drink_cans, Drinks_bottles_containers_and_drums, Face_mask, Foam_sponge, Food_cans, Food_containers, Hard_hats, Jute_sack_filled, Light_bulbs_or_tubes, Organic_waste, Other, Other_bottles_containers_and_drums, Other_metal_pieces, Other_sanitary_items, Other_textiles, Packaging_plastic_sheeting, Paraffin_or_wax_pieces, Plastic_sheeting, Plastic_tubes, Plastic_polystyrene_pieces, Toys_and_party_poppers).
  - Units and formats:
    - Latitude: decimal degrees with three decimals, N/S.
    - Longitude: decimal degrees with three decimals, E/W.
    - Sample_Depth: meters.
    - All litter category columns: kilograms (kg).

- Temporal and spatial coverage
  - Spatial focus: Portoviejo River, Ecuador (specific coordinates provided for collection reference).
  - Temporal focus: 2021–2022, with weekly category breakdowns.

- Use cases and relevance for data leadership
  - Provides a structured, standards-aligned dataset for tracking plastic pollution transport along a riverine system.
  - Demonstrates application of standardized categorization (OSPAR) and rigorous QA processes.
  - Supports evaluation of interventions (Azure System) and informs broader data-driven decisions to reduce plastic leakage.
  - Data governance notes: clear responsibility chain (field collection, data assembly, analysis), explicit metadata, and documentation to support discoverability and reuse.

- Limitations and considerations for data users
  - Gaps due to days with high river flow leading to missed collections; exact missing dates not always captured.
  - Contextual details about site locations along the river are limited beyond the recorded coordinates.