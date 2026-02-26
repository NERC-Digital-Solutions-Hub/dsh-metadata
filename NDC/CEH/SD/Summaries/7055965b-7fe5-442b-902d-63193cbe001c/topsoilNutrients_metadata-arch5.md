# Topsoil nutrient model estimates [Countryside Survey]

## Overview
- Describes topsoil nutrient data for Great Britain at 0–15 cm depth, focusing on total nitrogen (N) concentration (%), C:N ratio, and Olsen-Phosphorus (mg/kg).
- Based on 2007 field data; N data come from 1024 cores (and 1110 plots in 1998 for comparison), Olsen-P from 1068 plots in 2007 (65% also in 1998).
- Mean values within habitat and parent material characteristics are modelled using a mixed-model approach, informed by Land Cover Map 2007 and a Soil Parent Material Model (2009).

## Datasets and Variables
- Model-estimated means for habitat/parent material combinations; parent material characteristic used is the Dominant grain (DOM_GRAIN).
- Key data attributes include:
  - LCM_CLASS and LCM_NUMBER (derived from Land Cover Map 2007)
  - DOM_GRAIN (dominant grain size)
  - SOIL_GROUP (soil texture descriptor)
  - CACO3_RANK (carbonate content)
  - NCONC_98, NCONC_07 (mean total N concentration for 1998 and 2007)
  - TOTN_07SE (standard error for TOTN_07)
  - CN_98, CN_07 (C:N ratio for 1998 and 2007)
  - CN_07SE (SE for CN_07)
  - OLSEN_98, OLSEN_07 (Olsen-P for 1998 and 2007)
  - OLSEN_07SE (SE for Olsen-P in 2007)
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Methods and Modelling
- Experimental design: 256 original 1 km × 1 km squares; data from Main Plots within these squares.
- Collection methods: soil cores (15 cm long, 5 cm diameter) following Emmett et al. protocols.
- Analytical methods:
  - Total N concentration measured with a CEH Lancaster UKAS-accredited method SOP3102.
  - Olsen-P determined from air-dried, <2 mm soil using 0.5 M NaHCO3 extraction; colorimetric analysis (molybdenum blue), with dialysis step to mitigate reagent effects.
- Calibration and quality control details referenced in Emmett et al. (2008, 2010) and standard Defra/NERC Joint Codes of Practice.

## Spatial Coverage and Sampling Design
- Coverage: Great Britain; areas such as urban and littoral rock are not sampled and thus have no data.
- Sampling intensity: 1024 plots for total N in 2007; 1110 plots for N in 1998; Olsen-P measured on 1068 plots in 2007.
- 75% of 2007 plots were also sampled in 1998 for nitrogen data.
- Data are model-derived means by habitat/parent material, not raw measurements for all grid cells.

## Data Quality, Provenance, and Governance
- Quality control adhering to Defra/NERC Joint Codes of Practice; detailed QC procedures described in referenced reports.
- Provenance relies on multiple key sources:
  - Emmett et al. 2008, 2010 (Soils Manual and statistical reports)
  - Scott 2008 (Statistical report)
  - Morton et al. 2011 (Land Cover Map 2007)
  - Countryside Survey technical reports and related data centre records
- Supporting documentation and data lineage referenced via DOIs and project reports.

## Limitations and Considerations for Use
- Some habitat/parent material combinations have insufficient sample sizes, limiting reliable mean estimates (as indicated in the model approach).
- Areas not sampled by Countryside Survey (e.g., urban, littoral rock) have no associated data; users should avoid extrapolating beyond modelled domains.
- The dataset provides model-estimated means rather than raw measurements for all combinations; caution advised when interpreting small-area estimates or SE values.

## Access, Sharing, and Maintenance
- Data and supporting documents are linked to Countryside Survey outputs and Centre for Ecology & Hydrology/NERC data resources.
- References to technical reports and data-centre records provide guidance for data access, re-use, and potential updates or expansions.

## References and Supporting Documents
- Emmett, B.A. et al. (2008, 2010): Countryside Survey technical reports on soils and statistics
- Scott, W.A. (2008): CS Technical Report No. 4/07
- Morton, R.D. et al. (2011): Land Cover Map 2007 documentation
- Additional CS materials and related publications cited for methodology and model framework