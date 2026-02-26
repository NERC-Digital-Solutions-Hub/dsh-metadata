# Vertical profile data of light transmission in Atlantic forests along a disturbance gradient

- Purpose and context
  - Provides vertical profiles of light transmission (PAR) across a disturbance gradient in montane humid Atlantic forest, Brazil.
  - Associated with the paper Tropical forest light regimes in a human-modified landscape, Fauset et al., Ecosphere.
  - Enables assessment of environmental health and forest structure effects on light regimes across intact, logged, secondary, and fragmented forests.

- Study area and plots
  - Location: Núcleo Santa Virginia, Serra do Mar State Park, near São Luís do Paraitinga, São Paulo, Brazil.
  - Environment: montane moist dense forest with high rainfall (~2300 mm/yr), cool temperatures (~17°C), frequent fog; surrounding inland areas are pastoral with patches of private forest.
  - Plots and disturbance gradient
    - Continuous forest plots: intact-K, intact-M, logged (pre-1977 selective logging), and secondary (mid-stage, post-charcoal clear-cut).
    - Fragment plots: fragment-C and fragment-L, each with edge (≈30 m from edge) and interior (≈100 m) transects; adjacent to cattle pasture.
  - Plot sampling scale: 1-ha permanent plots within the park and newly established plots in fragments outside the reserve; multiple sampling points per plot to cover spatial variation.

- Light profile measurements
  - Instrumentation: 19 PAR sensors built with GaAsP photodiodes; each sensor calibrated against a LI-COR 190 quantum sensor.
  - Reference: one open-sky sensor connected to a data logger for a canopy/open-sky baseline.
  - Deployment: sensors suspended from rope over tree branches; measurements every 30 seconds, averaged per minute.
  - Height and geometry: 1 m interval vertical profile, sensor-supported on a plastic bar/ring system; maximum sampling height 18 m; in one case, a canopy tower used.
  - Sampling design: within each plot, 10 sampling locations; subplots of 20 x 20 m (10 x 10 m for fragments); each point sampled for 1 hour to 3 days under diffuse light conditions.
  - Tree measurements: height of the sampled tree tops measured with laser, hypsometer, or visual estimation.

- Data processing and derivation
  - Diffuse condition selection: manual identification of periods free from sunflecks and sun angle effects to compute % transmission.
  - Profile construction: for each point, compute mean % transmission relative to open-sky reference across diffuse periods.
  - Plot-level means: average % transmission at each 1 m height across sampling points; for fragments, combine edge and interior data.
  - Handling missing portions:
    - If the top of the tree is below the top sensor, interpolate to 100% transmission at the canopy top.
    - If the bottom sensor is above 1 m, assume transmission below bottom sensor equals that value.
    - For heights above the top sensor, assume 100% transmission.
  - Depth-based profiles: also derive profiles as depth from canopy top (0 m at canopy top) up to the mean sample tree height; extrapolate if the sampled tree is shorter than plot mean height.
  - Outputs include both height-based and depth-based mean profiles with associated variability.

- Data files and metadata
  - Profiles.csv: means of percent transmission (% transmission) at different heights; includes
    - height (m above ground), mean_transmission, point (plot identifier), interpol/extrap flags, sd (standard deviation), top flag, depth (below canopy top)
  - MeanHeightProfiles.csv: plot-level mean profiles by height above ground
    - Height (m), Mean_Transmission, SD_Transmission, Plot
  - MeanDepthProfiles.csv: plot-level mean profiles by depth below canopy
    - Depth (m), Mean_Transmission, SD_Transmission, Plot
  - ProfilesMetadata.csv: per-profile metadata
    - Plot name, Plot Code, Latitude/Longitude, Plot Area (ha), Fragment area (ha), ProfileID (with edge/interior codes for fragments), Dates of light profile collection, Estimated sample tree height (m)

- Relevance for monitoring and data stewardship
  - Demonstrates a standardized approach to capturing and processing forest light environments across a disturbance gradient.
  - Provides calibrated, georeferenced, and richly described datasets suitable for integration with environmental monitoring portals and cross-dataset analyses.
  - Encapsulates data provenance, measurement protocols, and quality-control steps to support reproducibility and secondary analyses in environmental health and policy assessment.