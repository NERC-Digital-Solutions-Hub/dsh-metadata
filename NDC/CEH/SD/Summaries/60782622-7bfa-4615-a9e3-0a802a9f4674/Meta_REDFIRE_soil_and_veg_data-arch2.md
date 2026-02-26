# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Provides soil and vegetation radionuclide activity concentrations and calculated dose rates for the Red Forest near Chernobyl, Ukraine, covering 2016–2017.
- Data intended to support environmental health assessment and monitoring of policy-relevant outcomes over time.
- Exhibits plot-level metadata, sampling details, radionuclide measurements across grassy vegetation, deciduous tree wood, and soil, plus dose-rate calculations.

## Data structure and scope
- Plot-level metadata: plot number and location; Northing and Easting coordinates; historical context of pine forest presence.
- Environmental conditions: burn score for 2016; ambient dose rates measured in September 2016 and March 2017.
- Sampling information: date of vegetation and soil sampling; fresh mass (FM) and dry mass (DM) for grassy vegetation and other vegetation; DM/ FM fractions and related notes (with some DM fractions estimated where missing).
- Matrices measured: grassy vegetation, other vegetation, and soil samples (DM and FM where applicable).
- Radionuclides measured: Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240 (with some Am-241 and Pu isotopes estimated for certain matrices using site-specific transfer parameters).
- Dose-rate calculations: weighted absorbed internal and external dose rates; total weighted absorbed dose rates for grassy vegetation, tree wood, and other biological and environmental components (including bacteria) across specific isotopes and aggregations.
- Uncertainty reporting: measurement uncertainties provided for key isotopes (K=1.96) for specific grassy vegetation concentrations; several entries flagged as not available (n/a).
- Transfer parameters: use of CR wo-soil transfer parameters for Agrostis gigantea and Pinus sylvestris (wood) where applicable; Cs-137 and Sr-90 tree transfer parameters referenced from Ukrainian sources.

## Key variables and measurements
- Plot identifiers and location: Plot_number, Plot_location, Northing, Easting.
- Vegetation history and condition: Plot_pine_forest_past_history, Plot_burn_score_2016.
- Ambient dose rates: Ambient_dose_rate_September_2016_µSv_per_h, Ambient_dose_rate_March_2017_µSv_per_h.
- Sampling metadata: Date_of_vegetation_and_soil_sampling; Grassy_vegetation_sample_FM_g; Grassy_vegetation_sample_DM_g; Grassy_vegetation_sample_DM_fraction; Other_vegetation_sample_FM_g; Other_vegetation_sample_DM_g; Soil_DM_percentage_March_2017; Soil_DM_percentage_September_2017; Soil_pH_September_2017; Soil_LOI_September_2017.
- Activity concentrations (dried mass and fresh mass): Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240 for grassy vegetation (DM and FM), tree wood (FM), and soil (DM).
- Uncertainties: Activity_concentration_uncertainty values for grassy vegetation isotopes (Sr-90, Cs-137, Am-241, Pu isotopes) where provided.
- Dose-rate calculations: Weighted_absorbed_internal_dose_rate and Weighted_absorbed_external_dose_rate for each isotope and substrate (grassy vegetation, tree wood, soil-associated categories); Total_weighted_absorbed_dose_rate for combined matrices and for bacteria where applicable; Totals across isotopes for grassy vegetation, tree, and general measurements.
- Data quality notes: Several fields marked as n/a (data not available); DM fractions for plot 11.3 estimated from plots 11.1 and 11.2; some predicted activity concentrations are noted for Am-241 and Pu isotopes in grassy vegetation and tree wood.

## Sampling context and methods
- Sampling occurred in the Red Forest (CEZ), with soil and vegetation collected and analyzed for activity concentrations and related mass metrics.
- Transfer parameter references indicate use of site-specific relationships derived from Beresford et al. 2020 and Ukrainian sources for tree and soil transfers, enabling calculation of activity concentrations in vegetation from soil measurements where direct measurements were not available.

## Notable data features and caveats
- Some data fields are not available (n/a), and certain DM fractions or activity concentrations are estimated rather than measured.
- Uncertainties are provided for selected grassy vegetation measurements (K=1.96); other uncertainties are not specified in the excerpt.
- Explicit notes indicate the methodologies for estimating Am-241 and Pu isotopes in grasses and pine wood based on site-specific transfer parameters.

## Data provenance and references
- Transfer parameters and methodological references:
  - Am-241 and Pu isotopes in grassy vegetation and Pinus sylvestris (wood) transferred with CR wo-soil parameters from Beresford et al. 2020 (doi provided).
  - Sr-90 and Cs-137 tree transfer parameters (deciduous trees) from Ukrainian sources (JNPAE 2020) alongside measured soil concentrations.
- Data context aligns with environmental radiological monitoring and modelling practices for contaminated forest ecosystems.

## Potential uses for analysts monitoring the environment
- Validation and quality assurance of environmental radiological monitoring data across time (2016–2017) in the CEZ.
- Standardized outputs for maps, charts, and dashboards to illustrate spatial and temporal trends in radionuclide activity and dose rates.
- Integration with other environmental datasets to enhance the value of datasets beyond single-use analyses.
- Enabling broader data access and reuse by providing comprehensive plot-level metadata, measurement details, and dose calculations.
- Supporting policy-performance assessments related to environmental contamination, remediation progress, and ecological risk characterization.

## Data gaps and considerations for interpretation
- Several fields are marked n/a; interpret with caution where data are missing or estimated.
- Uncertainty information is limited to certain grassy vegetation measurements; propagating uncertainties through dose calculations will require careful consideration.
- Dependence on transfer parameters from external studies introduces model-based assumptions for Am-241 and Pu isotopes in vegetation and trees.