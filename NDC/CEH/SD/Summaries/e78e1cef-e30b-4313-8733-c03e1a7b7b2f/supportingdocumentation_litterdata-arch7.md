# Supporting documentation to dataset: Anthropogenic litter data collected from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Dataset of weekly anthropogenic litter weights (in kilograms) by category collected from the Portoviejo River, Ecuador (Feb 2021–Dec 2022).
- Part of the NERC-funded project on reducing plastic waste in the Eastern Pacific; aims to monitor riverine transport of litter toward the ocean and support pollution-reduction interventions.

## Experimental design and sampling regime
- Location: Portoviejo River, Ecuador, coordinates 1°01'23.9"S, 80°29'35.6"W.
- Time frame: February 2021 to December 2022.
- Sampling cadence: Daily on weekdays (Monday–Friday) excluding bank holidays.
- Interruptions: Occurred in March–April due to high river flow/height (>4.5 m); exact non-collection days are not recorded.
- Data coverage: Generally even outside the two interruption months.

## Collection methods
- Barrier system: Azure System by Ichthion Limited; continuously traps floating litter and transports it to a shore-based sorting area.
- Sorting and categorization: Anthropogenic litter separated from organic material and categorized according to the OSPAR Guidelines (Edition 1.0, 2010).
- Measurement: Each category weighed with a hand scale; results recorded in a field spreadsheet, then entered into digital spreadsheets as weekly kilogram weights per category.

## Quality control
- Supervision: Constant oversight by the lead engineer (Desiree G. Hidalgo, Ichthion).
- Data collection: Conducted by Ichthion field officers; assembly and reporting overseen by the lead field engineer.
- Data interpretation/analysis: Led by Dr. Lara Pinheiro (University of Exeter).

## Data structure and fields
- File: LitterData_PortoviejoRiver.csv (Excel format).
- Structure: 39 columns including:
  - Spatial/temporal identifiers: Site, Year, Month, Week.
  - Location: Latitude (±, 3 decimal places), Longitude (±, 3 decimal places).
  - Sampling detail: Sample_Depth (meters).
  - Litter categories: Aerosol_and_spray_cans; Animal_waste; Bags_shopping_empty; Bags_shopping_filled; Bottles_glass; Caps_and_lids; Cardboard; Cartons_tetrapak_other; Clothing; Cosmetics_bottles; Cups; Cutlery_trays_straws; Drink_cans; Drinks_bottles_containers_and_drums; Face_mask; Foam_sponge; Food_cans; Food_containers; Hard_hats; Jute_sack_filled; Light_bulbs_or_tubes; Organic_waste; Other; Other_bottles_containers_and_drums; Other_metal_pieces; Other_sanitary_items; Other_textiles; Packaging_plastic_sheeting; Paraffin_or_wax_pieces; Plastic_sheeting; Plastic_tubes; Plastic_polystyrene_pieces; Toys_and_party_poppers.
- Units: Latitude/Longitude to 3 decimals; Sample_Depth in meters; All litter category columns (H to AN) in kilograms.
- Note: The dataset records weekly totals per category for each site/record.

## Spatial and temporal coverage
- Temporal: February 2021 through December 2022, by week.
- Spatial: Data include Site identifiers with associated latitude/longitude; sampling focused on the Portoviejo River locale as described.

## Data standards and categorization
- Categorization follows the OSPAR Guidelines for Monitoring Marine Litter on Beaches in the OSPAR Maritime Area (Edition 1.0, 2010).

## Data limitations and considerations for GIS use
- Some days missing due to high river flow; exact dates of non-collection not documented.
- Data gaps possible around interruption months (March–April 2021–2022 range unspecified).
- Multiple categories and weekly weights enable time-series and spatial analyses, but users should account for possible missing weeks.

## Provenance and contacts
- Data collection and assembly conducted by Ichthion Limited; lead engineer Desiree G. Hidalgo managed QA and reporting.
- Data interpretation and analysis supported by Dr. Lara Pinheiro, University of Exeter.