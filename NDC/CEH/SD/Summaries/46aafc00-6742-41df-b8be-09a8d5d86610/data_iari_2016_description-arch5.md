# Experimental crop biomass and gas flux (methane, nitrous oxide, and ammonia) data from continuous and intermittently flooded rice fields, India, month-month 2016

## Overview and aim
- Describes data from a 2016 rice field experiment in Delhi, India, comparing continuous flooding (CF) vs intermittent flooding (IF) and five nitrogen fertiliser treatments.
- Focus on emissions (CH4, N2O, NH3), nitrogen use efficiency (NUE), yield, and related soil and climatic context.
- Aims to support understanding of environmental trade-offs between water management and greenhouse gas emissions, and to assess fertiliser strategies.

## Study design and site
- Location: Indian Agricultural Research Institute (IARI), New Delhi, India; site ID IARI_rice_kharif_2016; site name IARI_ND; altitude 228 m.
- Plot design: split-plot with two irrigation regimes (CF and IF) and five fertiliser treatments; 6 x 7 m plots; three replicates per treatment.
- Crop and management: Rice variety Pusa 44; transplanting 12–13 July 2016; harvest 3–5 October 2016; basal P, K, Zn applied; diverse nitrogen strategies including control (no N), FYM + neem-coated urea, leaf-colour-chart (LCC) based NCU, neem-coated urea (NCU) full N, and prilled urea (PRI).
- Data collection window: 12 July 2016 to 31 October 2016.

## Data collected
- Irrigation depths and water table dynamics (CF vs IF).
- Soil properties and texture (0–15 cm), bulk density, pH, soil carbon and nitrogen contents.
- Meteorological data (temperature, rainfall, relative humidity, evapotranspiration, wind).
- Gas fluxes: methane (CH4), nitrous oxide (N2O), ammonia (NH3) fluxes measured via static chambers.
- Ammonia volatilisation losses and associated measurements.
- Crop yield and biomass, including grain and straw, and nitrogen content (N concentration) in plant parts.
- Nitrogen use efficiency (NUE) calculated for total harvest and grain harvest, relative to controls within each irrigation regime.

## Data files and contents
- irrigation.csv: water depth measurements for CF and IF plots over time.
- weather.csv: daily meteorological data (dates, min/max temps, rainfall, humidity, sunshine, evapotranspiration, wind).
- site_properties.csv: plot-level properties (irrigation, treatment), soil pH, total N/C, bulk density, texture composition, and replicate details.
- NH3.csv: ammonia flux measurements (NH3_flux) by date, irrigation regime, treatment, and replicate.
- N2O_CH4.csv: nitrous oxide and methane flux measurements (N2O_flux, CH4_flux) by date, regime, treatment, and replicate.
- soil_NO3_NH4.csv: soil nitrate and ammonium concentrations (NO3-N, NH4-N) by date, regime, treatment, and replicate.
- crop_biomass_N.csv: biomass data (grain and straw) and nitrogen contents (grain_N_conc, straw_N_conc) per date, regime, and replicate.
- Additional methodological references and measurement details (e.g., chamber design, sampling times, and calculation formulas) are provided within the document.

## Methods and measurement details
- Gas flux calculation: F = (dC/dt) × (ρ × V) / A, where dC/dt is the rate of concentration change over time, ρ is air density, V is chamber volume, and A is ground area.
- CH4 measured with GC-FID; N2O measured with GC-ECD.
- NH3 volatilisation measured with static chambers and titration of boric acid solution; fluxes below 1 g NH3-N ha^-1 d^-1 treated as zero due to methodological limitations.
- Sampling protocol: 0, 30, and 60 minutes for CH4 and N2O; dedicated chambers for NH3 volatilisation with separate bases from GHG measurements.
- Experimental controls and repeatability: five fertiliser treatments across CF and IF with three replicates per treatment.

## Data governance, provenance, and quality considerations for Data Stewards
- Provenance: dataset produced by IARI and researchers including Cowan, Bhatia, Jain, Drewer, and colleagues; clear site management and start/end dates.
- Metadata scope: detailed site characteristics, irrigation regimes, fertiliser treatments, plot dimensions, sampling methodologies, and measurement instruments.
- Data quality notes:
  - Texture analysis NA for 2/3 replicates in site_properties.csv; missing texture data acknowledged.
  - NH3 flux values below a threshold are set to zero; reflect measurement limits.
  - Consistent units across files (e.g., N inputs in kg N ha^-1, NO3-N and NH4-N in mg kg^-1, fluxes in g N or g CH4/N2O per ha per day, etc.).
- Interoperability considerations:
  - Data structured by date, irrigation regime, treatment, and replicate; alignment across files by date, plot identifiers, and regime is essential for integration.
  - Multiple data streams (soil, gas fluxes, weather, biomass) require careful schema matching for FAIR reuse.
- Documentation needs for reuse:
  - Include dataset-wide metadata: licensing, data access terms, recommended citation, and any use restrictions.
  - Provide a data dictionary and a crosswalk table linking replicate IDs across files.
  - Clarify any units or measurement differences across instruments or sampling rounds.
  - Consider adding a data dictionary with standardized variable names to improve interoperability with other rice-gas datasets.

## Reuse considerations for Data Stewards
- Suitable for studies on irrigation management, greenhouse gas emissions, nitrogen use efficiency, and crop yield under contrasting flooding regimes.
- Potential uses include meta-analyses on rice paddy emissions, assessment of fertiliser strategies, and evaluation of water-use efficiency vs. environmental trade-offs.
- Users should account for the mixed design (CF vs IF with multiple N treatments) and ensure proper statistical alignment when combining CF/IF with fertilizer treatments.

## References and methodological sources
- Cowan et al., 2021: Experimental comparison of CF and IF flooding with implications for CH4, N2O, and NH3 emissions, NUE, and yield.
- Bhatia et al., various methodological works on gas flux measurement and ammonia volatilisation.
- Page et al., 1982; Bremner, 1965: Standard soil analysis methods referenced for nutrient measurements.
- Pathak et al., 2002, 2003: Related emissions studies in the Indo-Gangetic plains.