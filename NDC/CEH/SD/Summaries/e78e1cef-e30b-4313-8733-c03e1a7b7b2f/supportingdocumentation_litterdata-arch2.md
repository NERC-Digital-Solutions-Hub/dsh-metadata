# Supporting documentation to dataset: Anthropogenic litter data collected from the Portoviejo River, Ecuador, 2021-2022

## Purpose and context
- Part of the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, aimed at reducing plastic leakage, supporting sustainable, circular plastics resource flow, and mitigating pollution impacts on livelihoods and wildlife.
- The dataset records weekly litter weights (kg) by category to monitor riverine transport of anthropogenic litter from the Portoviejo River toward the ocean.
- The data collection employs a river clean-up technology intervention (Azure System) to trap litter and assess pollution pathways.

## Study site and sampling period
- Location: Portoviejo River, Ecuador (1° 01' 23.9" S, 80° 29' 35.6" W).
- Timeframe: February 2021 – December 2022.
- Sampling cadence: Daily on weekdays (excluding bank holidays); interruptions occurred during high river flow/heights (>4.5 m), mainly in March and April; exact non-collection days are not fully documented.
- Data coverage otherwise is described as even outside the interruption periods.

## Data collection methods
- Barrier system: Azure System by Ichthion Limited continuously traps floating litter and directs it to a shore-based sorting area via a conveyor belt.
- Sorting and categorization: Litter identified as anthropogenic versus organic; anthropogenic items categorized according to the OSPAR Guidelines for Monitoring Marine Litter on Beaches (Edition 1.0, 2010).
- Measurement: Each category weighed (kg) on a hand scale and recorded in a field spreadsheet, later digitized into the dataset.
- Quality control during collection: Supervised by lead field engineer Desiree G. Hidalgo (Ichthion); data assembly and reporting handled within Ichthion and by University of Exeter collaborators.

## Data structure and content
- File: LitterData_PortoviejoRiver.csv (Excel).
- Structure: 39 columns containing spatial, temporal, and litter-category data.
- Key variables:
  - Site, Year, Month, Week
  - Latitude, Longitude (3-decimal places; ±N/S and ±E/W)
  - Sample_Depth (meters)
  - Litter categories (e.g., Aerosol_and_spray_cans, Animal_waste, Bags_shopping_empty, Bags_shopping_filled, Bottles_glass, Caps_and_lids, Cardboard, Cartons_tetrapak_other, Clothing, Cosmetics_bottles, Cups, Cutlery_trays_straws, Drink_cans, Drinks_bottles_containers_and_drums, Face_mask, Foam_sponge, Food_cans, Food_containers, Hard_hats, Jute_sack_filled, Light_bulbs_or_tubes, Organic_waste, Other, Other_bottles_containers_and_drums, Other_metal_pieces, Other_sanitary_items, Other_textiles, Packaging_plastic_sheeting, Paraffin_or_wax_pieces, Plastic_sheeting, Plastic_tubes, Plastic_polystyrene_pieces, Toys_and_party_poppers)
- Measurement unit: kilograms (kg) for all litter category columns (columns H to AN); latitude/longitude in decimal format; sample depth in meters.

## Data quality and stewardship
- Quality assurance led by expert field personnel with oversight by the lead engineer; data interpretation and analysis contributed by an academic partner (University of Exeter).
- Data was collected, reviewed, and prepared for sharing across project members and relevant portals, ensuring reproducibility and standardization.

## Relevance for environmental monitoring and policy
- Provides standardized, time-series, category-specific measurements of anthropogenic litter along a river-to-sea transport pathway.
- Enables assessment of pollution pathways, effectiveness of intervention technologies (Azure System), and temporal trends in litter types.
- Supports cross-site comparisons and meta-analyses under standardized OSPAR-based categorization, aiding policy evaluation and targets for plastic leakage reduction.