# Description of the Data and file structure

## Overview
- Recorded data: freshwater macroinvertebrates abundance in England, from Environment Agency.
- Format: long-form (year, month, day, site, sample, taxon, abundance) stored as an RDS file accessible in R.
- Purpose: originally to understand water quality; later used in published research.

## Data content and structure
- Data are derived from EA Ecology and Fish Explorer Macroinvertebrate database and pooled by family and broader taxonomic groupings.
- Single dataset file in RDS format.
- Columns include: riverbasin, agency_area, waterbody, wfd_waterbody_id, site_id, full_easting, full_northing, season, year, month, day, Latitude, Longitude, sample_id, order_taxon, family_taxon, total_abundance, year_scaled, group.
- Missing data coded as NA.

## Timeframe and sampling design
- Sites across England, collected 2002–2019.
- Sampling seasons: spring (March–May) and autumn (September–November).
- Data collected using three-minute kick-samples (standardized semi-quantitative method).
- Data before 2002 excluded due to limited abundance recording.

## Processing and scope
- Final dataset derived from the EA’s Ecology and Fish Explorer Macroinvertebrate database.
- Abundance data summed at the family level within specified taxa.
- Only data after filtering: three-minute kick-sample predominant (≈99%), minimum three years of data in both spring and autumn per site.

## Dataset size and coverage
- 67,757 macroinvertebrate samples from 5,009 sites (out of 10,136 in the original dataset).
- Covers ~2,774 waterbodies across ten river basins under the Water Framework Directive (WFD) in England.
- A national distribution with bias toward mid-to-lower perennial reaches, reflecting monitoring program aims rather than intrinsic biodiversity.

## Quality control and reliability
- Post-2002 improvements: more exact abundance estimates and enhanced quality control.
- Independent re-analysis conducted for one in every ten samples.
- Data restricted to 2002–2019 (despite earlier collection dating from 1991).

## Data access and usage
- Public access link: https://environment.data.gov.uk/ecology-fish
- Used in published research: Powell et al. 2022, Global Change Biology (Abundance trends for river macroinvertebrates vary across taxa, trophic group and river typology).

## Data values and units
- Values are discrete counts of individuals (abundance) for macroinvertebrate taxa.