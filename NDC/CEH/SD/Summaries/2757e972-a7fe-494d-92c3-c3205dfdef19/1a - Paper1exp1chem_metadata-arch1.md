# Soil Core Dataset Description

## Overview
- A dataset of soil core samples with treatment information (biochar and wetted, biochar only, or un-amended) and multiple chemical and physical properties measured.
- Treatments are distinguished by full names, shortened names, and a biochar amendment flag.
- Measurements include chemical composition, nutrient availability after incubation, and soil physical properties at two time points (immediately after mixing and after 40 days).

## Key Variables (with units)
- soilcorenumber: Individual soil sample/core identifier
- treatmentfullname: Full name of the soil treatment (biochar and wetted)
- treatmentnamenowet: Full name of the soil treatment (biochar)
- shorttreatmentname: Shortened treatment name
- biocharamendment: Indicates if the sample is un-amended or amended with biochar
- temperature: Soil temperature
- pH.water: Soil pH in water at a 1:2.5 ratio
- total.C.percent: Total carbon content (%)
- total.N.percent: Total nitrogen content (%)
- CN ratio: Carbon-to-nitrogen ratio
- extract.nh4-n.mgkg: Extractable ammonium (mg/kg)
- extract.no3-n.mgkg: Extractable nitrate after incubation (mg/kg)
- bulkdens.after.mix.gcm3: Bulk density immediately following mixing (g/cm3)
- bulkdens.fortydays.after.mix.gcm3: Bulk density at 40 days after mixing (g/cm3)
- WFPS.field.moist.proportion: Water-filled pore space under field-moist conditions (proportion)
- WFPS.after.wetting.proportion: Water-filled pore space immediately after wetting (proportion)

## Data context and usage
- Enables comparison of biochar-containing treatments against controls, across incubation time, and across multiple soil properties.
- Supports analysis of relationships between soil chemistry (C, N, CN), nutrient availability (NH4+, NO3-), and soil physical state (bulk density, WFPS).

## Potential analyses for analysts
- Compare treatment effects on total C, total N, and CN ratio.
- Assess how biochar amendment influences bulk density over time (immediately vs 40 days).
- Explore relationships between CN ratio and extractable nitrogen species (NH4-N, NO3-N).
- Model how WFPS changes with treatment and incubation stage.
- Investigate associations between soil pH, temperature, and nutrient availability.

## Data quality and considerations
- Ensure consistent units across variables (percent, mg/kg, g/cm3, dimensionless proportions).
- Address missing values and confirm timing alignment for after-incubation measurements.
- Maintain clarity on treatment naming conventions when integrating with external datasets.