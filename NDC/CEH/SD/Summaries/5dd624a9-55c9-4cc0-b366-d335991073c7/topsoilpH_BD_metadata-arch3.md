# Topsoil pH and bulk density model estimates [Countryside Survey]

## Overview
- Dataset describing topsoil pH and bulk density for 0–15 cm depth in Great Britain, using Countryside Survey data.
- Based on 2614 cores from 591 1km × 1km squares collected in 2007; extensive sampling design described in Emmett et al. 2008/2010.
- Mean values across habitat/parent material combinations modelled using mixed models; dominant habitat and parent material derived from Land Cover Map 2007 and the 2009 Parent Material Model.
- Areas such as urban and littoral rock are not sampled and have no associated data.
- Some habitat/parent material combinations had insufficient sample sizes to estimate means.

## Data collection and sampling design
- Soil pH and bulk density measured in 2614 plots located within 591 main plots across 1km squares in 2007.
- Soil sampling used a standardized 15 cm long by 5 cm diameter core (field protocol described in Emmett et al. 2008).

## Modeling approach
- Means estimated with mixed-model methods for selected habitats and parent material characteristics.
- For pH: parent material characteristic = Dominant grain (CACO3_RANK); for bulk density: Dominant grain (DOM_GRAIN).
- Model inputs include habitat from Land Cover Map 2007 and parent material from the PMM 2009; 1978, 1998, and 2007 data periods used for trend/temporal context.
- Tables and metadata specify which variables are used and how they were derived (see Table 1 in the document).
- Some habitat/parent material combinations had insufficient samples to yield reliable estimates.

## Data attributes and metadata
- Key attributes include:
  - LCM_CLASS and LCM_NUMBER (Land Cover Map 2007 class and code 1–23)
  - DOM_GRAIN (dominant grain size)
  - SOIL_GROUP (texture category: Heavy/Medium/Light)
  - CACO3_RANK (carbonate content: none/low/medium/high)
  - PH_78, PH_98, PH_07 with associated SE (standard errors)
  - BULKD_98, BULKD_07 with associated SE
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700)
- Data are presented as modelled means with accompanying uncertainty where applicable.

## Experimental design and sampling regime
- Sampling conducted across 591 1km squares, with 2614 plots sampled.
- Targeted to support habitat- and parent-material–level inferences across GB.

## Collection, calibration, and analytical methods
- pH measurement: 10 g field-moist soil mixed with 25 ml deionised water (1:2.5 ratio by weight).
- Bulk density: derived from detailed weight measurements during soil processing.
- Calibration and analytical procedures are detailed in Emmett et al. 2008 and 2010.

## Quality control and governance
- Quality control adheres to the Defra/NERC Joint Codes of Practice.
- Full methodological details and calibration steps are documented in the referenced reports (Emmett et al. 2008, 2010) and associated technical reports.

## Data sources and supporting documents
- Data derived from Countryside Survey and linked to: Land Cover Map 2007 (Morton et al. 2011) and the British Geological Survey Soil Parent Material Model.
- Key references include Emmett et al. (2008, 2010), Scott (2008), and related technical reports and DOIs as listed in the document.

## Relevance to monitoring frameworks (for authors)
- Provides a structured, model-based approach to deriving soil health indicators across habitats and parent materials.
- Integrates remote-sensed land-cover data with soil material models to produce spatially explicit estimates.
- Delivers transparency through detailed data attributes, modeling approach, and quality-control references, enabling auditing and replication.
- Highlights data gaps and limitations (non-sampled areas and some combinations with small sample sizes) important for monitoring coverage planning and data governance.