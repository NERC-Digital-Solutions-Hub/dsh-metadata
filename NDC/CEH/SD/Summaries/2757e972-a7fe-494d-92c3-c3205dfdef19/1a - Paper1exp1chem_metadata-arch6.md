# soilcorenumber, Description = Individual number given to the soil sample/core.

## Overview
- A data dictionary describing soil core samples across different treatments, including biochar amendments and wetting status.
- Captures both chemical and physical soil properties at two time points (immediately after mixing and after 40 days).

## Key variables

- soilcorenumber: Individual number given to the soil sample/core.
- treatmentfullname: The full name of the soil treatment (biochar and wetted).
- treatmentnamenowet: The full name of the soil treatment (biochar).
- shorttreatmentname: A shortened treatment name.
- biocharamendment: Is the sample un-amended or amended with biochar?
- temperature: The soil temperature of the sample.
- pH.water: The pH of the soil in water at a 1:2.5 ratio.
- total.C.percent: The total carbon content of the soil as a percentage.
- total.N.percent: The total nitrogen content of the soil as a percentage.
- CN ratio: The ratio of total carbon to nitrogen content in the soil.
- extract.nh4-n.mgkg: The extractable ammonium in the soil.
- extract.no3-n.mgkg: The extractable nitrate in the soil after the start of the incubation.
- bulkdens.after.mix.gcm3: The bulk density of the soil in g/cm^3 immediately following mixing of the soil.
- bulkdens.fortydays.after.mix.gcm3: The bulk density of the soil in g/cm^3 forty days following mixing of the soil.
- WFPS.field.moist.proportion: The water filled pore space of the soil field moist (gravimetric water content × (bulk density / total porosity)).
- WFPS.after.wetting.proportion: The water filled pore space of the soil immediately following wetting (gravimetric water content × (bulk density / total porosity)).

## How the data can be used
- Compare treatment types (e.g., biochar alone vs. biochar with wetting) across chemical and physical properties.
- Analyze treatment effects over time by contrasting measurements at mixing vs. 40 days after mixing.
- Compute derived metrics (e.g., CN ratio) and explore relationships between carbon, nitrogen, and nutrient availability (NH4+, NO3-).
- Create dashboards or pivot tables to enable self-service exploration of treatment effects on soil properties.

## Data quality and integration notes
- Look for consistent treatment naming across records (treatmentfullname, treatmentnamenowet, shorttreatmentname).
- Check for missing values in key fields (e.g., NH4, NO3, CN ratio) and handle accordingly.
- When combining with other datasets, ensure consistent units (e.g., bulk density in g/cm^3, percentages for C and N, mg/kg for extractables).
- Be mindful of unitless temperature values if units are not specified; clarify units when merging with other sources.