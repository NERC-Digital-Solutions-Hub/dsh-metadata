# Experimental crop biomass and gas flux (methane, nitrous oxide, and ammonia) data from continuous and intermittently flooded rice fields, India, month-month 2016

- Provides a multi-variable dataset from a 2016 rice field experiment in Delhi, India, comparing continuous flooding (CF) and intermittent flooding (IF) with five nitrogen fertiliser treatments.
- Key measured outcomes include greenhouse gas fluxes (CH4, N2O, NH3), crop yield and nitrogen use efficiency (NUE), soil nitrogen content, and a range of environmental and agronomic variables.
- Data are organized into multiple files specifying irrigation, weather, site properties, gas fluxes, soil nitrogen, and crop biomass, enabling cross-variable analyses and data integration.

## Experimental scope and site

- Location: Indian Agricultural Research Institute (IARI), New Delhi, India; Indo-Gangetic alluvial tract, 28°40' N, 77°12' E; altitude 228 m.
- Soil: Silty clay loam (Typic Ustochrept), bulk density 1.38 g cm-3, soil pH 8.01, organic carbon 4.2 g kg-1, total N 0.24 g kg-1.
- Crop and timing: Rice cultivar Pusa 44; transplanted 12–13 July 2016; harvest early October 2016.
- Experimental design: Split-plot with two irrigation regimes (CF and IF) and five nitrogen fertiliser treatments, each with three replicates; plot size 6 x 7 m.
- Climate context: Subtropical/semi-arid; mean July–October temperatures 35°C/18°C; rainfall and temperature data collected near the site.

## Treatments

- Irrigation regimes: Continuous flooding (CF) vs Intermittent flooding (IF); IF managed by soil surface cracking indicators.
- Fertiliser treatments (five total):
  - CON: Control, 0 N
  - FYM: 50% N from farmyard manure + 50% N from neem-coated urea (NCU)
  - LCC: Leaf Colour Chart-based NCU application
  - NCU: 100% N from neem-coated urea
  - PRI: 100% N from prilled urea
- Nitrogen input level: 120 kg N ha-1 for all fertiliser treatments except CON (0 N)
- Basal nutrients: All treatments received 26 kg P ha-1, 50 kg K ha-1, and 10 kg Zn ha-1
- Experimental layout: Two irrigation treatments crossed with five fertiliser treatments, each with three replicates

## Data collected and content

- Gas flux measurements:
  - CH4 and N2O fluxes via static chamber method with GC analysis (FID for CH4, ECD for N2O)
  - NH3 volatilisation fluxes measured with dedicated static chambers and titration of boric acid solution
- Soil and crop measurements:
  - Soil NO3-N and NH4-N contents
  - Crop biomass (grain and straw) and nitrogen content; grain and whole-plant NUE calculations
  - Grain weight, biomass dry weights, and N concentrations for yield/NUE estimation
- Meteorological and environmental data:
  - Weather data: daily min/max temperature, rainfall, relative humidity, sunshine, evapotranspiration, wind speed
  - Water management: irrigation depth and water-table heights for CF and IF plots
- Site properties:
  - Soil pH, total N and C, bulk density, and texture components (sand, silt, clay)
  - Replicate identifiers and irrigation regime per plot
- Data files (descriptions):
  - irrigation.csv: Water depth measurements and water-table heights for CF and IF plots
  - weather.csv: Daily weather and environmental variables (temp, rainfall, RH, sunshine, ET, wind)
  - site_properties.csv: Irrigation regime, fertiliser treatment, replicate, pH, total N and C, bulk density, texture
  - NH3.csv: NH3 flux data with treatment, replicate, and date
  - N2O_CH4.csv: N2O and CH4 flux data with treatment, replicate, and date
  - soil_NO3_NH4.csv: Soil nitrate and ammonium data (NO3-N, NH4-N) by date, treatment, replicate
  - crop_biomass_N.csv: Grain and straw biomass (dry weight) with grain/straw nitrogen concentrations
- Data quality notes:
  - NH3 fluxes below 1 g NH3-N ha-1 d-1 are treated as zero flux due to methodological limits
  - Some site-property texture analyses described as NA for most replicates (limited soil texture data)

## Measurement methods and data processing

- Gas flux calculation:
  - Based on concentration changes over time (0, 30, 60 minutes) within static chambers
  - CH4 flux: CH4-C per area per time; N2O flux: N2O-N per area per time; calculations follow standard gas flux equations
  - Measurements calibrated with gas standards (CH4: 2–5 ppm; N2O: 500–1000 ppb)
- NH3 volatilisation:
  - Chamber-based sampling; NH3 trapped in boric acid, titrated to determine NH3-N mass
- NUE calculations:
  - Harvest NUE: total plant N above control baseline under the same irrigation regime
  - Grain NUE: grain-specific N above control baseline under the same irrigation regime
- Plant sampling:
  - Biomass harvested from one square meter per plot, dried and weighed
  - Nitrogen content determined by Kjeldahl analysis
- Data integration:
  - Datasets designed to support cross-referencing across irrigation regime, fertiliser treatment, replicate, and time
  - Potential to merge with referenced literature for comparative analyses on emissions, NUE, and yield responses

## Data quality, limitations, and considerations

- Patchy soil texture data: texture analyses performed on a limited number of replicates, with NA values for others
- NH3 data: zero-flux designation applied when measurements fall below detection threshold
- Experimental scope: field-scale experiment with replication (three replicates) and cross-treatment mixing; generalizability may be bounded by site-specific conditions
- Documentation depth: detailed methodological notes, units, and file descriptions aid reproducibility and secondary analyses

## Potential data products and analysis opportunities

- Time-series dashboards of CH4, N2O, and NH3 fluxes by irrigation regime and fertiliser treatment
- Comparative analysis of IF vs CF impacts on GHG emissions and NUE across treatments
- Relationship analyses between soil NO3-N/NH4-N and gas fluxes, moderated by irrigation and fertilizer type
- Yield-NUE trade-off assessments under different irrigation and nutrient management strategies
- Meta-analyses linking these data with regional rice-wheat systems and gas emission studies

## References and data provenance

- Cowan, N., Bhatia, A., Drewer, J., et al. (2021). Experimental comparison of continuous and intermittent flooding of rice in relation to methane, nitrous oxide and ammonia emissions and the implications for nitrogen use efficiency and yield. Agriculture, Ecosystems & Environment. https://doi.org/10.1016/j.agee.2021.107571
- Bhatia, A., Pathak, H., Jain, N., Singh, P.K., et al. (2005). Global warming potential of manure amended soils under rice-wheat system in the Indo-Gangetic Plains. Atmospheric Environment, 39, 69-76. https://doi.org/10.1016/j.atmosenv.2005.07.052
- Bremner, J.M. (1965). Inorganic forms of nitrogen. In Black, C.A. (ed.), Methods of Soil Analysis, Part 2. American Society of Agronomy.
- Page, A.L., Miller, R.H., Keeney, D.R. (eds.) (1982). Methods of Soil Analysis; 2. Chemical and microbiological properties. American Society of Agronomy.
- Pathak, H., Bhatia, A., Prasad, S., Jain, M.C., et al. (2002, 2003). Emissions of N2O and CH4 in rice-wheat systems, Indo-Gangetic Plains. Environmental Monitoring and Assessment; Agriculture, Ecosystems & Environment.