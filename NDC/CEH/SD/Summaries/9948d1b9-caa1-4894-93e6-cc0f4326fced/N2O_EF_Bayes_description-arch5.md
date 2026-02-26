# Nitrous oxide emission factors of mineral fertilisers in the UK and Ireland: experimental data for the period (1998 - 2019)

- Overview
  - Collates data from 38 experimental sites across the UK and Ireland, yielding 641 mineral fertiliser N2O emission factor (EF) estimates from field measurements (1998–2019).
  - Data cover ammonium nitrate (AN), calcium ammonium nitrate (CAN), and urea, with and without nitrification inhibitors (Dicyandiamide [DCD], MIP, NBTP).
  - Measurements largely used flux chamber methods; one study used eddy covariance.
  - Aims to support a Bayesian analysis of EF differences by fertiliser type and field management and to establish priors for future Bayesian EF work.

- Data Content and Variables
  - File: Farm_Flux_and_Soil
  - Key variables (12 fields):
    - Location and time: Year, Location (UK or Ireland, with subregions E/I/NI/S/W)
    - Fertiliser and inhibitors: Fertiliser (AN, CAN, Urea), Inhib (DCD, MIP, NBTP, NA if none)
    - Application details: Amount applied (kg N), Applications (number of events), Mean_N_app
    - Field context: Field_manage (Arable/Grass), Crop_Type
    - Measurement and EF: Meas.Method (Manual chamber or eddy covariance), EF (percent of N applied)
    - Reference: Source of data
  - Summary statistics: 641 EF events overall; 293 AN events, 63 CAN events, 118 Urea events; additional EFs for inhibitors (38 with DCD; 129 with DCD or NBTP) and recalculated AEDA data.

- Data Sources and Composition
  - Data derived from:
    - Published studies explicitly measuring N2O EF after mineral fertiliser application.
    - Raw data from the Agricultural and Environmental Data Archive (AEDA) used to compute EF 25 days after application via a log-normal Bayesian approach.
  - The dataset aggregates numerous studies (e.g., Abdalla 2009; Baggs 2003; Bell 2015; Cardenas 2019; Cowan et al. 2019a/b; Dobbie & Smith 2003; Misselbrook 2014; Smith et al. 2012; etc.) across England, Ireland, Scotland, Wales, and Northern Ireland.
  - AEDA data sources comprise multiple InveN2Ory datasets ( Fertiliser experiments at Bedfordshire, Devon, Ceredigion, County Down, Warwickshire, Dumfries, East Lothian, etc.) with DOIs provided.

- Data Collection and Processing Methods
  - Data collection approaches:
    - Extracted from publications where measuring N2O EF was a stated aim.
    - Raw AEDA data used to calculate EFs for 25 days post-application using a log-normal Bayesian framework to reflect temporal and spatial distribution of N2O fluxes after fertiliser events.
  - Literature search: 1998–2019 window with targeted keywords; cross-referencing cited literature.

- Data Structure and Units
  - EF is recorded as a percentage of total N applied.
  - Measurements include method (manual chamber or eddy covariance) and context (field type, crop type, inhibitors).
  - Data are organized with explicit coding for location, country/region, fertiliser type, inhibitor type, and measurement reference.

- Data Provenance and Documentation
  - Extensive references listed for each EF event (original studies and AEDA sources).
  - AEDA sources include multiple site-specific datasets with versioned records from the Freshwater Biological Association.
  - The dataset also notes recalculated AEDA data for consistency across studies.

- Implications for Data Stewardship
  - Rich, multi-source compilation suitable for deriving priors and cross-study synthesis of N2O EF across fertiliser types and management practices.
  - Strong provenance through explicit references, site information, and measurement methods; supports reproducibility and traceability.
  - Useful baseline for Bayesian analyses and future EF updates as new data become available.

- Practical Considerations and Challenges
  - Heterogeneity across studies in measurement methods (flux chamber vs eddy covariance), field conditions, and temporal coverage.
  - Inhibitor treatments add complexity to comparability (DCD, NBTP, MIP) requiring careful metadata handling.
  - Data integration from published studies and AEDA requires consistent documentation to maintain traceability and updateability.
  - Ongoing updates would benefit from standardized metadata schemas and portalized access to original sources and recalculated datasets.