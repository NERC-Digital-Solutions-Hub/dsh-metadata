# Nitrous oxide emission factors of mineral fertilisers in the UK and Ireland: experimental data for the period (1998 - 2019)

## Overview
- Compiles 641 mineral fertiliser N2O emission factor (EF) estimates from 38 experimental sites across the UK and Ireland (1998–2019).
- EF estimates derive from field measurements; breakdown by fertiliser type: 293 for ammonium nitrate (AN), 63 for calcium ammonium nitrate (CAN), 118 for urea.
- Additional EF counts include 38 for AN or CAN with nitrification inhibitor DCD, and 129 for urea with DCD or NBTP (a urease inhibitor).
- Most data collected via flux chamber measurements; one study used eddy covariance.
- Primary aim: to support a Bayesian analysis of EF, examining differences by fertiliser type and field management, and to establish a prior distribution for future EF work.

## Data coverage and scope
- Period: 1998–2019.
- Geography: United Kingdom and Republic of Ireland.
- Fertiliser types and treatments:
  - AN, CAN, Urea.
  - Inhibitors: DCD, MIP (a polymer), NBTP (or NA for none).
  - Some datasets attribute multiple inhibitors to the same treatment.
- Measurement approach: predominantly flux chambers; one study used eddy covariance.
- Data assembled to enable Bayesian upscaling of N2O fluxes post-fertilisation and to inform priors for future EF analyses.

## Data collection and provenance
- Data sources:
  - Published studies explicitly measuring N2O and reporting EF after fertiliser application.
  - Raw data from the Agricultural and Environmental Data Archive (AEDA), recalculated to EF metrics.
- Data gathering process:
  - Literature search for articles published after January 1998 and before April 2019, using N2O, emission factor, mineral fertiliser, nitrification inhibitors, etc.
  - AEDA data used to calculate EFs for 25 days post-application using a log-normal Bayesian approach (accounts for log-normal spatial/temporal distribution of N2O fluxes).
- References include a broad set of studies (e.g., Abdalla 2009; Baggs 2003; Bell 2015; Cowan et al. 2019a/2019b; Dobbie & Smith 2003; Smith et al. 2012; and many others).

## Data structure and variables
- File: Farm_Flux_and_Soil
- Key fields:
  - Year = Location: Year and location of experiment (UK or Ireland).
  - Year = Country: Country-level definition (England, Republic of Ireland, Northern Ireland, Scotland, Wales).
  - Year = Fertiliser: Fertiliser type (AN, CAN, Urea).
  - Year = Inhib: Inhibitor type (DCD, MIP, NBTP; NA if none).
  - Year = Amount applied: Amount of fertiliser applied (kg N).
  - Year = Applications: Number of fertiliser applications.
  - Year = Mean_N_app: Average mass of N applied per fertiliser event.
  - Year = Field_manage: Field management (Arable or Grass).
  - Year = Crop_Type: Type of crop grown.
  - Year = Meas. Method: Measurement method (Manual chamber or eddy covariance).
  - Year = EF: Emission factor (N2O emissions as a percentage of total N applied).
  - Year = Reference: Source of data.
- Data sources include both published EF datasets and recalculated AEDA entries, aligned to the same EF format.

## Methodology and use of the data
- Bayesian framework:
  - Data used to estimate emission factors and to generate prior distributions for EF in future work.
  - Log-normal Bayesian approach employed to calculate EFs from raw AEDA data, addressing spatial and temporal distribution of N2O fluxes after fertiliser events.
- Data units and interpretation:
  - EF expressed as a percentage of total nitrogen applied.
  - 25-day post-application window used for AEDA-derived EF calculations.
- Data are prepared to support comparisons across fertiliser types, inhibitors, field management, and measurement methods, with attention to variability and uncertainty in EF estimates.

## Data access, reuse, and documentation
- Data files referenced:
  - Farm_Flux_and_Soil (EF dataset, primary file for the study).
  - AEDA-derived and published EF data, with explicit lineage to original studies and InveN2Ory datasets by location and year (e.g., Bedfordshire 2011; Devon 2013; Ceredigion 2011–12; County Down 2012–13; Warwickshire 2013; Dumfries 2011; East Lothian 2011; etc.).
- Data provenance notes:
  - Free text in the dataset documents the source of each EF estimate (published study or AEDA-derived).
  - AEDA entries include DOIs and publisher attribution (Freshwater Biological Association) for traceability.
- Intended use:
  - Facilitates Bayesian inference for EF and supports the development of priors for future nitrous oxide emission work in UK and Ireland contexts.

## Considerations for analysts
- Data gaps and scale:
  - Potential lack of data at local scales or for certain fertiliser-inhibitor combinations.
- Data accessibility and harmonisation:
  - Data drawn from multiple sources with varying formats; careful cleaning and standardisation required.
- Study design and comparability:
  - Variation in measurement methods (flux chamber vs. eddy covariance) may influence EF estimates.
- Temporal and spatial variability:
  - Log-normal distribution of fluxes and temporal upscaling considerations addressed via the Bayesian approach.
- Data protection and reporting:
  - Greater attention to consistent metadata and clear documentation to improve discoverability and reuse, aligning with the archetype’s emphasis on data discoverability and governance.