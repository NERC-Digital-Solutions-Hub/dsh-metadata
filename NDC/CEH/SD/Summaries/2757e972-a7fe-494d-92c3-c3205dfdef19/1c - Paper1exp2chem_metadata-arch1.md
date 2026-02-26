# soilcorenumber, Description = Individual number given to the soil sample/core.

## Overview
- Dataset of soil core samples with identifiers and treatment context.
- Includes basic physico-chemical properties and moisture metrics.
- treatmentfullname indicates the full name of the soil treatment (biochar and wetted).
- Key measurements: pH (in water), total carbon and nitrogen, carbon:nitrogen ratio, extractable inorganic N (NH4+, NO3− after incubation start), bulk density, and moisture/filling metrics (WFPS and WHC proportion).

## Variables and Descriptions
- soilcorenumber: Individual number given to the soil sample/core.
- soilcorename: Name of the individual soil sample.
- treatmentfullname: The full name of the soil treatment (biochar and wetted).
- pH.water: The pH of the soil in water at a 1:2.5 ratio.
- total.C.percent: The total carbon content of the soil as a percentage.
- total.N.percent: The total nitrogen content of the soil as a percentage.
- CN ratio: The ratio of total carbon to nitrogen content in the soil.
- extract.nh4-n.mgkg: The extractable ammonium in the soil (mg/kg).
- extract.no3-n.mgkg: The extractable nitrate in the soil after the start of the incubation (mg/kg).
- bulkdensitygcm3: The bulk density of the soil (g/cm3).
- wfpsproportion: The water-filled pore space of the soil (dimensionless proportion).
- whcproportion: The proportion of the maximum water holding capacity of the soil at the time of gas sampling (dimensionless proportion).
- , Description = . (placeholders with missing descriptions)
- , Description = . (placeholders with missing descriptions)
- , Description = . (placeholders with missing descriptions)

## Potential Analyses and Modelling
- Explore correlations between carbon content, nitrogen content, and CN ratio.
- Assess effects of the soil treatment (biochar and wetted) on pH, C/N balance, inorganic N (NH4+, NO3−), bulk density, and moisture metrics.
- Model relationships between WFPS/WHC and inorganic N after incubation start.
- Use soilcorenumber and soilcorename to ensure traceability and reproducibility across analyses.

## Data Quality and Accessibility Considerations
- Most variables include explicit descriptions and units, aiding cleaning and standardisation.
- Some fields are placeholders with missing descriptions, indicating incomplete metadata.
- Data appears tabular with clearly defined columns, facilitating programmatic access and reproducible analyses.

## How Analysts can Use This Data
- Clean, transform, and normalise variables (e.g., CN ratio, N fractions) for comparative analyses.
- Compute correlations and build predictive models to understand how treatments influence soil chemistry and moisture.
- Integrate with other datasets by leveraging identifiers (soilcorenumber, soilcorename) to maintain provenance.