# Topsoil invertebrate model estimates [Countryside Survey]

- A dataset from the Countryside Survey (CS) describing topsoil invertebrates (0–8 cm depth) across Great Britain, including total catch, mite:springtail ratio, number of broad taxa, and Shannon diversity index.
- Based on 947 soil cores from 256 1 km × 1 km squares analyzed in 2007; ancestry and methods detailed in Emmett et al. 2008, 2010; sampling comparable to 1978 and 1998 CS data for modeling.

## What the data represent and how it was modeled

- Estimates of mean invertebrate values within selected habitats and parent material characteristics across GB.
- Modeling approach:
  - Means estimated using CS data from 1978, 1998, and 2007.
  - Habitat/parent material characteristics derived from Land Cover Map 2007 (LCM2007) and the British Geological Survey Soil Parent Material Model (2009).
  - For each model, the dominant habitat/parent material characteristic was chosen to minimize AIC.
- Data coverage caveats:
  - Areas such as urban and littoral rock are not sampled by CS (no associated data).
  - Some habitat/parent material combinations have insufficient sample sizes to estimate means.

## Data attributes and structure

- Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700).
- Core variables (examples):
  - CATCH_98, CATCH_07: mean total invertebrate catch (1998 and 2007) by habitat/DOM_GRAIN.
  - TAXA_98, TAXA_07: mean number of broad invertebrate taxa (1998 and 2007).
  - RATIO_98, RATIO_07: mean mite:springtail ratio (1998 and 2007).
  - SHAN_98, SHAN_07: mean Shannon diversity index (1998 and 2007).
  - LCM_CLASS, DOM_GRAIN, SOIL_GROUP, CACO3_RANK: metadata reflecting land cover, dominant grain size, soil texture, and carbonate content from the parent material model.
- Data are modeled by combining LCM2007 class and parent material characteristics (DOM_GRAIN, SOIL_GROUP, etc.) for each habitat-material combination.

## Sampling, collection, and analysis methods

- Sampling regime:
  - 256 CS squares revisited from the original 1978 network.
  - Soil cores: 4 cm diameter, 8 cm length; collected after removing surface vegetation and leaving litter layer intact.
  - Cores extracted for invertebrates using a dry Tullgren method.
- Laboratory processing:
  - Invertebrates identified and counted to major taxa (taxonomic level 1) and grouped into broad taxa categories.
  - Broad taxa categories include a comprehensive list (acarina, arachnida, chilopoda, coleoptera, collembola, crustaceans, diptera, etc.).
- Quality control (QC):
  - Regular reassembly and recount by a second staff member to check for operator error.
  - Any substantive counting differences trigger review and resolution; changes are documented on sample records.

## Data provenance, metadata, and governance

- Data are derived from the Countryside Survey technical reports:
  - Emmett et al. (2008) Soils Manual.
  - Scott (2008) Statistical Report.
  - Emmett et al. (2010) Soils Report from 2007.
  - Related materials: Land Cover Map 2007 (1 km raster), Soil Parent Material Model.
- Metadata integration:
  - Attributes and coding schemes linked to LCM2007 and the BGS Soil PMM.
  - Provides a clear mapping between habitat types, parent materials, and modeled invertebrate indicators.
- Governance considerations (aligned with monitoring framework aims):
  - Data provenance and methodological transparency are documented.
  - Data are structured to support comparisons over time (1998 and 2007 model estimates).
  - Data accessibility and open sharing are supported by linking to data sources and supporting documents, though urban/littoral areas are not represented.

## Relevance for policy monitoring and environmental health assessment

- Enables monitoring of soil invertebrate community indicators across GB habitats and soil types.
- Facilitates trend analysis and evaluation of management interventions at a landscape scale, with modeled estimates to account for habitat and soil variability.
- Supports reporting through multi-year comparisons (1998 vs. 2007) and integration with land cover and soil material data.
- Useful for identifying data gaps (areas not represented, some habitat-material combinations with small sample sizes) and for guiding future targeted data collection.

## Limitations and considerations for use

- Not all areas included (urban and littoral rock lack data).
- Some habitat/parent material combinations have insufficient sample sizes for reliable mean estimates.
- Data reflect modeling based on available years (1998 and 2007) and may require careful interpretation when extrapolating to other years or conditions.
- Reliance on primary data sources and method-specific QC means users should reference Emmett et al. and Scott (2008, 2010) for full methodological context.

## References / Supporting documents

- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report. CEH.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (GB). NERC- Environmental Information Data Centre.
- British Geological Survey: Soil Parent Material Model.