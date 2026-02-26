# Soil Core Sample Dataset Description

- Purpose and use
  - A field-scale dataset of soil cores collected to monitor environmental health and policy-relevant soil quality over time.
  - Structured for standardised analysis, QA/QC, and transformation into outputs (reports, maps, charts) and uploading to data portals.
  - Supports comparisons of treatments (biochar amendment and wetted vs. non-wetted) across sites, depths, and times.

- Dataset structure at a glance
  - Identifying and contextual fields: soilcorenumber (individual core ID), site (field site), depth (soil depth), replicate (repeat from same treatment), timesample (sampling time).
  - Treatments:
    - biocharamendment: whether the sample is amended with biochar or not.
    - wettedtreatment: whether the sample is periodically wetted to a high water content or not.
  - Measurements (before or during incubation):
    - pH.water: soil pH in water at a 1:2.5 ratio.
    - total.C.percent: total carbon as a percentage.
    - total.N.percent: total nitrogen as a percentage.
    - CN ratio: carbon-to-nitrogen ratio.
  - Extractable nutrients:
    - extract.nh4-n.mgkg: extractable ammonium (mg/kg).
    - extract.no3-n.mgkg: extractable nitrate after the start of incubation (mg/kg).
  - Physical properties and mass:
    - drysoilweightg: dry soil weight in grams.
    - gravwatercontproportion.before: gravimetric water content as a proportion before incubation.
    - bulkdensitygcm3.before: bulk density before incubation (g/cm3).
    - particledensitygcm3: particle density of the soil (g/cm3).
  - Calculated porosity metrics (before incubation):
    - totalporosityproportionbefore: total porosity, computed as 1 - (bulk density / particle density).
    - wfpsproportionbefore: water-filled pore space before incubation, calculated as gravimetric water content * (bulk density / total porosity).

- Key definitions and calculations
  - Total porosity before = 1 - (bulk density / particle density).
  - WFPS before = gravimetric water content × (bulk density / total porosity).

- Data quality and accessibility considerations for analysts
  - Data should be verified, quality assured, cleaned, and transformed to enable standardised outputs.
  - Datasets are stored and uploaded to appropriate portals to support broader data access.
  - Strategic challenges include increasing dataset value by integrating with other data and enabling access to underlying data used to create final outputs.