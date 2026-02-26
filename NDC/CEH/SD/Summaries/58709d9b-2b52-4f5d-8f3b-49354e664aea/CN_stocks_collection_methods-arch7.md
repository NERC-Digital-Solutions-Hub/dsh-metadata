# Soil sampling

## Overview
- Describes a soil sampling and analysis workflow to calculate carbon and nitrogen stocks by depth.
- Data are organized in a depth-resolved CSV (Soil_C_budgets_to_depth.csv) with fields for land use, site, replicate, soil level, depth, core properties, bulk density, and C/N stocks.

## Sampling and preparation
- Two soil samples per site using a 4 cm width auger, collected to the maximum feasible depth.
- Soils sieved to 2 mm to remove stones and roots; stones weighed to determine gravel/chalk proportion.
- Cores split into 5 cm depth increments; dried at 80°C for 48 hours after sieving.
- Samples stored at 25°C until processing.

## Bulk density and density adjustments
- Bulk density (BD) calculated as mass/volume.
- BD adjusted for gravel using: Adjusted BD = (unadjusted BD) × (1 − %gravel/100).

## Carbon and nitrogen analysis
- Each depth fraction ground in a ball mill (25 s−1 for 2 minutes).
- Carbonates removed with 37% HCl, with effervescence ceasing before further processing.
- Samples redried; ~10 mg used for combustion analysis (Elementar Vario EL), calibrated with acetanilide standard.
- Carbon and nitrogen stocks calculated for each depth using: C_t_ha = 100 × (core depth/100) × corrected BD × raw C%; N_t_ha similarly for nitrogen.

## Quality control
- Standards and blanks run every 20 samples on the combustion analyser.
- 5% analytical replicates included.

## Data set: Soil_C_budgets_to_depth.csv
- Data definitions (examples):
  - Land Use: land use type
  - Site: site identifier
  - Replicate: replicate (1 or 2)
  - Soil level: top, middle, bottom
  - Soil Depth from surface: depth from surface (5 cm increments where possible)
  - Core depth: total length of the core
  - Core diameter: auger diameter
  - Core volume: pi × r^2 × h
  - Dry wt: soil weight of this increment
  - Gravel wt: weight of stones >2 cm
  - %gravel: proportion of the core by gravel
  - Bulk density with gravel: BD including gravel
  - BD corrected for gravel: BD of soil excluding gravel
  - N post acid: total nitrogen after acid treatment
  - C post acid: total carbon after acid treatment
  - C t ha: carbon stock (tonnes per hectare)
  - N t ha: nitrogen stock (tonnes per hectare)
  - CN post acid: carbon-to-nitrogen ratio after carbonate removal

## GIS and data use considerations
- Enables mapping of carbon and nitrogen stocks by depth, site, and land use.
- Suitable for 2D/3D or layered map visualizations; requires consistent depth intervals and careful handling of missing increments.
- Clear unit definitions and data definitions facilitate integration into GIS workflows and data products.