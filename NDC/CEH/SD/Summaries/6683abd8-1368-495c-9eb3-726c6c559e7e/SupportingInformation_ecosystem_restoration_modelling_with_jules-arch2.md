# Background and experimental design

- Objective: Evaluate the global mitigation potential of five ecosystem-based land management pathways using a Dynamic Global Vegetation Model (DGVM) to assess contribution toward meeting the 1.5°C target.

- Five pathways studied:
  - Forest Restoration
  - Reforestation
  - Reduced Harvest
  - Agroforestry
  - Silvopasture

- Modelling framework and capabilities:
  - Uses the JULES model (JULES-BE branch, vn5.1) with functionality to represent agroforestry and to automatically plant new agricultural areas with a user-defined set of Plant Functional Types (PFTs).

  - Global grid: N96e (1.875° x 1.25°) with each cell containing land-use proportions for each pathway.

  - Data downscaling: Primary datasets downsampled to 1% of the N96e cell size and converted to cell-percent values.

- Spatial data and constraints:
  - Primary datasets for land use and forest condition:
    - Global map of forest condition for forest pathways
    - ESA-CCI Landcover maps (2000) for cropland and grazing lands (agricultural pathways)
  - Overlay with additional constraints:
    - Precipitation, biodiversity, and social constraints to reduce available land for restoration pathways.

- Meteorology and baseline data:
  - Forcing: UKESM1 meteorological outputs
  - Periods: 1880-2014 (historical) and 2015-2100 (SSP1-2.6)
  - Resolution: 3-hourly on N96e grid
  - Baseline land use: IMAGE (HYDE) dataset for 1880-2014 historical and 2015-2020 SSP1-2.6

- Land-use transition design:
  - 2021-2030: natural land conversion to crops/pastures decreases linearly to a fixed level by 2030.
  - 2031-2100: seven simulations:
    - Control: no further land-cover transitions
    - P1–P5: one pathway each
    - All: all pathways implemented
  - Pathway area expansion: restoration areas increase linearly to full extent by 2040, then held constant.

- Extended simulation:
  - Extended run to 2150 using meteorological data 2091-2100 repeated five times (to cover an additional 50 years due to data limits).

- Data quality and structure:
  - Quality control: JULES is maintained to high standards; robust and numerically stable within the Met Office Earth System Model suite.

  - Output format: raw model output in netCDF; one file per year per simulation.
    - File naming: jules.oneearth.v4_<simulation>.carbon.<year>.nc
    - Simulations and year ranges:
      - hist: Historical (1881-2000)
      - noluc: No land-use change (2001-2150)
      - all: Sum of land changes for P1–P5 (2001-2150)
      - P1: Forest Restoration (2001-2150)
      - P2: Reforestation (2001-2150)
      - P3: Reduced Harvest (2001-2150)
      - P4: Agroforestry (2001-2150)
      - P5: Silvopasture (2001-2150)

  - Variables and units:
    - frac: Fractional cover of each surface type (dimensioned as x, y, type, time)
    - cs: Soil carbon in each soil carbon pool (kg m^-2)
    - c_veg: Total vegetation carbon per PFT (kg m^-2)
    - cv: Gridbox mean vegetation carbon (kg m^-2)
    - Time: Annual means (calendar year)
    - Surface-type taxonomy: 1–24 defined (various natural/plantation/urban/water/bare soil categories)
    - PFTs: 1–20 (defined per type)
  - Spatial and temporal metadata: Includes latitude/longitude per grid, and annual timesteps.

- Provenance and link to publication:
  - Dataset underpinning the publication: Littleton et al. (2021) Environmental Research Letters, “Dynamic modelling shows substantial contribution of ecosystem restoration to climate change mitigation.”
  - JULES code: publicly available at Met Office Science Repository Service (example branch/version noted in documentation).

- Relevance for environmental monitoring and analysis:
  - Provides globally distributed, spatially explicit projections of how ecosystem restoration pathways could contribute to climate mitigation.
  - Data is designed for standardised outputs, enabling comparison across pathways and integration with other environmental datasets.
  - Accessibility: raw model outputs (netCDF) with clear naming conventions and accompanying metadata; code and model versions publicly available for reproducibility.