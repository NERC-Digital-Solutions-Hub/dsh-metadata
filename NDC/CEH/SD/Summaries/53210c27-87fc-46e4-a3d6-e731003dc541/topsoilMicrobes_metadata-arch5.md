# Topsoil microbe model estimates [Countryside Survey]

## Overview
- Represents topsoil microbes in the 0–15 cm layer, including bacterial community structure (via ordination axis 1 scores) and diversity indices (Shannon and Simpson).
- Based on >1000 samples from 233 1 km × 1 km squares across Great Britain collected in 2007.
- Bacterial map shows alignment with other soil parameters (pH, carbon) and biotic features (plant diversity).
- Model-based estimates of mean values for habitat and parent material combinations, derived from Land Cover Map 2007 and Parent Material Model 2009; some areas (e.g., urban, littoral rock) lack sampling data; some habitat/parent material combos have insufficient samples.

## Data scope and sampling design
- Microbial measurements taken across over 1000 plots within 233 1 km × 1 km squares (2007 Countryside Survey).
- Collection method: soil cores (15 cm long, 4 cm diameter) following Emmett et al. 2008.
- Analytical approach: bacterial communities profiled by tRFLP; community similarities assessed with two-dimensional NMDS ordination; diversity indices computed from relative peak abundances.
- Experimental design and related statistical approaches described in Emmett 2008, Griffiths et al. 2011, and Scott 2008.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Data attributes and metadata
- Attributes include:
  - LCM_CLASS and LCM_NUMBER: derived from Land Cover Map 2007; dominant habitat class.
  - DOM_GRAIN: qualitative dominant grain size from BGS Soil PMM.
  - SOIL_GROUP: soil texture description (Heavy/Medium/Light) from PMM.
  - CACO3_RANK: carbonate content ranking (none/low/medium/high).
  - NMDS107 and NMDS107_SE: mean NMDS axis 1 scores and standard error.
  - MSHAN07 and MSHAN07_SE: mean Shannon diversity index and SE.
  - MSIMP07 and MSIMP07_SE: mean Simpson diversity index and SE.
- Data are modeled means for habitat/parent material combinations; further methodological references provided for data derivation (LCM2007, soil PMM).
- Citation: Henrys, P.A.; et al. (2014). Model estimates of topsoil microbes [Countryside Survey]. NERC Environmental Information Data Centre. DOI: 10.5285/53210c27-87fc-46e4-a3d6-e731003dc541.
- Spatial reference and data access: OSGB 1936 / British National Grid; data accessible via NERC EIDC with the provided DOI.

## Methods and quality control
- Collection and analytical methods:
  - Soil microbial measurements via 15 cm cores.
  - Molecular profiling of bacterial communities using tRFLP.
  - NMDS ordination to assess community structure; diversity indices calculated from relative tRFLP peak abundances.
- Quality control and methodological details are documented in Griffiths et al. 2011; additional sampling and statistical methods described in Emmett 2008 and Scott 2008.
- Data limitations noted: some habitat/parent material combinations lack sufficient samples to estimate means.

## Access, provenance, and governance
- Data provenance draws on 2007 Countryside Survey data, combined with Land Cover Map 2007 (LCM2007) and Soil Parent Material Model (PMM 2009); several technical reports underpin methods.
- Primary data citation for reuse: Henrys et al. 2014; hosted in the NERC Environmental Information Data Centre with a DOI for citation and access.
- Areas without data (e.g., urban, littoral rock) are acknowledged as not sampled; model estimates cover only data-supported habitat/parent material combinations.
- Potential for updates exists if new survey data become available; documentation links to original reports facilitate understanding of methods and limitations.

## Implications for data stewardship
- Reuse readiness: well-documented with clear metadata tying variables to LCM2007 and PMM, and explicit spatial reference, enabling interoperability with other GB soil datasets.
- Provenance tracing: strong lineage from field collection to tRFLP analysis, NMDS processing, and model-based estimates; multiple sources cited for transparency.
- Gaps and future work: ongoing stewardship should track data gaps (unsampled areas; underrepresented habitat-material combos) and plan for updates with new survey rounds.
- Documentation needs: maintain and update methodological references (Emmett 2008; Griffiths 2011; Scott 2008) alongside dataset metadata to support reproducibility and appropriate use.