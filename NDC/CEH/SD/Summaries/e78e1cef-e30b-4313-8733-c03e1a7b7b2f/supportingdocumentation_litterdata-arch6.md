# Supporting documentation to dataset: Anthropogenic litter data collected from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Contains weekly weight (in kilograms) by litter category for the Portoviejo River, collected Feb 2021 – Dec 2022.
- Part of the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, aiming to reduce plastic leakage and support sustainable, circular plastics resource flows.
- Data collected to monitor riverine transport of anthropogenic litter toward the ocean using an intervention barrier technology (Azure System).

## Experimental design and sampling
- Location: Portoviejo River, Ecuador (coordinates provided in the dataset).
- Timeframe: February 2021 to December 2022.
- Sampling cadence: daily on weekdays (excluding bank holidays).
- Gaps: interruptions during days of high river flow/height (over 4.5 m), typically in March and April; exact days of non-collection are not recorded.
- Coverage: generally even outside the noted interruption months.

## Collection methods
- Barrier technology: Azure System (Ichthion Limited) traps floating litter and directs it to a shore-based sorting area.
- Sorting: anthropogenic litter separated from organic material and categorized according to OSPAR Guidelines for Monitoring Marine Litter (Beavh guideline, 2010).
- Weighing: items weighed using a hand scale and recorded in a field spreadsheet; data later transferred to digital spreadsheets as weekly weights per category.

## Quality control
- Data collection supervised by lead engineer (Desiree G. Hidalgo, Ichthion).
- Field officers collected data; data assembly and revision performed by the lead engineer.
- Data interpretation and analysis conducted by Dr. Lara Pinheiro (University of Exeter).

## Data structure and format
- File: LitterData_PortoviejoRiver.csv (Excel format).
- Contents: 39 columns including
  - Metadata: Site, Year, Month, Week, Latitude, Longitude, Sample_Depth
  - Litter categories (e.g., Aerosol_and_spray_cans, Animal_waste, Bags_shopping_empty, Bags_shopping_filled, Bottles_glass, Caps_and_lids, Cardboard, etc., up to Toys_and_party_poppers)
- Units
  - Latitude: decimal degrees with 3 decimals, N/S
  - Longitude: decimal degrees with 3 decimals, E/W
  - Sample_Depth: meters (m)
  - All litter category columns (H to AN): kilograms (kg)
- Data organization: weekly totals per category, across multiple sites/records, with geographic coordinates and depth included.

## Data quality considerations and limitations
- High-quality data ensured through expert supervision and standardized categorization (OSPAR guidelines).
- Data gaps due to river conditions: exact days when collection did not occur are not recorded; only known that high-flow days caused interruptions.
- While generally consistent, the dataset reflects operational constraints of daily weekday collection and barrier-based retrieval.

## Context and potential uses
- Enables monitoring of riverine transport of anthropogenic litter from Portoviejo River toward the Eastern Pacific.
- Supports assessment of plastic pollution inputs for policy, mitigation evaluation, and stakeholder communication.
- Provides a structured basis for analyses, dashboards, or reports to explore trends across litter categories and time.