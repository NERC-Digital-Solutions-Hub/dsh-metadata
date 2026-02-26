# Soil Core Sample Data Dictionary

## Overview
- Dataset describes individual soil core samples with identifiers, sample names, and associated treatment.
- Contains both chemical and physical soil properties suitable for map-based visualization and spatial analysis.
- Some fields have complete definitions and units; others are placeholders without descriptions.

## Key fields and descriptions
- soilcorenumber: Individual number given to the soil sample/core.
- soilcorename: Name of the individual soil sample.
- treatmentfullname: The full name of the soil treatment (biochar and wetted).
- pH.water: The pH of the soil in water at a 1:2.5 ratio.
- total.C.percent: The total carbon content of the soil as a percentage.
- total.N.percent: The total nitrogen content of the soil as a percentage.
- CN ratio: The ratio of total carbon to nitrogen content in the soil.
- extract.nh4-n.mgkg: The extractable ammonium in the soil (mg/kg).
- extract.no3-n.mgkg: The extractable nitrate in the soil after the start of the incubation (mg/kg).
- bulkdensitygcm3: The bulk density of the soil in grams per cubic centimeter.
- wfpsproportion: The water-filled pore space of the soil (gravimetric water content × (bulk density / total porosity)).
- whcproportion: The proportion of the maximum water holding capacity of the soil at the time of gas sampling.
- , Description = . and subsequent placeholder fields: Indicate missing or unspecified field descriptions.

## GIS applications
- Map spatial distributions of soil chemistry (pH, carbon, nitrogen, CN ratio) and physical properties (bulk density, moisture metrics).
- Link properties to treatment types and specific cores for comparative analyses.
- Integrate with other GIS layers (soil types, land use, sampling locations) to support spatial decision-making.

## Data quality and preparation considerations
- Data may be dispersed across multiple sources; ensure proper linkage by soilcorenumber/soilcorename.
- Some fields lack descriptions; consider filling missing metadata to improve interoperability.
- Verify units and consistency (percent for C and N, mg/kg for extracts, g/cm3 for bulk density).
- Confirm calculation method for CN ratio and wfpsproportion if combining datasets.