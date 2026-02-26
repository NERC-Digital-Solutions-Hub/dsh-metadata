# Experimental crop biomass and gas flux (methane, nitrous oxide, and ammonia) data from continuous and intermittently flooded rice fields, India, month-month 2016

- Purpose and scope
  - Describes data from a 2016 field experiment in Delhi comparing continuous flooding (CF) and intermittent flooding (IF) in rice cultivation.
  - Investigates environmental tradeoffs of IF vs CF with respect to methane (CH4), nitrous oxide (N2O), and ammonia (NH3) emissions, nitrogen use efficiency (NUE), and yield.
  - Includes related agronomic and soil data to enable correlation analyses and predictive modeling.

- Study design and treatments
  - Location: Indian Agricultural Research Institute (IARI), New Delhi, India; silty clay loam soil, Typic Ustochrept.
  - Crop: Rice (cv. Pusa 44); transplanting on 12–13 July 2016; harvest 3–5 October 2016.
  - Plot design: split-plot with three replicates; irrigation regime as main plot (CF vs IF) and five nitrogen (N) fertilizer treatments as subplots.
  - Plot size: 6 x 7 m.
  - Irrigation: CF with 25 irrigations; IF with 15 irrigations; IF irrigation triggered by soil surface cracking.
  - Fertilizer treatments (Table 2): five treatments including a no-N control (CON) and four N-containing strategies:
    - FYM: 50% N from farmyard manure + 50% N from neem-coated urea (NCU), total N 120 kg N ha-1.
    - LCC: Leaf Colour Chart–based NCU application (total N 120 kg N ha-1).
    - NCU: 100% N via neem-coated urea (120 kg N ha-1).
    - PRI: 100% N via prilled urea (120 kg N ha-1).
  - Additional basal nutrients: P, K, Zn applied to all treatments.

- Site and crop details
  - Site information: IARI_ND, altitude 228 m, coordinates 28°40' N, 77°12' E.
  - Soil and climate: Typic Ustochrept; pH 8.01, organic carbon 4.2 g kg-1, total N 0.24 g kg-1, bulk density 1.38 g cm-3.
  - Agronomic management: nursery-grown seedlings, 30 days old; transplantation spacing 20 x 15 cm; baseload P, K, Zn applied.

- Data collected
  - Irrigation depths and water table data (irrigation.csv).
  - Soil properties and site characteristics (site_properties.csv).
  - Meteorological data (weather.csv) including daily min/max temperatures, rainfall, humidity, sunshine, evapotranspiration, wind speed.
  - Gas flux measurements:
    - CH4 and N2O fluxes using static chambers and GC detectors (N2O: ECD; CH4: FID) (N2O_CH4.csv).
    - NH3 fluxes using static chambers and boric acid titration (NH3.csv).
  - Ammonia volatilization losses (NH3 flux methodology and calculations).
  - Soil inorganic nitrogen (NO3-N, NH4-N) data (soil_NO3_NH4.csv).
  - Plant biomass and nitrogen content (crop_biomass_N.csv) with grain and straw components.
  - Rice biomass and nitrogen content data (grain and straw, with NUE calculations) (embedded in crop_biomass_N.csv).

- Measurements and methods
  - Gas sampling: static chambers placed over plots; samples collected at 0, 30, and 60 minutes for CH4 and N2O; fluxes calculated from concentration change over time.
  - CH4 analysis: gas chromatography with flame ionization detector.
  - N2O analysis: GC with electron capture detector.
  - NH3 volatilization: chamber-based collection with boric acid trapping and titration; fluxes below 1 g NH3-N ha-1 d-1 treated as zero due to methodological limits.
  - NUE calculations: based on total plant harvest and grain harvest, subtracting corresponding control values for the same irrigation regime.

- Data organization and files (CSV)
  - irrigation.csv: water depth measurements for CF and IF plots.
  - weather.csv: daily meteorological data (Tmin, Tmax, Tmean, rainfall, humidity, sunshine, ET, wind).
  - site_properties.csv: soil texture, pH, bulk density, SOC, total N, irrigation method, treatment, replication, and other soil properties.
  - NH3.csv: NH3 flux measurements (NH3_Flux) with treatment, replicate, and date.
  - N2O_CH4.csv: N2O and CH4 flux measurements with date, treatment, replicate.
  - soil_NO3_NH4.csv: nitrate and ammonium contents in soil (NO3-N, NH4-N).
  - crop_biomass_N.csv: biomass data (grain and straw, dry weight) and nitrogen content (grain and straw) with NUE calculations.

- Data quality and notes
  - NH3 fluxes below detectable thresholds are set to zero in the dataset.
  - Field data are from a single experimental site and season (Delhi, 2016), which may limit generalizability but enables detailed, site-specific analysis.
  - Data are designed to support analyses of how irrigation regime and fertilizer strategy influence CH4, N2O, and NH3 emissions, NUE, and yield, with accompanying soil and weather context.

- References and provenance
  - Core study: Cowan et al., 2021, Agriculture, Ecosystems & Environment.
  - GHG methodology references and soil analysis standards cited in the dataset documentation.