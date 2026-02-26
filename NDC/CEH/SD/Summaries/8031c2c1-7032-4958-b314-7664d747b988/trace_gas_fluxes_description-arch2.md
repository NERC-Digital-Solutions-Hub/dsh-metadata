# Supporting Documentation

## Overview
- Documents Hampshire Avon trace gas flux datasets from experimentally manipulated plots across three sub-catchments.
- Provides dataset identifiers, depositors, contact, file-level summaries, structure, and detailed methods.
- Aims to support standardised, quality-assured data suitable for monitoring environmental health and policy performance, with potential for integration with other data sources and publication through appropriate portals.

## Datasets and Contacts
- Datasets:
  - Hampshire Avon: trace gas fluxes from experimentally manipulated plots in three sub-catchments (Dataset name 1)
  - Hampshire Avon: trace gas fluxes from experimentally manipulated plots in three sub-catchments (Dataset name 2)
- Depositor: James Stockdale
- Contact: james.stockdale@york.ac.uk

## Part One: File Summary
- gasflux_chalk.csv
  - Description: CO2, CH4 and N2O fluxes from lysimeters, measured using automated chamber method.
  - Location: OS Grid Reference ST 85862 38261
  - From/To: From 04Aug2015; To not specified
- gasflux_clay.csv
  - Description: CO2, CH4 and N2O fluxes from lysimeters, measured using automated chamber method.
  - Location: OS Grid Reference ST 92218 27263
  - From/To: From 04Mar2015; To 04Aug2015
- gasflux_greensand.csv
  - Description: CO2 and CH4 fluxes from lysimeters, measured using automated chamber method.
  - Location: OS Grid Reference SU 09720 57896
  - From/To: From not specified; To 01Sep2015

## Part Two: Dataset Structure
- All three files share the same CSV format and variables (exact variable list not provided in the summary).

## Part Three: Methods Summary
- Experimental setup
  - Near-continuous greenhouse gas measurements using a SkyLine2D suspended mobile platform.
  - Sequential, automated measurements of all plots per site with a non-steady state chamber.
  - Lysimeters contain intact soil and vegetation monoliths from unimproved pastures across three underlying geologies in the Hampshire Avon catchment.
- Measurements and instruments
  - CO2 fluxes: Infra-red gas analyser (IRGA) Li-Cor 8100 (model 8100).
  - CH4 fluxes: Campaign-mode measurements using Fast Greenhouse Gas Analyzer (FGGA; model 907-0010) by Los Gatos Research.
  - N2O fluxes: Campaign-mode measurements using Isotopic N2O Analyzer (INA; model 914-0027) by Los Gatos Research.
- Procedure and timing
  - Chamber closure duration: 180 seconds (adjusted to 300 seconds in campaign-mode).
  - CO2 deadband: 60 seconds.
  - Flux calculation and QC
    - CO2: calculated with Li-Cor 8100 software (v2.0.0); QC to remove poorly fitted slopes (R^2 < 0.7) or high variability (CV > 50%) when fluxes are not near zero (-0.5 to 0.5 µmol CO2 m^-2 s^-1).
    - CH4 and N2O: fluxes calculated via linear regression; QC applied similarly to CO2 fluxes.