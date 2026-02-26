# Data file name: FADOE_yield.csv

## Overview
- Post-flowering yield characteristics of Brassica nigra under Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Sampling conducted over two years (2018 and 2019) across field sites with location changes between fields.
- Experimental setup includes four pollution treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON).

## Experimental design and data collection
- Field layout: FADOE rings distributed within a wheat field; two rings per treatment.
- Plant material: 24 plants per ring; plants removed after flowering for maturation in an insect mesh-covered polytunnel before harvest.
- Treatments and locations: rings assigned to D, O3, D+O3, CON; 2018 field coordinates: 51.482853, -0.897749; 2019 field coordinates: 51.482374, -0.895855.
- Harvest and measurements (per plant/pod as described):
  - Developed pods (no. developed pods) and undeveloped pods (no. undeveloped pods); percent pod development.
  - Pods: ten random pods bagged, oven-dried at 70 °C, weighed; pod mass; seeds removed, counted, and weighed from bagged pods; seeds per pod.
  - Aboveground biomass: plant dry mass; seeds obtained from threshing; seeds counted and weighed (plant-level).
  - Totals: total seeds and total seed mass including seeds in pods.

## Data structure and variables
- Data stored in a CSV named FADOE_yield.csv.
- Key variables (as described in the data description):
  - Year, Ring, Treatment, Plant no.
  - No. developed pods, No. undeveloped pods, % pod development
  - No. pods bagged, Mass of pods
  - Mass of seeds in bagged pods, No. seeds (pods), No. seeds per pod
  - Plant dry mass, No. seeds (plant), Seed mass (plant)
  - No. seeds total (including seeds in pods), Seed mass total (including seeds in pods)
- Measurement details include: counts, masses, and derived metrics such as pod development percentage and seeds per pod.

## Provenance, processing, and quality
- Provenance: field-based, two-year study with explicit treatment assignments and ring identifiers; precise geolocation provided per year.
- Processing: plant material matured in controlled environment before harvesting; multiple drying/ weighing steps; derived metrics calculated from raw counts and weights.
- Documentation alignment: methodologies for pod and seed measurement clearly described to support reproducibility.
- Data quality considerations: the dataset will require quality assurance, cleaning, and possible transformation prior to sharing; include documentation of any data processing steps performed.

## Governance, sharing, and stewardship considerations
- Sharing readiness: dataset intended to be uploaded to relevant portals and catalogued with holdings; sharing limitations and embargoes should be respected; update mechanisms should be in place.
- Metadata and standards: ensure complete metadata (definitions, units, methods, date ranges, location details) to support discoverability and reuse; consider clear data dictionary and provenance notes.
- Access and updates: establish versioning and update schedules; clearly document any data limitations or proprietary constraints.
- Challenges to anticipate (from archetype perspective):
  - Incomplete understanding of user needs, timely data delivery, ensuring metadata completeness, interoperability across systems, handling large datasets, and integration with legacy databases.

## Recommendations for Data Stewards
- Create a comprehensive metadata record including variable definitions, units, data collection timelines, treatment mapping, and field locations.
- Implement a data dictionary mapping each column to its measurement method and unit; document any derived metrics and calculation formulas.
- Establish data quality checks (range checks, consistency across rings/treatments, handling missing values) and maintain a change log.
- Plan for data sharing with clear access controls, licensing, and any embargo periods; set up update/versioning workflows.
- Align with data governance practices to ensure discoverability, interoperability, and reusability for future researchers examining environmental stressors on Brassica nigra yields.