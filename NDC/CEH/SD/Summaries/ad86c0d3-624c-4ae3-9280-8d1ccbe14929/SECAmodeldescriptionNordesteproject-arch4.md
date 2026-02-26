# SECA model description

- Purpose and scope
  - Describes the output data structure of a preliminary SEcA (Shrubland Ecosystem Assessment) model version (Fortran).
  - SEcA calculates ecosystem energy and carbon balance fluxes for a semi-arid shrubland, initially focusing on the Caatinga.
  - Main program reads required inputs and calls subroutines to compute the resistance network, fluxes (energy, water, carbon), and above-ground state variables.
  - Limitations: currently no soil water balance or soil heat transfer model.

- Model architecture and key concepts
  - Multicomponent surface: nine components total (eight tree/shrub species + bare soil) with non-overlapping cover fractions summing to 1.
  - Uses a mechanistic A–g model and plant water stress functions; resistance network and flux partitioning based on Verhoef and Allen (2000).
  - Latent heat flux (λE) is the sum over components, each with PM_i and Y_i terms that couple net radiation, aerodynamic and surface resistances.
  - Aerodynamic and boundary layer resistances calculated with a combination of within-canopy, surface, and atmospheric resistances; highest species r*>0 and some simplifications (e.g., ra,s set to 100 s m−1).
  - Photosynthesis and transpiration parameterizations include Farquhar-like models (and JULES/Farquhar variants), with plant water stress influencing stomatal conductance and photosynthetic rates.
  - Results include total net CO2 flux and canopy-level CO2 concentration, with adjustments for boundary layer resistances between canopy and atmosphere.

- Data inputs and sources
  - Micrometeorological driving data from the Embrapa Tropical Semiárido Research Station (Pernambuco, Brazil):
    - Atmospheric pressure, precipitation, soil water content, incoming radiation, air temperature, humidity, wind speed/direction (inputs for 2011).
  - Plant physiological data
    - Maximum Rubisco carboxylase activity (Vcmax) and maximum electron transport rate (Jmax) from A–Ci and temperature response curves for dominant species.
    - Measurements include photosynthesis at saturating light and ambient CO2, and dark respiration, using LI-COR systems.
  - Plant structural data
    - Plant Area Index (PAI) and Leaf Area Index (LAI) estimated daily from NDVI, calibrated with Landsat NDVI data; species-level partitioning derived from a monitoring plot to distribute total PAI/LAI among species.
  - Model input parameters (Table 1)
    - Species-specific cover fractions, plant height, leaf width, physiological parameters (Vcmax, Jmax) and other structural/physiological constants.
    - Configuration options for model components (e.g., SECA ALL, JULES for J parameter sets, Sinclair or Dewar for soil water stress models).
    - Soil and hydraulic parameters, including soil water retention parameters (theta_r, theta_s, alpha, n) fitted with Van Genuchten parameters from Petrolina site data.
    - Various switches and q parameters controlling stress models, Jacob’s model option, and other modeling choices.
  - Model configuration and notes
    - Specific notes on naming changes (species updates since 2019) and updated photosynthetic parameters.
    - Final sections specify how soil water stress models are switched (JULES, Sinclair, Dewar) and how stress is applied (stomatal, physiological, mesophyll, or all).

- Outputs and data products
  - Four output files produced:
    - resistancesCaatinga.txt: timestamps and various resistances (aerodynamic, within-canopy, boundary layer, surface) for each species and soil, plus related descriptors.
    - variablesCaatinga.txt: timestamps and meteorological/plant variables (air temperature, canopy temperature, vapor pressure deficits, CO2 concentrations at reference and canopy levels, leaf-level and canopy parameters).
    - enbalCaatinga.txt: energy balance components (net radiation, available energy, sensible and latent heat fluxes, soil heat flux, and evapotranspiration) by surface component.
    - CO2Caatinga.txt: soil water stress factors, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.
  - Example context
    - Outputs correspond to runs using the JULES Farquhar model with Sinclair plant water stress switched on (Ψs = -1 MPa).

- Implementation notes
  - The core equations are solved iteratively, particularly for stomatal/photosynthesis-related resistances (r8).
  - References underlying the model framework include Verhoef and Allen (2000), Huntingford et al. (1995), VA2000, Clark et al. (2011), Egea et al. (2011), and related JULES/Farquhar integrations.

- Data provenance, researchers, and references
  - Researchers involved in data collection and model input curation include:
    - Anne Verhoef (model development and runs)
    - Raquel Carolina Miatto, Luiza Helena Menezes Cosme, Tomas Ferreira Domingues, Magna Soelma Beserra de Moura (plant physiology and micrometeorology)
    - Moonlight et al. (plant structural input collation)
    - Rodolfo Nobrega, Colin Prentice, and collaborators for modelling guidance
  - Key references: Verhoef & Allen (2000); Verhoef & Egea (2014); Miranda et al. (2020); Moonlight et al. (2020); Souza et al. (2016).