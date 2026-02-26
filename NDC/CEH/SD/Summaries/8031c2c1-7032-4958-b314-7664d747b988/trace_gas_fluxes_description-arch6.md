# Supporting Documentation

## Dataset Overview
- Focus: Hampshire Avon trace gas fluxes from experimentally manipulated plots in three sub-catchments.
- Included datasets: gasflux_chalk.csv, gasflux_clay.csv, gasflux_greensand.csv.
  - gasflux_chalk.csv: CO2, CH4 and N2O fluxes; location OS Grid Reference ST 85862 38261; From 04Aug2015; description notes automated chamber method.
  - gasflux_clay.csv: CO2, CH4 and N2O fluxes; location OS Grid Reference ST 92218 27263; From 04Mar2015 to 04Aug2015; description notes automated chamber method.
  - gasflux_greensand.csv: CO2 and CH4 fluxes; location OS Grid Reference SU 09720 57896; From 17Mar2015 to 01Sep2015; description notes automated chamber method.
- Depositors: Named in the documentation; Primary contact: James Stockdale (james.stockdale@york.ac.uk).

## Datasets Included
- All three files share the same CSV format and structure (uniform data layout across sites).
- Datasets capture trace gas fluxes from lysimeters containing intact monoliths of soils and vegetation in unimproved pastures across three geologies.

## Dataset Structure
- All three CSV files use the same variable set (as noted in Part Two: Dataset structure). Specific variable names are not enumerated in the summary.

## Methods and Instrumentation
- Measurement approach: Near-continuous, combining gas analysers with a purpose-built suspended mobile platform (SkyLine2D) and a non-steady state chamber.
- Sites and plots: Three sites within the Hampshire Avon catchment, representing different underlying geologies.
- Gases and instruments:
  - CO2: Measured continuously using an infrared gas analyser (IRGA; Li-Cor 8100, model 8100).
  - CH4 and N2O: Measured in campaign-mode using cavity-enhanced absorption spectrometers (FGGA for CH4; INA for N2O; both from Los Gatos Research).
- Measurement protocol:
  - Chamber closure: 180 seconds for standard measurements; extended to 300 seconds in campaign-mode.
  - Deadband: 60 seconds for CO2 measurements.
  - Flux calculation:
    - CO2: Calculated with Li-Cor software (version 2.0.0) and post-flux quality control.
    - CH4 and N2O: Fluxes calculated by linear regression, with QC similar to CO2.

## Data Quality Control
- CO2 QC criteria:
  - Exclude if r^2 < 0.7 for slope fit.
  - Exclude if coefficient of variation (CV) > 50%.
  - Exclude if fluxes are between -0.5 and 0.5 µmol CO2 m^-2 s^-1 (not close to zero).
- CH4 and N2O QC criteria: Linear-regression-derived fluxes subjected to similar quality checks as CO2.
- QC aims to remove poorly fitted or highly variable flux measurements to ensure reliable flux estimates.

## Location and Provenance
- Three sub-catchment sites with distinct underlying geologies in the Hampshire Avon catchment.
- Precise OS grid references provided for each site:
  - Chalk site: ST 85862 38261
  - Clay site: ST 92218 27263
  - Greensand site: SU 09720 57896

## Access and Contact
- Depositor information provided (Name and Contact details available in the dataset metadata).
- Primary contact for data inquiries: James Stockdale (james.stockdale@york.ac.uk).

## Notes and Considerations for Use
- Data comprise data from three sites with different geologies, measured using a sophisticated near-continuous platform and a non-steady state chamber, requiring awareness of site-specific conditions and instrument configurations.
- Data are provided as CSVs with a uniform structure; users should confirm variable definitions from Part Two (Dataset structure) when integrating into analyses.
- Patchy or partial periods may exist given variable start/end dates across sites; verify time ranges before comparative analyses.
- Encouraged practices include verifying data quality via the stated QC criteria and contacting the depositor for any data clarification or access questions.