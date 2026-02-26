# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a cropland and a grassland on lowland peatland soils, East Anglia Fens, UK, 2016 to 2019

- Time series of land surface–atmosphere exchanges including net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured at two managed lowland peatland environments in the East Anglian Fens, England, UK
- Sites:
  - Cropland (EF-SA): high-value horticultural crops; subsided peat over clay; drainage via sub-surface pipes
  - Grassland (EF-GF): restored wetland grassland within the Great Fen Project; managed with low-intensity grazing
- Periods:
  - EF-SA: 2016-11-17 to 2018-09-24
  - EF-GF: 2017-04-27 to 2019-03-31
- Ancillary data: meteorological and soil physics observations; turbulence-characterising variables

## Study sites

- Location: The Fenland, UK; largest contiguous lowland peatland soils in the UK; climate temperate maritime
- Cropland (EF-SA): coordinates 52.44° N, 0.41° E, -2 m amsl
  - Peat over clay; peat subsidence ~2 m since drainage; drainage via pipes and ditches
  - Properties: peat bulk density ~0.62 g cm-3; pH ~6.84; organic C ~30.8%; C/N ~16.4
- Grassland (EF-GF): coordinates 52.47°, -0.19°, -1 m amsl
  - Former arable peatland; rewetted and restored; low-intensity grazing; drainage network present but not connected to regional system
  - Peat depth ~2 m; soil pH 5.2–6.0; organic C ~30%; total N ~1.4%

## Sampling regime

- Automated measurements of flux, meteorology, and soil physics
- Flux observation height: 2.6 m at both sites
- Data cadence: 20 Hz raw data; 30-minute flux and ancillary means
- Observations span:
  - EF-SA: 2016-11-17 to 2018-09-24
  - EF-GF: 2017-04-27 to 2019-03-31

## Flux data acquisition

- Eddy covariance (EC) measurements of NEE (μmol CO2 m-2 s-1), H (W m-2), LE (W m-2), and τ (kg m-1 s-2)
- Open-path EC systems with:
  - Ultrasonic anemometer thermometer
  - LI-COR LI-7500 infrared gas analyser
- Wind measurements: Gill WindMaster (EF-SA) and Solent R3 (EF-GF)
- Data logging: CR3000 data loggers
- Ancillary turbulence metrics recorded alongside turbulence data

## Ancillary data

- Co-located sensors for meteorology and soil physics:
  - Air temperature (Ta) and relative humidity (RH) at 2 m
  - Net radiation (Rnet) and components (SWin, SWout, LWin, LWout)
  - Soil heat flux (G) at two locations
  - Water level and pressure transducers for peat surface monitoring
  - Volumetric water content (VWC) and soil temperature (Tsoil) at multiple depths
  - Precipitation measured at co-located stations
- Data logged as 30-minute means or sums

## Data processing

- Processing tool: EddyPRO® Flux Calculation Software Version 6.1
- Flux computation: 30-minute block-averaged fluxes
- Corrections and QC included:
  - Quality control of raw 20 Hz data
  - Angle of attack correction for sonic anemometers
  - 2D rotation to align with local terrain
  - Corrections for high/low-frequency co-spectral attenuation
  - Humidity effects on H, density corrections on LE and CO2
  - Random uncertainties per Finkelstein & Sims
- Derived metrics produced:
  - Wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter z/L
  - Flux footprints (Kormann & Meixner model)

## Quality control

- Outliers removed via median absolute deviation (MAD)
- Non-stationary turbulence periods removed
- Flux ranges enforced:
  - H: -200 to 500 W m-2
  - LE: -60 to 600 W m-2
  - NEE: -70 to 35 μmol CO2 m-2 s-1 (EF-SA) and -40 to 30 μmol CO2 m-2 s-1 (EF-GF)
- Night-time NEE removal; u* thresholds: 0.22 m s-1 (EF-SA), 0.16 m s-1 (EF-GF)
- Fluxes retained if >75% of flux originated from target ecosystem (footprint)
- Weekly visual QC; manual removal of clearly erroneous values

## Data gap-filling and flux partitioning

- Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005)
- Partitioning NEE into:
  - Gross Ecosystem Production (GEP)
  - Total Ecosystem Respiration (TER)
  - Based on Ta-driven partitioning (Reichstein et al., 2005)
- Tools: REddyProc package in R (Reichstein et al., 2016)

## Details of data structure

- Time series provided as two separate CSV files per site
  - Contain tabular data in ASCII format
  - Gap-filled and partitioned flux and ancillary data supplied as complete time series
  - Missing records denoted by -9999

## Nature and units of recorded values

- Variables described in a dedicated table (Table 1 in the document), including:
  - DateTime (UTC), NEE (μmol CO2 m-2 s-1) and NEE_filled, NEE_filled_sd
  - LE (W m-2) and LE_filled, LE_filled_sd
  - H (W m-2) and H_filled, H_filled_sd
  - τ (kg m-1 s-2) and τ_sd
  - Storage terms: CO2_strg, LE_strg, H_strg
  - Ta (°C), RH (%), VPD (hPa), Pa (kPa)
  - SWin, SWout, LWin, LWout, Rnet (W m-2)
  - G1, G2 (W m-2)
  - Tsoil1–3 (°C), VWC1–4 (%)
  - Precipitation (mm over 0.5 h and total)
  - WaterLevel (mm), Windspeed (m s-1), Winddir (degrees)
  - Footprint metrics: x_peak, x_70, x_90
  - Ustar (m s-1), TKE (m-2 s-1), L (m), zL
  - NEE_filled_sd, LE_filled_sd, H_filled_sd
  - GEP and TER (μmol CO2 m-2 s-1)

## Acknowledgments

- Funded by Natural Environment Research Council (NERC) awards NE/R016429/1 (UK-SCAPE) and NE/P014097/1 (SEFLOS)
- EF-SA site established under Defra SP1210; COSMOS-UK data contributions
- Gratitude to landowners for access

## References (selected)

- Evans et al. related to peatland projects and COSMOS-UK
- Methodological references for QC, flux calculations, and data processing (Finkelstein & Sims; Foken et al.; Moncrieff et al.; Reichstein et al.; Reichstein et al.; Schotanus et al.; Webb et al.; Wilczak et al.)