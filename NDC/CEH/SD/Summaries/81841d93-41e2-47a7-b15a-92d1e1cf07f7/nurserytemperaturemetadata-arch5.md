# Long-term multisite Scots pine trial, Scotland: temperatures and temperature variances for tree nurseries, 2007-2012

## Overview
- Multisite common garden trial of Scots pine seedlings conducted at three nurseries in Scotland (NW Inverewe Gardens, NE James Hutton Institute Aberdeen, NG James Hutton Institute Aberdeen glasshouse) from 2007 to 2012.
- Main aim: assess the impact of temperature differences on growth and development of seedlings.
- In 2010, NG seedlings were moved outdoors to Glensaugh; all plants repotted into larger pots and reorganised into new blocks.

## Source material and experimental design
- Seed origin: 10 trees from each of 21 native Scottish populations (210 families total), representing the species’ native range with three populations from each of seven seed zones.
- Propagation: seeds germinated and grown into 24 half-sibling progeny per family (total 5,040 individuals).
- nursery allocation: 8 seedlings per family moved to each of the three nurseries (1,680 per nursery).
- Layout: 40 randomised blocks (trays) per nursery; each block contained two trees per population (total 42 trees per block).

## Temperature recording and data captured
- Data collection: Hourly temperatures recorded at each nursery site using data loggers.
- Recording period: September 2007 (NG and NE) and November 2007 (NW) through March 2012.
- Measurement setup: Loggers suspended 50 cm above ground under an aluminium foil-covered funnel; no artificial light used.
- Derived daily metrics per nursery: DailyMaximum, DailyMinimum, DailyAverage, DailyVariance.
- Daily variance partitioning: DaytimeVariance (sunrise to sunset) and NighttimeVariance (sunset to sunrise); sunset/sunrise times determined from timeanddate.com for each site.
- Data completeness: If more than one hourly record per 24 hours was missing, that day’s metrics were not calculated (and omitted).

## Dataset structure and metadata
- File: NurseryTemperature.txt
- Key fields:
  - Nursery (NE, NG, NW) and Description; Year (2007–2010); Month (1–12); Day (1–31); Date (day/month/year)
  - DailyMaximum (°C), DailyMinimum (°C), DailyAverage (°C), DailyVariance (°C²)
  - DaytimeVariance (°C²), NighttimeVariance (°C²)
- Site coordinates and descriptive context included in provenance; temperature data aligned to local times and daily aggregations.

## Data quality, governance and usage considerations
- Data quality notes:
  - Temperature data aggregated to daily metrics; some days omitted due to missing hourly records.
  - Temporal and spatial coverage across three distinct nursery environments (outdoor western, outdoor eastern fruit cage, indoor glasshouse) with a later relocation/outdoor transition in 2010.
- Governance and provenance:
  - Source: James Hutton Institute; clear lineage from seed collection through experimental setup to daily temperature records.
  - Metadata provides detailed method descriptions, units, and site-specific information to support data reuse, replication, and integration with other datasets.
- Potential use cases:
  - Analyses of how environmental temperature variation across sites affects Scots pine seedling growth.
  - Cross-site temperature comparisons and time-series assessments within 2007–2012.
  - Data suitable for metadata-driven discovery and integration into broader plant phenology or climate-growth studies.