# Shrubland Ecosystem Assessment (SEcA) model

## Overview
- A preliminary Fortran-based ecosystem model that calculates energy, water, and carbon balance processes for a semi-arid shrubland system, with an initial focus on the Caatinga.
- Reads input data and executes calculations of the resistance network, fluxes (energy, water, CO2) and above-ground state variables.
- Currently does not include a soil water balance or a soil heat transfer model.
- Funded by the Newton/NERC/FAPESP Nordeste project NE/N012488/1.

## Model structure and approach
- Describes multi-component energy and carbon balance for a shrubland/forest system using a mechanistic photosynthesis and transpiration framework.
- Represents the surface as nine components: eight tree/shrub species (majority of vegetated cover) and bare soil; each component has a fixed fractional coverage that sums to one and non-overlapping cover.
- Uses a resistance-network and a Penman–Monteith–based formulation to partition latent heat flux (lambda_E) and other fluxes among components.
- Aerodynamic, boundary-layer, and within-canopy resistances are calculated from established parameterizations (Verhoef & Allen 2000; Huntingford et al. 1995).
- Photosynthesis and stomatal conductance are computed via a mechanistic model, with further attention to leaf-level and canopy-level CO2 exchange.
- Includes a Farquhar-based photosynthesis approach (in line with JULES) and supports selected plant water-stress models (Sinclair, JULES, and Dewar paradigms) as configured in the input.
- The system is solved iteratively to obtain the stomatal resistance (r_l) and related fluxes.

## Data and validation inputs
- Micrometeorology: Data from Embrapa Tropical Semiarid Research Station (Pernambuco, Brazil) from a 16 m meteorological tower; variables include pressure, precipitation, soil moisture, short/longwave radiation, air temperature and humidity, wind speed/direction; 2011 inputs used for outputs.
- Plant physiology: Species-specific Vcmax and Jmax obtained from A-Ci curves and temperature response curves (2–3 leaves per species; LI-COR 6400/6800).
- Plant structure: Daily estimates of Plant Area Index (PAI) and Leaf Area Index (LAI) derived from NDVI versus soil moisture relationships, calibrated against Landsat NDVI, and partitioned among species using dominance/crown-area information from a monitoring plot (50 x 100 m) within the Nordeste network.
- Model inputs: Species-specific structural and physiological parameters (Table 1). Includes cover fractions, heights, leaf widths, and physiological values (Vcmax, Jmax, etc.). Notes on naming changes and updated parameter estimates (e.g., photosynthetic parameters) are provided.
- Soil and stress parameters: Soil water retention parameters (theta_r, theta_s, alpha, n) fitted with Van Genuchten to Petrolina site data; switches for soil water stress models (JULES curvi linear, Sinclair, Dewar); locstress to select where stress is applied (stomatal, physiological, mesophyll, or all); q parameters for linear vs. non-linear stress representations depending on model (1.0 for linear as in JULES; Sinclair/Dewar settings may differ).

## Model configuration and options
- Plant water stress models: JULES, Sinclair, and Dewar options available; stress can be applied at various plant compartments (stomatal, physiological, mesophyll, or all).
- Model switches and parameters governing the Jacobs/JULES/Dewar/SOX family implementations are included (switchjacobs values 1–4 or 0 for Jarvis-Stewart approach).
- Input includes both structural and physiological parameters for each species, as well as hydraulic parameters and soil-plant-water status settings.

## Model outputs
- Four output files:
  - resistancesCaatinga.txt: Aerodynamic and within-canopy resistances, boundary layer resistances, surface resistances, and stomatal conductances for the eight species plus soil; timestamped by year, month, day, and decimal time.
  - variablesCaatinga.txt: Time-stamped state variables including air/canopy temperatures, vapor pressure deficits, CO2 concentrations at reference and within-canopy levels, leaf/cloud temperature values for species, and leaf/within-canopy vapor pressure differentials.
  - enbalCaatinga.txt: Energy-balance variables; total ecosystem net radiation, available energy, component-wise net radiation, available energy, soil heat flux, evapotranspiration, and sensible heat flux per component.
  - CO2Caatinga.txt: Plant- and canopy-level CO2-related outputs; soil water stress factors for the eight species, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.
- Outputs are provided for runs using the JULES Farquhar model with Sinclair-based plant water stress (Ψ at canopy level set to -1 MPa in reported results).

## Data sources and site-specific notes
- Micrometeorological and physiological data are specific to the Caatinga context and derived from field measurements and established literature (e.g., Verhoef & Allen 2000; VA2000; JULES/Clark et al. 2011; Sinclair/Dewar references).
- Soil and atmospheric parameters are tailored to local Caatinga conditions, with calibration against Landsat NDVI and field measurements.

## Researchers and collaborations
- Model development and runs performed by Anne Verhoef (University of Reading, UK).
- Contributors:
  - Raquel Carolina Miatto (plant physiology, Univ. of São Paulo, Brazil)
  - Luiza Helena Menezes Cosme (plant physiology, Univ. of São Paulo, Brazil)
  - Tomas Ferreira Domingues (plant physiology, Univ. of São Paulo, Brazil)
  - Magna Soelma Beserra de Moura (micrometeorology, EMBRAPA)
  - Magna Moonlight (plant species identification, Royal Botanic Garden Edinburgh)
  - Rodolfo Nobrega (plant structural indices and input collation, Imperial College)
  - Colin Prentice (modelling advice, Imperial College)
  - Anne Verhoef (modelling, University of Reading)

## References
- Verhoef A. and Allen, S.J. (2000). A SVAT scheme describing energy and CO2 fluxes for multi-component vegetation: calibration and test for a Sahelian savannah.
- Verhoef, A. and Egea, G. (2014). Modeling plant transpiration under limited soil water: comparison of different plant and soil hydraulic parameterizations.
- Miranda, R. de Q. et al. (2020). Realistic and simplified models of plant and leaf area indices for a seasonally dry tropical forest.
- Moonlight, P. et al. (2020). Expanding tropical forest monitoring into Dry Forests: the DRYFLOR protocol.
- Souza, R. et al. (2016). Vegetation response to rainfall seasonality and interannual variability in tropical dry forests.

## Contact
- For further information, contact Prof Anne Verhoef (a.verhoef@reading.ac.uk).