# Data collected by Vicky Bowskill (https://orcid.org/0000-0003-0293-327X) as part of PhD research with School of Environment, Earth and Ecosystem Sciences, Faculty of Science, Technology, Engineering and Mathematics, The Open University, Walton Hall, Milton Keynes, MK7 6AA

## Overview
- Nutritive data for floodplain meadow hay collected on 4 sites in central England.
- Part of PhD research at The Open University; funded by NERC CENTA2 grant NE/S007350/1.
- Linked publications provide the full method description and data context.

## Dataset and structure
- Data file: 1 CSV file.
- Structure:
  - Columns: variables
  - Rows: records
  - Sites: 3
  - Years: 2
  - Samples per site: 6 (bulked pairwise in year 2 to reduce sampling costs)
  - Replicates per sample: 2
  - Each data point is the mean of two replicates.

## Measurements and lab methods
- Near Infrared Spectroscopy (NIRS) for: Crude Protein (CP), Metabolisable Energy (ME), Acid Digestible Fibre (ADF), Neutral Digestible Fibre (NDF).
- Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES) for: P, B, Ca, Cu, K, Mg, Mn, Mo, Na, Se, S, Zn.
- Inductively Coupled Plasma Mass Spectrometry (ICP-MS) for Iodine (I).

## Data labels and units
- Key labels:
  - GDD: Accumulated Growing Degree-days (thermal time)
  - AET: Accumulated Actual Evapotranspiration
  - GFratio: Graminoid:Forb ratio
  - CP: Crude Protein
  - ME: Metabolisable Energy
  - ADF: Acid Digestible Fibre
  - NDF: Neutral Digestible Fibre
- Additional measured elements: P, B, Ca, Cu, K, Mg, Mn, Mo, Na, Se, S, Zn
- Units:
  - gm2: grams per square metre
  - gkg: grams per kilogram
  - mgkg: milligrams per kilogram
  - percent: percent content
  - offtake: calculated as (% × yield) / 100
  - Mjkg: MegaJoules per kilogram

## Provenance and references
- Funded by: NERC CENTA2 grant NE/S007350/1
- Linked publications include:
  - Full method description: https://doi.org/10.1016/j.biocon.2023.110140
  - Additional data context: https://doi.org/10.21954/ou.ro.00097871

## Practical considerations for data management (Data Leaders perspective)
- Data scope and context are clearly defined (sites, years, sampling design, replication, and averaging of replicates).
- Clear description of analytical methods and resulting data labels facilitating reuse and integration with other datasets.
- Metadata elements captured (units, label definitions, and off-take calculation) support data discoverability and correct interpretation.
- Provenance and funding details are provided, aiding stewardship, reproducibility, and collaboration.
- Availability in a single CSV file with explicit structure aids ease of access and downstream analysis.