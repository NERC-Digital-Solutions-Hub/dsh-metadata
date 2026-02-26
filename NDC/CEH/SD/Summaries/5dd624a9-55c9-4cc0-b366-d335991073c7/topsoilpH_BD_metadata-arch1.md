# Topsoil pH and bulk density model estimates [Countryside Survey]

## Overview
- Topsoil depth: 0-15 cm. 
- Data are from Countryside Survey (CS) and represent 2614 cores from 591 one-kilometre squares across Great Britain, collected in 2007.
- Mean values by habitat and parent material are estimated using mixed models, incorporating CS data from 1978, 1998, and 2007.
- Habitat and parent material characteristics are derived from the Land Cover Map 2007 (LCM2007) and the British Geological Survey’s Parent Material Model (2009).
- Urban and littoral rock areas are not sampled; some habitat/parent material combinations have insufficient sample sizes.

## Data collection and sampling design
- Measured soil pH and bulk density in samples from 2614 plots located on the CS Main Plots within the 591 squares.
- Collection method: 15 cm long by 5 cm diameter plastic core following the protocol described in Emmett et al. (2008).

## Analytical methods
- Topsoil pH: measured on 10 g of field-moist soil with 25 ml deionised water (soil-to-water ratio 1:2.5 by weight).
- Bulk density: estimated via detailed weight measurements during soil processing.
- Quality control: Defra/NERC Joint Codes of Practice followed.

## Dataset attributes
- LCM_CLASS: Derived from Land Cover Map 2007 (habitat classification, e.g., dominant land cover).
- LCM_NUMBER: Integer code (1-23) from LCM2007.
- DOM_GRAIN: Dominant grain size from the BGS Soil Parent Material Model.
- SOIL_GROUP: Broad soil texture category (Heavy, Medium, Light).
- CACO3_RANK: Carbonate content rank (none, low, medium, high) from the Soil PMM.
- PH_78, PH_78SE: Mean soil pH and standard error for 1978 (modelled by LCM_CLASS and CACO3_RANK).
- PH_98, PH_98SE: Mean soil pH and standard error for 1998 (modelled by LCM_CLASS and CACO3_RANK).
- PH_07, PH_07SE: Mean value (and standard error) for 2007 (text notes indicate pH-related values; the table also references soil nitrogen for PH_07 in one line, which may be a typographical inconsistency).
- BULKD_98, BULKD_98SE: Mean bulk density and standard error for 1998 (modelled by LCM_CLASS and DOM_GRAIN).
- BULKD_07, BULKD_07SE: Mean bulk density and standard error for 2007 (modelled by LCM_CLASS and DOM_GRAIN).

## Model details
- Estimation approach: Mixed models to derive habitat- and parent-material-specific means.
- Parent material characteristic selection:
  - For pH: Dominant carbonate content (CACO3_RANK).
  - For bulk density: Dominant grain (DOM_GRAIN).
- Some habitat/parent material combinations could not be estimated due to insufficient samples.

## Spatial reference
- Coordinate system: OSGB 1936 / British National Grid (EPSG: 27700).

## Data quality, limitations, and scope
- Not sampled: Urban areas and littoral rock regions do not have data.
- Some habitat/parent material combos have inadequate sample sizes, limiting estimation in those cases.
- Data focus on topsoil (0-15 cm) and may not reflect deeper soil properties.
- Some attribute descriptions in the documentation show potential inconsistencies (e.g., PH_07 described in one section as pH, and in another as soil nitrogen concentration); users should consult the referenced CS reports for precise definitions.

## References and provenance
- Emmett, B.A. et al. (2008, 2010): CS Technical Reports No. 03/07 and No. 09/07 (Soils Manual and Soils Report from 2007).
- Scott, W.A. (2008): CS Technical Report No. 4/07 (Statistical Report).
- Morton, R.D. et al. (2011): Land Cover Map 2007 (GB) data.
- Countryside Survey materials and the British Geological Survey’s Soil Parent Material Model (PMM).

## Practical considerations for analysts
- Use the mixed-model estimates to compare pH and bulk density across habitats and dominant parent materials, accounting for standard errors (PH_*SE, BULKD_*SE).
- Be mindful of data gaps in urban/littoral areas and certain habitat/parent material combinations.
- When integrating with other datasets, align to the OSGB 27700 coordinate framework and note the 0-15 cm soil depth focus.
- Reference the primary CS documents for detailed methodologies, sampling protocols, and calibration steps.