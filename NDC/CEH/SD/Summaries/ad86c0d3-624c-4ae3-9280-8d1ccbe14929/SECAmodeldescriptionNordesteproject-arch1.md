# Background

- Purpose and scope
  - Describes the structure of the output data from a preliminary SEcA (Shrubland Ecosystem Assessment) model, implemented in Fortran.
  - Focuses on Caatinga shrubland; currently no soil water balance or soil heat transfer model.
  - Main program reads inputs and calls subroutines to compute the resistance network, energy, water, and carbon fluxes, plus above-ground state variables.
  - Funded by Newton/NERC/FAPESP Nordeste project NE/N012488/1; contact Prof. Anne Verhoef for more information.

- SEcA model description and approach
  - An ecosystem model of energy and carbon balance fluxes for shrubland/multi-tree systems.
  - Uses a mechanistic A–G (assumed photosynthesis) model with various plant water-stress functions; builds on Verhoef & Allen (2000).
  - Latent heat flux (λE) is the sum over surface components (eight tree/shrub species + bare soil), each with fractional coverage ci.
  - Fluxes combine Penman–Monteith terms (PMi) with resistance terms (Yi).
  - Nine surface components represent Caatinga vegetation: eight species plus bare soil; coverages do not overlap.
  - Aerodynamic and surface resistances are computed using parameterizations from Huntingford et al. (1995) and VA2000; r*a, r*b, r*s, and r_l,l enter the calculations.
  - The model includes both within-canopy and canopy-to-atmosphere resistances; stomatal conductance and leaf-level photosynthesis feed into the stomatal resistance model (Jacobs et al. 1996) and depend on PAR, surface temperature, and leaf CO2 status.
  - The Y terms (Y_i) are derived from multi-component resistance relationships (VA2000 derivations) and lead to component- and total-ecosystem fluxes.
  - Net radiation for each component is computed from Rn,i; soil heat flux is assumed zero for vegetated components and 30% of Rn for bare soil.
  - Total CO2 flux (Pc) is the sum of component contributions minus soil/root respiration; canopy CO2 concentration is derived from atmospheric conditions and resistances.
  - The model solves equations iteratively (Eqns 1–17) with an embedded photosynthesis model (Farquhar; JULES variant used in some runs).
  - The Farquhar model is implemented; some runs use JULES with Sinclair or Dewar stress formulations.

- Data sources and data types (micrometeorology, plant physiology, and structure)
  - Micrometeorological data (3.1)
    - Collected at the Embrapa Tropical Semiarid Research Station, Pernambuco, Brazil (approx. 9°S, 40°W, 350 m a.s.l.).
    - Data from a 16 m tower and vicinity; variables include pressure, precipitation, soil moisture, incoming radiation, air temperature, humidity, wind speed/direction.
    - Model inputs provided for 2011 only.
  - Plant physiology (3.2)
    - Maximum Rubisco activity (Vcmax) and maximum electron transport (Jmax) obtained from A–Ci curves and temperature response curves.
    - Measurements used eight plant species, with PPFD saturating light tests and respiration measurements using LI-COR systems.
  - Plant structure (3.3)
    - Plant Area Index (PAI) and Leaf Area Index (LAI) derived daily from NDVI, calibrated with Landsat NDVI, and verified against Landsat data.
    - Species-level partitioning of PAI/LAI based on monitoring-plot data; dominance and crown area used to allocate totals to species inputs.
  - Model input parameters (3.4)
    - Table 1 lists species-specific structural (c, h, l) and physiological parameters (Vcmax, Jmax, etc.), plus albedo, emissivity, and other constants.
    - Structural data and parameters updated (June 2019; with updates to Oct 2020 for species names and values).
    - Inputs include hydraulic and soil water-stress parameters, with soil-water retention parameters (θr, θs, α, n) fitted to Van Genuchten curves from Petrolina site.
    - Model configuration controls available for plant water-stress models (JULES, Sinclair, Dewar), locations of stress application (locstress), and Jacob’s vs JULES/Dewar parameterization switches.

- Model inputs, configuration, and parameters
  - Species and structural parameters
    - Nine components: eight tree/shrub species plus bare soil; each with coverage ci, height hi, leaf length li, etc.
    - Example values (illustrative): ci values vary across species; hi ranges ~3.8–5.0 m; li ranges ~0.015–0.133 m.
  - Physiological parameters
    - Vcmax and Jmax values differ by species and are tied to chosen model configuration (e.g., ALL for Vcmax, JULES for Jmax in certain runs).
  - Environmental and stress parameters
    - Drought stress model choice (JULES, Sinclair, or Dewar) and the stress application locus (locstress).
    - qs, qb, qm values (default 1.0 for linear behavior in Sinclair/Dewar contexts).
    - Soil hydraulic parameters Ψr*, Ψ0, qs, qb, qm, etc., with soil water retention (θr, θs, α, n) specified.
  - Notes on updates and consistency
    - Parameter values were updated (2019–2020) with improved photosynthetic parameters for several species.
    - Some species names and inputs were revised in 2020; users should ensure consistency with the input file used.

- Outputs and file structure
  - Four output files produced by the model (with JULES Farquhar configuration and Sinclair stress on):
    - resistancesCaatinga.txt: time-stamped aerodynamic and surface resistances; columns include within-canopy and boundary-layer resistances for each species and soil, surface resistances, and stomatal conductances.
    - variablesCaatinga.txt: time-stamped state variables; includes air and within-canopy temperatures, vapor pressure deficits, CO2 concentrations at reference and canopy levels, leaf-level and canopy-level vapor deficits, and leaf CO2 concentrations for the eight species.
    - enbalCaatinga.txt: energy balance outputs; total and component-wise net radiation, available energy, sensible and latent heat fluxes, soil heat flux, and evapotranspiration by component (including bare soil).
    - Co2Caatinga.txt: carbon flux outputs; soil-water-stress factors per species, leaf- and canopy-level photosynthesis, soil respiration, and net ecosystem CO2 flux.
  - Data conventions
    - Time references: year, month, day in year, decimal time within day/year.
    - Component ordering follows the eight tree/shrub species in Table 1, followed by soil (bare soil) where applicable.

- Researchers and references
  - Key contributors: Anne Verhoef (lead), Raquel Carolina Miatto, Luiza Helena Menezes Cosme, Tomas Ferreira Domingues, Magna Soelma Beserra de Moura, Moonlight et al., Rodolfo Nobrega, Colin Prentice.
  - Primary references: Verhoef and Allen (2000); Verhoef and Egea (2014); Miranda et al. (2020); Moonlight et al. (2020); Souza et al. (2016); plus related JULES/ Jacobs model references.

- Limitations and context
  - Current implementation lacks a soil water balance and soil heat transfer model.
  - Micrometeorological and input data are centered on 2011; broader temporal applicability may require additional data.
  - Output data are designed to support analysis of energy, water, and CO2 fluxes in a multi-species Caatinga system and can inform model intercomparisons or parameter sensitivity studies.

- Practical implications for analysts
  - The data structure supports component-wise analysis of ET, GPP, NEE, and CO2 fluxes, enabling correlation studies and model-data comparisons at the species and ecosystem levels.
  - Detailed inputs (species-specific parameters, NDVI-based NDVI-to-PAI/LAI mapping, and soil hydraulics) provide opportunities to calibrate or test alternative configurations (e.g., switching stress models or adjusting hydraulic parameters).
  - Metadata and provenance are explicit (model version, configuration, and data sources) to support reproducibility and traceability.