# Supporting documentation to dataset: Anthropogenic litter data collected from the Portoviejo River, Ecuador, 2021-2022.

## Overview
- Dataset of litter weights (in kilograms) by category per week, collected Feb 2021–Dec 2022.
- Part of the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, aimed at reducing plastic leakage and supporting sustainable plastics flows and livelihoods.
- Collected to monitor riverine transport of anthropogenic litter from the Portoviejo River toward the ocean using a river clean-up barrier technology (Azure System).

## Study Area and Temporal Coverage
- Location: Portoviejo River, Ecuador (Latitude 1.023325° S, Longitude 80.493222° W).
- Sampling period: February 2021 to December 2022.
- Sampling cadence: daily on weekdays (excluding bank holidays); interruptions on days of high river flow/height (>4.5 m), mainly in March–April; exact non-collection days not consistently recorded.

## Methods

### Collection System
- Barrier technology: Azure System by Ichthion Limited, directing litter via a conveyor belt to a on-shore sorting area.

### Laboratory/Field Processing
- Sorting: Anthropogenic vs. organic material; categorisation of litter according to the OSPAR Guidelines for Monitoring Marine Litter on Beaches (Edition 1.0, 2010).
- Measurement: Weighing of each category using a hand scale; data recorded in a field spreadsheet and then transferred to digital spreadsheets as weekly kilograms per category.

### Quality Control
- Data collection supervised by lead field engineer (Desiree G. Hidalgo, Ichthion).
- Data assembly, revision, and reporting managed within Ichthion and by the University of Exeter.
- Data interpretation and analysis conducted by Dr. Lara Pinheiro (University of Exeter).

## Data Structure and Variables

### File
- LitterData_PortoviejoRiver.csv

### Structure
- 39 columns, including:
  - Location and timing: Site, Year, Month, Week, Latitude, Longitude, Sample_Depth.
  - Litter categories (each as a separate column, weights in kilograms): Aerosol_and_spray_cans; Animal_waste; Bags_shopping_empty; Bags_shopping_filled; Bottles_glass; Caps_and_lids; Cardboard; Cartons_tetrapak_other; Clothing; Cosmetics_bottles; Cups; Cutlery_trays_straws; Drink_cans; Drinks_bottles_containers_and_drums; Face_mask; Foam_sponge; Food_cans; Food_containers; Hard_hats; Jute_sack_filled; Light_bulbs_or_tubes; Organic_waste; Other; Other_bottles_containers_and_drums; Other_metal_pieces; Other_sanitary_items; Other_textiles; Packaging_plastic_sheeting; Paraffin_or_wax_pieces; Plastic_sheeting; Plastic_tubes; Plastic_polystyrene_pieces; Toys_and_party_poppers.
- Units/formats:
  - Latitude: [+N, -S], 3 decimal places.
  - Longitude: [+E, -W], 3 decimal places.
  - Sample_Depth: meters (m).
  - Category columns: kilograms (kg).

## Data Scope and Use for Monitoring Frameworks
- Provides weekly, category-specific weights to monitor plastic and litter trends along a river system.
- Facilitates assessment of intervention effectiveness (Azure System) in reducing upstream-to-ocean litter transport.
- Useful for governance, reporting, and informing future monitoring designs; aligns with standardized category definitions (OSPAR guidelines).

## Limitations and Gaps
- Unrecorded exact non-collection days due to high river flow; data gaps exist for specific days in March–April 2021–2022.
- Data collection interruptions and potential gaps in metadata may affect time-series continuity.
- Data governance considerations indicated by the need to ensure transparency, metadata completeness, and potential barriers to publicly sharing datasets.

## Governance and Data Sharing Considerations
- Dataset assembled from field-collected data by a private contractor and a university partner; highlights the importance of clear data provenance and stewardship.
- Emphasizes the need for metadata enrichment and robust data governance to support reuse and verification.
- Public sharing of underlying datasets may present barriers; the workflow includes documenting collection methods, categories, and quality control to facilitate responsible sharing and interpretation.