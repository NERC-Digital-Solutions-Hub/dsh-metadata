# Nitrous oxide emission factors of mineral fertilisers in the UK and Ireland: experimental data for the period (1998 - 2019)

- Purpose: Compile experimental N2O emission factors (EFs) from mineral fertilisers to enable consistent environmental monitoring and to support Bayesian analysis and prior distributions for future EF work in the UK and Ireland.

## Scope and dataset overview

- Data span: 1998–2019 from 38 experimental sites across the UK and Ireland.
- Total EF events: 641 N2O EF estimates derived from field measurements.
- Fertiliser types and treatments:
  - AN (293 EF events), CAN (63), Urea (118).
  - Dicyandiamide (DCD) inhibitors applied to some AN/CAN; NBTP or MIP inhibitors applied to some urea cases (129 EF events with inhibitors).
- Measurement methods: Flux chamber measurements in most studies; one study used eddy covariance.
- Primary use: Bayesian analysis of EF differences by fertiliser type and field management; to establish prior distributions for future EF work.
- Data sources: Published studies reporting explicit N2O EF measurements and raw data from the Agricultural and Environmental Data Archive (AEDA).

## Data collection and methodological approach

- Data sources:
  - i) Published studies explicitly measuring N2O EF after mineral fertiliser application.
  - ii) AEDA raw data used to calculate EFs for 25 days post-application using a log-normal Bayesian approach (accounts for spatial and temporal distribution of N2O fluxes).
- Literature search: Google Scholar (1998–2019) with keywords related to N2O, fertilisers, nitrification inhibitors, N-use efficiency, and related terms.
- Analytical framework: Bayesian estimation of cumulative fluxes and emission factors, with prior related to vegetable/grassland contexts; supports standardised cross-study comparisons.

## Data structure and content

- File: Farm_Flux_and_Soil
- Key fields:
  - Location and year: UK or Ireland; England, Ireland, Northern Ireland, Scotland, Wales.
  - Fertiliser: AN, CAN, Urea.
  - Inhibitors: DCD, MIP, NBTP, or none.
  - Amounts and applications: kg N applied; number of applications; mean N per application.
  - Field management: Arable or Grass; Crop type.
  - Measurement method: Manual chamber or eddy covariance.
  - EF: Emission factor as a percentage of total N applied.
  - Reference: Source of data.
- Data units: EF expressed as % of total N applied.

## Data sources and references

- Primary dataset composition:
  - Numerous published studies (e.g., Abdalla 2009; Baggs 2003; Bell 2015; Cardenas 2019; Cowan 2019a/2019b; Dobbie & Smith 2003; Harty 2016; Hinton 2015; Jones 2005; Krol 2017; Misselbrook 2014; Roche 2016; Skiba 2013; Smith 2012; etc.).
- AEDA/InveN2Ory datasets:
  - Fertiliser and manured-site experiments across various UK locations (Bedfordshire, Devon, Ceredigion, County Down, Warwickshire, Dumfries, East Lothian, etc.) with DOIs provided for each dataset.
- Access and sharing:
  - Data underpin national inventories and research platforms (InveN2Ory; Agricultural Greenhouse Gas Inventory Research Platform).
  - DOIs and references included to enable data retrieval and reuse.

## Implications for environmental monitoring and policy

- Standardised dataset enabling cross-site, cross-treatment comparisons of N2O EF across the UK and Ireland.
- Supports development of priors for Bayesian modelling of fertiliser-related N2O emissions, aiding policy evaluation and scenario analysis.
- Demonstrates integration of multiple data sources (published studies and public archives) into a single, queryable dataset aligned with monitoring responsibilities.

## Practical considerations and limitations

- Diversity of study designs and measurement methods (mostly chamber-based; one eddy covariance) introduces heterogeneity.
- Inhibitor treatments are varied (DCD, NBTP, MIP), requiring careful interpretation when comparing EFs across treatments.
- Data quality and availability depend on published datasets and the InveN2Ory/AEDA repositories; ongoing data sharing enhances value for monitoring and policy scrutiny.

## How this aligns with the Analysts Monitoring the Environment archetype

- Data verification and standardisation: Consolidates EF data from varied sources into a consistent structure suitable for monitoring and policy evaluation.
- Analysis and outputs: Provides a ready dataset for Bayes-based EF estimation and trend assessment across fertiliser types and management practices.
- Data stewardship: Includes clear data lineage, multiple sources, and linked datasets (AEDA/InveN2Ory) with stable identifiers (DOIs) for reuse and portal deposition.