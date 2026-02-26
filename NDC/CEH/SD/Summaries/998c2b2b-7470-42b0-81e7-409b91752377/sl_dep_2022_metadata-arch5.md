# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2022)

- Purpose and scope
  - Study of how high ambient ammonia (NH3) affects forest vegetation, bryophytes, lichens, and soil at Queensberry Estate, central Sri Lanka (site coordinates 6.9693° N, 80.5911° E; altitude 1645 m).
  - NH3 enhancement system operated in 2022, controlled by wind direction (5–75° and 185–255°) and threshold wind speeds (0.3–10 m s⁻¹).
  - NH3 concentrations measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses from April to December 2022.
  - Bi-directional deposition model used to estimate deposition and emission fluxes to soil, understory vegetation, tree trunks, and tree canopy.

- Measurement and data collection details
  - Data collection height: 1.5 m; measurements taken along monitoring quadrats with wind-controlled NH3 release.
  - Deployment period and cadence: monthly NH3 concentration analyses from April–December 2022.
  - Instrumentation: ALPHA samplers for NH3 concentration measurement.
  - Site specifics: tropical sub-montane forest at Queensberry Estate, with model-based deposition estimates for multiple surfaces.

- Modeling and flux estimation
  - Core model: four-layer canopy compensation point model; bi-directional NH3 exchange accounting for stomatal compensation point and soil re-emission potential.
  - Deposition flux formulation: Fχ(z) = χa / Rt, where Rt is the total resistance to dry deposition; deposition velocity Vd = 1/Rt.
  - Surface-specific resistances and parameterizations:
    - Soil surface: quasi-laminar boundary layer resistance (Rbg) with specific parameterization.
    - Tree trunks: quasi-laminar boundary layer resistance (Rb(tt)); dependent on friction velocity, Reynolds number, and related constants.
    - Understory vegetation: stomatal deposition flux characterized by stomatal resistance (Rs) with LAI dependency.
    - Canopy and cuticular deposition: multiple parameterizations for cuticular deposition flux (Rw) with LAI dependence and seasonal (day/night) adaptations.
  - Cuticular deposition parameterizations (Rw) explored:
    1) Rw(min) with exponential scaling and LAI⁰·⁵ dependence (Massad et al., 2010).
    2) Rw(day) and Rw(night) using ambient NH3 and LAI⁰·⁵ with day/night conditions (Jones et al., 2007).
    3) DEPAC-based module scaling with Haarweg LAI (DEPAC; van Zanten et al., 2010).
    4) Rw = (5000 / Cd) / LAI⁰·⁵ (Stutton et al., 1998) with Cd representing capacitance.
  - Additional parameterizations incorporate LAI, relative humidity, temperature, solar radiation, and other environmental factors.
  - Output: deposition flux to soil (Fg), understory (Fs_us), tree trunks (Ftt), tree canopy (Fs_tc), and corresponding cuticular deposition fluxes (Fw_us_*, Fw_tc_*, Fd_us_*, Fd_tc_*), plus emission indicators when negative.

- Data structure and metadata
  - Dataset composition: 144 measurements across 13 NH3-related parameters.
  - File format: CSV with clearly defined columns:
    - Distance (m): distance from NH3 source; negative values indicate southwest, positive indicate northeast.
    - Month: month-year of observation.
    - NH3_conc (µg m⁻³): monthly average NH3 concentration at 1.5 m.
    - Deposition and flux components: Fg, Fs_us, Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones, Fd_us, Ftt, Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc (all in kg ha⁻¹; negative values indicate emission).
  - Descriptions and units provided for each column to support reuse and interoperability.
  - Access and provenance notes: complete methodological details and findings discussed in Deshpande et al. (2024); dataset is a component of a larger approach to estimate ammonia deposition across vegetation and substrates.

- Quality control and data curation
  - Visual data checks performed; obvious instrument- or logger-related errors removed.
  - Regular missing values attributed to scheduled power cuts; additional gaps during sensor replacement.
  - Data structure and documentation prepared to support dataset discoverability and reuse; references to underlying methodology for transparency.

- Data governance, sharing, and provenance (relevant to Data Stewards)
  - Data provenance: explicit site description, sampling methodology, and wind-direction gating ensure traceability of data generation.
  - Standards and metadata: structured CSV with explicit units, definitions, and parameter descriptions to facilitate discovery, understanding, and interoperability.
  - Sharing and cataloging: dataset intended for upload to relevant data portals and catalogue holdings; methodology and full analysis are published in Deshpande et al. (2024).
  - Scope for reuse: supports cross-site comparisons (e.g., with Scotland) and examination of bi-directional NH3 deposition processes across forest components.
  - Funding acknowledgement: UKRI GCRF South Asian Nitrogen Hub.

- Context and references
  - Core methodological references spanning deposition models, resistances, and parameterizations (Massad et al., 2010; Jones et al., 2007; Sutton et al., 1998; van Zanten et al., 2010; Chamberlain et al., 1968; Chamberlain et al., 1984; Nemitz et al., 2000; Wesely & Hicks, 1977; Owen & Thomson, 1963; Schuepp, 1977; Stutton et al., 1998).
  - Related study: Deshpande AG et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments (Atmos Environ, 2024).