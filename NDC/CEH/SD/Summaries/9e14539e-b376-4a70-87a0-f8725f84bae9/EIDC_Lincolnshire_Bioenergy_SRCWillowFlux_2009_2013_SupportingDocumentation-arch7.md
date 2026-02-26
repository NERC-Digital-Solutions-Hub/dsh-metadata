# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a short rotation coppice willow ( Salix viminalis ) plantation, Lincolnshire, UK, 20092013

- The dataset provides time series observations of surface-atmosphere exchanges including net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ), collected via micrometeorological eddy covariance (EC) between 2009-10-14 00:30 and 2013-10-01 00:00, with ancillary weather, soil physics data, and turbulence/quality metrics.
- Flux data are processed to 30-minute averaging periods using EddyPRO, including quality control corrections and turbulence-related adjustments; random uncertainties are provided.
- Gap-filled and partitioned fluxes are included: NEE_filled with corresponding uncertainty, partitioned into GEP (gross ecosystem production) and TER (total ecosystem respiration).

## Study site

- Location: SRC willow flux observation site, Lincolnshire, UK (53°19'10.37"N, 0°35'3.06"W).
- Area and layout: mature 9.4 ha commercial bioenergy plantation.
- Climate: temperate maritime; mean annual air temperature ~9.8 ± 0.7 °C and precipitation ~614 ± 93.5 mm year-1 (1981–2010).
- Soils: Beccles 1 association, seasonally waterlogged fine loams over Charnmouth Mudstone; bulk density ~1.4 ± 0.2 g cm-3; pH ~5.8 ± 0.3; upper 0.3 m soil C ~68.3 t ha-1 and N ~11.0 t ha-1.
- Management: established on former arable land in 2000; coppiced in 2001; biomass harvested March 2011 and October 2013; limited inputs post-harvest in 2011 (Fibrophos 0.5 Mg/ha, lime) and compost wood waste (15 Mg/ha); rainfed with no irrigation.

## Sampling regime

- Automated flux, meteorological and soil physics measurements conducted from 2009-10-14 00:30 to 2013-10-01 00:00.
- Flux tower setup: open-path EC system on a tall mast at the plantation center; measurement height adjusted to ~twice canopy height.

## Flux data acquisition

- Variables: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2) with 20 Hz raw data.
- Instruments: Mk4 Hydra sonic anemometer-thermometer; LI-7500IR gas analyser; data logged with 30 Hz sampling on a Hydra datalogger.
- Ancillary EC inputs: full turbulence and atmosphere density corrections applied during processing.

## Ancillary data acquisition

- Net radiation components (Rnet, SWin, SWout, LWin, LWout) and below-canopy photosynthetic photon flux density (PPFDbc) from below-canopy sensors.
- Soil surface energy and state: soil heat flux (G) at two locations, volumetric water content (VWC) in upper 0.3 m, soil temperature (Tsoil) at 0.05 m at two locations.
- Air and atmospheric variables: air temperature (Ta) and relative humidity (RH) from weather station measurements.
- Data are captured as 30-minute means (precipitation as sums) via a CR10x datalogger.

## Data processing

- Eddy covariance processing: EddyPRO v6.1; 30-minute block averages; QC includes 20 Hz data quality checks, angle-of-attack corrections, 2D coordinate rotation, corrections for co-spectral attenuation, humidity effects, and density corrections for LE and CO2.
- Uncertainty and auxiliary metrics calculated: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).
- Quality control: outliers removed via median absolute deviation; fluxes filtered by EddyPRO quality flag; physically plausible ranges applied; footprint analysis via ART Footprint Tool to ensure >75% flux origin within the target ecosystem; visual inspection and manual removal of clearly erroneous values.

## Gap-filling and flux partitioning

- Gap-filling: Marginal Distribution Sampling approach (Reichstein et al., 2005) for NEE, H, LE.
- Partitioning: NEE partitioned into GEP and TER using Reichstein et al. (2005) methodology, driven by air temperature.
- Tools: REddyProc package in R (Reichstein et al., 2016) used for gap-filling and partitioning.

## Data structure and content

- Format: single .csv time series file covering 2009-10-14 00:00 to 2013-10-01 00:00, with 30-minute records; time stamps refer to the end of each 30-minute period.
- Missing data: denoted as -9999.
- Key variables (examples):
  - NEE_filled, NEE_filled_sd
  - GEP, TER
  - H_filled, H_filled_sd
  - LE_filled, LE_filled_sd
  - NEE (uncorrected), LE, H, Tau, Ta, RH, VPD
  - Rnet, SWin, SWout, LWin, LWout
  - PPFDbc, G1/G2, Tsoil1/Tsoil2, VWC1/VWC2, Precipitation
  - windspeed, winddir, FootprintFraction
  - Ustar, TKE, L, zL, NEE
- Variable descriptions and units are aligned with LI-COR conventions and Reichstein et al. (2016) conventions.

## Usage notes for GIS applications

- Provides time-resolved flux data with support variables (footprint fraction, wind direction, stability) useful for spatially contextualizing flux measurements and designing map-based data products.
- The footprint metric enables spatial weighting and assessment of representativeness for GIS analyses that integrate flux data with land-use or habitat layers.
- 30-minute temporal resolution enables near-real-time or historical trend mapping when combined with other environmental layers.

## Acknowledgments and references

- Data collection funded by the Natural Environment Research Council (CarboBiocrop) and CEH Integrating Fund.
- Key references for processing and interpretation include Reichstein et al. (2005, 2016), Mauder et al. (2013), Papale et al. (2006), Moncrieff et al. (1997, 2004), and associated methodological sources.
- Related site and soil studies cited (Drewer et al., 2012; Morrison et al., 2019; Rowe et al., 2016; Robertson et al., 2017).

## Data access

- Data file: Lincolnshire_Bioenergy_SRCWillow_2009_2013.csv
- Timeframe covered: 2009-10-14 to 2013-10-01
- Point of contact/acknowledgements include landowners and associated research projects.