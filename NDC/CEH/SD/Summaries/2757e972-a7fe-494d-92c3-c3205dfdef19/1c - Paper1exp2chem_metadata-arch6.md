# Soil Sample Core and Chemical Properties Data Dictionary

## Overview
- A data dictionary describing measurements for soil samples/cores, including identifiers, treatment details, chemical properties, and physical properties relevant to soil analysis.
- Intended to support analysis of soil health and treatment effects (e.g., biochar and wetted treatments) and enable data-driven exploration by end users.

## Key fields and units

- soilcorenumber: Individual number assigned to the soil sample/core. (no unit)
- soilcorename: Name of the individual soil sample. (no unit)
- treatmentfullname: Full name of the soil treatment (e.g., biochar and wetted). (no unit)
- pH.water: pH of the soil in water at a 1:2.5 ratio. (pH units)
- total.C.percent: Total carbon content of the soil as a percentage. (%)
- total.N.percent: Total nitrogen content of the soil as a percentage. (%)
- CN ratio: Ratio of total carbon to nitrogen content in the soil. (dimensionless)
- extract.nh4-n.mgkg: Extractable ammonium in the soil, in mg/kg. (mg/kg)
- extract.no3-n.mgkg: Extractable nitrate in the soil after the start of the incubation, in mg/kg. (mg/kg)
- bulkdensitygcm3: Bulk density of the soil in grams per cubic centimeter. (g/cm3)
- wfpsproportion: Water-filled pore space of the soil (gravimetric water content × (bulk density / total porosity)). (dimensionless)
- whcproportion: Proportion of the maximum water holding capacity of the soil at the time of gas sampling. (dimensionless)
- ., Description = . (unspecified field placeholder)
- ., Description = . (unspecified field placeholder)

## Derived metrics and considerations

- CN ratio is provided as a derived metric from total C and total N.
- wfpsproportion is a calculated value using gravimetric water content, bulk density, and total porosity.
- whcproportion reflects soil moisture relative to maximum water holding capacity at sampling time.

## Data quality and cleaning considerations

- Some fields appear as placeholders with no descriptions or values, indicating missing or undefined data.
- Data may come from multiple systems or formats, requiring standardization of field names, units, and measurement methods.
- Potential inconsistencies in treatment naming (e.g., variations of “biochar and wetted”) should be harmonized.
- Missing values (e.g., in placeholder fields) may require imputation or exclusion depending on analysis.

## Potential analyses and outputs

- Compare soil chemical properties (pH, total C/N, extractable N forms) across treatments and cores.
- Assess relationships between carbon and nitrogen contents (CN ratio) and moisture metrics (wfpsproportion, whcproportion).
- Explore how treatments influence soil fertility indicators (extract.nh4-n and extract.no3-n) over incubation.
- Create dashboards or self-serve reports enabling end users to filter by soilcorenumber, soilcorename, and treatmentfullname.
- Produce summary tables and charts (e.g., bar charts of C%, N%, CN ratio by treatment; scatter plots of pH vs. NH4-N).

## Usage notes and guidance

- Ensure units are consistent when aggregating (e.g., percentages for C and N, mg/kg for extractable N forms).
- Validate that CN ratio values align with total C and total N percentages.
- When sharing outputs, provide metadata on measurement methods and treatment definitions to support interpretation.