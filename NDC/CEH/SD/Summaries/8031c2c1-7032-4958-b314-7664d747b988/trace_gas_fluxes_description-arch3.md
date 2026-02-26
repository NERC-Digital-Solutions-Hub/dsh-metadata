# Supporting Documentation

## Part One: File summary
- Datasets involved: gasflux_chalk.csv, gasflux_clay.csv, gasflux_greensand.csv (two dataset titles referenced; depositor is James Stockdale with contact provided).
- Depositor/contact: James Stockdale; james.stockdale@york.ac.uk.
- Dataset specifics:
  - gasflux_chalk.csv: Location OS Grid Reference ST 85862 38261; Description: CO2, CH4, and N2O fluxes from lysimeters measured using an automated chamber method; From date noted as 04 Aug 2015.
  - gasflux_clay.csv: Location OS Grid Reference ST 92218 27263; Description: CO2, CH4, and N2O fluxes from lysimeters measured using an automated chamber method; From 04 Mar 2015 to 04 Aug 2015.
  - gasflux_greensand.csv: Location OS Grid Reference SU 09720 57896; Description: CO2 and CH4 fluxes from lysimeters measured using an automated chamber method; From 17 Mar 2015 to 01 Sep 2015.

## Part Two: Dataset structure
- All three files share the same CSV format and structure.
- The dataset comprises the same type of variables across files (exact variable list not provided in excerpt).

## Part Three: Methods summary
- Measurement approach:
  - Near-continuous greenhouse gas measurements using a novel suspended mobile platform (SkyLine2D) and sequential automated measurements across plots at each site.
  - Non-steady-state chamber technique used for flux measurements.
- Study context:
  - Lysimeters containing intact monoliths of soils and vegetation from unimproved pastures across three different underlying geologies in the Hampshire Avon catchment.
- Instruments and flux types:
  - CO2: Infra-red gas analyser (IRGA; Li-Cor 8100, model 8100).
  - CH4: Campaign-mode measurements with Fast Greenhouse Gas Analyzer (FGGA; model 907-0010; Los Gatos Research).
  - N2O: Campaign-mode measurements with Isotopic N2O Analyzer (INA; model 914-0027; Los Gatos Research).
- Measurement protocol:
  - Chamber closure duration: 180 seconds (except campaign-mode periods extended to 300 seconds).
  - CO2 flux calculation: Li-Cor 8100 software (version 2.0.0) with a deadband of 60 seconds and post-flux quality control.
  - Quality control for CO2: remove poorly fitted slopes (R^2 < 0.7) or highly variable fluxes (CV > 50%) not near zero (fluxes between -0.5 and 0.5 µmol CO2 m^-2 s^-1).
  - CH4 and N2O fluxes: calculated using linear regression with a similar QC approach to CO2.
- Data processing and quality:
  - Flux calculations include post-processing quality checks to ensure reliability.
  - Data are collected from plots across sites with specified geographic coordinates, enabling traceability to locations and geology.