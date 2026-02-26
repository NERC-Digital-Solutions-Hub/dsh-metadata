# Experimental crop biomass and gas flux (methane, nitrous oxide, and ammonia) data from continuous and intermittently flooded rice fields, India, month-month 2016

## Data Description
- Data collected from a 2016 field experiment in Delhi rice paddies, including:
  - Irrigation depths
  - Soil properties
  - Meteorological conditions
  - Gas fluxes of ammonia (NH3), methane (CH4), and nitrous oxide (N2O)
  - Crop yield measurements
  - Soil nitrogen content

## Overview
- Intermittent flooding (IF) vs continuous flooding (CF) to reduce water use and methane emissions, with potential environmental tradeoffs.
- Study design: split-plot with four fertiliser types across two irrigation regimes, replicates included.
- Outputs of interest include emissions (CH4, N2O, NH3), nitrogen use efficiency (NUE), and yield.

## Site Information
- Site: IARI (Indian Agricultural Research Institute), New Delhi, India (IARI_ND)
- Season: kharif 2016 (monsoon)
- Coordinates: 28°40' N, 77°12' E; Altitude: 228 m
- Crop: Rice cultivar Pusa 44
- Soil: Silty clay loam (Typic Ustochrept); alluvial parent material
- Climate: Subtropical, semi-arid
- Experimental dates: transplanting around 12–13 July 2016; harvest 3–5 October 2016
- Previous cropping: rice-wheat in the past three years
- Site staff: Site manager Arti Bhatia; additional staff listed

## Crop Information
- Plot size: 6 x 7 m
- Transplanting: 30-day-old seedlings
- Nutrients: basal P (26 kg P ha-1), K (50 kg K ha-1), Zn (10 kg Zn ha-1) applied to all treatments
- Fertiliser treatments (N inputs 0 or 120 kg N ha-1):
  - CON: Control, no nitrogen
  - FYM: 50% N as farmyard manure + 50% N as neem coated urea (NCU)
  - LCC: Leaf Colour Chart-based NCU application
  - NCU: 100% N through neem coated urea
  - PRI: 100% N through prilled urea

## Experimental Design
- Design: split-plot with two irrigation regimes (CF and IF) and five fertiliser treatments, each with three replicates
- Irrigation: CF with 25 irrigations; IF with 15 irrigations
- Rice model: CF/IF regimes represent common regional practice; transplanting in mid-July; baselining with basin irrigation
- Measurements span irrigation depth, timing of N applications, and crop management events
- Details on fertilizer practices include timing and N input per treatment

## Plant Sampling and Yield Estimation
- Harvest: vegetation samples collected to estimate biomass; yields measured from 1 m2 per plot in triplicate
- Processing: grains separated, dried; moisture measured; samples dried at 65°C for 48 h
- Nitrogen analysis: total N content in plant tissue using Kjeldahl method; separate calculations for grain and stem/leaf
- Nitrogen Use Efficiency (NUE): calculated relative to control plots under the same irrigation method
  - Harvest NUE: total plant harvest
  - Grain NUE: grain harvest
- NUE reflects additional yield effects due to fertiliser application above controls

## Gas Sampling and Analysis (CH4 and N2O)
- Method: static chamber technique using transparent chambers (50 cm x 30 cm x 100 cm)
- Chamber setup: soil base frames inserted to 10 cm depth; airtight through water fill
- Sampling: gas samples drawn at 0, 30, and 60 minutes
- Analysis:
  - CH4: gas chromatography with flame ionization detector (FID)
  - N2O: gas chromatography with electron capture detector (ECD)
- Calibration: standards for CH4 and N2O included
- Flux calculation: F = (dC/dt) × (ρ × V) / A
  - F: soil flux (nmol m-2 s-1)
  - dC/dt: rate of concentration change (nmol mol-1 s-1)
  - ρ: air density (mol m-3)
  - V: chamber volume (m3)
  - A: ground area enclosed by chamber (m2)

## Ammonia Volatilisation Measurement
- Method: static chambers (18 cm x 18 cm x 30 cm) placed between rice rows for 1 hour
- NH3 captured in boric acid solution; titration with 0.001 N sulfuric acid used to determine NH3-N
- Calculation: N = [( vol of NH3-N captured in boric acid ) × 28.014] / A
  - 28.014 accounts for NH3-N molar mass and stoichiometry
  - A is the soil area enclosed by the chamber
- Data handling: fluxes below 1 g NH3-N ha-1 d-1 discounted to zero due to methodological limitations

## Data Files Included
- irrigation.csv: water depth measurements for CF and IF plots
- weather.csv: daily meteorological data (temperature, rainfall, RH, sunshine, evapotranspiration, wind)
- site_properties.csv: management and soil properties (pH, soil N/C, bulk density, texture, etc.)
- NH3.csv: NH3 flux measurements by treatment, replicate, and date
- N2O_CH4.csv: N2O and CH4 flux measurements by treatment, replicate, and date
- soil_NO3_NH4.csv: soil nitrate and ammonium concentrations by date and plot
- crop_biomass_N.csv: biomass data (grain and straw) with N content
- All files contain metadata describing units and measurement contexts

## References
- Bhatia et al. (2005, 2016) on greenhouse gas emissions and management in rice-wheat systems
- Bremner (1965) methods for inorganic nitrogen analyses
- Cowan et al. (2021) experimental comparison of CF and IF regarding emissions and NUE
- Page et al. (1982) Methods of soil analysis
- Pathak et al. (2002, 2003) emissions studies in Indo-Gangetic plains
- Additional methodological references for gas flux calculations and sampling techniques