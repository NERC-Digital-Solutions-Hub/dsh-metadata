# Long-term multisite Scots pine trial, Scotland: temperatures and temperature variances for tree nurseries, 2007-2012

## Overview
- Multisite common garden trial of Scots pine seedlings conducted across three nurseries in Scotland from 2007 to 2012.
- Primary data focus: hourly and daily temperature metrics (max, min, average, and variance) to assess environmental differences among sites and their potential impact on seedling growth.

## Experimental Design
- Seed sources: from ten trees per population, across 21 native Scottish Scots pine populations (210 families total; 24 half-sibs per family; 5,040 individuals).
- Nursery locations:
  - NW: outdoors at Inverewe Gardens, western Scotland.
  - NE: outdoors in a fruit cage at the James Hutton Institute, Aberdeen.
  - NG: unheated glasshouse at the James Hutton Institute, Aberdeen.
- Allocation and layout:
  - 8 seedlings per family moved to one of three nurseries (total 1,680 per nursery).
  - Trees organized into 40 randomised trays (blocks) per nursery; each block contained two trees per population (42 trees per block).
  - In 2010, NG seedlings moved outdoors to Glensaugh, Aberdeenshire, and all plants repotted into larger 3 L pots with new substrate and fertiliser; blocks reorganised.

## Temperature Data Collected
- Recording period and method:
  - Hourly temperature data loggers deployed 50 cm above ground under foil-covered funnels; data collected September 2007 (NG/NE) or November 2007 (NW) until March 2012.
- Metrics computed:
  - DailyMaximum, DailyMinimum, DailyAverage, DailyVariance (0:00–23:00).
  - DaytimeVariance (sunrise–sunset) and NighttimeVariance (sunset–sunrise) calculated for each day.
- Data quality notes:
  - If more than one hourly record within a day was missing, the daily metrics for that day were not calculated and omitted.

## Data File and Variables
- File: NurseryTemperature.txt
- Key fields:
  - Nursery (Description) and Unit: NE, NG, NW
  - Year (2007–2010)
  - Month (1–12)
  - Day (1–31)
  - Date (Day/Month/Year)
  - DailyMaximum (°C)
  - DailyMinimum (°C)
  - DailyAverage (°C)
  - DailyVariance (°C²)
  - DaytimeVariance (°C²)
  - NighttimeVariance (°C²)

## Data Quality and Gaps
- Possible patchy data due to missing hourly records; daily metrics omitted when data gaps exceed tolerance.
- No artificial lighting; natural site conditions differ by nursery (outdoor vs. glasshouse), which may influence temperature profiles.

## Potential Uses for Data Support
- Build self-serve dashboards and pivot analyses comparing temperature regimes across nurseries and years.
- Combine with growth or phenotypic data to explore relationships between temperature exposures and seedling performance.
- Data cleaning, verification, and enhancement (e.g., imputing small gaps, documenting data provenance) to promote reuse.
- Share early prototypes with stakeholders to refine data products and encourage broader data sharing and reuse.