# 1. Background

- The document describes the output data structure from a preliminary SEcA model (Shrubland Ecosystem Assessment) written in Fortran, focusing on Caatinga shrubland. The main program reads inputs, runs subroutines to calculate resistance networks, energy, water, and carbon fluxes, and outputs state variables. The current version lacks a soil water balance and a soil heat transfer model.
- Funded by the Newton/NERC/FAPESP Nordeste project NE/N012488/1; contact Prof Anne Verhoef for more information.

## SECA model description and scope

- Purpose: describe component and total energy and carbon balance fluxes for a multi-vegetation shrubland ecosystem using a mechanistic A-g (photosynthesis) framework with plant water stress functions.
- Key approach: resistance network and flux partitioning based on Verhoef and Allen (2000); integrations include Penman-Monteith terms and component-specific resistances (canopy air-to-surface, within-canopy, boundary layer, and soil).
- System structure: nine surface components at Caatinga (eight tree/shrub species + bare soil) with non-overlapping cover fractions summing to 1.
- Outputs of the model: latent heat flux, total available energy, evapotranspiration, net radiation, CO2 fluxes, and other energy balances; photosynthesis and respiration are modeled with incorporated Farquhar-style physiology (JULES) variations.
- Calculations are iterated to solve the system of equations (Eqns 1–17) for stomatal/leaf processes and photosynthesis.

## Inputs and data sources

- Micrometeorological data
  - Sourced from Embrapa Tropical Semiarid Research Station (Pernambuco, Brazil) on a 16 m tower; variables include atmospheric pressure, precipitation, soil water content, short/longwave radiation, air temperature, humidity, wind speed/direction; data primarily for 2011 inputs.
- Plant physiological data
  - Maximum Rubisco carboxylase activity (Vcmax) and maximum electron transport rate (Jmax) obtained from A–Ci curves and temperature responses using LI-COR systems; measurements for eight dominant species.
- Plant structural data
  - Plant Area Index (PAI) and Leaf Area Index (LAI) estimated daily from NDVI–soil moisture relationships, calibrated with Landsat NDVI, and partitioned among species using field monitoring plots (50 x 100 m) to allocate ecosystem PAI/LAI to species.
- Model input parameters
  - Species-specific structural, physiological, and hydraulic parameters (Table 1). Note: June 2019 parameters are current with October 2020 renaming; updated photosynthetic parameters (Vcmax, Jmax) provided.
  - Model configuration options: structural parameters, physiological parameters, and hydraulic/soil-water stress parameters; choices include JULES, Sinclair, and Dewar stress models; switches for stress location and Jacob/JULES integration; soil water retention parameters (theta_r, theta_s, alpha, n) fitted to local VG curves.
  - Additional soil/moisture and stress parameters: residual and saturated soil moisture contents, VG fitting parameters, and water-stress curve modifiers.

## Model outputs

- Four output files generated:
  - resistancesCaatinga.txt: time-stamped aerodynamic, within-canopy, boundary layer, and surface resistances for each species and soil, plus related metrics.
  - variablesCaatinga.txt: time-stamped state variables including reference and within-canopy temperatures, vapor pressure deficits, CO2 concentrations at multiple levels, and surface temperatures for each component.
  - enbalCaatinga.txt: energy balance outputs including total and component-wise net radiation, available energy, sensible and latent heat fluxes, ET, and soil heat flux components.
  - CO2Caatinga.txt: CO2-related outputs including soil water stress factors, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.
- Data are provided on a daily timescale with fields for year, month, day, decimal time, and component-specific measurements.

## Model status, provenance, and contacts

- Development and runs conducted by Anne Verhoef, with team contributing plant physiology, micrometeorology, plant structure, and modelling inputs.
- Project context and references:
  - Verhoef & Allen (2000); Verhoef & Egea (2014); Miranda et al. (2020); Moonlight et al. (2020); Souza et al. (2016).
- Researchers involved
  - Raquel Miatto, Luiza Cosme, Tomas Domingues, Magna Moura, Moonlight, Rodolfo Nobrega, Colin Prentice, Anne Verhoef (various roles in physiology, micrometeorology, structural indices, modelling).
- Contact: Prof Anne Verhoef (a.verhoef@reading.ac.uk)

## Practical notes for data stewardship

- Data lineage and context: clearly document the CAATINGA-specific vegetation composition, NDVI-derived PAI/LAI estimates, and field-derived physiological parameters; note any aliases or renamings of species parameters since 2019–2020.
- Data formats and accessibility: outputs are plain-text files with fixed column structures; ensure metadata captures column definitions, units, and time conventions (daily timestamps, decimal time within day/year).
- Provenance and versioning: link outputs to the exact model configuration (which stress model used, soil parameters, and file of input parameters) and the specific SECA version and run date.
- Data quality and interoperability: although the model is multi-component and uses various parameterizations (JULES, Sinclair, etc.), maintain a mapping between species and their corresponding columns in outputs; consider providing a schema or JSON metadata to improve machine-readability.
- Gaps and caveats: current SECA runs exclude soil water balance and soil heat transfer; document this limitation for downstream reuse and future integration with full soil physics.