# Subset of turbulent energy fluxes, meteorology and soil physics observations collected at eddy covariance sites in southeast England, June 2019

## Overview of dataset
- Time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE) plus supporting meteorological and soil physics data.
- Collected at five eddy covariance (EC) flux tower sites across southeast England.
- Subset of flux and ancillary observations extracted from longer-term time series for the HyTES Campaign calibration in June 2019 (HyTES airborne imaging spectrometer flown over EC sites during 2019-06-28 to 2019-06-29).
- Data provided as calibration data for the Net-Sense/HyTES campaign under the Copernicus LSTM mission.

## Study sites
- Five EC sites: three croplands (two on clay soils, one on drained lowland peat) and two managed grasslands (on chalk and drained lowland peat).
- Site coordinates not provided in the dataset for security reasons; contact author to obtain.
- Instruments and site conditions summarized in a corresponding table detailing land cover, soil type, and deployed sensors.

## Sampling regime
- Automated flux, meteorological, and soil physics measurements span 2019-06-22 00:30 to 2019-07-06 00:00.
- Data are structured as time series with 30-minute averaging for most variables.

## Flux data acquisition
- Turbulent fluxes of sensible heat (H) and latent heat (LE) measured above the canopy via open-path EC systems.
- EC systems include a sonic anemometer thermometer and an infrared gas analyser, logging at 20 Hz and then aggregated to 30-minute means.
- Measurement heights vary by site (2.0–5.0 m).
- Horizontal/vertical sensor separations are defined to maintain consistent geometry across sites.

## Ancillary data acquisition
- Air temperature (TA) and relative humidity (RH) at 2.0 m height; barometric pressure from IRGAs.
- Net radiation (Rnet) and components of the shortwave/longwave fluxes (SWin, SWout, LWin, LWout).
- Soil heat fluxes (G) at 0.03 m depth at two sites using HFP sensors.
- Soil water content (VWC) and soil temperature (TS) at 0.1 m depth.
- Precipitation measured with SBS500 tipping bucket rain gauges.
- Data logged at 0.1 Hz and aggregated to 30-minute means; precipitation sums are 30-minute totals.

## Data processing
- Turbulent flux densities calculated with EddyPRO Flux Calculation Software v6.1.
- Processing steps include QC of raw 20 Hz data, angle-of-attack corrections, two-dimensional rotation to align with terrain, cospectral attenuation corrections, density corrections, and height adjustments for wind measurements.
- QC involved outlier removal, non-stationarity checks, and footprint representativeness (target ecosystem > 80% using the ART Footprint Tool).
- Visual inspection of data weekly to remove clearly erroneous values.

## Data gap-filling and flux partitioning
- Gaps in EC data (LE, H) filled using Marginal Distribution Sampling via REddyProc in R.
- Gap filling applied to complete site time series before extraction for HyTES dataset.

## Details of data structure
- Time series provided as separate CSV files per site.
- Time range: 2019-06-22 00:30 to 2019-07-06 00:00.
- Missing records denoted by -9999.
- Variable naming and structure aligned with Table 2 (flux, micrometeorological, and soil physics variables).

## Nature and units of recorded values
- TIME_START and TIME_END define observation window.
- LE: latent heat flux density (W m-2); LE_qc indicates quality (0 = high quality, 1–3 = gap-filled or lower quality).
- H: sensible heat flux (W m-2); H_qc similar quality flags.
- G1, G2: soil heat flux at 0.03 m depth (W m-2).
- TA: air temperature at 2.0 m (°C); TA_qc quality flag.
- VPD: vapour pressure deficit (hPa); VPD_qc quality flag.
- RNET, SWIN, LWIN, SWOUT, LWOUT: radiation components (W m-2).
- PA: barometric pressure (kPa).
- P: precipitation (mm per 0.5 h).
- RH: relative humidity (percent); P and other qc flags as applicable.
- WS: wind speed at EC height (m s-1); WD: wind direction (degrees north); QC flags for meteorology variables.
- TS: soil temperature at 0.1 m (°C); VWC: soil volumetric water content at 0.1 m (% vol).

## Acknowledgments
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCAPE National Capability) and NE/N018125/1 (ASSIST).
- COSMOS-UK project contributed additional meteorological and soil data for the BD-OG site.
- Gratitude to landowners and site managers for access and permission to install sensors.

## References
- Includes foundational methodological references for QC, EC processing, footprint analysis, gap-filling, and data processing tools (EddyPRO, REddyProc) and related micrometeorology literature.