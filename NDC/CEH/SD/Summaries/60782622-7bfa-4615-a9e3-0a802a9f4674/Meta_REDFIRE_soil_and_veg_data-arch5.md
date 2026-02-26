# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Dataset describing soil and vegetation radionuclide activity concentrations and calculated dose rates at the Red Forest, Chernobyl, Ukraine, for 2016–2017.
- Contains extensive plot-level metadata, vegetation and soil sampling results, and dose-rate calculations across multiple isotopes and matrices.

## Data contents and structure
- Plot and location data
  - Plot_number, Plot_location, Northing, Easting
  - Plot_pine_forest_past_history (whether the area around the plot was pine forest in the past)
  - Plot_burn_score_2016 (2016 burn assessment)
- Environmental measurements
  - Ambient_dose_rate_September_2016_µSv_per_h
  - Ambient_dose_rate_March_2017_µSv_per_h
- Sampling and sample characteristics
  - Date_of_vegetation_and_soil_sampling
  - Grassy_vegetation_sample_FM_g, Grassy_vegetation_sample_DM_g, Grassy_vegetation_sample_DM_as_fraction
  - Other_vegetation_sample_FM_g, Other_vegetation_sample_DM_g
  - Soil_%_DM_in_March_2017, Soil_%_DM_in_September_2017, Soil_pH_September_2017, Soil_%_LOI_September_2017
  - n/a data not available indicators for incomplete fields; a DM fraction for plot 11.3 was estimated from neighboring plots
- Isotope-specific activity concentrations
  - Grassy vegetation (DM and FM): Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240; includes uncertainties
  - Tree-related samples: Cs-137, Am-241, Pu-238, Pu-239, Pu-240 (FM and/or DM where applicable)
  - Soil samples (DM): Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240
  - Total and per-isotope columns for grassy vegetation, tree, soil, bacteria where applicable
  - Some concentrations are predicted values (e.g., Am-241 and Pu isotopes for grassy vegetation and trees)
- Dose rate calculations
  - Internal and external weighted absorbed dose rates per isotope for grassy vegetation, tree, soil, bacteria
  - Total weighted absorbed dose rates per matrix and overall totals (e.g., total for grassy vegetation, tree, soil, bacteria; and overall totals)
  - Units: µGy per hour (for dose rates), with ambient rates provided in µSv per hour
- Transfer parameters and methodology notes
  - Use of CR_wo-soil transfer parameters for Agrostis gigantea (grassy vegetation) and Pinus sylvestris (wood) from Beresford et al. 2020
  - Tree transfer parameters for Sr-90 and Cs-137 from CEZ (Ukrainian site) data
  - Explicit notes linking to literature and data sources for transfer coefficients
- Documentation and caveats
  - n/a fields indicate data not available
  - Some values (e.g., plot 11.3 DM fraction) estimated from related plots
  - Several dose-related values are described as predicted or modeled rather than directly measured

## Metadata, provenance and methods
- Sampling period: 2016–2017 with specific sampling dates (date fields present)
- Measurements and calculations
  - Fresh mass (FM) and dry mass (DM) measures used for vegetation samples
  - Soil properties include DM percentage, LOI, pH
  - Dose-rate calculations include weighted contributions from internal and external pathways across multiple isotopes and matrices
- Data lineage and references
  - Transfer parameters and methodology grounded in published studies (e.g., Beresford et al. 2020; J Environ Radio)
  - Tree parameter data referenced to Ukrainian CEZ site data
  - Notes indicate transfer parameter sources and relevant DOIs/links

## Data quality, challenges and governance considerations
- Completeness and gaps
  - Numerous fields marked as not available (n/a), indicating incomplete data coverage
  - Some concentrations and dose rates are predicted rather than measured
- Data consistency and units
  - Consistent use of units (Bq/kg DM/FM for activity concentrations; µGy/h or µSv/h for dose rates)
  - Clear documentation of when DM vs FM values are used
- Data curation needs
  - Maintain a comprehensive data dictionary and metadata to document field meanings, units, and any estimations
  - Track data provenance, versioning, and any imputed values (e.g., DM fraction for plot 11.3)
  - Clearly flag predicted vs measured values and cite the underlying sources
- Interoperability and reuse
  - Complex naming conventions and mix of measured/predicted fields may require harmonization for cross-dataset reuse
  - Documentation of transfer parameters and calculation methods essential for reproducibility

## Sharing, licensing and reuse considerations
- The dataset appears designed for radiological risk assessment and ecological dose modeling
- Users should consult referenced literature for transfer parameters and methodological context
- Licensing and access terms are not provided in the text; confirm data use permissions and citation requirements with the data publisher

## References and sources
- Beresford et al. 2020; https://doi.org/10.1016/j.jenvrad.2018.02.007
- CEZ Ukrainian site data: https://doi.org/10.15407/jnpae2020.03.256