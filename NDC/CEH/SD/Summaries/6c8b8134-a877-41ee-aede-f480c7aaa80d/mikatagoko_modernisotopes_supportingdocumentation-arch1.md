# Stable oxygen and hydrogen isotope composition of precipitation, river water and lake water in the Five Lakes of Mikata catchment, 2011-2012 and 2020-2022 - SUPPORTING DOCUMENTATION

## Overview
- Provides stable isotope data (δ18O, δ2H, and d-excess) for precipitation, river water, and lake water in the Five Lakes of Mikata catchment.
- Sampling periods: March 2011–January 2012 and July 2020–July 2022.
- Sample types and counts: 463 lake/river water samples (weekly) and 120 rainwater samples (event-based); six-depth water-column data for Lake Suigetsu on six dates during 2020–2022.
- Accompanying data include total precipitation and average temperature for each subsampling period, plus temperature and salinity profiles with depth in Lake Suigetsu.
- Aim: to determine if catchment water composition reflects East Asian Monsoon variability.

## Sampling and collection details
- Water samples (lake and river) collected weekly from Hasu River, Lake Mikata, and Lake Suigetsu between 1 Mar 2011–3 Jan 2012 and 15 Jul 2020–29 Jul 2022.
- Sampling method: submerging a collection vessel in the top ~50 cm of water; minimal headspace; algae filtered with 50 µm PET mesh if present.
- Sampling locations changed between intervals but within the same depth range to reflect average surface-lake conditions.
- Rainwater samples (n = 120) collected 13 Jul 2020–29 Jul 2022 in Wakasa using a 3D-printed funnel and glass bottle holder; silicon oil added to prevent evaporation; snow samples collected from pristine areas and melted with silicone oil.
- Meteorological data: automated Netatmo weather station for temperature, humidity, precipitation to accompany isotope data.
- Lake Suigetsu water-column profiling: six dates (Dec 2020, Apr 2021, Aug 2021, Nov 2021, Apr 2022, Jul 2022); water sampled every 2 m from surface to 10 m, every 5 m to 30 m, then every 2 m to 34 m; used sealable van Dorn sampler; temperature and salinity profiled with Hydrolab DS5; higher-resolution data for several dates.
- 2011–2012 surface data lack accompanying precipitation and water-column data due to pilot-study scope.

## Analytical methods
- Oxygen isotopes (δ18O): measured with Isoprime 100 mass spectrometer using CO2 equilibration. Subsamples (200 µl) equilibrated at 40 °C, trapped, then analyzed against CO2 reference with internal standards CA-HI and CA-LO; results expressed relative to VSMOW. Typical standard deviation < 0.05 ‰.
- Hydrogen isotopes (δ2H): measured in duplicate with TC-EA-IRMS (continuous flow, high-temperature conversion). Subsamples (0.5 µl) converted to water vapour, reduced to hydrogen gas, and analyzed against reference; samples measured five times. Standard deviation < 0.5 ‰.
- d-excess: calculated as δ2H − (8 × δ18O), used as a proxy for evaporation effects and moisture source deviations from the Global Meteoric Water Line.
- Calibration/reference: measurements tied to VSMOW; internal standards used for accuracy checks.

## Data structure and content
- Two CSV files:
  - mikatagoko_modernisotopes_results.csv: isotope data plus precipitation and temperature metrics.
    - Key fields include: Sample Type (LakeRiver/Rainwater/Column), Location (lake/area), Sampling Position (specific site codes), Sampling Depth (m, for water-column samples), Vessel Set/Sealed dates and times, Corrected δ18O and δ2H (with VSMOW2 scaling), d-excess, Total Precipitation (mm) and Average Temperature (°C) for the observation period, plus metadata for data batches.
  - lakesuigetsu_tempsalinity_results.csv: water temperature and salinity by depth and date.
    - Key fields include: Sampling Date, Sampling Depth (m), Water Temperature (°C), Water Salinity (%).
- Data organization notes: columns labeled with codes and units; detailed “Further Information” descriptions explain each field (e.g., nature of sample, sampling position, depth, and batch analysis).

## Quality control and data considerations
- Data corrected against laboratory standards; results influenced by precipitation composition, transit times through the catchment, lake–sea interactions, and minor evaporation.
- Sampling protocol accounted for access limitations (e.g., bridge repairs, snowfall, lake freezing); location changes deemed to minimally affect isotope values, as sampling remained within similar depth ranges and away from direct inputs.
- 2011–2012 precipitation and water-column data absent due to pilot-study scope; later periods include richer meteorological context via Netatmo data.

## Potential uses and considerations for analysis
- Assess how isotope signatures in precipitation, rivers, and lakes track East Asian Monsoon variability over two distinct periods.
- Investigate relationships between d-excess and monsoon-derived moisture sources or evaporation effects within the Mikata catchment.
- Use lake temperature and salinity profiles to contextualize isotope data with hydrological mixing and stratification dynamics.
- Compare contemporary (2020–2022) isotope patterns with earlier (2011–2012) data to identify potential shifts in moisture sources or catchment processes.
- Leverage the structured data fields for reproducible analyses, including data provenance (batches, sampling dates, and exact locations).