# Background and experimental design

- Global assessment of ecosystem-based land management pathways for climate mitigation using a Dynamic Global Vegetation Model (DGVM).
- Five pathways studied: Forest Restoration; Reforestation; Reduced Harvest; Agroforestry; Silvopasture.
- Goal: quantify spatial mitigation potential and contribution to 1.5°C target; inform land restoration importance in climate strategies.

## Data generation methods

- Spatial distribution for each pathway derived from global datasets:
  - Forest pathways: Global map of forest condition.
  - Agricultural pathways: ESA-CCI Landcover 2000 for cropland and grazing lands.
- Overlay with additional layers: precipitation, biodiversity, social constraints to reduce available land area from theoretical maxima.
- Global land use distributions modeled in JULES (N96e grid; 1.875° × 1.25°) with cell-level land-use proportions.
- Primary datasets re-sampled to uniform resolution (1% of N96e cell size) and converted to cell-percent values.
- Model variant: JULES-BE branch (supports agroforestry) using JULES v5.1.
- Forcing: UKESM1 meteorology (1880–2014 historical; 2015–2100 SSP1-2.6) at 3-hourly timestep.
- Baseline LU data: HYDE/IMAGE lineage (1880–2014 historical; 2015–2020 SSP1-2.6).
- 2021–2030 transition rate decreases linearly to 2030; post-2030, seven simulations run (control + P1–P5 + all pathways).

## Simulation design and scenarios

- Configurations:
  - Control: no further land cover transitions after 2030.
  - P1: Forest Restoration.
  - P2: Reforestation.
  - P3: Reduced Harvest.
  - P4: Agroforestry.
  - P5: Silvopasture (20% tree cover).
  - All: all pathways combined.
- Restoration areas expand linearly to 2040, reaching full extent, then held constant for remainder of the simulation.
- Extended run to 2150 using meteorology 2091–2100 repeated five times (to span >2100 due to data availability).

## Spatial and temporal resolution

- Grid: N96e global grid (approx. 1.875° × 1.25°).
- Time: annual means per calendar year; simulations span 1881–2150 (hist 1881–2000; noluc 2001–2150; others 2001–2150).

## Data structure and contents

- File format: netCDF (raw model output).
- File naming: jules.oneearth.v4_<simulation>.carbon_<year>.nc.
- Simulations available: hist; noluc; all; P1; P2; P3; P4; P5 (years vary by file group as listed).
- Variables:
  - frac: fractional cover of each surface type (dimension x, y, type, time).
  - cs: soil carbon in each soil carbon pool (kg m−2) (x, y, sclayer, scpool, time).
  - c_veg: total vegetation carbon per Plant Functional Type (PFT) (kg m−2) (x, y, pft, time).
  - cv: gridbox mean vegetation carbon at end of timestep (kg m−2) (x, y, time).
- Spatial/biophysical details:
  - Includes 20 PFT definitions; extensive surface-type taxonomy; notes on soil carbon layers (no layering used in these simulations for Evergreen shrubs plantation).
- Notes:
  - All values are annual means.
  - Latitude/longitude coordinates provided per file.

## Quality control and provenance

- JULES is maintained to high standards due to ties to the UK Earth System Modelling effort.
- Model outputs and structure are designed for robustness and numerical stability within Met Office atmospheric model suite.

## Access, provenance, and references

- Dataset provides raw model outputs underpinning the publication: Littleton et al. (2021) Environmental Research Letters 16, 124061.
- JULES code is publicly available (Met Office repository): code.metoffice.gov.uk/trac/jules (registration required).
- Specific version used: r12164_biotiles_harvest (repository branch: dev/emmalittleton/r12164_biotiles_harvest).

## Data products and opportunities for data support

- Potential data products:
  - Spatial dashboards showing pathway-specific and aggregate mitigation potential across regions.
  - Time-series visualizations of carbon pools and vegetation carbon per pathway.
  - Comparisons of restoration scenarios versus control and all-pathways scenarios.
  - Data cubes or GIS-ready layers for cross-analysis with biodiversity, precipitation, and land-use datasets.
- Data handling considerations for support:
  - Handle multiple simulations (hist, noluc, all, P1–P5) and align years across files.
  - Convert netCDF outputs to GIS-friendly formats or tabular summaries for end users.
  - Translate units and variable definitions (e.g., frac, cs, c_veg, cv) for non-specialist audiences.
  - Document assumptions: linear expansion of restoration areas to 2040, constant post-2040, and extended 2150 run methodology.
  - Provide metadata mapping for surface-type taxonomy and PFT definitions to facilitate interoperability with other datasets.
- Practical use cases for exploration:
  - Assess regional contributions to 1.5°C mitigation from each pathway.
  - Evaluate spatial trade-offs between restoration and other land uses under SSP1-2.6 forcing.
  - Support policy discussions on scalable restoration strategies and their long-term carbon implications.