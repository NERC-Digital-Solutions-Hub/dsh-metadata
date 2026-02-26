# High-resolution ammonia concentration data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Scope and purpose
- Data from an NH3 enhancement experiment at the Glencorse woodland (Edinburgh area) to study ammonia effects on forest vegetation, bryophytes, lichens, and soil.
- Aimed at enabling analysis of NH3 concentrations, plume movement, and deposition under controlled release conditions.

## Data collection and experimental setup
- Location: Glencorse woodland (latitude 55.8539°, longitude -3.2151°, altitude 200 m).
- Experimental design: NH3 release only when wind conditions meet direction (275–345 degrees) and speed thresholds (0.3–10 m s^-1).
- Release system: Three horizontally laid 20 m PVC tubes at ground levels 0.5, 1.35, and 2.2 m; NH3 injected from a stainless steel line through a mass flow controller and solenoid valve into the air flow, with release through 6 holes per tube.
- Control and measurement downwind: A Picarro NH3/H2O analyzer located ~10 m downwind; air sampled at four heights (0.5, 1, 1.5, 2.5 m).
- Sampling system: Valve manifold controlled by LabVIEW; 2 minutes sampling per height; four 5.5 m PTFE inlets; inlet temperature maintained at ~40°C; purge flow 7 slpm during non-sampling and up to 12 slpm during sampling.
- Temporal coverage: Data collected across multiple campaigns in Sep–Nov 2021 and Aug–Sep 2022.
- Data timing: NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz intervals; timestamps in GMT.

## Quality control and data processing
- Visual quality checks performed; obvious instrument or data issues removed.
- Gaps arising from valve switching filled by linear interpolation.
- Acknowledged lag effects due to adsorption/desorption on inlet surfaces and switching between concentration regimes.
- Heating may cause some volatilisation of NH4NO3 aerosol, but expected to yield a smooth background NH3 signal.

## Data structure and metadata
- Dataset size: 97,378 measurements across 6 parameters.
- File format: CSV with columns including:
  - Timestamp (dd/mm/yyyy, 1-minute timestamps)
  - NH3_status (valve type and status indicators)
  - NH3_flow (through MFC into release manifold)
  - Wind_speed (below-canopy)
  - Wind_direction (below-canopy)
  - NH3_conc (NH3 concentration downwind)
  - Inlet_height (sampling height)
- Instrument metadata embedded in columns (manufacturers, sensors) to capture cross-instrument details.
- Data provenance and experimental methods are documented and linked to the accompanying publication.

## Access, licensing, and provenance
- Funded by the UKRI GCRF South Asian Nitrogen Hub.
- Primary publication for methodology and findings: Deshpande AG et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments (Atmos Environ, 2024). DOI provided.

## Practical considerations and caveats for use
- Temporal resolution: 10 Hz NH3 data averaged to 0.016 Hz; downstream analyses should account for this averaging.
- Potential lag and bias: adsorption/desorption in inlet lines and switching effects may introduce lag relative to actual concentration changes.
- Data gaps: interpolated over valve-switch gaps, so users should treat interpolated sections accordingly.
- Measurement context: results are tied to controlled release conditions and may not generalize beyond the experimental setup without considering wind and release controls.
- Data stewardship notes: ensure ongoing updates and clear linkage to the 2024 Atmos Environ article for full methodology and analysis context.

## Key references
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.