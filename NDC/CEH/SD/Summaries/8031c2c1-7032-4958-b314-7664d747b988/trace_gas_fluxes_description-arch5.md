# Supporting Documentation

- Documents three Hampshire Avon trace gas flux datasets derived from experimentally manipulated plots in three sub-catchments.
- Datasets and depositor details:
  - Datasets: gasflux_chalk.csv, gasflux_clay.csv, gasflux_greensand.csv
  - Depositor: James Stockdale (contact: james.stockdale@york.ac.uk)
- File-level metadata highlights provided for each dataset (From/To dates, description, location).

## Datasets and Depositors

- Datasets
  - gasflux_chalk.csv: CO2, CH4, and N2O fluxes from lysimeters; location OS Grid ST 85862 38261; From 04Aug2015; To unspecified.
  - gasflux_clay.csv: CO2, CH4, and N2O fluxes from lysimeters; location OS Grid ST 92218 27263; From 04Mar2015; To 04Aug2015.
  - gasflux_greensand.csv: CO2 and CH4 fluxes from lysimeters; location OS Grid SU 09720 57896; From unspecified; To 01Sep2015.
- Depositor and contact
  - Primary contact: James Stockdale (james.stockdale@york.ac.uk)

## Dataset Structure

- All three files share the same CSV format and variables (specific variables not listed in the summary).
- Purpose: provide time-resolved greenhouse gas flux measurements from lysimeters across three geologies in the Hampshire Avon catchment.

## Methods and Measurement Details

- Platform and approach
  - Near-continuous measurements using a SkyLine2D suspended mobile platform with non-steady state chambers.
  - Lysimeter-based, intact monolith soils and vegetation from unimproved pastures; three underlying geologies.
- Instrumentation
  - CO2: Infra-red gas analyser (Li-Cor 8100, model 8100).
  - CH4: Fast Greenhouse Gas Analyzer (FGGA; model 907-0010).
  - N2O: Isotopic N2O Analyzer (INA; model 914-0027).
- Measurement protocol
  - Flux measurements: 180-second chamber closures; campaign-mode CH4/N2O extended to 300 seconds.
  - CO2 fluxes: deadband of 60 seconds; calculated using Li-Cor software (v2.0.0) with post-flux quality control.
  - CH4/N2O fluxes: calculated by linear regression with similar quality control to CO2.
- Quality control and filtering
  - CO2: remove poorly fitted slopes (R^2 < 0.7) or highly variable fluxes (CV > 50%) not close to zero (-0.5 to 0.5 µmol CO2 m^-2 s^-1).
  - CH4 and N2O: quality-controlled with criteria analogous to CO2 fluxes.
- Data interpretation
  - Fluxes reported as calculated from the described regression approaches; QC-dominated filtering applied to ensure reliability.

## Data Governance and Stewardship Considerations

- Metadata and discoverability
  - Ensure a unified metadata record for all three files, including dataset name, depositor, contact, date ranges, locations, methods, instruments, units, and QC criteria.
- Data availability and embargo
  - From/To fields indicate coverage windows; some records have missing end or start dates. Confirm data availability status, embargo conditions, and update timelines.
- Data quality and provenance
  - Document data processing steps (raw vs. processed fluxes), QC decisions, and software versions (e.g., Li-Cor v2.0.0) to enable traceability.
- Standards and interoperability
  - Align metadata with standard data governance schemas for environmental flux data to facilitate interoperability across portals.
- Storage, versioning, and sharing
  - Upload to appropriate data portals and catalog holdings; implement versioning and change logs; plan for updates when new measurements or corrections arise.
- Responsibilities and contact
  - Maintain depositor contact information for inquiries and data requests; consider assigning a steward for ongoing data updates and metadata curation.

## Actionable Recommendations for Data Stewards

- Validate and complete missing date fields (From/To) for all datasets; publish a consistent coverage window.
- Create and publish a single, cohesive metadata record encompassing all three files (structure, units, methods, QC criteria, and provenance).
- Record and expose detailed variable definitions, units, and data transformation steps used in flux calculations.
- Preserve raw measurements alongside processed fluxes, with clear documentation of QC filters applied.
- Establish a clear data update workflow and embargo policy, including versioning and change logs.