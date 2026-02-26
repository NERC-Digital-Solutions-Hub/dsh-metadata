# High-resolution ammonia concentration data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Data collection and purpose
- Ammonia (NH3) enhancement experiment conducted in the Glencorse woodland near Edinburgh to study effects on forest vegetation, bryophytes, lichens, and soil.
- Location: Glencorse woodland (approx. 55.8539°N, -3.2151°W; altitude ~200 m).
- Experiment designed to release NH3 only when wind conditions (below canopy) meet specified direction (275–345°) and threshold speeds (0.3–10 m s^-1) to study plume movement.

## Experimental setup and release mechanism
- NH3 release system comprises three 20 m long PVC tubes arranged parallel, with release holes every 20 cm around the circumference.
- Release is driven by a fan that creates positive pressure into the tubes; NH3 is supplied from a cylinder through a mass flow controller (MFC) and a solenoid valve, injecting into the fan airflow.
- Activation occurs only under correct wind conditions and is regulated by the solenoid valve.

## Measurement system and sampling design
- NH3/H2O analyser: Picarro G2123, located ~10 m downwind of the release system; housed in a custom air-conditioned enclosure.
- Sampling heights: 0.5 m, 1.0 m, 1.5 m, and 2.5 m above ground, using a custom sampling system.
- Data collection: four heights sampled sequentially for 2 minutes each per campaign; sampling performed under automatic control (LabVIEW).
- Inlet system: 5.5 m PTFE tubing per inlet, heated to ~40 ± 3 °C to minimize adsorption/desorption delays; continuous purge flow with changes in flow during sampling.
- Data frequency: NH3 concentrations recorded at 10 Hz, averaged to 0.016 Hz intervals; all timestamps in GMT.

## Data handling, quality control, and processing
- Quality control performed visually; obvious instrument/mislogging/power issues removed.
- Gaps during valve switching filled by linear interpolation.
- Lag effects acknowledged due to NH3 adsorption/desorption at inlets; heating may volatilize some NH4NO3, contributing to a relatively constant background.

## Data structure and contents
- Dataset contains 97,378 measurements across 6 parameters.
- Data format: CSV with columns including:
  - Timestamp (date/time)
  - NH3_status (valve type)
  - NH3_flow (slpm; from MFC)
  - Wind_speed (ms^-1; below-canopy instruments)
  - Wind_direction (degrees; below-canopy instruments)
  - NH3_conc (ppb; from G2123 and Picarro)
  - Inlet_height (m; measurement height)
- Instrument sources noted for each parameter (e.g., G2123, Picarro, WXT536, Vaisala).

## Data timeline and availability
- Sampling campaigns occurred on:
  - 16 Sept – 23 Sept 2021
  - 28 Sept – 1 Oct 2021
  - 6 – 10 Oct 2021
  - 3 – 9 Nov 2021
  - 10 Aug – 27 Sept 2022
- Complete details of experimental design, methodology, analysis, and findings are published in Deshpande et al. (2024).

## Funding
- Funding provided by the UKRI Global Challenges Research Fund (GCRF) South Asian Nitrogen Hub.

## References
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.

## Relevance for monitoring frameworks
- Provides high-resolution, wind-controlled NH3 concentration data suitable for evaluating atmospheric deposition and plume dynamics in forested environments.
- Demonstrates a structured data collection approach with clearly defined metadata, instrumentation, and sampling regimes.
- Highlights data quality considerations, including lag from inlet adsorption/desorption and background volatilization, relevant for interpreting environmental health measures.
- Useful for validating or calibrating monitoring models and informing future data governance, metadata completeness, and data sharing practices to support policy scrutiny and decision-making.