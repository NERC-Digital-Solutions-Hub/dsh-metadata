# Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017 Dataset Documentation

## Overview
- Dataset maps the Input to Yield Ratio (IYR) for winter wheat farming in England from 2010 to 2017.
- IYR = ratio of agrochemical inputs (fertilisers and pesticides) to agricultural yield (reward).
- Four mapped products at 1 km resolution: IYR for nitrogen fertilisers, phosphorus fertilisers, pesticide risk to earthworms, and pesticide risk to honeybees.
- Values are scaled so the maximum value in each dataset is 1, enabling proportional comparisons across inputs and harms.
- Scope supports evaluating trade-offs between yields and agrochemical inputs at large spatial scales and identifying where sustainability actions are most needed.

## Data Content and Structure
- Four single-layer TIFF rasters (1 km resolution) in British National Grid coordinate system:
  - input_to_yield_ratio_honeybees.tif
  - input_to_yield_ratio_nitrogen_fertilisers.tif
  - input_to_yield_ratio_phosphorus_fertilisers.tif
  - input_to_yield_ratio_earthworms.tif
- Areas with no data where winter wheat was not grown are omitted.
- Dataset is provided via the Environmental Information Data Centre (EIDC).

## Methodology and Provenance
- Data integration process combined spatially explicit estimates to produce IYR values for four harms.
- Timeframe: 2010–2017; individual data sources have different reporting periods, so values were averaged across years to maximize data availability.
- Key data sources:
  - Pesticide applications: FERA Pesticide Utilisation Survey (PUS)
  - Fertiliser usage: Defra Fertiliser Usage (British Survey of Fertiliser Practice)
  - Winter wheat area: UKCEH Land Cover Plus: Crops map (2017)
  - Pesticide toxicity to honeybees and earthworms: Pesticide Properties Database (PPDB)
  - Wheat yields: Defra June Survey of Agriculture and Horticulture (2018) for average yields
- Process overview (see Figure 2 in the documentation):
  - Map pesticide and fertiliser applications to winter wheat areas
  - Convert applications to risk values using toxicity data
  - Derive IYR by comparing inputs to estimated yields
  - Produce four IYR rasters representing the different harms/inputs
- Additional outputs include maps and distributions (Figure 1) illustrating how IYR relates to yields.

## Metadata, Standards, and Documentation
- Data are versioned (Version 1.0; 11/07/2023) with formal metadata and methodological detail.
- All four rasters are 1 km resolution and aligned to a consistent grid for comparability.
- Scaled IYR values facilitate cross-harm comparisons within each product dataset.
- Detailed methodology and product creation process are documented; more in-depth methodology available in Bullock et al. (2023).

## Access, Citation, and Reuse
- Citation required: Fincham et al. (2023). Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017. NERC Environmental Information Data Centre. DOI to be inserted.
- Data access: Environmental Information Data Centre (http://eidc.ceh.ac.uk/).

## Applications and Implications for Data Stewardship
- Enables large-scale assessment of sustainability in arable farming and informs decisions about targeting improvements or land-use changes (e.g., ecosystem restoration).
- Useful for researchers and policy makers evaluating the balance between agricultural rewards and environmental harms.
- The scaled IYR format supports cross-study comparability but requires clear interpretation of relative versus absolute values.

## Quality, Limitations, and Data Gaps
- Temporal alignment challenges due to differing reporting periods across input datasets; averaging across years mitigates but does not eliminate temporal misalignment.
- Some grid cells lack data where winter wheat is not grown, limiting spatial completeness.
- Use of scaled values means absolute input or harm magnitudes are not represented; interpretation should focus on relative harms across space.
- Methodological complexity (combining multiple data sources with toxicity data) necessitates careful provenance tracking and clear citation.

## Documentation and Acknowledgements
- Acknowledges funding from ASSIST and AgZero+ projects; data licensing assistance from Caroline Cowan (UKCEH).
- References Defra, FERA, PPDB, UKCEH datasets and Bullock et al. 2023 for methodological context.