# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2008 to 2013

## Summary of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured above a Miscanthus plantation.
- Observations collected using open-path eddy covariance (EC) system from 2008-05-01 00:30 to 2013-02-18 00:00, with ancillary weather and soil physics data and turbulence variables.
- Data include gap-filled and partitioned fluxes, plus derived variables and uncertainties for end-user self-serve analyses.

## Study site and context
- Location: Miscanthus x. giganteus plantation, 53°19'10.07"N, 0°35'18.65"W, ~11.5 ha, ~10 km north of Lincoln, UK.
- Climate: temperate maritime (mean temperature ~9.8°C; mean annual precipitation ~614 mm).
- Soils: Beccles 1 soil association, seasonally waterlogged fine loams; detailed soil properties provided (bulk density, texture, soil organic carbon and nitrogen, pH).
- Management: established 2006 on former arable land, rhizomes planted at 10,000 ha−1, no fertilizer until 2010 (Fibrefoss 660 kg ha−1), harvested annually in spring (from 2008 onward).

## Data collection and instrumentation
- Flux measurements: EC system on a movable mast, height adjusted to ~2× canopy height; fluxes for NEE, H, LE, and τ measured with a sonic anemometer-thermometer and an infrared gas analyser; 20 Hz raw data logged.
- Ancillary measurements: meteorology (air temperature, relative humidity, net radiation, shortwave/longwave radiation, PPFD below canopy) and soil physics (soil heat flux, volumetric water content, soil temperature) collected with multiple sensors and logged as 30-minute means.
- Time resolution: 30-minute flux averaging periods; NaN-like gaps coded as -9999.

## Data processing and quality control
- Processing: EddyPRO v6.1 used for QC, coordinate rotation, tilt correction, co-spectral corrections, humidity and density corrections; fluxes aggregated to 30-minute means.
- Quality control (QC): outliers removed via median absolute deviation; EddyPRO quality flags used; fluxes beyond specified ranges excluded; footprint analysis (ART Footprint Tool) to ensure ≥75% of flux originates from target ecosystem; manual review of weekly plots for anomalies.
- Footprint and uncertainty: derived metrics include wind speed, direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L); random uncertainties calculated per established methods.

## Gap filling and flux partitioning
- Gap filling: missing EC data (NEE, LE, H) filled with Marginal Distribution Sampling.
- Flux partitioning: NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Reichstein et al. (2005) framework driven by air temperature.
- Tools: REddyProc package in R used for gap filling and partitioning (Reichstein et al. 2016).

## Data structure, variables, and units
- Data delivery: a single CSV file containing the time series (2008-05-01 00:30 to 2013-02-18 00:00).
- Time stamps: end of each 30-minute period (UTC).
- Core variables (example): NEE (μmol CO2 m−2 s−1), NEE_unc, LE (W m−2), LE_unc, H (W m−2), H_unc, τ (kg m−1 s−2), τ_unc, CO2_strg (μmol CO2 m−2 s−1), Ta (°C), RH (%), VPD (hPa), SWin/SWin_total (W m−2), SWout/LWin/LWout/Rnet (W m−2), PPFDbc (μmol photons m−2 s−1), G (W m−2), Tsoil (°C), VWC (%), Windspeed (m s−1), Winddir (degrees), FootprintFraction (%), Ustar (m s−1), TKE (m−2 s−1), L (m), zL (dimensionless). 
- Gap-filled outputs: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP; each with corresponding uncertainty metrics.
- Data gaps: represented by -9999.

## Usage notes for data support
- Provides a long-term carbon balance context (2008–2013) for a commercial Miscanthus plantation, useful for benchmarking, model validation, and cross-site comparisons.
- Includes both raw and processed (gap-filled and partitioned) fluxes, enabling both direct observation-based analyses and model-driven investigations.
- Detailed metadata, methodological references, and QC steps support reproducibility and integration with other micrometeorological datasets.

## Acknowledgments and references
- Data collection funded by the NERC CarboBiocrop project and CEH Integrating Fund; authors thank landowners.
- References listed for methodologies (QC procedures, footprint analysis, eddy covariance processing, gap-filling and partitioning algorithms, and related site studies).