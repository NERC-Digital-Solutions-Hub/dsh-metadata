# Overview of the dataset

- Net ecosystem exchange (NEE) of CO2 and methane (CH4) fluxes were measured at a hemi-boreal ombrotrophic fen in southern Sweden (Mycklemossen) from August 2017 to September 2019, with a drought year (2018) used to compare drought and non-drought fluxes and recovery in 2019.
- Four ecotypes were monitored: sphagnum, eriophorum, heather, and open water, to assess drought responses across vegetation types.
- Data are intended to support data exploration, quality assessment, and the creation of data products (e.g., dashboards or reports) to facilitate end-user use and interpretation.

## Site and sampling design

- Location: Mycklemossen fen, ca. 100 km north of Gothenburg, Sweden (58.3673 N, 12.1686 E; ~75 m a.s.l.), part of the Skogaryd research catchment.
- Habitat: Hemi-boreal bog-like fen with water table high enough for open water areas year-round; vegetation includes Calluna vulgaris (heather), Sphagnum spp. (moss), and Eriophorum vaginatum (sedge).
- Experimental setup: A transect containing all four vegetation types with 24 random replicate points across four blocks; each point classified as sedge, heather, sphagnum, or open water (water).
- Collars: PVC collars installed at ~2 cm depth (20 cm inner diameter, 10 cm height) at all measurement points.

## Measurement system and protocol

- Instrument: SkyLine2D automated chamber system (University of York) to measure surface GHG fluxes.
- Chamber details: Clear cylindrical chamber (20 cm inner diameter, 40 cm height) mounted on a motorised trolley; lowered onto collars to measure over ~4 minutes.
- Sampling cadence: System cycles through pre-selected positions, enabling ~10 measurements per day per chamber; full cycle takes ~2.5 hours.
- Gas analysis: Headspace gas circulated sequentially through a LICOR LI-8100 IRGA for CO2 and a cavity ringdown laser (LGR UGGA-91) for CO2 and CH4.
- Mixing: No chamber fan; previous tests showed no significant difference with or without a fan, indicating adequate mixing from flow through the analyser.
- Data recording: Data logged with a Campbell Scientific CR1000x data logger.
- Flux calculations: CO2 and CH4 fluxes calculated from the slope of gas concentration vs time using linear regression; minimum 20 seconds of headspace mixing (deadband) and specific time windows (90 s for CO2, 240 s for CH4). Daylight adjustments to CO2 flux based on a light response curve to account for chamber attenuation.

## Data processing and quality control

- Software: SAS 9.4 for data manipulation and analysis.
- Primary quality controls:
  - CO2 flux: R^2 of CO2 flux regression must be ≥ 0.9.
  - CH4 flux: Regression must have P < 0.05 to be accepted; otherwise treated as zero flux.
- Outliers: Flux values beyond ±1.96 standard errors of the mean excluded.
- Night-time and still-air adjustments: Filters applied to avoid overestimation under still atmospheric conditions (per Koskinen et al. 2014 and Lai et al. 2012).
- Additional filtering: Fluxes where the mean CO2 concentration change before and after chamber closure exceeded 25 ppm within a 20-second pre/post window were discounted (per Jarveoja et al. 2020); this led to 329 fluxes being excluded.
- Outputs: Cleaned flux estimates for CO2 and CH4 suitable for downstream analyses of drought responses and carbon balance.

## Data structure and content

- Structure: A single dataset table with eight variables ordered as:
  - DATETIME: Date and time of flux measurement (dd:mmm:yyyy:hh:mm:ss)
  - DATE: Date of measurement (dd/mm/yyyy)
  - TIME: Time of measurement (hh:mm:ss)
  - PLOT: Experimental plot number
  - ECOTYPE: Dominant vegetation type of the plot (sphagnum, heather, eriophorum, water)
  - BLOCK: Block number of the experimental design
  - CH4_flux: Methane flux (nmol m⁻² s⁻¹)
  - CO2_flux: Net ecosystem exchange of CO2 (µmol m⁻² s⁻¹)

- Documentation and units: Variable names, descriptions, and units are provided in the dataset as described above.

## Provenance and references

- Keane et al. (2018): Method description of the SkyLine2D chamber system and flux measurement approach.
- Keane et al. (2021): Carbon dioxide and methane flux response and recovery from drought in a hemiboreal fen.
- Koskinen et al. (2014) and Lai et al. (2012): Guidance on night-time and turbulence-related adjustments in chamber measurements.
- Jarveoja et al. (2020): Method for identifying diel, temperature-related flux patterns.
- Mosier (1989): Chamber techniques overview.
- Heinemeyer et al. (2013): Evaluation of carbon balance estimates from automated ground-level flux chambers.

## Usage notes

- Suitable for assessing drought effects on CO2 and CH4 fluxes across ecotypes, and for cross-study comparisons of automated chamber data processing and quality control.
- Data are best used with awareness of the filtering thresholds (R^2, P-values, night-time adjustments) and the exclusions (329 fluxes) to understand potential biases or gaps in temporal coverage.