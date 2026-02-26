# A set of 14400 summaries of mainland GB peak river flow data describing widespread flooding events as modelled using the Grid-to-Grid hydrological model and UKCP18 meteorological data based on RCP8.5 for 12 members of a perturbed parameter ensemble

## Overview
- Dataset comprises 14,400 event summaries describing widespread flooding events across mainland Great Britain.
- Generated using the Grid-to-Grid hydrological model driven by UKCP18 12-member perturbed parameter ensemble (PPE) of the Hadley Centre 12km Regional Climate Model (RCM).
- Covers two time-slices: present day (1981-2010) and future (2051-2080), based on RCP8.5 scenario.
- Created under the UK Climate Resilience AquaCAT project; authors include UKCEH and collaborators. Upload date: 2022-01-20 (Version 0.2).

## Data generation and scope
- Event generation and extraction:
  - Grid-to-Grid uses gridded precipitation, temperature, and potential evaporation as inputs.
  - Utilizes UKCP18 PPE (12 ensemble members) to drive the Grid-to-Grid model to produce gridded daily river-flow time series for baseline and future periods.
  - Events are national, spatially aggregated, and defined when at least 0.1% of the 1 km gridcells on the GB river network exceed a location-specific threshold T(x) and this condition is met twice per year on average.
  - An event is a sequence of consecutive days; only the timestep-wise maxima across the event duration are retained.
  - Each event records flow for every gridcell on the river network (not limited to cells exceeding the threshold).
- Data representation:
  - 360-day model years for the RCM.

## Data structure and file naming
- For each of the 12 ensemble members and two time periods, there is a NetCDF file named:
  - G2G_events_RCMXX_YSTART_YEND.nc
  - XX: ensemble member number (01–15, excluding 02, 03, and 14)
  - YSTART/YEND: 198012 to 201011 (present) or 205012 to 208011 (future)
- Contents of each file:
  - Flow: maximum flow (m^3/s) observed at a given location over an event duration.
  - Annual probability of exceedance (APoE): probability that a given flow value is exceeded in any year.
  - Daily probabilities derived from empirical daily flow distributions; Poisson approximation used to compute annual probabilities.
  - Locations defined by GB National Grid Northings/Eastings (in meters).
  - Flow is recorded only on the river network; land gridcells marked -1; sea gridcells missing.

## NetCDF metadata and summary information
- Global attributes:
  - RCM: 04
  - period: 198012_201011
  - event_threshold: Annual prob of exceedence < 0.865
  - area_lower_limit: 0.1% minimum coverage
- Summary information per event (in summary_RCM**_****12_****11.csv):
  - Nominal starting day (based on 30/360-day years)
  - Event ID number
  - Event length (days)
  - Maximum Annual Probability of Exceedance across the event
  - Area (km^2) exceeding POT2 threshold (flow > threshold, exceeded twice a year on average at any point during the event)
  - Nominal season: DJF (Winter), MAM (Spring), JJA (Summer), SON (Autumn)

## Variables, units, and data encoding
- Flow values: maximum within each event (m^3/s)
- Annual and daily exceedance probabilities: unitless (probability)
- Location coordinates: Northings and Eastings (meters) on the GB National Grid
- Data encoding notes:
  - Flow values stored for river-network gridcells; non-river cells set to -1 or missing as appropriate
  - 360-day year usage noted; timestep and seasonal labeling aligned to standard season conventions

## Access, provenance, and related work
- Authors: Alison Kay, Vicky Bell, Adam Griffin, Lisa Stewart (UK Centre for Ecology & Hydrology); Paul Sayers, Sam Carr (Sayers and Partners LLP)
- Funders: UK Climate Resilience AquaCAT project
- Related literature and in-prep references detailing methodology and applications:
  - Widespread flooding events under climate change using a UKCP18 ensemble (in prep)
  - Comparison of statistical methods for widespread flooding events under climate change (in prep)
  - Event-based climate change risk assessment – spatial coherence in fluvial flood risk (in prep)
  - Foundational methods: use of grid-based hydrological model with RCM outputs; UKCP18 land projections methodology

## Data governance and stewardship considerations
- Governance focus for Data Stewards:
  - Ensure metadata quality and completeness across all 12 ensemble members and both time periods; verify consistency of naming conventions and file contents.
  - Maintain provenance: include authors, funders, upload date, and version (v0.2) for traceability.
  - Document data model decisions (threshold T(x), grid resolution, 360-day year assumption, POT2 threshold, event definition) to aid reproducibility and user understanding.
  - Manage accessibility and discoverability via standardized repository structure; ensure clear guidance on how to interpret maximum-event flows, APoE, and area metrics.
  - Assess data availability and limitations:
    - Large, multi-file NetCDF dataset across 12 ensemble members and two periods; plan for storage, access latency, and data transfer considerations.
    - Threshold-based event definitions and model-driven data may imply uncertainties; provide guidance on uncertainty interpretation and how PPE variations influence results.
    - No explicit licensing details in the summary metadata; confirm licensing and usage rights with authors or data stewards before redistribution.
  - Establish update and versioning strategy if future revisions or additional ensemble members are released; record changes in summary information and global attributes.
  - Link to related publications and preprints to support users in understanding the methodology and limitations.

## References (projects and related work)
- Griffin, A.; Stewart, E.; Kay, A.; Sayers, P.; Carr, S. (in prep). Widespread flooding events under climate change using a UKCP18 ensemble. To be submitted to HESS.
- Griffin, A.; Stewart, E.; Kay, A.; Sayers, P.; Carr, S. (in prep). Comparison of statistical simulation methods for widespread flooding events in the UK under climate change. To be submitted to Hydrology Research.
- Sayers, P.; Carr, S.; Griffin, A.; Stewart, E.; Kay, A.; Bell, V. (in prep). Event-based climate change risk assessment – Exploring the impact of changing spatial coherence on fluvial flood risk in the UK. To be submitted to Journal of Flood Risk Management.
- Bell, V.A.; Kay, A.L.; Jones, R.G.; Moore, R.J.; Yamazaki, K. (2007). Use of a grid-based hydrological model and regional climate model outputs to assess changing flood risk. Int. J. Climatol. 27, 1657-1671.
- Murphy, J.; Harris, G.; Sexton, D.; Kendon, E.; Bett, P.; Clark, R.; Yamazaki, K. (2019). UKCP18 land projections: science report. Met Office.