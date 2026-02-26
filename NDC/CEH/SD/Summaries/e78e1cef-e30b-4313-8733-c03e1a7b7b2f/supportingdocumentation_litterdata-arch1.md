# Supporting documentation to dataset: Anthropogenic litter data collected from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Data record weights (kilograms) for anthropogenic litter by category, per week within each month of sampling.
- Part of the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, aimed at reducing plastic leakage, supporting a circular plastics resource flow, and mitigating pollution on livelihoods and wildlife.
- Data collected to monitor riverine transport of litter from the Portoviejo River toward the ocean using a barrier-based intervention (Azure System).

## Location, time frame, and sampling regime
- Location: Portoviejo River, Ecuador. Coordinates: 1°01'23.9" S, 80°29'35.6" W.
- Sampling period: February 2021 – December 2022.
- Sampling cadence: daily on weekdays excluding bank holidays.
- Data gaps: interruptions during days of high river flow/height (>4.5 m), typically in March and April; exact days not recorded.

## Collection method and waste categorisation
- Barrier technology: Azure System by Ichthion Limited. Operates to trap floating litter and direct it via a conveyor to a shore-based sorting area.
- Sorting and weighing: On shore, litter categorized by type using OSPAR Guidelines for marine litter (Beaches in the OSPAR Maritime Area, Edition 1.0, 2010); weights recorded with a hand scale and logged in field spreadsheets, then compiled into digital spreadsheets as weekly kilogram totals per category.

## Quality control and analytical roles
- Data collection supervision: Lead field engineer ( Desiree G. Hidalgo, Ichthion).
- Data assembly and reporting: Ichthion and University of Exeter staff.
- Data interpretation and analysis: Dr. Lara Pinheiro (University of Exeter).

## Data structure and contents
- File: LitterData_PortoviejoRiver.csv (one Excel file).
- Scope: 39 columns in total.
- Core identifiers: Site, Year, Month, Week, Latitude, Longitude, Sample_Depth.
- Spatial/measurement details:
  - Latitude: decimal degrees, three decimals, with N/S sign.
  - Longitude: decimal degrees, three decimals, with E/W sign.
  - Sample_Depth: meters (m).
- Litter categories (example subset of 39 total categories): Aerosol_and_spray_cans; Animal_waste; Bags_shopping_empty; Bags_shopping_filled; Bottles_glass; Caps_and_lids; Cardboard; Cartons_tetrapak_other; Clothing; Cosmetics_bottles; Cups; Cutlery_trays_straws; Drink_cans; Drinks_bottles_containers_and_drums; Face_mask; Foam_sponge; Food_cans; Food_containers; Hard_hats; Jute_sack_filled; Light_bulbs_or_tubes; Organic_waste; Other; Other_bottles_containers_and_drums; Other_metal_pieces; Other_sanitary_items; Other_textiles; Packaging_plastic_sheeting; Paraffin_or_wax_pieces; Plastic_sheeting; Plastic_tubes; Plastic_polystyrene_pieces; Toys_and_party_poppers.
- Measurement unit per variable: kilograms (kg) for the category columns (H to AN); geographic and depth columns use their specified units.
- Temporal resolution: weekly totals per category, per site.

## Data provenance and intended use
- Data produced to quantify riverine litter transport and evaluate intervention effectiveness (Azure System) in reducing plastic leakage toward the Eastern Pacific.
- Suitable for analyses of temporal trends, category distributions, and potential correlations with hydrological conditions or intervention periods.
- Metadata and data provenance tied to project organization (Ichthion, University of Exeter) and oversight by a lead engineer and project investigators.