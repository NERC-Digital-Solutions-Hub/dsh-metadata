# The UK Butterfly Monitoring Scheme (UKBMS)

- Aims and scope
  - Collates butterfly data from over 2,000 sites annually across the UK.
  - Uses multiple standardized methods to estimate population abundance for various species.
  - Data underpin monitoring and conservation, with outputs intended for use by researchers and practitioners.

- Key data collection methods
  - All-species transects
    - Fixed-route line transects (typically 2–4 km) sampled weekly from early April to late September.
    - Count all butterfly species within a fixed-width 5 m band along the transect.
    - Routes fixed to enable year-to-year comparison; taken 10:45 am to 3:45 pm under suitable butterfly activity conditions.
    - Weather criteria: dry; wind < Beaufort 5; temperature ≥ 13°C with ≥ 60% sunshine, or > 17°C if overcast.
    - Transects are divided into habitat/management sections; over 1,000 sites have all-species transects in recent years.
  - Single-species transects
    - Follow the all-species methodology but record only for a few weeks during the focal species’ flight period.
  - Timed counts and egg/larval web counts
    - Timed counts: abundance of a focal species recorded over a set duration in a defined area, within weather constraints.
    - Egg/larval web counts: count eggs or larval webs on suitable habitat areas.
  - Wider Countryside Butterfly Survey (WCBS)
    - Reduced-effort survey for wider countryside habitats (e.g., farmland), established in 2009.
    - Based on the BTO Breeding Bird Survey approach: two parallel 1-km transects within 1-km squares, subdivided into 10 sections.
    - Typically 2–4 visits per year (minimum 2 visits in July/August; spring visits encouraged).

- Data collection and entry
  - Field recording on standard forms.
  - Online data entry via ukbms.org/mydata or Transect Walker software (free download).
  - Data input by the recorder or the regional transect coordinator; regional coordinators gather data for all sites in their region.
  - Online and Transect Walker data uploaded into an Oracle database containing all records.

- Data processing and site indices
  - Site indices are computed only for sites with sufficient monitoring visits; WCBS indices are not calculated due to limited visits.
  - For transect sites, missing values are imputed using a General Additive Model (GAM) to produce a site index.
  - Site indices are relative measures of population size (not absolute counts); proportional relationships to actual population size vary by species.

- Quality control and validation
  - In-field automatic checks in Transect Walker flag potential data entry errors (e.g., abnormally high counts, records outside known flight periods).
  - Regional transect coordinators perform ongoing checks for questionable records.
  - Additional automated/manual validation includes queries for records outside known distribution, outside typical flight periods, first-time site records, and anomalous abundances.

- Data format and outputs
  - Site Indices stored as text files (.txt).
  - Columns include:
    - Species (scientific name per Fauna Europaea)
    - Common name (per Emmet & Heath)
    - Year (year of the site index)
    - Site Index (relative abundance index for the year and species)
  - If a species at a site in a given year cannot yield an accurate index due to insufficient monitoring, the value is recorded as -2.

- Notes on data lineage and comparability
  - Site indices are designed to be comparable across years within the same site and species, using standardized methodologies and validation steps.
  - Data are cross-checked against other butterfly datasets (e.g., Butterfly Conservation’s BNMs) to ensure consistency in species distribution and flight periods.