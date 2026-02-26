# Topsoil carbon model estimates [Countryside Survey]

## Overview
- GIS-ready dataset of topsoil carbon estimates (0–15 cm depth) for Great Britain.
- Model-based values derived from Countryside Survey data (1978, 1998, 2007) across 1 km grid squares.
- Variables include loss-on-ignition (%), carbon concentration (g kg-1), and carbon density (t ha-1).

## What’s in the dataset
- Sample scope: 2614 cores from 591 1 km × 1 km squares in GB (data from 2007; earlier years drawn from modelled relationships).
- Model outputs per habitat/parent material combination:
  - LOI (loss-on-ignition) values at 1978, 1998, 2007; LOISE (standard errors).
  - Carbon concentration (g kg-1) for 1978, 1998, 2007; CCONC_SE (standard errors).
  - Carbon density (t ha-1) for 1978, 1998, 2007; CDENS_SE (standard errors).
- Derived attributes (examples):
  - LCM_CLASS (Land Cover Map 2007 broad habitat class)
  - DOM_GRAIN (dominant grain size from the Soil Parent Material Model)
  - SOIL_GROUP (soil texture descriptor: Heavy/Medium/Light)
  - CACO3_RANK (carbonate content ranking)
- Units and references for attributes are documented in the dataset description.

## Spatial reference and extent
- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700)
- Spatial coverage: Great Britain, at 1 km grid resolution
- Depth: 0–15 cm (topsoil)

## Modelling approach and data derivation
- Means by habitat/parent material combinations estimated from Countryside Survey data using models linked to:
  - Land Cover Map 2007 for dominant habitat
  - Soil Parent Material Model (2009) for dominant material
- For each habitat/parent material combination, the parent material characteristic that minimised AIC was selected.
- Urban and littoral rock areas are not sampled and have no data; some habitat/parent material combinations have insufficient data to estimate mean values.
- LOI and CCONC/CDENS values are model-derived for the year combinations; standard errors accompany estimates.

## Data structure and attributes (GIS focus)
- Core measurement fields per year include:
  - LOI_78, LOI_98, LOI_07 and LOI_78SE, LOI_98SE, LOI_07SE
  - CCONC_78, CCONC_98, CCONC_07 and CCONC_78SE, CCONC_98SE, CCONC_07SE
  - CDENS_78, CDENS_98, CDENS_07 and CDENS_78SE, CDENS_98SE, CDENS_07SE
- Supporting fields:
  - LCM_CLASS (linked to LCM2007)
  - DOM_GRAIN (dominant grain size from Soil PMM)
  - SOIL_GROUP (texture category)
  - CACO3_RANK (carbonate content ranking)

## Experimental design, collection, and methods
- Sampling for LOI:
  - 1197 plots in 256 1 km squares (1978)
  - 1098 plots in 256 squares (1998)
  - 2614 plots in 591 squares (2007)
- Field method:
  - Soil cores 15 cm long, 5 cm diameter; 2 mm sieving; LOI by drying, combusting at 375°C
  - Carbon concentration measured with a total elemental analyser (SOP3102)
- Data processing:
  - Bulk density and LOI/carbon measurements combined to estimate topsoil carbon density (g cm^-3) and area-based densities (t ha^-1)

## Quality control and provenance
- QC followed Defra/NERC Joint Codes of Practice
- Primary references:
  - Emmett et al. 2008, 2010 (Soils Manual and Soils Report)
  - Scott 2008 (Statistical Report)
  - Morton et al. 2011 (Land Cover Map 2007 dataset)
- Linkages to Land Cover Map 2007 and Soil PMM documentation (BGS)

## Usage notes and limitations
- Data are model-based estimates, not raw measurements for all years; uncertainties are reflected in standard error fields.
- Areas not sampled (e.g., urban, littoral rock) have no corresponding data.
- Some habitat/parent material combinations may have limited sample sizes, affecting estimate reliability.
- Appropriate for GIS-based mapping of topsoil carbon across GB, enabling policy, land management, and environmental assessment analyses.

## How to use in GIS
- Join by LCM_CLASS and DOM_GRAIN (and related attributes) to map LOI, CCONC, and CDENS across the 1 km grid.
- Use LOISE, CCONC_SE, and CDENS_SE fields to assess uncertainty in mapped layers.
- Leverage OSGB (EPSG:27700) projection for alignment with other GB-wide GIS datasets.
- Integrate with related datasets (LCM2007, Soil PMM) to interpret spatial patterns by habitat type and parent material.