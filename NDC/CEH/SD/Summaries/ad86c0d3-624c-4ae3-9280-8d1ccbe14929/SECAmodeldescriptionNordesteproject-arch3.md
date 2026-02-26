# Shrubland Ecosystem Assessment (SEcA) model

- An initial, Fortran-based model focusing on Caatinga shrubland to calculate ecosystem energy and carbon balance fluxes.
- Describes a multi-component vegetation system (nine surface components: eight tree/shrub species plus bare soil) using a resistance-network/flux-partitioning framework (based on Verhoef and Allen 2000; VA2000).
- Currently does not include a soil water balance or soil heat transfer model; intended to drive and compare energy- and CO2-flux outputs for environmental monitoring and policy evaluation.
- Funded by the Newton/NERC/FAPESP Nordeste project NE/N012488/1; contact: Prof Anne Verhoef.

- ## Model purpose and outputs
  - Computes total latent heat flux, evapotranspiration, energy balance components, and CO2 fluxes (net ecosystem exchange, GPP, etc.) for a semi-arid multi-component shrubland.
  - Uses a mechanistic photosynthesis/transpiration framework with plant water stress functions and a multi-component resistance network.
  - Outputs four data files:
    - resistancesCaatinga.txt: aerodynamic, within-canopy, boundary layer, surface, and stomatal conductances for each component.
    - variablesCaatinga.txt: environmental and plant-state variables (temperatures, vapour pressure deficits, CO2 concentrations, leaf-level and canopy temperatures, etc.).
    - enbalCaatinga.txt: energy balance results (net radiation, available energy, fluxes per component, soil heat flux, ET, etc.).
    - CO2Caatinga.txt: soil water stress factors, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.

- ## Model structure and key components
  - Multi-component SVAT approach: eight vegetation components plus bare soil, with non-overlapping coverage fractions summing to unity.
  - Core equations include:
    - Latent heat flux: sum over components of c_i P_Mi Y_i, with Penman–Monteith and resistance terms.
    - Aerodynamic and surface resistances: r_a,i, r_b,i, r_s,i, r_l,i, r_a,a, and soil resistance r_s, for each component.
    - Net radiation for each component and available energy (A_i, R_n,i, etc.) and their dependence on albedo, emissivity, and surface temperature.
    - CO2 flux across canopy and soil layers, with atmospheric interplay and a boundary-layer correction factor.
  - Photosynthesis and transpiration parameterisations, including:
    - Farquhar/JULES-based representations (with the Sinclair plant water stress option in the example runs).
    - Stomatal conductance linked to CO2, photosynthesis rate, PAR, leaf temperature, and water stress.
  - Iterative solution: the full set of equations (1–17) is solved iteratively to determine leaf/soil processes and fluxes.

- ## Data inputs and sources
  - Micrometeorological data driving and validating the model:
    - Embrapa Tropical Semiarid station data (Pernambuco, Brazil): pressure, precipitation, soil moisture, incoming/outgoing radiation, air temperature, humidity, wind speed/direction; 2011 inputs used for provided outputs.
  - Plant physiological data:
    - Maximum Rubisco carboxylase activity (Vcmax) and maximum electron transport rate (Jmax) measured via A-Ci curves and temperature response curves for selected species.
  - Plant structural data:
    - Plant Area Index (PAI) and Leaf Area Index (LAI) estimated daily using NDVI, Landsat calibration, and a conversion to species-level allocation based on permanent plot data (dominance and crown area).
  - Model input parameters (Table 1):
    - Species-specific structural parameters: cover fractions, plant heights, leaf widths.
    - Physiological parameters: Vcmax, Jmax, and related coefficients.
    - Photosynthesis model configuration: options include JULES, Sinclair, and Dewar stress models; parameter choices for qs, qb, qm and Jacbos/JULES variants.
    - Soil-water-stress parameters and VG soil-retention parameters (theta_r, theta_s, alpha, n) fitted to observed soil-water retention curves at the Petrolina site.
  - Note: some species names and parameters were updated post-2020, affecting cover fractions and inputs.

- ## Model configuration and parameterization
  - Structural configuration captures nine components with species-specific parameters (e.g., c_i [cover], h_i [height], l_i [leaf width], etc.).
  - Physiological parameters include Vcmax, Jmax, and T-dependent values for each species, with JULES-based and Sinclair-based stress options.
  - Soil and leaf water stress parameters specify the form and application location of stress (stomatal, physiological, mesophyll, or all) and stress curve shapes (e.g., qs, qb, qm).
  - The current example uses JULES Farquhar with Sinclair leaf water stress (Ψ_l = -1 MPa) to illustrate outputs.

- ## Model outputs and interpretation
  - Resistances file (resistancesCaatinga.txt): tracks resistances and conductances across components and within the canopy, enabling monitoring of flux pathways and potential bottlenecks.
  - Variables file (variablesCaatinga.txt): records environmental states and leaf/soil temperatures, VPD, CO2 concentrations at reference and canopy levels, and leaf- to canopy-level gas variables.
  - Energy balance file (enbalCaatinga.txt): provides total and component-level net radiation, available energy, ET, sensible heat flux, and component energy partitioning.
  - CO2 file (Co2Caatinga.txt): reports soil water stress factors, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.
  - Outputs are specifically generated for runs with the JULES Farquhar model and the Sinclair water-stress assumption used in the reported results.

- ## Status, limitations, and usage notes
  - Preliminary model: focuses on a Caatinga shrubland system; aims to support monitoring and policy-evaluation efforts by providing mechanistic estimates of energy and carbon exchange.
  - Limitations: no soil water balance or explicit soil heat transfer model; some parameter values and species names may have been updated after 2019–2020, requiring careful re-parameterisation for new runs.
  - Data provenance: outputs reflect inputs and parameter choices from 2011 data; model setup and parameters are described for transparency and reproducibility.
  - Contact for more information: Prof Anne Verhoef (The University of Reading, UK).

- ## Researchers involved
  - Anne Verhoef (model development and runs)
  - Raquel Carolina Miatto (plant physiology)
  - Luiza Helena Menezes Cosme (plant physiology)
  - Tomas Ferreira Domingues (plant physiology)
  - Magna Soelma Beserra de Moura (micrometeorology, EMBRAPA)
  - Magna Moonlight? (Moonlight) et al. (plant species identification and input collation)
  - Rodolfo Nobrega (plant structural indices and input collation)
  - Colin Prentice (modelling advice)
  - Additional collaborators from Imperial College and collaborating institutes

- ## References and basis
  - Verhoef A. & Allen S.J. (2000) SVAT scheme for multi-component vegetation; Ecological Modelling.
  - Verhoef A. & Egea G. (2014) Modeling plant transpiration under limited soil water; Agriculture and Forest Meteorology.
  - Miranda R. de Q. et al. (2020) NDVI-based PAI/LAI models; IJATEGO.
  - Moonlight P. et al. (2020) DRYFLOR protocol; Plants, People, Planet.
  - Souza R. et al. (2016) Vegetation response in tropical dry forests; Hydrological Processes.