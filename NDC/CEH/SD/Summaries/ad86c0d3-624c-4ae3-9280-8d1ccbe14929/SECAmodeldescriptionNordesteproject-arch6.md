# Background

- The document describes the output data structure from a preliminary SEcA model (Shrubland Ecosystem Assessment) written in Fortran, focused on semi-arid shrubland (Caatinga) ecosystem.
- The model computes energy- and carbon-balance fluxes and uses a mechanistic A-g model with plant water-stress functions; currently no soil water balance or soil heat transfer model.
- The work is funded by the Newton/NERC/FAPESP Nordeste project NE/N012488/1.
- For further information, contact Prof. Anne Verhoef.

## SECA model description (scope and mechanics)

- Describes component and total energy and CO2 balance fluxes for multi-species vegetation (eight tree/shrub species + bare soil).
- Uses a multi-component resistance network and flux partitioning based on Verhoef and Allen (2000); VA2000.
- Total latent heat flux (λE) is computed as a sum over components, with PMi and Yi terms representing Penman–Monteith and resistance combinations for each component.
- Nine surface components distinguished for Caatinga: eight vegetation species plus bare soil; cover fractions sum to unity; bare soil applies to soil patches not shadowed by plants.
- Aerodynamic and surface resistances are calculated using parameterizations from Huntingford et al. (1995) and related literature; multiple resistances (within-canopy, bulk boundary layer, surface) are defined per component.
- The model incorporates multiple parameterizations for aerodynamics, canopy resistance, stomatal conductance (via a mechanistic model), leaf CO2 dynamics, and soil moisture effects on stomatal resistance.
- Photosynthesis and transpiration are solved iteratively (Eqns 1–17 with a chosen photosynthesis model; Farquhar model implemented; JULES option included).

## Data inputs and driving data (micrometeorology and biology)

- Micrometeorological data (3.1) are from Embrapa Tropical Semiarid, Pernambuco, Brazil: 16-meter meteorological tower data (pressure, precipitation, soil moisture, radiation, temperature, humidity, wind) since 2011; model outputs shown use 2011 inputs.
- Plant physiological data (3.2) include maximum Rubisco carboxylase activity (Vcmax) and maximum electron transport rate (Jmax). Derived from A–Ci curves and temperature response data for eight species, using portable photosynthesis systems (LI-COR 6400/6800) with various measurements (A–Ci, PPFD-limited assimilation, dark respiration).
- Plant structural data (3.3) consist of Plant Area Index (PAI) and Leaf Area Index (LAI) estimated daily, using NDVI–soil moisture relationships calibrated with Landsat NDVI, and partitioned among species using permanent plot data on dominance and crown area (driven by the Nordeste project plot network).
- Model input parameters (3.4) include species-specific structural, physiological, hydraulic, and soil parameters. The document provides a table of values for each species (cover fraction, height, leaf width, physiological Vcmax and Jmax, JULES parameters, stomatal, and stress-related inputs). Note: some species were renamed in 2020; values may have changed accordingly.
- Soil water retention and VG parameters are included for soil moisture modeling (θr, θs, α, n) based on Van Genuchten fits from Petrolina site.

## Model inputs (parameterization and configuration)

- Structural parameters: species-specific cover fractions (c_i), heights (h_i), and leaf widths (l_i) for all nine components (eight vegetation species + soil).
- Physiological parameters: Vcmax, Jmax, and related photosynthesis model inputs (with JULES and JULES-like configurations).
- Hydraulic and soil-water stress parameters: soil water stress factors, q parameters, and Ψ(0) values for different models ( Sinclair, Dewar, etc.).
- The input file also includes references to specific model choices and switches (e.g., to select Jacobs model vs. JULES-based beta models, and stress application location).
- Soil water retention parameters (θ_r, θ_s, α, n) were fitted to regional soil data ( Petrolina site).

## Model outputs

- The model yields four output files:
  - resistancesCaatinga.txt: time-stamped aerodynamic and surface resistances for the canopy components and soil; includes resistances between within-canopy points, boundary layers, and stomatal conductances.
  - variablesCaatinga.txt: time series of atmospheric and surface temperatures, vapour pressure deficits, CO2 concentrations at reference, canopy, and leaf levels, and other state variables.
  - enbalCaatinga.txt: energy balance components per time step, including total net radiation, total available energy, sensible and latent heat fluxes, and component-wise fluxes (net radiation, available energy, soil heat flux, evapotranspiration, etc.).
  - CO2Caatinga.txt: CO2-related outputs, including soil water stress factors for the eight species, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.
- Output data are provided for runs using the JULES Farquhar model with Sinclair (or related) plant water-stress assumptions, as noted (Ψ_s0 = -1 MPa in the example run).

## Specific data structures and content details

- Resistances file structure: year, month, day, decimal day, decimal year, then arrays for aerodynamic resistances and component-wise resistances, plus stomatal conductances for eight species.
- Variables file structure: time stamps plus temperatures, different VPDs, CO2 concentrations at multiple heights, leaf-level and soil-level humidity indicators, and intra-leaf CO2 concentration differences across eight species.
- ENBAL file structure: per-time-step energy and flux sums; includes per-component net radiation, available energy, soil heat flux, evapotranspiration, and sensible heat flux per component (eight species + soil).
- CO2 file structure: soil water stress factors, leaf- and canopy-level photosynthesis rates, soil respiration, and net ecosystem CO2 flux.
- Species ordering follows Table 1 in the document; all seven or eight listed vegetation components are included in the same order across inputs and outputs.

## Researchers involved

- Anne Verhoef (model development and runs)
- Raquel Carolina Miatto (plant physiology)
- Luiza Helena Menezes Cosme (plant physiology)
- Tomas Ferreira Domingues (plant physiology)
- Magna Soelma Beserra de Moura (micrometeorology, EMBRAPA)
- Peter Moonlight (plant species identification)
- Rodolfo Nobrega (plant structural indices, input collation)
- Colin Prentice (modelling advice)

## References and provenance

- Verhoef A. and Allen, S.J. (2000) A SVAT scheme describing energy and CO2 fluxes for multi-component vegetation: calibration and test for a Sahelian savannah.
- Verhoef, A. and Egea, G. (2014) Modeling plant transpiration under limited soil water: comparison of parameterizations.
- Miranda et al. (2020) Realistic and simplified models of plant and leaf area indices for a seasonally dry tropical forest.
- Moonlight et al. (2020) DRYFLOR protocol for permanent plots.
- Souza et al. (2016) Vegetation response to rainfall seasonality in tropical dry forests.