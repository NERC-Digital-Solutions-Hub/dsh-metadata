# The UK Butterfly Monitoring Scheme (UKBMS)

- Overview
  - UKBMS collects data from over 2,000 sites yearly across the UK.
  - Butterflies are primarily counted along fixed linear transects (Pollard walks) to estimate population abundance for several species using standardized methods; Wider Countryside Butterfly Survey (WCBS) provides reduced-effort sampling.

- Data collection methods
  - All-species transects
    - Fixed-route line transect, typically 2–4 km, 45 minutes to 2 hours, weekly from April to September.
    - 5 m wide counting belt along the transect; routes fixed to enable year-to-year comparison.
    - Transects sampled to reflect habitat types and management; usually 26 counts per year.
    - Walk times: 10:45–15:45; weather criteria: dry, wind < Beaufort 5, temperature thresholds (≥13°C with ≥60% sunshine or ≥17°C if overcast).
  - Single-species transects
    - Follow all-species methodology but recorded only on a few weeks during the focal species’ flight period.
  - Timed counts and egg/larval web counts
    - Timed counts record abundance of a specific species over a set time/area; weather constraints similar to transects.
    - Egg/larval web counts record eggs or larval webs in suitable habitat.
  - Wider Countryside Butterfly Survey (WCBS)
    - Reduced-effort sampling targeting wider countryside habitats (farmland).
    - Based on the BTO Breeding Bird Survey, uses two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits (minimum 2 visits in July/August), spring visits encouraged.

- Data collection, entry, and storage
  - Field data recorded on standard forms; entered online via ukbms.org/mydata or Transect Walker software (free download).
  - Data entered by the recorder or regional transect coordinator; coordinators compile data for their region.
  - Online data and Transect Walker files uploaded into an Oracle database containing all records.

- Data processing and quality control
  - Site indices require sufficient monitoring visits; WCBS sites excluded from index calculations due to limited visits.
  - For transect sites, a General Additive Model (GAM) is used to impute missing values and calculate the site index.
  - Validation checks include automatic checks in Transect Walker, regional coordinator reviews, and further automated/manual checks for out-of-range records, records outside known flight periods, new site records, and anomalous counts.

- Nature and units of recorded values
  - Site indices are relative measures of population size (not absolute counts) and correlate with more intensive methods like mark-recapture.
  - The index represents a relatively constant proportion of the actual population, varying by species due to detectability.

- Data format and fields
  - Site indices stored as a text file with columns:
    - Species (scientific name per Fauna Europaea)
    - Common name (vernacular, per Emmet & Heath references)
    - Year (year the site index is calculated)
    - Site Index (relative population index for the species/year)
    - Missing data indicated as -2 when a site was not monitored sufficiently to compute an accurate index

- Additional context
  - Historical method references include Pollard & Yates (1993) and Rothery & Roy (2001) for GAM-based imputation approaches.