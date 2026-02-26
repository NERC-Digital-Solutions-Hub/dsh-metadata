# soilcoreno

- Overview
  - This dataset schema captures soil gas flux measurements with a biochar treatment, including sample metadata, measurement timing, cumulative gas flux, gas concentrations at start, environmental and soil properties, and biochar characteristics. It supports analysis of how biochar influences CO2, CH4, and N2O fluxes under varying soil moisture and temperature.

- Key data fields

  - Sample and treatment metadata
    - soilcoreno: Individual number for the soil sample/core
    - timepoint: Timepoint of measurements
    - biochartreatment: Whether the sample is un-amended or amended with biochar
    - dayfromstart: Days since start of measurements for this gas analysis
    - hourfromstart: Hours since start of measurements for this gas measurement

  - Gas flux (cumulative)
    - ugCO2-Cfluxg-1cumu: CO2 cumulative flux in ug CO2-C per g dry soil
    - ngCH4-Cfluxg-1cumu: CH4 cumulative flux in ng CH4-C per g dry soil
    - ngN2O-Nfluxg-1cumu: N2O cumulative flux in ng N2O-N per g dry soil
    - ugCO-Cfluxg-1cumu: CO cumulative flux in ug CO-C per g dry soil

  - Gas concentrations at start (t0)
    - CO2ppmt0: CO2 ppm in the static chamber headspace at t0
    - CH4ppmt0: CH4 ppm in the static chamber headspace at t0
    - N2Oppmt0: N2O ppm in the static chamber headspace at t0
    - COppmt0: CO ppm in the static chamber headspace at t0

  - Environmental and soil context
    - tempair: Temperature of the soil at the time of gas measurement
    - gravwatercontentproportion: Gravimetric water content as a proportion
    - chambaream2: Soil area within the static chamber
    - headvolm3: Volume of the static chamber headspace
    - datetimefirst: Date and time of the first soil gas flux measurement
    - drysoilweightg: Weight of the dry soil in the soil core (g)
    - biocharweight: Dry biochar weight added to the soil
    - biocharfraction: Proportion of dry soil weight that is biochar
    - bulkdensitygcm3: Soil bulk density (g/cm^3)
    - wfpsproportion: Water-filled pore space (gravimetric content × (bulk density / total porosity))
    - maximumwhc: Maximum water holding capacity of the soil
    - proportionofwhc: Proportion of WHC at the time of gas sampling

- Use cases and analysis notes
  - Ideal for examining correlations and causal effects of biochar on CO2, CH4, and N2O flux under different moisture and temperature conditions
  - Supports development of predictive models for gas flux responses to treatment and environmental variables
  - Use t0 concentrations to inform baseline conditions and interpret flux dynamics
  - Normalize flux by dry soil weight and account for chamber geometry (chambaream2, headvolm3)

- Data quality and integration considerations
  - Units are explicitly defined; ensure consistent units when merging with other datasets
  - Watch for missing values and consider unit conversions or re-derivations as needed
  - Maintain clear metadata and provenance (e.g., datetimefirst, timepoint) to support reproducibility