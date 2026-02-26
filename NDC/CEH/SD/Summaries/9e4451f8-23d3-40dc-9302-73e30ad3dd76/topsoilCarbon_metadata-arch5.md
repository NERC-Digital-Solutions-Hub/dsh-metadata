# Topsoil carbon model estimates [Countryside Survey]

## Overview
- Dataset represents topsoil (0–15 cm) carbon metrics: loss-on-ignition (%), carbon concentration (g kg-1), and carbon density (t ha-1).
- Based on 2614 cores from 591 1 km × 1 km squares across Great Britain, analyzed in 2007.
- Mean values estimated for habitat/parent material combinations using a mixed-model approach across 1978, 1998, and 2007 data.
- Means are modeled using dominant habitat and parent material characteristics derived from the Land Cover Map 2007 (LCM2007) and the 2009 Soil Parent Material Model; some areas (e.g., urban, littoral rock) are not sampled and certain combos have insufficient samples.

## Data content and structure
- Variables included: LOI_78, LOI_98, LOI_07; CCONC_78, CCONC_98, CCONC_07; CDENS_78, CDENS_98, CDENS_07; and associated standard errors (LOISE, CCONCSE, CDENSE, etc.).
- Dominant habitat/parent material characteristics used to produce model estimates:
  - Dominant grain (DOM_GRAIN)
  - Calcium carbonate content rank (CACO3_RANK)
- Descriptive fields derived from LCM2007 and the BGS Soil Parent Material Model (SOIL_GROUP, DOM_GRAIN, etc.).
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Spatial and attribute schema
- Spatial coordinates aligned to British grid system; explicit geometry attributes not listed but implied by 1 km square sampling framework.
- Data attributes include:
  - LCM_CLASS and LCM_NUMBER (habitat classifications from LCM2007)
  - DOM_GRAIN, SOIL_GROUP, CACO3_RANK (parent material classifications)
  - LOI_78, LOI_98, LOI_07 and SE (standard errors)
  - CCONC_78, CCONC_98, CCONC_07 and SE
  - CDENS_78, CDENS_98, CDENS_07 and SE
- Units: LOI in percent; C concentration in g/kg; carbon density in t/ha; DOM_GRAIN, CAC03_RANK as coded categories.

## Methods
- Experimental design: LOI measured for 1197 plots (1978), 1098 plots (1998), and 2614 plots (2007) across 256, 256, and 591 squares respectively.
- Collection: soil samples collected with 15 cm × 5 cm cores following Emmett et al. (2008).
- Analytical methods:
  - LOI: 10 g sub-sample, dried at 105°C, combusted at 375°C, LOI% calculated.
  - Carbon concentration: measured with an elemental analyser (CEH SOP3102); UKAS-accredited method.
  - Carbon density: derived from carbon concentration and bulk density (combining LOI and C concentration with density considerations).
- Model estimates integrate habitat and parent material characteristics, selecting the dominant grain and carbonate content as model predictors.

## Quality control and provenance
- Followed Defra/NERC Joint Codes of Practice; detailed QC procedures in Emmett et al. (2008, 2010).
- Related technical reports and datasets cited for sampling, methods, and calibration details (e.g., CS Technical Reports 03/07, 04/07, 09/07; Land Cover Map 2007 documentation).

## Limitations and caveats
- Some habitat/parent material combinations lack adequate sample sizes, limiting the reliability of mean estimates for those groups.
- Areas not sampled (e.g., urban areas, littoral rock) have no associated data, affecting spatial coverage.
- Model-based estimates may have higher uncertainty in regions with sparse data or non-interoperable legacy systems.
- Data are tied to specific classifications (LCM2007, Soil PMM); ensuring alignment with current schemas is necessary for reuse.

## Governance, sharing and stewardship considerations
- Metadata should clearly document: sampling design, years of data (1978, 1998, 2007), habitat/parent material model choices, and the dependent variables with units.
- Coordinate system and spatial referencing must be preserved (OSGB 27700) to maintain compatibility with other GB datasets.
- Record data provenance, versioning, and QC status; include references to Emmett et al. and CS Technical Reports for traceability.
- Note data gaps (urban/littoral areas) and uncertainty (standard errors) to inform data users and risk assessments.
- Ensure licensing, access restrictions, and update pathways are defined if new years of data or revised models are added.

## References and supporting documents
- Emmett, B.A., et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual.
- Emmett, B.A., et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report.
- Mort, R.D., et al. (2011). Land Cover Map 2007 documentation.
- Related datasets: Countryside Survey outputs and Soil Change analyses; CEH SOPs for laboratory methods.