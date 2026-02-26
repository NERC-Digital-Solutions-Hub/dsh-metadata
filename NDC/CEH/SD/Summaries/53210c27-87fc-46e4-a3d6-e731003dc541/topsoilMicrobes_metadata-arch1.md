# Topsoil microbe model estimates [Countryside Survey]

- The Countryside Survey (CS) dataset provides model estimates of topsoil microbes for the 0–15 cm depth, linking bacterial community structure (via ordination axis 1 scores) and diversity (Shannon and Simpson indices) to habitat and parent material characteristics across Great Britain.
- Data are based on more than 1,000 samples from 233 one-kilometre squares collected in 2007, analyzed to derive mean values for habitat/parent material combinations using mixed-model approaches.

## Data content and structure

- Contains model-estimated mean values for habitat/parent material combinations derived from Land Cover Map 2007 (LCM2007) and the BGS Soil Parent Material Model (2009).
- Variables include bacterial community structure (NMDS axis 1, NMDS107) and diversity indices (Shannon, MSHAN07; Simpson, MSIMP07), with associated standard errors (NMDS107_SE, MSHAN07_SE, MSIMP07_SE).
- Includes land cover and soil descriptors: LCM_CLASS, LCM_NUMBER, DOM_GRAIN, SOIL_GROUP, CACO3_RANK.
- Some habitat/parent material combinations have insufficient samples, and areas not sampled by CS (e.g., urban, littoral rock) have no data.

## Variables (Data attributes)

- LCM_CLASS: Dominant land cover at broad habitat level (from LCM2007).
- LCM_NUMBER: Integer code for LCM2007 class (1–23).
- DOM_GRAIN: Dominant grain size category from the Soil Parent Material Model.
- SOIL_GROUP: General soil texture category (Heavy/Medium/Light) from the Soil Model.
- CACO3_RANK: Carbonate content ranking (none/low/medium/high).
- NMDS107: Mean NMDS axis 1 score for bacterial community structure (modelled with LCM_CLASS and CACO3_RANK).
- NMDS107_SE: Standard error for NMDS107.
- MSHAN07: Mean Shannon diversity index for bacterial communities (modelled with LCM_CLASS and SOIL_GROUP).
- MSHAN07_SE: Standard error for MSHAN07.
- MSIMP07: Mean Simpson diversity index for bacterial communities (modelled with LCM_CLASS and SOIL_GROUP).
- MSIMP07_SE: Standard error for MSIMP07.

## Experimental design and collection

- Microbial measurements collected from over 1,000 plots within 233 1 km × 1 km squares as part of the 2007 Countryside Survey.
- Collection method: soil cores (15 cm long, 4 cm diameter) following standard CS field protocols.
- Analyses: bacterial communities profiled via tRFLP; NMDS used to assess community similarities; diversity indices computed from tRFLP peak abundances.

## Analytical methods and modelling

- Modelling: mean values estimated using mixed-model approaches, incorporating dominant habitat and parent material characteristics (derived from LCM2007 and the Parent Material Model 2009); parent material class chosen to minimize AIC.
- Data interpretation relies on ordination (NMDS) of bacterial communities and diversity metrics (Shannon, Simpson).
- Quality control details are documented in Griffiths et al. (2011).

## Spatial reference and data access

- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Data citation: Henrys, P.A.; Keith, A.M.; Robinson, D.A.; Emmett, B.A. (2014). Model estimates of topsoil microbes [Countryside Survey]. NERC Environmental Information Data Centre. https://doi.org/10.5285/53210c27-87fc-46e4-a3d6-e731003dc541

## Limitations and notes

- Urban areas and littoral rock are not sampled by CS and have no associated data for this dataset.
- Some habitat/parent material combinations lack sufficient sample sizes for reliable mean estimation.
- Data availability and discoverability are aided by dataset metadata and associated technical reports (see Griffiths 2011 for quality control and methodological details).

## References

- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Griffiths, R.I. et al. (2011). The bacterial biogeography of British soils. Environmental Microbiology.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report. CEH.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (1 km raster dominant Target Class, GB). NERC-EDC.