# WildCrickets06I_EarlyLatencyVsSurvival Description of content

## Overview
- Describes a dataset of individual male crickets with lifespan classified by early-life mating latency.
- EarlyLatency is categorized as High (H) or Low (L) effort based on whether the time to mate in early life is above or below the population median.
- Key fields include Year (year the cricket was alive), Lifespan (in days), and EarlyLatency (H/L).

## Data fields
- Year: Year when the cricket was alive.
- Lifespan: Lifespan in days.
- EarlyLatency: High (H) or Low (L) effort in time to mate, determined by whether the early-life latency is above or below the population median.

## Data quality and considerations
- EarlyLatency is a derived variable requiring a defined method for calculating the population median latency.
- Units: Lifespan in days; Year as calendar year.
- Consider potential missing values or inconsistencies in year, lifespan, or latency coding.

## Uses and implications for data leaders
- Enables analysis of the relationship between early-life mating effort and lifespan.
- Demonstrates a compact, well-documented data asset suitable for governance, with clear definitions, units, and a derived variable.
- Highlights needs for metadata, provenance, versioning, and discoverability when sharing with researchers or partners.

## Governance and data management actions
- Develop a data dictionary and metadata with field definitions, EarlyLatency calculation method, data source, cohort, and update cadence.
- Ensure consistent data formats, discoverability, and appropriate access controls for sharing across networks.
- Implement data quality checks for Year, Lifespan, and EarlyLatency coding.