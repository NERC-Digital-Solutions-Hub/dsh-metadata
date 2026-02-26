# Half hourly fluxes of sensible heat, latent energy and carbon, observed by eight eddy covariance towers in the Northern Chihuahuan Desert, 2018-2019

- Overview
  - Dataset collected at Sevilleta Refuge, New Mexico, USA, from 2018-11-01 to 2019-11-01.
  - Eight eddy covariance towers (REC systems) deployed to test new design and to investigate spatial variability of fluxes.
  - Ten towers considered in footprint analysis: the eight REC towers plus two AmeriFlux towers (US-Seg and US-Ses) for footprint context.
  - Main sensors on towers: Gill Windmaster sonic anemometer, Honeywell HIH-4000 relative humidity sensor, Vaisala GMP343 CO2 sensor.
  - Data were pre-processed and quality-controlled, with gap-filling and flux corrections applied to produce fluxes (H for sensible heat, LE for latent heat, NEE for net ecosystem exchange).

- Preprocessing and processing
  - Raw data pre-processing performed with EdiRe software (v1.5.0.32) including spike detection, coordinate rotation, frequency response correction, cross-correlation, and WPL correction.
  - Half-hourly data gaps were filled using code published on GitHub; data subsequently subjected to season-specific u* filtering with REddyProc (v1.2).
  - Cospectra analysis conducted with Hamming window (segment size 512) and 30 frequency distribution bins to derive frequency-specific correlations.
  - Time lags between gas/CO2 sensors and sonic anemometer were determined by covariance testing at delays (0, 5.5, 7 s); water lag constant across RH 5–90%.
  - Spike filtering used a Tukey’s fence-based approach with k = 30 to avoid over-filtering.
  - Flux signs: positive values correspond to fluxes from the atmosphere; NEE negative indicates a terrestrial carbon sink.
  - Data gaps are present; some fields show 0 values where appropriate (e.g., certain diagnostic fields).

- Data files and structure
  - 1–8: Flux data (SEG_EC1_fluxes, SEG_EC2_fluxes, SEG_EC3_fluxes, SEG_EC4_fluxes; SES_EC1_fluxes, SES_EC2_fluxes, SES_EC3_fluxes, SES_EC4_fluxes)
    - Time reference: Date_Time (center of half-hour, DD/MM/YYYY HH:mm).
    - Meteorological and flux-related variables include: P (air pressure), mean_vCO2 (CO2 concentration), mean_vT (air temperature), mean_cRH (relative humidity), wind components (mean_gU_pre_rot, mean_gV_pre_rot, mean_gW_pre_rot), mean_gT_virt, mean_cH2O, mean_c_e (water vapor), Wind_Dir, mean_Wind_Spd, sigma_V, friction_velocity, Height, MO_stability (Height/Monin-Obukhov length), Hc (sensible heat flux after frequency correction), cLEc (latent heat flux after frequency correction), Fcc (NEE after correction).
    - Notes: includes quality-controlled, gap-filled fluxes and associated diagnostic fields.
  - 9–18: Footprint data (SEG_EC1_footprint_80, SEG_EC2_footprint_80, SEG_EC3_footprint_80, SEG_EC4_footprint_80, SEG_EC0_footprint_80, SES_EC1_footprint_80, SES_EC2_footprint_80, SES_EC3_footprint_80, SES_EC4_footprint_80, SES_EC0_footprint_80)
    - Structure: x (Easting in meters, UTM 13N, NAD83), y (Northing in meters, UTM 13N, NAD83).
    - Represents the 80% footprint boundary for the ten towers.
  - 19–20: Land cover data (SEG_Extract_land_cover, SES_Extract_land_cover)
    - Land cover maps within 440 m radius around US-SEG and US-SES towers.
    - Categories: 0 = barren, 1 = shrubland, 2 = herbaceous, 4 = (unspecified in summary; appears as a code used in the dataset).
    - Resolution: 1 m2 cells.

- Variables and interpretation
  - Fluxes: Hc (sensible heat), cLEc (latent heat), Fcc (net ecosystem exchange) after frequency response correction.
  - Meteorology: air temperature, humidity, CO2 concentration, wind components and speed, air pressure.
  - Turbulence and footprint metrics: friction velocity, Monin-Obukhov stability ratio, footprint geometry for interpretation of flux measurements.
  - Land cover and footprint: land cover within 440 m, footprint extents for 80% area to contextualize flux measurements spatially.

- Data quality and usage notes
  - The dataset integrates multiple corrections (frequency response, WPL, coordinate rotation) and gap-filling to enable robust analyses of fluxes.
  - Time lags between gas sensors and sonic anemometer are explicitly estimated and applied.
  - Spike removal and outlier handling follow a defined statistical approach to minimize distortions.
  - Users should consider the 80% footprint definitions when linking fluxes to land cover types and spatial variability.
  - Land cover data provide context for interpreting flux variability related to vegetation type and structure.

- References
  - Key methodological and software references for eddy covariance analysis, gap-filling, footprint modeling, and flux corrections (Aubinet et al.; Burba; Clement; Falge et al.; Kljun et al.; Reichstein et al.; Tukey; Webb et al.).