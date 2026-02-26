# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a winter wheat field, Lincolnshire, UK, 2012

## Overview
- Time series of surface-atmosphere fluxes and ancillary meteorological/soil observations over a winter wheat crop in Lincolnshire, UK during the 2012 growing season.
- Fluxes measured with an open-path eddy covariance (EC) system at 3.0 m height; data processed to 30-minute means.
- Gap-filled and partitioned data provided (NEE further split into GEP and TER) using standardized methods; data quality control and footprint assessments included.

## Study site & sampling regime
- Location: arable cropland, approximately 10 km north of Lincoln, UK (53°19'17.89"N, 0°35'7.83"W).
- Climate: temperate maritime; mean annual air temperature ~9.8°C and annual precipitation ~614 mm (1981–2010 data).
- Soils: Beccles 1 association, seasonally waterlogged fine loams; pH ~6.32; bulk densities ~1.46–1.53 g cm^-3 in upper 0–0.3 m; particle fractions ~49% sand, 36% silt, 15% clay.
- Sampling window: 2012-04-05 00:30 to 2012-08-08 00:00 UTC.
- Flux footprint: evaluated per record; fluxes considered representative if >75% originated within the target ecosystem.

## Data collected
- Fluxes: Net Ecosystem Exchange (NEE, μmol CO2 m^-2 s^-1), Sensible heat (H, W m^-2), Latent heat (LE, W m^-2), Momentum (τ, kg m^-1 s^-2).
- Ancillary meteorology & soil: Net radiation (Rnet) and components (SWin, SWout, LWin, LWout), soil heat flux (G), air temperature (Ta), relative humidity (RH), soil temperature (Tsoil), soil volumetric water content (VWC), rainfall (precipitation), wind speed and direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L) and stability (z/L).
- Data resolution: 20 Hz raw EC signals; 30-minute aggregated means; quality-controlled and gap-filled data provided.

## Data processing & quality control
- Processing: EddyPRO software v6.1; corrections for instrument tilt, coordinate rotation, spectral attenuation, density effects, and humidity-related corrections; random uncertainties estimated.
- Quality control: median absolute deviation outlier removal; non-stationarity checks; flux value ranges (H: -200 to 400 W m^-2, LE: -100 to 500 W m^-2, NEE: -70 to 35 μmol CO2 m^-2 s^-1); NEE flagged at night when SWin < 20 W m^-2; friction velocity threshold of 0.07 m s^-1; footprint representativeness verification; visual manual checks.

## Gap filling & flux partitioning
- Gap filling: Marginal Distribution Sampling (MDS) approach for EC gaps (Reichstein et al. 2005); meteorological gaps filled via linear relationships from nearby weather stations.
- Partitioning: NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Ta-driven approach; executed with REddyProc (R package) following Reichstein et al. 2005, 2016.

## Data structure & variables
- File: Lincolnshire_Winter_Wheat_2012.csv (single time-series CSV from 2012-04-05 00:30 to 2012-08-08 00:00 UTC).
- Gap-filled and partitioned data included; missing records denoted by -9999.
- Variable types and columns: NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, CO2_strg, LE_strg, H_strg, Pa, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G1, G2, Tsoil1, Tsoil2, Tsoil3, Tsoil4, VWC1, VWC2, VWC3, VWC4, Precipitation, Windspeed, Winddir, Ustar, TKE, L, zL, FootprintFraction, x_peak, x_70, x_90, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.
- Notes: Table 1 in the original document defines units and descriptions for all variables (e.g., DateTime in yyyy-mm-dd HH:MM UTC; NEE in μmol CO2 m^-2 s^-1; etc.).

## Spatial representativeness and GIS considerations
- Footprint and representativeness metrics provided (FootprintFraction, x_peak, x_70, x_90), enabling mapping of the observed flux sources and upwind influence.
- Site coordinates enable geolocation mapping and integration with regional GIS datasets (soil, climate, land cover).
- Gap-filled and partitioned flux components (GEP, TER) support spatial analyses of carbon and energy fluxes across canopy scale.

## Access, acknowledgments & references
- Data generation supported by Natural Environment Research Council (NE/R016429/1) and Carbo-Biocrop project; landowner access acknowledged.
- Dataset and processing methods align with established eddy covariance standards and have associated methodological references (e.g., Reichstein et al., Mauder et al., Moncrieff et al., EddyPRO, REddyProc).