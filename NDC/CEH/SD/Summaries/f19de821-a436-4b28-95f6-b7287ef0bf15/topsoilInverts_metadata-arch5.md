# Topsoil invertebrate model estimates [Countryside Survey]

## Overview
- Dataset represents soil invertebrates from 0 - 8 cm depth.
- 947 cores from 256 1km x 1km squares across Great Britain.
- Sampling conducted in 2007; includes mean estimates for habitat/parent material combinations derived from 1978, 1998, and 2007 data via a mixed model.
- Model inputs linked to Land Cover Map 2007 and a Soil Parent Material Model (2009); some areas (urban, littoral rock) are not sampled and some habitat/parent material combos have insufficient data.

## Data provenance and modeling
- Primary data: Countryside Survey (CS) soil invertebrates; objectives include estimating means by habitat and parent material characteristics.
- Data sources for modeling:
  - Land Cover Map 2007 (LCM2007) for dominant habitat level.
  - British Geological Survey Soil PMM (Parent Material Model) for dominant material characteristics.
- Model selection details:
  - Parent material characteristic used to minimise AIC in each model.
  - Dominant habitat/parent material characteristics drive model estimates (e.g., DOM_GRAIN, SOIL_GROUP).
- 1998, 2007 model estimates produced for several variables (e.g., Total Catch, Number of broad taxa, Mite:springtail ratio, Shannon index).

## Spatial and data attributes
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Core attributes (derived/observed):
  - LCM_CLASS; Description from Land Cover Map 2007.
  - DOM_GRAIN; Dominant grain size from PMM.
  - SOIL_GROUP; Soil texture category (Heavy/Medium/Light).
  - CACO3_RANK; Carbonate content ranking in PMM.
  - CATCH_98, CATCH_07; Mean total invertebrate catch (1998, 2007) by model.
  - CATCH_98SE, CATCH_07SE; Standard errors for CATCH_98 and CATCH_07.
  - TAXA_98, TAXA_07; Mean number of broad invertebrate taxa (1998, 2007) by model.
  - TAXA_98SE, TAXA_07SE; Standard errors for TAXA_98 and TAXA_07.
  - RATIO_98, RATIO_07; Mean mite:springtail ratio (1998, 2007) by model.
  - RATIO_98SE, RATIO_07SE; Standard errors for RATIO_98 and RATIO_07.
  - SHAN_98, SHAN_07; Mean Shannon diversity index (1998, 2007) by model.
  - SHAN_98SE, SHAN_07SE; Standard errors for SHAN_98 and SHAN_07.

## Methods

### Experimental design and sampling
- Sampling at all selected Main Plots within the 256 CS squares revisited from 1978.
- Core sampling: 4 cm diameter x 8 cm long white plastic cores.
- Vegetation surface removed; litter layer left intact; cores inserted into ground and later processed.

### Collection and analytical methods
- Invertebrates extracted from cores using a dry Tullgren method.
- Identification to major taxa (taxonomic level 1); broad taxa categories enumerated (e.g., Acari, Collembola, Diptera, etc.).
- For data processing, samples were reassembled and re-identified by a second staff member to assess potential operator error; substantive differences prompted resampling/resolution and were documented.

## Quality control
- Periodic cross-checking of identifications by a second operator.
- If discrepancies were found, adjustments were resolved by the counting team and recorded on per-sample sheets.

## Limitations and caveats
- Not all habitat/parent material combinations have sufficient sample sizes; some estimates rely on modelled data rather than direct observation.
- Urban and littoral rock areas are not sampled, so no associated data for those areas.
- Some models used to derive 1998/2007 estimates depend on model selection (e.g., AIC minimization) and may not reflect all local variations.
- Data context and methods are documented in supporting CS reports.

## Data provenance and references
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (1km raster dominant Target Class, GB). DOI: 10.5285/337f9dea-726e-40c7-9f9b-e269911c9db6.
- British Geological Survey. Soil Parent Material Model.

## Data accessibility and governance
- Data are linked to published technical reports and the Land Cover Map 2007/Soil PMM models, with citable references.
- Spatial data described in a standardized format suitable for ingestion into portals and catalogues; alignment with metadata standards (e.g., coordinate reference, attribute definitions) supports discoverability and reuse.

## Practical implications for Data Stewards
- Ensure metadata completeness: document LCM2007 and PMM sources, model approach, and variable definitions.
- Maintain data lineage: capture how each estimate (CATCH, TAXA, SHAN, RATIO) was derived (observed vs. modelled; 1998 vs. 2007).
- Versioning and updates: distinguish observed data from model-derived estimates; track changes across CS reports.
- Data quality and QC records: preserve cross-check procedures and discrepancy resolutions for auditability.
- Accessibility: provide clear references to supporting reports and data centre records; ensure data are accessible via portals and catalogues with proper licensing information.