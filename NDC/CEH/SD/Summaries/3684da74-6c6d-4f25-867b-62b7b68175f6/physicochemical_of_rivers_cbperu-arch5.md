# Environmental_CBPeru.csv

## Overview
- Dataset of measured physicochemical variables for 10 rivers in the glacial valleys of Parón, Huaytapallana, and Llanganuco, Cordillera Blanca, Ancash, Peru.
- Tied to the study on glacier retreat driving changes in aquatic macroinvertebrate biodiversity.
- Contains 37 environmental variables collected across two seasons (wet and dry) during two field campaigns (2019 and 2020).

## Dataset contents and structure
- File and scope:
  - Environmental_CBPeru.csv (environmental variable data presented in a single Excel sheet).
  - Sites are listed in the first column; environmental variables in the first row; season indicated by d (dry) or w (wet).
- Sites and geography:
  - 10 sites labeled P01–P10 across Parón, Huaytapallana, and Llanganuco valleys.
  - Table 2 provides geographic details per site: coordinates (UTM 18S), basin area, glacier area, glacier-covered percentage (GCC), distance to glacier, slope, altitude.
- Variables:
  - 37 variables spanning physical, chemical, and topographic data.
  - Physical/field measurements: turbidity (NTU), water temperature (°C), electrical conductivity (µS/cm), pH, dissolved oxygen (mg/L), Pfankuch Index (channel stability).
  - Nutrients and carbon: total nitrogen (TN, mg/L), total phosphorus (TP, mg/L), dissolved organic carbon (DOC, mg/L), dissolved inorganic carbon (DIC, mg/L), dissolved carbon (DC, mg/L).
  - Inorganic/organic elements and ions: fluorine (F, mg/L), chloride (Cl, mg/L), sulfate (SO4, mg/L), nitrate (NO3, mg/L).
  - Cations and trace metals: Al, B, Ca, K, Mg, Na, Si, Zn, Sr, Be, Cd, Co, Cr, Cu, Fe, Li, Mn, Ni, Pb, Se, Te, Ti (units mg/L where applicable).
- Methods and timing:
  - Collection periods: October 14–30, 2019 and October 7–16, 2020.
  - In situ measurements: Multi 3630 IDS multiparameter instrument with measurements every 5 seconds, averaged over 5 minutes.
  - Turbidity: measured in the laboratory using filtered water (10 mL).
  - Other parameters: determined from water samples in the University of Leeds lab using specified methods (Table 1).
  - Topographic and hydrological characterization: Pfankuch Index; slope from 12.5 m DEM; distance to glacier via Sentinel-2 imagery.

## Data structure and units
- Data organization:
  - Sites in the first column; environmental variables in the first row.
  - Season column indicates wet (w) or dry (d) season.
- Units overview:
  - Turbidity: NTU
  - Temperature: °C
  - Conductivity: µS/cm
  - pH: pH units
  - DO: mg/L
  - Pfankuch Index: dimensionless
  - TN, TP, DOC, DIC, DC: mg/L
  - Anions/cations/trace elements: mg/L (as listed for each parameter)

## Quality assurance and provenance
- Field equipment calibration prior to each field work.
- Use of certified standards for metals and other analytes, including Environment and Climate Change Canada references and ERM-CA022a interlaboratory standards.
- QA/QC procedures documented to ensure accuracy and precision of measurements.

## Data governance and usage notes
- Data collected in two field campaigns (2019 and 2020) to support analysis of how glacier retreat affects river chemistry and, by extension, aquatic biodiversity.
- Site-level and geospatial metadata provided to enable reproducibility and cross-site comparisons.
- Related publication: Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru.
- Contributors and roles specified (sample collection, laboratory analysis, supporting information, planning and management).
- References:
  - Pfankuch, J. D. (1975). Stream reach inventory and channel stability evaluation.
- Access considerations:
  - Dataset is documented with detailed methods and site metadata to facilitate reuse, proper attribution, and potential integration with other environmental or biodiversity data.