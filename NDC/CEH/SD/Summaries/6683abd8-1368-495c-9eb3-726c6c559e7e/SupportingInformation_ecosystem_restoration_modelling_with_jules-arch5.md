# Background and experimental design

- Purpose: Assess global mitigation potential of five ecosystem-based land management pathways (Forest Restoration; Reforestation; Reduced Harvest; Agroforestry; Silvopasture) using a Dynamic Global Vegetation Model (DGVM) to explore contributions to the 1.5°C target.

- Modelling framework: JULES (Be) branch, vn5.1, with an extended land-use class for agroforestry and features to plant new agricultural areas with user-defined Plant Functional Types (PFTs).

- Forcing and period:
  - Meteorological forcing from UKESM1.
  - Temporal coverage: Historical 1880-2014; SSP1-2.6 2015-2100.
  - Spatial resolution: N96e global grid (1.875° x 1.25°).
  - Climate data extended to 2150 by looping 2091-2100 data five times.

- Baseline and land-use data:
  - Baseline land use from HYDE-derived LUH2 (1880-2014 historical; 2015-2020 SSP1-2.6).
  - 2021-2030: natural land-to-crop/pasture conversion rate decreases linearly to a fixed level by 2030.

- Simulation design:
  - Post-2031 period includes seven simulations: one control (no further land cover transitions) plus one for each restoration pathway (P1–P5) and one combining all pathways.
  - Restoration areas expand linearly to full extent by 2040 and remain fixed thereafter.
  - Extended run to 2150 for each simulation.

- Data creation and processing:
  - Spatial distribution identified with global datasets (Global map of forest condition; ESA-CCI Landcover 2000 for cropland/grazing).
  - Overlay with precipitation, biodiversity, and social constraints to limit land availability.
  - Downscaling/normalization: primary datasets downsampled to 1% of N96e cell size; converted to cell percent values.

- Outputs and data structure:
  - Raw model outputs provided as netCDF files; one file per year per simulation.
  - File naming: jules.oneearth.v4_<simulation>.carbon_<year>.nc.
  - Main simulations and file counts:
    - hist: Historical run; 1881-2000 (120 files).
    - noluc: No land-use change; 2001-2150 (150 files).
    - all: Sum of changes from P1-P5; 2001-2150 (150 files).
    - P1: Forest Restoration; 2001-2150 (150 files).
    - P2: Reforestation; 2001-2150 (150 files).
    - P3: Reduced Harvest; 2001-2150 (150 files).
    - P4: Agroforestry; 2001-2150 (150 files).
    - P5: Silvopasture (20% tree cover); 2001-2150 (150 files).
  - Variables included:
    - frac: Fractional cover of each surface type (normalized 1).
    - cs: Soil carbon pool values (kg m^-2), with dimensions x, y, sclayer, scpool, time.
    - c_veg: Total vegetation carbon per PFT at timestep end (kg m^-2).
    - cv: Gridbox mean vegetation carbon (kg m^-2).
  - Dimensions and surface types are defined with a comprehensive type/definition mapping (from natural and plantation forests to different grass and shrub types; includes urban, water, bare soil, land ice as applicable).

- Documentation and provenance:
  - Data underpinning: Littleton et al. (2021) Environmental Research Letters report on ecosystem restoration contributions to climate mitigation.
  - JULES code: publicly available via the Met Office Science Repository Service; specific version used is r12164_biotiles_harvest (branch details provided).

- Data stewardship implications:
  - Governance: Raw model outputs require clear metadata, versioning, and linkage to the associated simulations and scenarios.
  - Metadata needs: Simulation name, year, forcing dataset, baseline LUH2/HYDE references, and the specific restoration pathway parameters.
  - Storage considerations: Large, annual netCDF files across multiple simulations; plan for scalable storage and efficient retrieval.
  - Reproducibility: Detailed provenance including dataset sources, downscaling steps, and model configuration is critical; access to JULES repository and version is provided.