# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK, using standardized methods to monitor butterfly populations.
- Primary method: all-species transects (Pollard walks) with fixed routes to enable year-to-year comparison.
  - Transect length typically 2–4 km, divided into habitat/management sections.
  - All butterfly species counted within a fixed 5 m wide band along the transect.
  - 26 counts per year, conducted weekly from early April to late September.
  - Counts occur between 10:45 and 15:45 under suitable butterfly-activity weather: dry conditions, Beaufort wind speed < 5, and temperature criteria (≥13°C with at least 60% sunshine, or >17°C if overcast).
- Transects are fixed once established to maintain comparability over time.
- Alternative methods:
  - Single-species transects follow the same methodology but record data in one week (or more) during the focal species’ flight period.
  - Timed counts measure abundance of a species over a set period and area under the same weather constraints.
  - Egg/larval web counts record eggs or larval webs in suitable habitats (e.g., Marsh Fritillary).

- Data collection process:
  - Field data recorded on standard forms and entered into Transect Walker software (free to download).
  - Data input by the recorder or by the regional transect coordinator; each transect coordinator aggregates data for their region.
  - Transect Walker files are uploaded to an Oracle database holding all records.

- Analytical methods:
  - Data validation occurs before analysis.
  - General Additive Models (GAM) are used to impute missing values and calculate site indices.
  - A Collated Index is produced by combining site indices across all sampling methods to generate a national annual index per species.
  - Missing values are estimated using a loglinear regression model that accounts for year effects (weather-related) and site effects (population differences across sites).
  - The Collated Index is updated annually as new data are incorporated; indices may shift slightly as past data are added.
  - Collated Indices are calculated for species recorded from five or more sites per year.

- Nature and units of recorded values:
  - Site indices are relative measures of population size and are scaled to be comparable with other abundance measures (e.g., set against MR methods).
  - Collated Indices are presented as the base-10 logarithm (Log10 Collated Index, LCI) and are standardized so the average index over the series equals 2, providing a relative time-series measure.

- Quality control:
  - Automatic checks in Transect Walker flag unusual counts or records outside known flight periods; recorders can modify data accordingly.
  - Regional coordinators review records for each region; additional automated and manual validation checks follow, including:
    - Records outside known distribution ranges,
    - Out-of-period records,
    - First-time records at a site,
    - Extremely high or unusual abundances.

- Format and storage of data:
  - Collated Indices are stored as CSV files.
  - Columns include: Species (scientific name per Fauna Europaea v2.2), Common name, Year, No. Sites, Collated Index, Time period.