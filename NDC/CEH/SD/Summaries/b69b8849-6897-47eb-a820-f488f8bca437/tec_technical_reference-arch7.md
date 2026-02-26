# 21.5 Environmental rate modifiers

- Purpose
  - Describe functions that introduce environmental dependencies in biogeochemical kinetics, enabling spatially explicit GIS visualizations of decomposition, microbial activity, litter decay, and related processes.
  - Provide mechanisms by which water availability, temperature, pH, soil texture (clay/silt), and macrofauna influence carbon and nutrient turnover in the biogeochemical model.

- Soil water potential effects
  - Two separate functions regulate:
    - Microbial activity (f_SM.Microbe)
    - Belowground litter decomposition (f_SM.Litter)
  - Based on averaged soil water potential Ψs with empirically derived parameters (Ψopt1, Ψth1, α1, Ψopt2, Ψth2, α2) from Moyano et al. and Manzoni et al.
  - Near-saturation conditions are treated as non-limiting for oxygen.

- Macrofauna water response
  - Macrofauna activity is driven by an effective saturation metric Se (not simply water potential).
  - The function f_aew confines activity to a range around field capacity, decreasing to zero at very dry or very wet conditions.
  - Macrofaunal dynamics are also modulated by substrate palatability and other environmental factors (as described in related figures).

- pH effects
  - Soil pH controls on microbial and macrofaunal activity are captured by f_PH.
  - f_PH = 1 for pH between 4.5 and 7.5; it decreases linearly to 0 at pH 2 and pH 12, where biogeochemical activity is impaired.
  - pH is prescribed at the start of a simulation and remains constant (no pH evolution over time).

- POC to MOC transfer modification (f_d)
  - The fraction of decomposed POC allocated to MOC (1 − f_d) is modulated by external conditions.
  - f_d is corrected by clay/silt content (F_cla, F_sil) and existing soil MOC (C_moc_in) to reflect surface saturation and protection effects.
  - Higher C_moc and more reactive surfaces increase MOC accumulation up to a limit; clay/silt presence can enhance or inhibit this depending on saturation.

- Clay content modifiers
  - Clay content affects:
    - The half-saturation constants for soil organic matter decay (f_clay)
    - The fraction of dead microbes allocated to DOC (f_clay,2)
    - Macrofauna activity (f_clay,3)
  - Functional forms are given to reflect inhibition of decomposition in higher clay contents and to adjust microbial and macrofaunal dynamics accordingly.
  - These modifiers tie to observed relationships between mineral surfaces and protective effects on organic matter.

- Temperature dependencies
  - Temperature controls operate through:
    - f_Tmic: impacts microbial reaction kinetics (activation-energy–based scaling)
    - f_T3 and f_T4: modulate macrofaunal activity and litter decomposition, respectively
  - Functions use activation energy, reference temperatures, and ambient temperatures to adjust rates, reflecting faster reactions at higher temperatures.

- DOC accessibility and palatability
  - DOC accessibility to microbes is currently assumed to be maximal (f_ad = 1), with possible future implementations to tie to effective saturation.
  - Macrofauna food palatability depends on the soil organic matter C:N ratio (f_pal = 1.6 − 0.004 × CN_som), linking feeding efficiency to litter quality.

- GIS applicability and visualization
  - These environmental rate modifiers are designed to produce map-ready, spatially explicit variables that drive rate processes across the landscape.
  - Their parameterizations enable spatial comparisons under different climate, soil texture, and moisture regimes.
  - Figures referenced (e.g., Fig. 45–47) illustrate how these modifiers respond to changes in Se, clay content, temperature, and related factors.

- Additional notes
  - Oxygen limitation near saturation is neglected in the described formulations.
  - pH is treated as a non-evolving, location-specific input, shaping activity throughout the simulation.
  - The section integrates multiple interactions (moisture, texture, chemistry, and biology) to provide realistic, GIS-enabled representations of biogeochemical dynamics.