# Subset of turbulent energy fluxes, meteorology and soil physics observations collected at eddy covariance sites in southeast England, June 2019

## Overview
- Calibration dataset for the Net-Sense/HyTES campaign under the Copernicus High Spatio-Temporal Resolution LSTM mission.
- May be extracted from longer-term eddy covariance (EC) time series, collected at five EC flux towers in southeast England.
- Focused on time period 2019-06-22 00:30 to 2019-07-06 00:00, during HyTES airborne campaign (2019-06-28 to 2019-06-29).

## What is included
- Time series of turbulent fluxes: sensible heat flux (H) and latent heat flux (LE).
- Supporting meteorological and soil-physics data.
- Data provided as subset files from longer-term observations, suitable for calibration with HyTES data.

## Study sites and instrumentation
- Five EC sites: three croplands (two on clay soils, one drained lowland peat) and two managed grasslands (on chalk and drained peat).
- Instrumentation summarized for each site, including:
  - Flux tower components: open-path eddy covariance systems with sonic anemometer and IRGA (e.g., Windmaster, LI-7500/LI-7500A) at varying heights.
  - Ancillary sensors: air temperature (TA), relative humidity (RH), barometric pressure, net radiometer (Rnet), soil heat flux plates, soil moisture and temperature probes, rain gauges.
- Site coordinates withheld for security; contact dataset authors to obtain locations.

## Data collection and structure
- Flux data: 20 Hz raw observations of turbulence components and water vapour, logged at CR3000; fluxes calculated and averaged to 30-minute intervals.
- Ancillary data: meteorology and soil physics measured at or near the EC towers, also at 30-minute means.
- Data organization: five separate CSV files (one per site) covering 2019-06-22 00:30 to 2019-07-06 00:00.
- Missing data: denoted by -9999; some records removed during QC.

## Variables and metadata
- Key variables (units):
  - LE, H: W m-2 (latent and sensible heat flux)
  - G1, G2: soil heat flux (W m-2)
  - TA: °C (air temperature at 2.0 m)
  - VPD: hPa (vapor pressure deficit)
  - RNET, SWIN, LWIN, SWOUT, LWOUT: W m-2 (net and short/longwave radiation components)
  - PA: kPa (barometric pressure)
  - P: mm per 0.5 h (precipitation)
  - RH: % (relative humidity)
  - WS, WD: m s-1, degrees (wind speed and direction at EC height)
  - TS: °C (soil temperature at 0.1 m)
  - VWC: %vol (volumetric soil moisture)
- Quality flags (QC) per variable:
  - 0 = high quality observed
  - 1 = gap-filled, good quality
  - 2 = gap-filled, acceptable quality
  - 3 = gap-filled, poor quality

## Data processing and quality control
- Flux calculations: EddyPRO v6.1, with 30-minute block averages.
- Processing steps include:
  - QC of raw 20 Hz data
  - Angle-of-attack corrections for sonic anemometers
  - 2D coordinate rotation to align with local terrain
  - Corrections for high/low-frequency cospectral attenuation
  - Density- and humidity-related corrections for H and LE
  - Footprint analysis to ensure representativeness of target ecosystem
  - Visual inspection and manual removal of clearly erroneous values
- Representativeness: fluxes considered from the target ecosystem if >80% originated within it (via ART Footprint Tool).

## Gap filling and flux partitioning
- Gaps in LE and H filled using Marginal Distribution Sampling (MDS) via REddyProc (R), applied to the full site time series before extraction for HyTES.

## Data structure and usage notes
- Time fields: TIME_START and TIME_END in YYYYMMDDhhmm.
- Data are provided as complete time series with -9999 for missing records.
- Subset is designed for calibration and analysis workflows typical of environmental monitoring and policy performance assessment.
- Access and provenance: data acquisition supported by NERC (UK-SCAPE ASSIST COSMOS-UK collaborations); dataset authors acknowledge landowners and site managers.

## Acknowledgments and references
- Data supported by NERC awards NE/R016429/1, NE/N018125/1.
- ASSIST and COSMOS-UK projects acknowledged; methodological references include standards for QC, eddy-covariance processing, and footprint analysis.