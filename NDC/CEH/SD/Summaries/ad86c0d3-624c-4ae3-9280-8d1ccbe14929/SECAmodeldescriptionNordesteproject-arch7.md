# 1. Background

- The document explains the structure of the output data from a preliminary SEcA model (Shrubland Ecosystem Assessment) written in Fortran.
- SEcA calculates ecosystem energy and carbon balance fluxes for a semi-arid shrubland system, initially focusing on Caatinga.
- The main Fortran program reads inputs and calls subroutines to compute the resistance network, fluxes (energy, water, carbon), and above-ground state variables.
- The current model lacks a soil water balance and a soil heat transfer model.
- Funding: Newton/NERC/FAPESP Nordeste project NE/N012488/1.
- Contact: Prof Anne Verhoef (University of Reading).

## 2. SECA model description

- Describes component and total energy- and carbon-balance fluxes for a shrubland/multi-tree ecosystem.
- Uses a mechanistic A-G-P (photosynthesis and transpiration) framework with a range of plant water stress functions.
- Resistance network and flux-partitioning follow Verhoef and Allen (2000); VA2000.
- Latent heat flux (λE) is computed as a sum over surface components (eight tree/shrub species plus bare soil), each with fractional coverage that sums to 1.
- The model defines available energy for the ecosystem and for each component, incorporating net radiation, soil heat flux, and radiation partitioning.
- Aerodynamic and surface resistances are computed using parameterisations (Huntingford et al. 1995), with within-canopy and boundary-layer resistances for each component.
- Stomatal conductance and leaf-level processes are modelled via a mechanistic stomatal resistance formulation (Jacobs et al. 1996) linked to photosynthesis and PAR, CO2, and soil moisture status.
- The Farquhar model and JULES framework are implemented for photosynthesis; the model solves for leaf stomatal and CO2 fluxes iteratively.
- The Caatinga setup distinguishes nine surface components: eight tree/shrub species plus bare soil; species cover fractions do not overlap.
- A canopy-source height framework is used, with resistances calculated between surface components and the canopy source height.
- Outputs include canopy temperature, vapour pressure deficits, atmospheric CO2 concentrations, and CO2 fluxes, with fluxes partitioned among components.

## 3. Micrometeorological and plant data

- Data driving and validating the model come from the Embrapa Tropical Semiarid Research Station (Pernambuco, Brazil) with a 16 m meteorological tower; data since 2011 (only 2011 inputs used in provided outputs).
- Measurements include pressure, precipitation, soil water content, incoming radiation, air temperature, humidity, wind speed/direction.

### 3.1 Micrometeorological data
- Site location: Caatinga vegetation, ~350 m above sea level.
- Sensors on/near a 16 m tower; inputs include standard meteorological variables for model runs.

### 3.2 Plant physiological data
- Parameters: maximum Rubisco activity (Vcmax) and maximum electron transport rate (Jmax).
- Determined from A-Ci curves and temperature response curves for dominant species (2–3 per species).
- Measurements include assimilation rates at saturating light and ambient CO2, plus dark respiration; conducted with LI-COR systems.

### 3.3 Plant structural data
- Plant Area Index (PAI) and Leaf Area Index (LAI) estimated daily.
- NDVI used to estimate NDVI–soil moisture relationships; Landsat-derived NDVI for calibration/verification.
- Daily NDVI used to estimate PAI/LAI following Miranda et al. (2020).
- Partitioning of PAI/LAI among species uses structural data from monitoring plots within the Nordeste project permanent plot network; dominance and crown area inform species-specific allocations.

### 3.4 Model input parameters
- Input parameter file includes species-specific and general parameters; Table 1 lists:
  - Structural parameters: cover fractions (c_i), plant heights (h_i), leaf widths (l_i).
  - Physiological parameters: Vcmax, Jmax by species.
  - Hydraulic parameters and soil-physics parameters (q, Ψ, etc.), with model configurations (e.g., ALL, JULES, Sinclair, Dewar).
  - Soil water retention parameters: residual and saturated moisture contents (θ_r, θ_s), Van Genuchten parameters (α, n).
  - Stress models and locations of stress application (locstress).
  - References to parameter sources and model variants (Jacobs, JULES, Dewar, Sinclair, etc.).
- Notes: Species renaming and updated photosynthetic parameters have occurred since June 2019.

## 4. Model outputs

- The model yields four output files:
  - resistancesCaatinga.txt: aerodynamic and surface resistances, with columns for year, month, day, time, and per-component resistances (within-canopy, boundary layer, surface) and stomatal conductances.
  - variablesCaatinga.txt: time series of air and surface temperatures, vapour pressure deficits, atmospheric CO2 concentrations at reference and within-canopy levels, leaf- and surface-level variables, and per-species leaf/canopy parameters.
  - enbalCaatinga.txt: energy balance components including total net radiation, total available energy, per-component radiation, available energy, soil heat flux, evapotranspiration, and sensible heat flux per component.
  - Co2Caatinga.txt: soil water stress factors per species, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.
- Notes:
  - Outputs shown correspond to runs using the JULES Farquhar model with Sinclair-based plant water stress (Ψ at canopy level = -1 MPa).
  - Data are time-stamped per day with decimal day/year formats.

## 5. Researchers involved

- Anne Verhoef (lead, model development and runs).
- Raquel Carolina Miatto (plant physiology, University of Sao Paulo).
- Luiza Helena Menezes Cosme (plant physiology, USP).
- Tomas Ferreira Domingues (plant physiology, USP).
- Magna Soelma Beserra de Moura (micrometeorology, EMBRAPA).
- Magna Moonlight (plant species identification, Royal Botanic Garden Edinburgh).
- Rodolfo Nobrega (plant structural indices, Imperial College, UK).
- Colin Prentice (modelling advice, Imperial College, UK).

## References

- Verhoef A. and Allen, S.J. (2000). A SVAT scheme describing energy and CO2 fluxes for multi-component vegetation: calibration and test for a Sahelian savannah.
- Verhoef, A. and Egea, G. (2014). Modeling plant transpiration under limited soil water: comparison of parameterizations for land surface models.
- Miranda, R. de Q. et al. (2020). Realistic and simplified models of plant and leaf area indices for a seasonally dry tropical forest.
- Moonlight, P. et al. (2020). Expanding tropical forest monitoring into Dry Forests: the DRYFLOR protocol for permanent plots.
- Souza, R. et al. (2016). Vegetation response to rainfall seasonality and interannual variability in tropical dry forests.