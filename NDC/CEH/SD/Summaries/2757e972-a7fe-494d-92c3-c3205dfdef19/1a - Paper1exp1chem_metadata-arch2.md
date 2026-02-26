# Soil Core Sample Data Schema and Measurements

## Overview
- Defines fields for soil core samples, including treatment metadata, physical-chemical properties, nutrient metrics, and moisture characteristics.
- Designed for environmental monitoring with standardized inputs to enable tracking soil health and treatment effects over time.
- Supports data quality assurance, transformation, storage, and sharing across monitoring portals.

## Data fields and descriptions

- soilcorenumber: Individual number assigned to the soil sample/core.
- treatmentfullname: Full name of the soil treatment (biochar and wetted).
- treatmentnamenowet: Full name of the soil treatment (biochar).
- shorttreatmentname: Shortened treatment name.
- biocharamendment: Indicates if the sample is un-amended or amended with biochar.
- temperature: Soil temperature of the sample.
- pH.water: Soil pH in water at a 1:2.5 ratio.
- total.C.percent: Total carbon content of the soil as a percentage.
- total.N.percent: Total nitrogen content of the soil as a percentage.
- CN ratio: Ratio of total carbon to nitrogen in the soil.
- extract.nh4-n.mgkg: Extractable ammonium (mg/kg).
- extract.no3-n.mgkg: Extractable nitrate (mg/kg) after the start of incubation.
- bulkdens.after.mix.gcm3: Bulk density after mixing (g/cm3).
- bulkdens.fortydays.after.mix.gcm3: Bulk density forty days after mixing (g/cm3).
- WFPS.field.moist.proportion: Water filled pore space under field-moist conditions (based on gravimetric water content, bulk density, and total porosity).
- WFPS.after.wetting.proportion: Water filled pore space immediately after wetting (based on gravimetric water content, bulk density, and total porosity).

## Purpose and usage notes
- The dataset is structured to facilitate cross-study comparisons and time-series monitoring of soil health indicators.
- Values should be stored in accessible data portals to enable broader data access and secondary analyses.