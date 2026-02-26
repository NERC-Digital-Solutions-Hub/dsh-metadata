# Supporting documentation to dataset: Anthropogenic litter data collected from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Dataset of weekly kilogram weights per category of anthropogenic litter collected from the Portoviejo River, Ecuador (Feb 2021 – Dec 2022).
- Created under the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, to monitor riverine transport and inform plastic pollution mitigation.

## Aims and governance context
- Supports monitoring of plastic leakage and evaluation of intervention via river clean-up technology (Azure System).
- Data categorization follows OSPAR Guidelines for Marine Litter Monitoring (Beaches in the OSPAR Maritime Area, Edition 1.0, 2010).
- Emphasizes data sharing readiness, standardization, and clear provenance for reuse by others.

## Experimental design and sampling regime
- Location: Portoviejo River, Ecuador (approximate site: 1°01'23.9"S, 80°29'35.6"W).
- Timeframe: February 2021 – December 2022.
- Approach: daily collection on weekdays (excluding bank holidays); data gaps during days of high river flow/height (>4.5 m) with missing exact non-collection dates.
- Data coverage is generally even outside interruption periods.

## Collection methods
- Barrier technology: Azure System by Ichthion Limited, directing floating litter to a shore sorting area via a conveyor.
- Onshore sorting: anthropogenic vs. organic material; categorization according to OSPAR guidelines.
- Measurement: weight of each category recorded with a hand scale and logged in field spreadsheets, then consolidated into digital spreadsheets as weekly category weights (kg).

## Quality control and governance
- Data collection supervised by lead field engineer Desiree G. Hidalgo (Ichthion).
- Data assembly and reporting overseen by Desiree G. Hidalgo; data interpretation and analysis by Dr. Lara Pinheiro (University of Exeter).

## Data structure and metadata
- Single Excel file: LitterData_PortoviejoRiver.csv.
- 39 columns including: Site, Year, Month, Week, Latitude, Longitude, Sample_Depth, and category columns such as Aerosol_and_spray_cans, Animal_waste, Bags_shopping_empty, Bags_shopping_filled, Bottles_glass, Caps_and_lids, Cardboard, Cartons_tetrapak_other, Clothing, Cosmetics_bottles, Cups, Cutlery_trays_straws, Drink_cans, Drinks_bottles_containers_and_drums, Face_mask, Foam_sponge, Food_cans, Food_containers, Hard_hats, Jute_sack_filled, Light_bulbs_or_tubes, Organic_waste, Other, Other_bottles_containers_and_drums, Other_metal_pieces, Other_sanitary_items, Other_textiles, Packaging_plastic_sheeting, Paraffin_or_wax_pieces, Plastic_sheeting, Plastic_tubes, Plastic_polystyrene_pieces, Toys_and_party_poppers.
- Units/formats:
  - Latitude: decimal degrees with 3 decimal places (N/S)
  - Longitude: decimal degrees with 3 decimal places (E/W)
  - Sample_Depth: meters (m)
  - Category columns (H to AN): kilograms (kg)

## Data quality, limitations, and notes for stewardship
- Acknowledges incomplete days due to high river flow; exact non-collection dates are not recorded.
- Data are structured for weekly aggregation by category, enabling trend analyses and reporting.
- As a steward, consider documenting data lineage, update cycles, and any future data appendices to maintain currency and discoverability.

## Accessibility and potential reuse considerations
- Clear documentation of methods, standards (OSP​AR), and data structure supports reuse by researchers and policymakers.
- Data provenance is maintained via project context, responsible personnel, and the systematic workflow from field collection to digital recording.