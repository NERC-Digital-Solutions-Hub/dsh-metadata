# Metadata for 'Long-term multisite Scots pine trial, Scotland: temperatures and temperature variances for tree nurseries, 2007-2012'

## Overview
- A long-term multisite experimental trial of Scots pine seedlings conducted in three nurseries in Scotland (NW, NE, NG) from 2007 to 2012.
- Focus of the metadata is on hourly temperature records and derived daily temperature statistics to assess environmental differences between nurseries and their potential impact on seedling growth.

## Spatial and temporal scope
- Sites:
  - NW: Inverewe Gardens, western Scotland (approx. 57.775714, -5.597181)
  - NE: Aberdeen area (James Hutton Institute), eastern Scotland (coordinates referenced but not explicitly listed in the dataset description)
  - NG: James Hutton Institute glasshouse, Aberdeen (coordinate details not explicit; later moved outdoors to Glensaugh in 2010)
- Time period for temperature data: September 2007 to March 2012 (hourly recordings at each site; data logger deployment aligned with site availability)
- Data resolution: daily summaries derived from hourly data; hourly measurements were used to compute daily maximum, minimum, average, and variance, plus daytime and nighttime variance

## Data collection and processing
- Temperature was recorded hourly using data loggers positioned 50 cm above ground under a foil-covered funnel.
- Derived daily measures per site: DailyMaximum, DailyMinimum, DailyAverage, DailyVariance.
- Daytime and nighttime variance were calculated by partitioning daily variance according to sunrise/sunset times obtained from timeanddate.com for each site.
- Days with missing hourly data (more than one missing hourly record in a 24-hour period) were omitted from the dataset
- Data were cleaned and standardized to enable cross-site comparisons

## Data contents and format
- Single dataset file: NurseryTemperature.txt
- Variables included:
  - Nursery (site code: NE, NG, NW)
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
- Units: temperatures in degrees Celsius; variances in square degrees Celsius
- Temporal format: Date field follows Day/Month/Year

## Data quality and limitations
- Missing hourly data leads to omission of that day’s daily statistics (no imputed values for those days)
- Some site coordinates are provided for NW and for the germination location at James Hutton Institute; precise coordinates for NE and NG locations are referenced but not fully enumerated in the metadata description
- The metadata focuses on temperature records; while the broader trial included seed provenance and planting design (210 families from 21 populations), these aspects are contextual rather than part of the temperature dataset

## Provenance and context
- Seed material: seeds from 21 Scottish Scots pine populations; full trial design involved 210 families with 24 half-sib progeny per family, distributed across the three nurseries
- Purpose: to evaluate how temperature differences among sites influence seedling growth and development
- Experimental layout: seedlings arranged in 40 randomized blocks per nursery; movement of NG plants to Glensaugh occurred in 2010

## Potential GIS applications
- Visualizing spatial and temporal temperature regimes across nursery sites
- Comparing microclimates between western, eastern, and glasshouse environments
- Integrating with phenotypic or growth data to analyze environmental drivers of seedling performance
- Time-series analysis of site-specific temperature patterns for climate or habitat suitability studies

## Access and practical notes
- Data file name: NurseryTemperature.txt
- Important processing notes: daytime vs nighttime variance requires sunrise/sunset times; daily statistics exclude days with insufficient hourly data
- Useful for map-based data visualizations and GIS-driven analyses of microclimate at multi-site plant trials