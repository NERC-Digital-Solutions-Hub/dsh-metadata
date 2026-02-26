# Clyde Estuary greenhouse gas and physiochemical water properties: Measurements across the tidal cycles - 2020-2022

- Overview
  - Longitudinal study of greenhouse gas (GHG) concentrations and physio-chemical water properties in the Clyde estuary, Scotland.
  - Eight surveys conducted during 2021–2022 under varying tidal, river flow, and seasonal conditions.
  - Measurements taken along a transect from near the tidal weir (L1) to offshore near Dunbarton (L10) at ten locations (L1–L10), at the surface and near-bed.
  - Aims to understand GHG sources/sinks, controls on production/transport/consumption, and the impact of stratification, salinity, flow, sediments, and pollutant inputs (e.g., urban wastewater).

- Spatial and Temporal Coverage
  - Ten sampling locations along the Clyde estuary (L1–L10), spanning from inland to offshore.
  - Distances from the tidal weir increase seawards; L5 is near the main dredged channel, with other sites positioned to avoid dredged areas.
  - Eight surveys carried out between Sep 2021 and May 2022; sampling started at high tide inland and proceeded seawards with the ebb.
  - Some data gaps due to rough weather (e.g., not collected for CET7 at L5–L10; CET6/CET8 at L9–L10; CET3 at L10).

- Sampling Design and Locations
  - Transect design to capture effects of location, salinity, river flow, and stratification on GHGs and water quality.
  - Depths: up to 12 m at offshore sites; landward sites typically < 6 m.
  - Specific notes for key sites: L3–L4 gap where the estuary is restricted; L5 near Shieldhall UWWTP outflow; L7–L8 downriver of White/Black Cart inputs; L10 offshore from River Leven.
  - Supplementary location details provided in Appendix 1 of the dataset.

- Data Collected and Parameters
  - GHGs: concentrations of CO2, CH4, and N2O; gas partial pressures via headspace equilibration; CH4, CO2, and N2O saturations and related metrics (e.g., CH4-Sat, CO2-Sat, N2O-Sat).
  - Dissolved and headspace gas data: CH4, CO2, N2O in water; pCO2air, pN2Oair, CH4/C02 related conversions to ppmv via gas laws.
  - Physico-chemical water properties: surface and near-bed measurements of conductivity (Cond), temperature (Temp), pH, dissolved oxygen (DO) and DO saturation (DO%), turbidity.
  - Carbon and nitrogen pools: total dissolved nitrogen (TDN), total dissolved carbon (TDC), dissolved organic carbon (DOC), dissolved inorganic carbon (DIC); nitrite-N (NO2-), nitrate-N (NO3-), ammonia-N (NH4+), and total phosphorus (TP) after digestion.
  - Additional metrics: SUVA254 (absorbance at 254 nm) as an indicator of DOC aromaticity; absorbance-based indicators linked to humic content and anthropogenic impact.
  - Unit and parameter details are defined in Table 2 of the dataset (e.g., Latitude/Longitude to 6 decimals, depth, temperature in °C, pH, NTU for turbidity, mg/L for nutrient species, μmol/L for gas concentrations, etc.).

- Methods and Calculations
  - Headspace gas sampling: three 200 mL syringes per location, equilibrated with 100 mL water and 100 mL ambient air, then transferred to sealed vials for GC analysis.
  - Analytical methods:
    - GHGs: Agilent GC (7890B) with headspace auto-sampler for CO2, CH4, N2O.
    - Turbidity: turbidity meter (NTU).
    - Water chemistry: filtration for sub-samples; TOC analyzer for TDN, TDC, DOC; UV/Vis for SUVA254; SEAL AQ2 for nitrite, nitrate, ammonia; phosphorous analysis after digestion.
  - Calculations:
    - Gas concentrations converted from headspace equilibrations to aqueous concentrations using mass-balance equations and Henry’s law-based temperature corrections.
    - Concentrations converted to units of ppmv using the Ideal Gas Law (ppmv = μmol/L × R × T).
    - DIC derived from TDC − DOC; data include gas-phase partial pressures and water-phase concentrations for CO2, CH4, and N2O.
  - Data processing and analysis: primary analysis conducted by Alison Brown as part of the IAPETUS 2 DTP NERC PhD project; supporting contributions from collaborators.

- Data Format, Units, and Accessibility
  - Data organized in a CSV format with a detailed column structure (Table 2), including Survey_Name, Location_Code, Depth (Surface/Near-bed), Sample_Code, Latitude, Longitude, Distance from tidal weir, Date, Time (GMT), Water_depth, Sample_depth, Cond, Temp, pH, DO, DO%, Turbidity, DOC, TDC, DIC, TDN, TP, ABS254, SUVA254, NH4, NO2, NO3, TN, pCO2air, pN2Oair, CH4Sat, CO2Sat, N2OSat, CH4, CH4-C, CO2, CO2-C, N2O, N2O-N, etc.
  - Missing data indicated by an asterisk; data gaps documented (weather-related).
  - Latitude/Longitude provided with six decimal places; distance from tidal weir (km) and location metadata accompany each site.

- GIS Applications and Map-Based Use
  - Suitable for creating transect maps of GHG concentrations and water quality along the Clyde estuary, showing spatial gradients from L1 to L10.
  - Ability to overlay with coastal outfalls and wastewater treatment plant (WWTP) locations and other industrial outfalls to investigate anthropogenic influences on GHGs and nutrients.
  - Time-enabled visualizations: multi-epoch maps showing changes across eight surveys, enabling trend analysis against tidal phase, river flow, and seasonality.
  - Potential analyses:
    - Correlate GHG concentrations and saturations with salinity, stratification indicators, and river flow.
    - Explore links between nutrient proxies (TN, TP, NO3−, NH4+) and GHG production/sinks.
    - Integrate with bathymetry and depth to examine depth-dependent GHG dynamics (surface vs near-bed).
  - Data structure supports GIS-ready workflows for data cleaning, transformation, and integration with supplementary datasets (e.g., EIDC data, land use, and hydrodynamic models).

- Acknowledgements and Context
  - Part of an IAPETUS 2 Doctoral Training Partnership; supported by NERC (Grant NE/S007431/1).
  - Field sampling supported by UK Centre for Ecology & Hydrology; Kelvin Harbour access provided by The Tall Ship Glenlee Trust.
  - Data collection and analysis contributed by a team of researchers and collaborators.