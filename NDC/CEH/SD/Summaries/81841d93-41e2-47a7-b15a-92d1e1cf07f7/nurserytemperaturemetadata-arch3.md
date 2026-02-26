# Metadata for 'Long-term multisite Scots pine trial, Scotland: temperatures and temperature variances for tree nurseries, 2007-2012'

- Purpose and scope
  - Documents a long-term, multisite common garden experiment with Scots pine seedlings (2007-2012) across three nurseries in Scotland.
  - Aimed at understanding how temperature differences across sites influence seedling growth and development.

- Study design and sources
  - Seed material: seeds from 10 trees from each of 21 native Scottish populations (210 families total; 24 half-sibling progeny per family).
  - Experimental setup: 1,680 seedlings per nursery arranged in 40 randomised blocks; two trees per population per block.
  - Nursery sites and conditions:
    - NW: outdoors at Inverewe Gardens (western Scotland)
    - NE: outdoors in a fruit cage at James Hutton Institute (Aberdeen)
    - NG: unheated glasshouse at James Hutton Institute
  - 2010 changes: NG plants moved outdoors to Glensaugh; all plants repotted into larger pots and reorganised into new blocks.

- Temperature data collection
  - Hourly temperature recordings at each nursery from Sept 2007 (NG/NE) or Nov 2007 (NW) to March 2012.
  - Data loggers positioned 50 cm above ground under an aluminium foil-covered funnel.
  - Daily statistics computed per site: minimum, maximum, average temperatures, and daily temperature variance.
  - Daytime vs. nighttime variance:
    - Daytime variance based on sunrise–sunset hours
    - Nighttime variance based on sunset–sunrise hours
    - Sunrise/sunset times obtained from timeanddate.com using site coordinates
  - Data handling: if more than one hourly record missing within a 24-hour period, that day's daily statistics were not calculated.

- Dataset details
  - Single data file: NurseryTemperature.txt
  - Key fields and units:
    - Nursery (NE, NG, NW)
    - Year (2007-2010)
    - Month (1–12)
    - Day (1–31)
    - Date (day/month/year)
    - DailyMaximum (°C)
    - DailyMinimum (°C)
    - DailyAverage (°C)
    - DailyVariance (°C²)
    - DaytimeVariance (°C²)
    - NighttimeVariance (°C²)

- Data quality, metadata, and governance
  - Metadata provides site descriptions, sampling scheme (population representation and replication), and detailed variable definitions.
  - Clear documentation of data processing (e.g., calculation of daily statistics, partitioning of variance into daytime/nighttime).
  - Explicit handling of missing data (skips calculation when hourly data gaps exceed tolerance).
  - Emphasizes reproducibility through recorded methods and standardized units, while noting the potential need for data management and openness in sharing underlying data and metadata.