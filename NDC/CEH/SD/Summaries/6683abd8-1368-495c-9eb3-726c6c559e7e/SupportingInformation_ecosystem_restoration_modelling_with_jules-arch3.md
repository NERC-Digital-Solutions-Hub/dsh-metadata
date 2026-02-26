# Dynamic modelling shows substantial contribution of ecosystem restoration to climate change mitigation

## Aim
- Assess the mitigation potential of five ecosystem-based land management pathways at a global scale: Forest Restoration; Reforestation; Reduced Harvest; Agroforestry; Silvopasture.
- Use a Dynamic Global Vegetation Model (DGVM) to analyze spatial distribution and quantify potential contributions toward meeting the 1.5°C target.

## Methods and data generation
- Global datasets identify spatial distribution for each pathway; forest pathways use the Global Map of Forest Condition, agricultural pathways use ESA-CCI Landcover (2000) for cropland and grazing lands.
- Additional overlays include precipitation, biodiversity, and social constraints to reduce available land area from potential maxima.
- Land-use distributions modeled in JULES (N96e grid; 1.875° x 1.25°) with cell-level land-use proportions per pathway.
- Primary datasets resampled to a uniform resolution (1% of N96e cell size) and converted to cell-percent values.
- JULES BE branch (v5.1) enables the agroforestry class and automated planting of new agricultural areas with user-defined plant functional types (PFTs).
- Forcing: UKESM1 meteorological outputs (1880–2014 historical; 2015–2100 SSP1-2.6) on a 3-hourly timestep; baseline land use from IMAGE (HYDE-based) for 1880–2014 and 2015–2020; 2021–2030 transition in land-cover change is linear toward a fixed 2030 level; 2031 onward, seven simulations (no further transitions; one per pathway; all pathways together).
- Restoration areas expand linearly, reaching full extent by 2040; extended 2150 run with repeated 2091–2100 meteorology to cover an additional 50 years.

## Simulation design and scenarios
- Seven simulations per pathway: hist (historical climate/land use), noluc (no land-use change beyond LUH2 up to 2030, then constant), all (sum of all land changes), and P1–P5 (individual pathways: Forest Restoration, Reforestation, Reduced Harvest, Agroforestry, Silvopasture).
- The full restoration areas are increased gradually to 2040 and held constant thereafter; multi-scenario runs enable attribution of carbon mitigation to specific pathways.

## Outputs, structure, and units
- Data are provided as raw model outputs in netCDF format; one file per year per simulation.
- File naming convention: jules.oneearth.v4_<simulation>.carbon_<year>.nc
- Variables include:
  - frac: fractional cover of surface types (unitless)
  - cs: soil carbon pools (kg m^-2)
  - c_veg: total vegetation carbon per PFT (kg m^-2)
  - cv: mean vegetation carbon (kg m^-2)
- Spatial and temporal dimensions:
  - Annually averaged values per calendar year
  - latitude/longitude coordinates per grid cell
  - Surface types and plant functional types enumerated (1–20, with detailed definitions)
- Data structure supports grid-scale carbon and land-cover dynamics, aligned with the publication: Littleton et al. (2021).

## Quality control and governance
- JULES is maintained to high standards due to its link to UK Earth System Modeling efforts.
- The dataset represents raw model outputs used to support policy-relevant climate-m mitigation insights, with clear documentation of simulations and forcing data.
- Data and model code are publicly referenced (JULES repository with specific branch), supporting reproducibility.

## Reproducibility, accessibility, and metadata
- Outputs are organized by simulation and year, with explicit description of each scenario (hist, noluc, all, P1–P5).
- The dataset underpinning the associated Environmental Research Letters publication is documented, including version references and repository links.
- Access to model code requires registration for the Met Office repository, emphasizing transparency and reproducibility.

## Relevance to monitoring frameworks
- Demonstrates how to structure an environmental monitoring framework around:
  - Scenario-based assessment of policy options (pathways) and their spatially explicit impacts.
  - Transparent data provenance, standardized file naming, and defined variables for consistent monitoring.
  - Integration of diverse data layers (climate forcing, land use, biodiversity, social constraints) to constrain policy-relevant land-use options.
  - Clear delineation of baseline, future, and sensitivity scenarios to evaluate policy efficacy.
  - Production of annual, gridded carbon and land-cover metrics suitable for dashboards, reports, and governance discussions.

## Practical implications for policy and data governance
- Supports the design of monitoring schemes that compare multiple restoration pathways and aggregate effects over time.
- Highlights the need for standardized, open data formats and robust metadata to enable cross-jurisdictional comparison and policy evaluation.
- Underlines the importance of documenting forcing data, scenario assumptions, and transformation steps to ensure traceability and trust in monitoring outputs.

## Key takeaways
- A rigorous, scenario-driven framework can quantify the global mitigation potential of ecosystem restoration pathways using spatially explicit DGVM modeling.
- Transparent data structures (netCDF outputs, well-defined variables, and consistent naming) facilitate monitoring, reporting, and policy evaluation.
- Reproducibility is supported by open repositories and clear documentation of simulations, forcing data, and model configurations, though some access to code may require registration.