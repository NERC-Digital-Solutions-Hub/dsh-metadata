# Net ecosystem carbon dioxide (CO2) exchange and meteorological observations from an eroded, high altitude, blanket bog, Scotland, 2018-2020

## Experimental design/sampling regime
- Time series observations of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), plus meteorological observations.
- Site: eroded upland blanket bog peatland (UK-BAL), Eastern Cairngorms, Scotland (56.93° N, -3.16° E, 642 m asl); maritime temperate montane climate (Dfc).
- Peat erosion is widespread; bare peat gullies 0.5–3 m deep, 2–10 m wide.
- No treatment in the flux tower footprint during the study period; peatland restoration (gully reprofiling) planned for the future.
- Data types: 30-minute NEE, LE, H (originally 20 Hz), plus 30-minute meteorological observations (originally 15 min).
- Time period: 04/07/2018 to 04/11/2020.
- Data coverage: NEE 51%, LE 54%, H 76%; biomet data 92–97% (longwave radiation 80% due to sensor fault mid-2019).
- Notable disruptions: data loss 14 Nov–27 Dec 2019 due to major power supply issue; peat restoration activities caused wind-blown peat affecting Li-7200RS spectral response; COVID travel restrictions delayed repairs until Aug 2020, resulting in discarded NEE and LE data up to mid-August 2020.
- Data update: this dataset updates a previously deposited, shorter dataset (daily data).

## Collection methods
- Eddy covariance (EC) system for fluxes:
  - Windmaster sonic anemometer at 3.2 m; LI-7200 gas analyser for CO2 and H2O; sensors separated by 0.1 m; LI-7200 inlet tube length 1.0 m.
  - Air temperature (Ta) and relative humidity (RH) at 2 m using Rotronic sensor.
  - Data logged at 20 Hz; 30-minute means used for analysis.
  - Canopy height assumed static at 0.25 m; fetch >1000 m in most directions (400 m to N due to cliff edge).
- Additional micrometeorology:
  - Net radiation (Rnet) and components; PAR; soil heat flux (G) at two locations; soil temperature at multiple depths; soil moisture; precipitation; water table depth.
  - All sensors scanned at 0.1 Hz; data aggregated to 30-minute means.
- Field context:
  - Fully vegetated landing surface; surface of bare peat gullies can move seasonally due to frost heave.
  - Vegetation described as semi-evergreen with light-to-moderate deer grazing.

## Calibration steps and values
- Gas analyser calibrated per manufacturer instructions pre-installation.
- No on-site span/zero checks during data capture due to remoteness; post-cleaning (Aug 2020) instrument performance indicated by signals near 99%.

## Analytical methods
- Flux calculations: 30-minute flux densities (NEE, LE, H) computed with EddyPRO v7.0.6; data screened for outliers and physically implausible values.
- Data processing:
  - 2D rotation of sonic data; corrections for cosine response; cross-correlation delays removed.
  - Corrections for high/low-frequency cospectral attenuation; humidity influence on LE; density corrections on CO2 and LE.
  - Random uncertainties estimated from covariance-based approach.
  - NEE storage term assumed negligible; NEE sign convention: positive from ecosystem to atmosphere.
- Quality control (QC) procedures:
  - Outliers detected via median absolute deviation; stationarity tests; flux ranges checked; low-turbulence periods identified via u* thresholds; CO2 fluxes excluded when u* < 0.17 m/s.

## Nature and Units of recorded values
- Data columns (examples with units): DateTime (yyyy-mm-dd HH:MM, UTC); NEE (μmol CO2 m^-2 s^-1); NEE_unc (μmol CO2 m^-2 s^-1); LE (W m^-2); LEE_unc (W m^-2); H (W m^-2); H_unc (W m^-2); Tau (kg m^-1 s^-1); Tau_unc; CO2_strg (μmol CO2 m^-2 s^-1); LE_strg (W m^-2); H_strg (W m^-2); Pa (kPa); Tair (°C); RH (%); VPD (hPa); radiation components (SWin, SWout, Lwin, LWout, Rnet) etc.; soil data (G1, G2, Tsoil), WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL; NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
- All fluxes reported as 30-minute processed values (gap-filled in QC section).

## Quality control
- Gap-filling and partitioning:
  - Gap-filling and partitioning of NEE into GEP and respiration using REddyProc (R) version 0.8-2/r14.
  - H, LE, and NEE gap-filled with marginal distribution sampling (MDS).
  - Annual sums rely on gap-filling using Braemar station data for missing periods.
  - Tair used as driving temperature for flux partitioning due to gaps in Tsoil.
  - Uncertainty for gap-filled fluxes derived from standard deviation of observations used for gap-filling.

## Details of data structure
- Data stored in a single CSV file with columns:
  DateTime, NEE, NEE_unc, LE, LEE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, Lwin, LWout, Rnet, G1, G2, Tsoil, WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP
- Refer to “Nature and Units” for definitions and units.

## Any other information useful to interpretation
- This dataset updates a prior deposition with shorter time resolution (30-minute data) and extended time series.
- Link to related dataset for cross-reference: https://catalogue.ceh.ac.uk/documents/b8c9fd3df9ea-4fd8-9557-9022884f711d
- References for methods and quality assessments used in data processing are provided (Mauder et al. 2013; Vickers & Mahrt 1997; Wilczak et al. 2001; Nakai et al. 2006; Moncrieff et al. 1997, 2004; Schotanus et al. 1983; Webb et al. 1980; Papale et al. 2006; Reichstein et al. 2016).