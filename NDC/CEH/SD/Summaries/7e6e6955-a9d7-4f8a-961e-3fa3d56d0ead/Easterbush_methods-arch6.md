# Carbon and nitrogen flux, meteorological, management, and soil data from a grazed, cut and fertilised temperate grassland in south east Scotland

## Overview
- A multi-domain dataset from Easter Bush, South East Scotland, covering carbon (C) and nitrogen (N) fluxes, meteorology, management, and soil properties.
- Includes daily and monthly measurements collected between 2002 and 2011, with some one-off soil data up to 2011.
- Aims to enable exploration of grassland C and N budgets, GPP/NPP, ecosystem respiration, and greenhouse gas fluxes (CH4, N2O, NOx) in the context of grazing, cutting, and fertilisation.

## Site description
- Location: Easter Bush, 10 km south of Edinburgh, UK.
- Layout: Two adjacent fields (South and North); data in this dataset come from the South field.
- Climate/soil: Mean annual rainfall ~947 mm; mean temperature ~9.0°C; imperfectly drained Macmerry soil (Eutric Cambisol), pH 5.1, clay 20–26%.
- Management: Permanent grassland (>20 years), dominated by Lolium perenne; main rooting zone ~0.31 m; groundwater ~0.85 m depth.

## Sampling regime and timespan
- Measurements span January 2002 to May 2011 (with various overlapping sub-sets for different variables).
- Data files capture daily, monthly, and one-off measurements across management, gas fluxes, leaching, soil properties, and met data.

## Data files Included and Content

- livestock_yield_fertiliser_daily.csv
  - Variables: Date, stocking density (LSU and head per m2), animal numbers (sheep, lambs, cows), YIELD DM/N/C offtake, mineral N fertiliser input, organic N and C fertiliser input.
  - Management details: Grazing by ewes/lambs, occasional heifers; silage cuts; fertiliser (NH4NO3/urea) applications; cattle slurry applications with sampling for N/C content.
  - Purpose: Link above-ground management with nutrient inputs and forage removal.

- N_C_leaching_flux_daily.csv
  - Variables: Date, DIC leaching flux, DOC leaching flux, DON leaching flux, NH4 leaching flux, NO3 leaching flux, modeled groundwater recharge, precipitation, actual evapotranspiration.
  - Setup: Suction cups at 30 cm depth (two positions: slope and hollow; only slope data included in the dataset).
  - Purpose: Quantify soil leaching losses of C and N and link to hydrology.

- N_C_leaching_conc_sampling_period.csv
  - Variables: Date, DIC/DOC leaching concentrations; TN/NH4/NO3 leaching concentrations (units: mg/L or mmol/L as indicated).
  - Purpose: Concentration data to accompany leaching flux measurements.

- Dry_N_conc_monthly.csv
  - Variables: Date, DELTA NH3 concentration, DELTA HNO3 concentration, DELTA NH4+ concentration, DELTA NO3- concentration.
  - Method: Derived from a DELTA denuder system located ~300 m from the main field.

- Flux_daily.csv
  - Variables (gas exchange related): Date, GPP (g C m-2 d-1), NPP (g C m-2 d-1), EcoResp (g C m-2 d-1), NEE (g C m-2 d-1), CH4 emissions (g C-CH4 m-2 d-1), N2O emissions (g N-N2O m-2 d-1) from chamber measurements and EC-derived values, NOx fluxes (g N-NO m-2 d-1).
  - CO2 exchange: Net Ecosystem Exchange measured by eddy covariance (EC) and closed-path IRGA; data quality control includes u* filtering, plausible CO2 range (330–450 ppm), and flux limits (-50 to 50 µmol m-2 s-1 for CO2; LE/H limits).
  - NPP/GPP partitioning: GPP and TER estimated with standard gap-filling and partitioning tool; NPP approximated as 50% of GPP after autotrophic respiration subtraction.

- soil_C_N_oneoff.csv
  - Variables: Soil mass, SOC (kg C m-2), SON (kg N m-2), by depth.
  - Sampling: May 2004 and May 2011; cores collected on a regular grid; soil fractions processed to <2 mm.

- metdata_daily.csv
  - Variables: Date, Precipitation (mm d-1), Temperature (daily mean, min, max), Soil temperature (daily mean), Volumetric water content (daily mean).
  - Measurements from depths 3.5, 7.5, 15, 30 cm; rainfall, air temperature, and soil moisture data included.

- References
  - Summary of methods and related studies for context and data processing, including flux measurement methods, N and C leaching, and GRV budgets.

## Data quality, units, and notes
- Blank values indicate no measurements on those days or data gaps.
- Some data are time-limited (e.g., NOx fluxes measured June 2009–August 2010; N2O fluxes with different methods across periods).
- NEE data were quality-checked and gap-filled using a standard online tool; NPP is derived, with GPP used as the primary driver.
- One-off soil C/N measurements and partial location data (slope only for leaching data) should be considered when aggregating or spatially analyzing.
- Units are provided in the data files metadata, including g C m-2 d-1 for fluxes, mg/L for concentrations, and various mass-based measures for soil carbon and nitrogen.

## How to use and potential data products
- Integrate management, meteorology, and flux data to build a comprehensive grassland C/N budget under grazing, cutting, and fertilisation.
- Create self-serve dashboards or pivotable summaries for:
  - Daily NEE, GPP, EcoResp, and NPP trends; CH4/N2O/NOx fluxes and their relation to fertiliser events and grazing pressure.
  - Leaching fluxes and concentrations (DIC, DOC, DON, NH4, NO3) and their association with rainfall and evapotranspiration.
  - Soil C and N stocks by depth and changes over May 2004 to May 2011.
  - Meteorological drivers of fluxes (soil moisture, temperature, precipitation).
- Combine with the dry deposition data to estimate total N inputs and budgets.
- Use the data to validate or calibrate ecosystem models requiring field-scale NEE, CH4, N2O, NOx, and leaching processes in grazed temperate grasslands.

## References and provenance
- Data are associated with multiple methodological references for NEE partitioning, gas flux measurement, leaching analyses, and dry deposition measurements, including work by Reichstein et al. (2005), Di Marco et al. (2004), Butterbach-Bahl et al. (1997), Kindler et al. (2011), and others listed in the document.