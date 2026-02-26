# The UK Butterfly Monitoring Scheme (UKBMS)

- Overview
  - UKBMS collects data from over 2,000 sites annually across the UK.
  - Population abundance is estimated using several standardized methods; site indices are relative measures of population size.

- Data collection methods
  - All-species transects: fixed-route line transects (2–4 km) recorded weekly Apr–Sep; data collected in a 5 m wide band along the transect; transects are fixed to enable year-to-year comparisons and are divided into habitat/management sections.
  - Weather and timing: transects conducted between 10:45 and 15:45 under suitable butterfly-activity conditions (dry; Beaufort windspeed ≤ 5; temperature ≥ 13°C with ≥ 60% sunshine, or >17°C if overcast).
  - Recording cadence: typically 26 counts per year.
  - Single-species transects: follow the all-species methodology but only a few weeks are recorded for the focal species.
  - Timed counts: species-specific counts over a set period/area, with same daily/weather constraints as transects.
  - Egg/larval web counts: count eggs or larval webs in suitable habitat areas.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort survey started in 2009; two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (minimum two in July/August); based on the BBS approach.

- Field data capture and data flow
  - Data are recorded on standard forms in the field.
  - Entered online via the UKBMS data entry site or via Transect Walker software.
  - Data are entered by the recorder or regional transect coordinators; each transect coordinator aggregates data for their region.
  - Online data and Transect Walker files are uploaded to an Oracle database containing all records.

- Data processing and indices
  - Site indices are calculated only for sites with sufficient monitoring visits; WCBS sites are excluded due to limited visits.
  - For transect sites, a General Additive Model (GAM) is used to impute missing values and to compute the site index.
  - Site index represents a relative measure of population size—proportional to true population size, with species-specific detectability differences (e.g., Marbled White more conspicuous than Dingy Skipper).

- Quality control and validation
  - Automatic checks in Transect Walker flag unusual counts or records outside known flight periods; recorders may adjust or override.
  - Regional transect coordinators review records for their region; data can be checked continuously during the season.
  - Additional automated/manual validation includes checks for records outside species’ known distribution, out-of-flight-period records, first-time site records, and outlier abundances.

- Data formats and storage
  - Site Indices are stored as a text file.
  - Columns include: Species (scientific name per Fauna Europaea), Common name, Year, Site Index.
  - If a species at a site in a given year cannot yield an accurate index due to insufficient data, the value is -2.

- Key references and context
  - Pollard, E. & Yates, T.J. (1993) Monitoring Butterflies for Ecology and Conservation.
  - Rothery, P. & Roy, D.B. (2001) Application of generalized additive models to butterfly transect count data.