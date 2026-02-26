# Ammonia concentration and deposition data from a peatland nitrogen pollution experiment, Whim Bog, Scotland, UK, 2002-2022

## Study overview
- Location: ombrotrophic bog at Whim Moss, near Edinburgh, Scotland (55.76566°, -3.27155°; altitude 316 m).
- Purpose: NH3 enhancement experiment to study effects of elevated atmospheric ammonia on vegetation, bryophytes, lichens, and soil.
- Setup: Enhancement system controlled by wind direction (180–215°) and wind speed (>2.5 m/s) to target monitoring quadrats.
- Timeframe: NH3 concentrations measured monthly from May 2002 to December 2022.
- Sampling: Lateral and vertical NH3 sampling locations updated during the study as needed.

## Data collection and measurements
- Instrumentation: UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers for NH3 concentrations.
- Sampling design: NH3 sampled along quadrats; locations changed over time.
- Output: 6296 measurements across 6 parameters, compiled into a CSV with monthly and case-specific data.

## Calculations and modeling of NH3 deposition
- Deposition model: Unidirectional resistance model estimating dry deposition to mixed moorland vegetation.
- Deposition flux: Fχ(z) = χa / Rt, where χa is ambient NH3 concentration at height z and Rt is total resistance.
- Resistance components:
  - Ra (aerodynamic resistance): derived from wind speed, friction velocity, and measurement/heights using height-dependent equations.
  - Rb (boundary-layer resistance): parameterized using Garland (1977) and Sutton et al. (1993) with Reynolds number Re*, Schmidt number Sc, and u*.
  - Rc (canopy resistance): daytime and nighttime formulations with constants A, B, Rbox; Rc depends on χ (adjusted concentration) during NH3 release periods.
- Special cases:
  - During NH3 release periods: 15-minute χ values computed from monthly averages; Rc is time-of-day dependent.
  - During no-release periods: Rc fixed at 20 s m^-1; Rt calculated with constant Ra and Rb.
- Time resolution: 15-minute concentrations during release periods; deposition flux calculated for each 15-minute interval and summed monthly.
- Data handling: CH3 data and deposition flux are validated and used to produce monthly deposition totals.

## Data structure and quality control
- Data structure: 6296 measurements of 6 parameters.
- Columns (CSV): Month, ID (sample label; E/W, Con/Amb), Distance (m; negative = upwind, positive = downwind), Height (m; above ground), NH3_conc (µg m^-3; 1 = monthly average NH3 conc), Dep_kg_ha (1 = monthly total NH3 deposition; 2 = monthly average deposition flux).
- NA handling: NA NH3_conc indicates missing concentration data (damaged/missing sampler); NA Dep_kg_ha indicates missing deposition data due to data gaps.
- Data quality: Visual QC to remove errors from instrument failure, damage, power cuts; monthly concentrations below ambient removed to avoid negative flux values; sampler changes caused intermittent missing values.

## Temporal coverage and locality details
- Spatial arrangement: Monitoring quadrats with east/west designations; distance from NH3 source indicates location relative to the release area.
- Temporal coverage: 2002–2022 with changes in sampling locations over time to support study requirements.

## Data availability and usage
- Data are provided in a CSV file with detailed metadata in the column descriptions, enabling reuse for analyses of NH3 concentration and dry deposition flux across space (distance from source) and time (monthly, 15-minute intervals during release periods).
- Researchers can leverage the data to examine correlations between ambient NH3, deposition flux, and environmental variables or to calibrate/validate deposition models.

## Funding
- Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme delivering National Capability.

## References (key related works)
- Cape et al. 2008; Fowler 1978; Garland 1977; Jones et al. 2007; Leith et al. 2004; Smith et al. 2000; Sutton et al. 1993; Tang et al. 2001; Wesely & Hicks 1977.