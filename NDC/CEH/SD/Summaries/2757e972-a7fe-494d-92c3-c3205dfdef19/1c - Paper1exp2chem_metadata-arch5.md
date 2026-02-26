# Soil Sample Core and Property Descriptions

## What this dataset covers
- Metadata for soil samples/cores collected during an incubation study, including identifiers, treatment information, and measured soil properties.

## Key fields and meaning
- soilcorenumber: Unique identifier for the soil core/sample.
- soilcorename: Name of the individual soil sample.
- treatmentfullname: Full name of the soil treatment (e.g., biochar and wetted).
- pH.water: pH of the soil measured in water at a 1:2.5 ratio.
- total.C.percent: Total carbon content of the soil (percent).
- total.N.percent: Total nitrogen content of the soil (percent).
- CN ratio: Ratio of total carbon to total nitrogen in the soil.
- extract.nh4-n.mgkg: Extractable ammonium (NH4-N) in mg/kg.
- extract.no3-n.mgkg: Extractable nitrate (NO3-N) in mg/kg after the start of incubation.
- bulkdensitygcm3: Bulk density of the soil (g/cm3).
- wfpsproportion: Water-filled pore space; calculated as gravimetric water content × (bulk density / total porosity).
- whcproportion: Proportion of the maximum water holding capacity at the time of gas sampling.
- Fields with blank descriptions: Placeholder fields present without descriptions.

## Computations and units
- CN ratio is a computed value from total C and total N.
- wfpsproportion is a derived metric using gravimetric water content, bulk density, and porosity.
- whcproportion reflects soil water status relative to maximum holding capacity at sampling time.
- Units used: mg/kg (extractables), percent (C and N), g/cm3 (bulk density), dimensionless ratios for CN, wfpsproportion, and whcproportion.

## Data quality, provenance, and governance considerations
- Metadata completeness: some fields have missing descriptions; fill in placeholders to improve discoverability.
- Consistency: ensure uniform units and naming across datasets and systems.
- Provenance: indicate whether measurements are pre- or post-incubation, and document how derived fields (CN ratio, wfpsproportion, whcproportion) are calculated.
- Data formats: align with standard soil data schemas to support interoperability.
- Access and sharing: prepare to upload to appropriate portals/catalogues; document any embargoes or data-sharing restrictions.

## Recommended actions for Data Stewards
- Advance metadata quality: complete descriptions for all fields; standardize field naming and units.
- Validate data: implement checks for unit consistency, value ranges, and correct calculation of derived metrics (CN ratio, wfpsproportion, whcproportion).
- Documentation: provide detailed methods for measurements and calculations, including any incubation conditions affecting nitrate, ammonium, and other properties.
- Interoperability: map fields to standard vocabularies and ensure compatibility with data portals and catalogs.
- Data governance: establish versioning, update routines, and clear ownership for each field; communicate data availability and any constraints to data users.