# Metadata for 'Long-term multisite Scots pine trial, Scotland: temperatures and temperature variances for tree nurseries, 2007-2012'

- Purpose: Regularly recorded temperatures to assess their impact on growth and development of Scots pine seedlings in a multisite common garden trial.
- Timeframe: 2007–2012.

## Source material and sample provenance
- Seed origin: 10 trees from each of 21 native Scottish Scots pine populations (210 families total).
- Population design: Represented across the species’ native range in Scotland, with three populations from each of seven seed zones.
- Germination and propagation: Seeds germinated at James Hutton Institute (Aberdeen); dormancy broken, stored briefly, then germinated and planted into pots.
- Family structure: Seeds from the same mother tree are treated as half-siblings; 24 progeny per family, 8 seedlings per family per nursery.

## Experimental design and sites
- Nurseries (three sites):
  - NW: outdoors at Inverewe Gardens, western Scotland.
  - NE: outdoors in a fruit cage at James Hutton Institute, Aberdeen.
  - NG: unheated glasshouse at James Hutton Institute, Aberdeen.
- Plant arrangement: 40 randomised trays (blocks) per nursery; each block contains two trees per population (total 42 trees per block).
- Plant relocation: In May 2010, NG seedlings moved outdoors to Glensaugh, Aberdeenshire.
- Potting and transplanting: All plants repotted in 2010 into larger pots with a specialized Ericaceous compost and slow-release fertilizer; re-organisation into new blocks.

## Temperature recording and data collection
- Data collection period: September 2007 (NG/NE) or November 2007 (NW) through March 2012.
- Measurement method: Hourly temperature using data loggers placed 50 cm above ground under an aluminium foil-covered funnel.
- Variables derived:
  - Daily maximum, minimum, and average temperatures (0:00–23:00).
  - Daily temperature variance; partitioned into daytime (sunrise–sunset) and nighttime (sunset–sunrise) variances.
- Data completeness: Days with missing hourly records >1 were omitted from daily calculations.
- Data file: NurseryTemperature.txt
  - Content: one dataset with fields describing site, date, and temperature statistics.

## Data fields and units (as in NurseryTemperature.txt)
- Nursery, Description: Site of nursery (NE, NG, NW).
- Year, Month, Day, Date: Temporal identifiers (2007–2010; months 1–12; days 1–31; full date).
- DailyMaximum, DailyMinimum, DailyAverage: Temperature metrics in °C for 0000–2300.
- DailyVariance: Temperature variance for the 0000–2300 window in °C².
- DaytimeVariance: Daytime variance in °C².
- NighttimeVariance: Nighttime variance in °C².

## Data quality, limitations, and notes
- Missing data handling: If more than one hourly record per 24 hours was missing, related daily metrics were not calculated.
- Spatial and temporal specificity: Temperature records are site-specific and time-bound to 2007–2012; daily statistics are derived from hourly data.
- Metadata scope: Includes precise site coordinates for provenance and explicit configuration of nurseries and plantings.

## Implications for data use and governance
- Suitable for analyses of how temperature and its diurnal variance influence seedling growth across different microclimates and management conditions.
- Enables cross-site comparisons among outdoor, semi-protected (fruit cage), and glasshouse environments.
- Facilitates integration with broader data efforts on phenotypic responses to temperature in Scots pine and supports reproducibility due to explicit experimental and measurement metadata.