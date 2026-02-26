# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2022)

## Purpose and scope
- Ammonia (NH3) enhancement experiment conducted in a tropical sub-montane forest at Queensberry Estate, Sri Lanka to study NH3 effects on forest vegetation, bryophytes, lichens, and soil.
- NH3 release is wind-controlled, activated when winds come from the monitoring quadrats at specified directions and speeds.
- NH3 concentrations measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analyses performed monthly from April to December 2022.
- Deposition (and potential emission) estimated with a four-layer canopy compensation point model, using a bi-directional resistance framework accounting for stomatal exchange and soil re-emission.

## Data collection and deposition modeling
- Measurements: ambient NH3 concentrations and deposition fluxes partitioned across soil surface, understory vegetation, tree trunks, and tree canopy.
- Deposition flux formulations use resistance concepts (e.g., boundary layer, trunk, stomatal, cuticular pathways) and environmental factors (LAI, solar radiation, temperature, humidity).
- Key model components:
  - Fχ(z) = χa / Rt (deposition flux at height z)
  - Rbg, Rb(tt), Rs, Rw parameterizations (with multiple approaches for cuticular deposition and LAI dependence)
  - Stomatal deposition fluxes dependent on stomatal resistance Rs and LAI
  - DEPAC and other parameterizations used for comparative analyses of cuticular deposition
- Complete methodology and equations are provided in the referenced Deshpande et al. (2024).

## Data structure and quality control
- Dataset comprises 144 measurements across 13 parameters.
- Data provided in a CSV with columns including:
  - Distance (m) from NH3 enhancement source
  - Month (year)
  - NH3_conc (µg m^-3)
  - Deposition flux components: Fg (soil), Fs_us (understory stomatal), Fw_us_* (understory cuticular; multiple parameterizations), Fd_us (cuticular from Sutton et al.)
  - Deposition flux components for trees: Ftt (tree trunks), Fs_tc (tree canopy stomatal), Fw_tc_* (tree canopy cuticular; multiple parameterizations), Fd_tc (tree canopy cuticular)
- Negative flux values indicate emission rather than deposition.
- Quality control: visual checks; removal of obvious instrument/ logger issues; regular gaps attributed to scheduled power cuts and sensor replacements.

## Data usage and accessibility
- Outputs typically delivered as clear formats (reports, maps, charts) to support environmental health assessment and policy performance monitoring over time.
- Datasets are stored and uploaded to appropriate portals to enable standardized access and reuse.
- The study and its methodology contribute to cross-site comparisons, notably with parallel work in Scotland (Deshpande et al., 2024), supporting broader nitrogen deposition assessments.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- References cited for methodology and context include Chamberlain (1968, 1984), Fowler (1978), Jones et al. (2007), Massad et al. (2010), Nemitz et al. (2000), Owen & Thomson (1963), Schuepp (1977), Sutton et al. (1998), van Zanten et al. (2010), Wesely & Hicks (1977), and Deshpande et al. (2024).