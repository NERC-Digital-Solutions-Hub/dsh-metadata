# Data collected by Vicky Bowskill (https://orcid.org/0000-0003-0293-327X) as part of PhD research with School of Environment, Earth and Ecosystem Sciences, Faculty of Science, Technology, Engineering and Mathematics, The Open University, Walton Hall, Milton Keynes, MK7 6AA

## Overview
- Nutritive data for floodplain meadow hay collected in central England as part of a PhD study.
- Dataset comprises measurements across multiple sites, years, and samples, with replicates averaged to produce a single data point per sample.

## Dataset structure and scope
- Reports data from 4 sites in central England (note: the data description also lists 3 sites in the data structure; there is a discrepancy to be mindful of).
- Structure details: 3 sites, 2 years, 6 samples per site, 2 replicates per sample (each data point is the mean of two replicates).
- Sampling design includes bulked pairwise sampling in year 2 to reduce costs.
- Data file format: 1 CSV file; columns represent variables, rows represent records.

## Measurements and lab methods
- Nutritional and content measurements:
  - CP: Crude Protein
  - ME: Metabolisable Energy
  - ADF: Acid Digestible Fibre
  - NDF: Neutral Digestible Fibre
  - GDD: Accumulated Growing Degree-days (thermal time)
  - AET: Accumulated Actual Evapotranspiration
  - GFratio: Graminoid:Forb ratio
  - P, B, Ca, Cu, K, Mg, Mn, Mo, Na, Se, S, Zn: mineral contents
  - I (iodine) derived via ICP-MS
- Analytical methods:
  - CP, ME, ADF, NDF measured by Near Infrared Spectroscopy (NIRS)
  - Mineral elements (P, B, Ca, Cu, K, Mg, Mn, Mo, Na, Se, S, Zn) by Inductively Coupled Plasma Optical Emissions Spectrometry (ICP-OES)
  - Iodine (I) by Inductively Coupled Plasma Mass Spectrometry (ICP-MS)

## Data labels, definitions, and units
- Guide to data labels:
  - GDD: Accumulated Growing Degree-days (thermal time)
  - AET: Accumulated Actual Evapotranspiration
  - GFratio: Graminoid:Forb ratio
  - CP: Crude Protein
  - ME: Metabolisable Energy
  - ADF: Acid Digestible Fibre
  - NDF: Neutral Digestible Fibre
- Units:
  - gm2: grams per metre square
  - gkg: grams per kilogram
  - mgkg: milligrams per kilogram
  - percent: percent content
  - offtake: offtake calculated as (% * yield) / 100
  - Mjkg: MegaJoules per kilogram

## Data file and provenance
- File format: 1 CSV file
- Data origin: Nutritive measurements from floodplain meadow hay across sites/years, with replicates averaged
- Funding: NERC CENTA2 grant NE/S007350/1
- Associated sources: Linked publications with full method description
  - doi:10.1016/j.biocon.2023.110140
  - doi:10.21954/ou.ro.00097871
- Accessibility: Data described as part of a PhD research project at The Open University; metadata and DOIs provided for methods and data context

## Potential analyses for data users
- Examine relationships between nutritive components (CP, ME, ADF, NDF) and environmental variables (GDD, AET)
- Compare across sites and years to assess spatial and temporal variation in hay quality
- Explore correlations between mineral contents and energy/fibre measures
- Use NIRS-derived measures alongside ICP-OES/ICP-MS data to evaluate prediction accuracy
- Develop or validate predictive models of hay nutritive value for livestock feeding under floodplain meadow conditions

## Considerations and caveats
- Inconsistencies in site count (4 sites described vs. 3 sites listed in structure) should be reconciled when using the dataset.
- Small sample design (6 samples per site, 2 replicates per sample) may limit statistical power for some analyses.
- Year 2 sampling used bulked pairwise methods to reduce costs, which may influence variance estimates.
- Data accessibility and database metadata are provided via linked DOIs; users should consult those sources for full methodological details.