# Fluvial hydrochemistry, CO2  efflux and delta   13 C-Dissolved inorganic carbon data for the Houzhai Catchment, Southwest China, 2016-2018

## Overview
- Dataset from the NERC project "Addressing a significant knowledge gap in fluvial system atmospheric CO2 efflux: the contribution from karst landscapes" (NE/N002806/1).
- Location: Houzhai catchment, Guizhou Province, SW China; a typical karst landscape.
- Time period: 2016–2018.
- Measurements cover CO2 efflux from streams, springs, reservoirs, and ponds, plus associated water chemistry and stable isotope data (δ13C-DIC).
- Aims include quantifying CO2 efflux and understanding hydrological and chemical controls within a karst catchment.

## Data contents
- Data file: a single CSV named flux_and_13C_data containing 19 columns.
- Key variables:
  - F_CO2 and F_sd: CO2 efflux rate and its standard deviation (μmol CO2 m^-2 s^-1).
  - TA, DIC, pCO2_DIC, pCO2_TA: total alkalinity, dissolved inorganic carbon, and CO2 partial pressures calculated from DIC and TA.
  - T, pH, EC, DO: temperature, pH, electrical conductivity, dissolved oxygen.
  - Water_depth, Flow_velocity: hydrological measurements.
  - DIC_TA and d13C-DIC: DIC estimated from TA and δ13C of DIC respectively.
- Sampling cadence: mostly monthly, with intensive sampling during rainfall events.
- Stable isotope data: δ13C-DIC collected concurrently with flux measurements.
- Site metadata referenced in Table 1 (lat/long, site type).

## Study area and sites
- Houzhai catchment area: 73.4 km^2; humid subtropical monsoon climate; ~1140 mm precipitation; mean temp ~20.1°C; altitude 1,220–1,400 m.
- Geology: Middle Triassic limestones and dolomite.
- Monitoring sites include streams, springs, sinkholes, reservoirs/ponds; numerous site IDs and coordinates provided (e.g., types such as Spring, Sinkhole, Reservoir, Stream).

## Methods and quality assurance
- CO2 flux measurement: floating chamber method with a 0.0028 m^3 chamber; measurements over 4 minutes, three repeats; flux calculated from CO2 accumulation rate.
- Flow velocity: depth-averaged mean flow velocity using an impeller flow meter; depth-based averaging rules for shallow waters.
- Water chemistry and isotopes: at deployment, measure T and pH; collect water samples within 15 minutes of flux measurement for [DIC], δ13C-DIC, and TA using headspace and titration methods; DIC estimated from TA, pH, and equilibrium constants when needed.
- CO2 partial pressures: pCO2 calculated from DIC (and also from TA) using Henry’s law; cross-checks between DIC- and TA-derived pCO2.
- QA/QC: calibration with three isotopically distinct carbon standards; standard every 10 samples to correct instrument drift; methods for DIC and δ13C-DIC described and referenced.
- Data structure notes: some DIC values may be estimated from TA, pH, and constants; units explicitly stated for each variable.

## Data structure and metadata
- Primary data file: flux_and_13C_data (19 columns) with defined headers:
  - Sequence, ID, Type, Date, Time, F-CO2_, F_sd, TA, T, pH, EC, DO, Water_depth, Flow_velocity, DIC, DIC_TA, pCO2_DIC, pCO2_TA, d13C-DIC.
- Units: F-CO2 and F_sd in μmol m^-2 s^-1; TA and DIC in mmol L^-1; T in °C; pH unitless; EC in μS cm^-1; DO in mg L^-1; depths and velocities in m and m s^-1; pCO2 in μatm; d13C-DIC in ‰.
- Site-level metadata included via Table 1 with latitude, longitude, and site type (e.g., Spring, Sinkhole, Stream, Reservoir).

## Data provenance and references
- Project: NE/N002806/1 (karst-attributed CO2 efflux study).
- Related methodological references:
  - Waldron et al., 2014 (headspace method for DIC and δ13C-DIC).
  - Zhang et al., 2019 (conceptual modelling of karst catchment storage dynamics).
- Data documentation supports replication and re-use, with explicit measurement protocols and QA steps.

## Data access and governance considerations for Data Stewards
- Provenance is clearly documented (project title, methods, QA, site information).
- Metadata completeness supports discoverability and interoperability across datasets and portals.
- Note on data quality:
  - Some DIC values may be estimated rather than directly measured; treat as derived data with appropriate caveats.
  - Units and calculation methods are specified, but users may need to reproduce pCO2 from DIC/TA using Henry’s law constants for transparency.
- Governance implications:
  - Ensure appropriate data licensing and access rights are defined for reuse and redistribution.
  - Maintain versioning and update processes if additional data or corrections are added (intensive rainfall event data may lead to higher temporal resolution in some sites).