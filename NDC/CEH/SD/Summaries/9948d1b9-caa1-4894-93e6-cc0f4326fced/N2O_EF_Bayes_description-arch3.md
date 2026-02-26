# Nitrous oxide emission factors of mineral fertilisers in the UK and Ireland: experimental data for the period (1998 - 2019)

## Aim and scope
- Presents a compiled dataset of N2O emission factors (EFs) from mineral fertilisers across 38 experimental sites in the UK and Ireland (total of 641 EF estimates).
- Compares EFs by fertiliser type (ammonium nitrate AN, calcium ammonium nitrate CAN, urea) and by field management and inhibitor use (e.g., DCD, NBTP/MIP).
- Provides data to support a Bayesian analysis of EF and to establish prior distributions for future EF work.

## Data design and dataset coverage
- Time and location: Experiments conducted between 1998 and 2019 across the UK and Ireland (England, Scotland, Wales, Northern Ireland, Republic of Ireland).
- Fertiliser treatments and inhibitors: Separate EF events for AN, CAN, and urea; subsets with nitrification inhibitors (DCD) and urease inhibitors (NBTP/MIP).
- Measurement methods: Flux chamber measurements dominate; one study used eddy covariance.
- Purpose of data: To inform Bayesian estimation of nitrogen fertiliser N2O EF and to analyse differences by fertiliser type and field management.

## Data collection and sources
- Data sources:
  - Published studies explicitly measuring N2O EF after mineral fertiliser application (641 EF events across multiple studies listed in Table 1).
  - Raw data from the Agricultural and Environmental Data Archive (AEDA), recalculated to EF values.
- Data collection approach:
  - Extract EF events from peer-reviewed articles.
  - Recalculate EF from AEDA raw data for 25 days post-application using a log-normal Bayesian approach (accounts for spatial and temporal distribution of N2O fluxes).
- Literature search:
  - Google Scholar search for articles published after Jan 1998 and before Apr 2019, using keywords related to N2O, fertilisers, inhibitors, and related terms.
- AEDA data sources:
  - Multiple InveN2Ory datasets and Fertiliser experimental sites (Bedfordshire, Devon, Ceredigion, County Down, Warwickshire, Dumfries, East Lothian), with DOIs provided.

## Data structure and units
- File: Farm_Flux_and_Soil
  - Location metadata: Year, Location (UK or Ireland), Country sub-division (E, I, NI, S, W).
  - Fertiliser and treatment: Fertiliser (AN, CAN, Urea), Inhib (DCD, MIP, NBTP, NA if none).
  - Agronomic details: Amount applied (Kg N), Applications (number of events), Mean_N_app (average N per event), Field_manage (Arable/Grass), Crop_Type.
  - Measurements: Meas (Flux measurement method; Manual chamber or Eddy covariance), EF (emission factor as % of total N applied).
  - Reference: Source of data (study or dataset).
- AEDA and related references provide the underlying dataset sources and versioning.

## Data sources and documentation
- Published studies contributing EF data (examples):
  - Abdalla et al. 2009; Baggs et al. 2003; Bell et al. 2015; Cardenas et al. 2019; Cowan et al. 2019a/2019b; Dobbie & Smith 2003; Harty et al. 2016; Hinton et al. 2015; Jones et al. 2005; Krol et al. 2017; Misselbrook et al. 2014; Roche et al. 2016; Skiba et al. 2013; Smith et al. 2012, etc.
- AEDA data sources (InveN2Ory and related datasets) with DOIs for specific fertiliser and manure experiments across multiple sites.

## Methods and analysis
- Bayesian framework:
  - Data are used to derive prior distributions for N2O EF in future work using Bayesian statistics.
  - Log-normal Bayesian approach applied to AEDA-derived data to estimate EFs for 25 days post-application, addressing spatial and temporal variability in N2O fluxes.
- Analytical aims:
  - Investigate differences in EFs by fertiliser form and by inhibitor use.
  - Provide a harmonised dataset suitable for meta-analysis and prior specification in subsequent EF modeling.

## Data quality, governance, and accessibility considerations
- Metadata and standardization:
  - Clear data structure and field definitions to facilitate reuse and reproducibility.
  - Metadata gaps addressed by linking to primary publications and AEDA dataset descriptions.
- Data sharing and openness:
  - Uses publicly available published data and open AEDA datasets with DOIs, supporting transparency.
- Challenges noted for monitoring frameworks (relevant to the archetype):
  - Heterogeneity across studies (measurement methods, field conditions, timing) necessitates careful harmonisation.
  - Dependence on diverse metadata, including inhibitor types and field management, to interpret EF variations.
  - Data lineage and provenance are explicit (references and dataset origins), aiding governance and quality assurance.

## Implications for monitoring frameworks
- Demonstrates how to assemble a multi-source environmental dataset (literature plus open data archives) for robust EF monitoring and Bayesian analysis.
- Shows the value of a structured data schema and explicit metadata to support data quality, governance, and future data integration.
- Provides a ready-made resource for informing prior distributions in monitoring programs and for evaluating fertiliser-related N2O emissions across regions.