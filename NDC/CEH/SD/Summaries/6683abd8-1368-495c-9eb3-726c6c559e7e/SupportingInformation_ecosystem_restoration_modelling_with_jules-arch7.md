# Background and experimental design

- Purpose: Assess global mitigation potential of five ecosystem-based, land-management pathways and their contribution to meeting the 1.5°C target using a spatially explicit approach.
- Pathways analyzed: Forest Restoration; Reforestation; Reduced Harvest; Agroforestry; Silvopasture.

## Methods overview

- Modelling framework: Dynamic Global Vegetation Model (DGVM) to simulate plant growth and ecosystem carbon balance under climate and land-use changes on a global grid.
- Data inputs and alignment:
  - Global forest condition map for forest pathways.
  - ESA-CCI Landcover maps (2000) to identify cropland and grazing lands for agricultural pathways.
  - Overlay with precipitation, biodiversity, and social constraints to downscale available land.
  - Global land-use distributions modelled in JULES on an N96e grid (1.875° x 1.25°) with cell-level land-use proportions.
  - Primary datasets re-sampled to a uniform resolution (1% of N96e cell size) and converted to cell percentages.
- Model and forcing:
  - JULES-BE branch of JULES v5.1, enabling agroforestry representation and automated planting of new agricultural areas with selected Plant Functional Types (PFTs).
  - Meteorological forcing from UKESM1: historical (1880-2014) and SSP1-2.6 (2015-2100), 3-hourly timesteps.
  - Baseline LU/land-use from HYDE-based HYDE-derived crop/pasture (1880-2014) and 2015-2020 SSP1-2.6; natural land conversion rates adjusted 2021-2030, then fixed from 2030 onward.
- Experimental design:
  - 7 simulations from 2031 onward: a control (no further land-cover transitions), one per pathway (P1–P5), and one with all pathways combined.
  - Restoration areas increase linearly over a decade to full extent by 2040, then remain fixed for the remainder of the 2001-2150 period.
  - Extended run to 2150 using meteorology from 2091-2100 repeated five times to cover 50 extra years (data beyond 2100 unavailable in driving dataset).

## Data generation and structure

- Annual spatial outputs:
  - Data presented as raw model output in netCDF format; one file per year per simulation.
  - File naming: jules.oneearth.v4_<simulation>.carbon_<year>.nc.
- Simulations and years:
  - hist: Historical run (1881-2000; 120 files).
  - noluc: No land-use change, future via LUH2 to 2030, then constant to 2150 (2001-2150; 150 files).
  - all: Sum of land changes from P1–P5 (2001-2150; 150 files).
  - P1: Forest Restoration (2001-2150; 150 files).
  - P2: Reforestation (2001-2150; 150 files).
  - P3: Reduced Harvest (2001-2150; 150 files).
  - P4: Agroforestry (2001-2150; 150 files).
  - P5: Silvopasture (20% tree cover) (2001-2150; 150 files).
- Variables and units (annual means per calendar year):
  - frac: Fractional cover of surface types (dimension: x, y, type, time; unitless).
  - cs: Gridbox soil carbon per soil carbon pool (kg m^-2; dimensions include sclayer, scpool, time).
  - c_veg: Total vegetation carbon per PFT (kg m^-2; dimensions include pft, time).
  - cv: Gridbox mean vegetation carbon (kg m^-2; time).
- Spatial and type details:
  - Type definitions cover 20 surface/vegetation categories (e.g., various broadleaf/needleleaf trees (natural/plantation), grasses (C3/C4), shrubs, cropland, pasture, urban, water, bare soil, land ice, etc.).
  - PFTs: 1-20 corresponding to defined vegetation types (aligned with surface types).
  - Lat/lon coordinates included for spatial referencing.
- Output scope:
  - Raw model outputs intended to support analysis of ecosystem restoration contributions to climate mitigation, as documented in Littleton et al. (2021).

## Data quality and accessibility

- Quality control: JULES maintained to high standards due to ties to UK Earth System Modelling efforts; emphasis on numerical stability and accuracy within Met Office model suite.
- Documentation and code:
  - Dataset underpins the referenced Environmental Research Letters article.
  - JULES code publicly available (Met Office Science Repository Service); specific version used noted in the dataset metadata.

## Practical notes for GIS use

- Spatial resolution: Global grid at 1.875° x 1.25° (N96e); primary-downscaled data downsampled to 1% of that cell size for initial distribution.
- Data format: netCDF, suitable for GIS analysis and integration with other gridded environmental datasets.
- Time coverage: 1881-2150 (varying across simulations; main analysis through 2100 with extended 2100-2150 period in P1–P5 scenarios).
- Application relevance: Enables spatial assessment of how targeted ecosystem restoration pathways could contribute to climate change mitigation, including mapping potential land-use changes, carbon pools, and vegetation dynamics across regions.