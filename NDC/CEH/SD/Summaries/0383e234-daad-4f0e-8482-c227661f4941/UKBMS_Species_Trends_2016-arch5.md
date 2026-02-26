# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to monitor butterfly populations.
  - Data are gathered using a standard fixed route approach (Pollard walks) and supplemented by other standardized methods for particular species or survey goals.

- Data collection methods
  - All-species transects
    - Fixed-route line transects (typically 2–4 km) sampled weekly from April to September.
    - Record all butterfly species within a fixed 5 m wide band; transects are designed to sample habitat types and must remain fixed across years for comparability.
    - Counts occur under specified weather conditions (e.g., suitable butterfly activity; temperature and wind criteria; time window).
  - Single-species transects
    - Follow the same methodology as all-species transects but record only focal species during select weeks.
  - Timed counts and egg/larval web counts
    - Timed counts record the abundance of a focal species over a set period and area; egg/larval counts record eggs or larval webs in suitable habitat.
  - Wider Countryside Butterfly Survey (WCBS)
    - Reduced-effort survey in farmland and wider countryside habitats.
    - Based on BTO Breeding Bird Survey design: two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (min 2 in July/August, spring visits encouraged).

- Data collection implementation
  - Field data are recorded on standard forms and entered online via the UKBMS data entry site or via Transect Walker software.
  - Data entry can be by the recorder or a regional transect coordinator; each transect region has a coordinator responsible for data submission.
  - Online data and Transect Walker files are uploaded into an Oracle database that stores all records.

- Analytical methods and indices
  - For wider countryside (WCBS) species
    - A two-stage model using all survey data to estimate annual seasonal patterns and then annual abundance changes.
    - Stage 1: generalized additive model (GAM) estimates annual seasonal flight patterns; daily estimates are normalised to a common seasonal pattern per year.
    - Stage 2: a model with seasonal values as an offset to estimate annual changes in abundance; accounts for varying seasonality.
  - For habitat specialists and regular migrants
    - GAM-based imputation for missing values and site indexing to derive a national Collated Index.
    - A log-linear regression is used to account for year and site effects and to produce species-wide trends since 1976.
  - Trend calculation
    - Linear regression on collated indices to quantify change over time.
    - Trends reported for entire series (1976–2016), last 20 years (1997–2016), and last 10 years (2007–2016).
  - Data interpretation
    - Site indices are relative measures of population size; Collated Indices are log10-transformed and scaled so the average index over the series equals 2.
    - Trends are described by slope, standard errors, and p-values (e.g., rapid decline/increase or stable).

- Quality control and validation
  - Automatic data-entry checks within Transect Walker flag improbable values and records outside known flight periods.
  - Regional transect coordinators review data for questionable records; continuous validation during the season.
  - Further automated/manual validation checks for range consistency, flight period consistency, first-time site records, and outliers.

- Data format and storage
  - Species Trends are stored as CSV with fields including:
    - Sci_Name, Common_name, No_years, Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change
    - 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change
    - 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change
  - Data are updated annually with new monitoring data; past years’ indices may adjust as data are incorporated.

- Governance and stewardship implications for large ecological datasets
  - The UKBMS demonstrates a comprehensive data pipeline from standardized field collection to centralized storage (Oracle DB) and sophisticated longitudinal analyses.
  - Emphasizes the need for consistent standards across data types (all-species, single-species, WCBS), robust metadata, and versioned outputs (indices and trends) that can change with new data.
  - Highlights the importance of documenting data processing methods (GAMs, imputation, index calculations) for reproducibility and downstream use.

- Key challenges for data stewardship
  - Incomplete understanding of user needs and priorities.
  - Timeliness of data provision from field teams and data creators.
  - Encouraging adherence to standards across diverse data types and collaborators.
  - Handling multiple systems and formats, including legacy or bespoke tools.
  - Managing very large datasets and data transfer logistics.
  - Maintaining and interoperating with older databases that may require non-standard, bespoke solutions.