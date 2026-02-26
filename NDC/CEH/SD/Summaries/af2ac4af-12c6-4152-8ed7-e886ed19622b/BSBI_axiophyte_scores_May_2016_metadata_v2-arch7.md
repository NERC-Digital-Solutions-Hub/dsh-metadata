# BSBI axiophyte scores - metadata, May 2016

## Overview
- Defines axiophytes as species indicative of high-quality habitat.
- Produces national (Great Britain) level axiophyte scores from county lists.
- An information product intended to enable understanding and exploration of habitat indicators via map-based data.
- Meta-list will be updated as more county-level lists become available.

## Data sources and scope
- County lists: 24 GB counties (downloaded February 2014 from the BSBI website). Irish lists (Antrim, Fermanagh, Waterford) excluded.
- Some counties are represented as two vice-counties (e.g., Cornwall).
- Geographic scope is GB-wide at county level (not including Isle of Man or Channel Islands in the main dataset).
- Data files include both raw published lists and cleaned/derived datasets.
- Axiophyte scores are derived from county lists and are supplemented by county occurrence data (VCCC).

## Methods and data processing
- Taxon name verification:
  - Raw lists checked against Stace 1997; Stace 2010 name changes recorded.
  - Hybrids, microspecies, subspecies/varieties generally excluded or treated as within species.
  - Exclusions include charophytes, neophytes, and natives known to be neophytes in a county.
- Data cleaning and alignment:
  - Cleaned axiophytes list (axiophytes_Feb_2014) created.
  - County occurrence data derived from the Vice-County Census Catalogue (VCCC) with similar cleaning; some records updated to reflect more recent information.
  - VCCC includes records up to 1999; may not reflect latest distributions.
- Scoring method:
  - For each species: axiophyte score = (number of counties where the species is listed as axiophyte) / (number of counties in which the species has been recorded in the VCCC).
  - Example: Acer campestre axiophyte in 4 of 16 counties ⇒ 25%.
  - Also computed an alternative score counting only counties where the species is extant (per VCCC): e.g., Adonis annua with 2/5 extant counties ⇒ 40%.
  - Scores calculated for 1420 native/archaeophyte taxa across the 24 included counties.
- Update plan:
  - The meta-list will be updated as more county-level lists become available.

## Data products (CSV files)
- axiophyte_scores.csv: Calculated overall axiophyteness scores (size ~60 KB).
- axiophytes_Feb_2014.csv: Raw county-level data used for scoring (size ~91 KB).
- counties_included.csv: Details of included counties (size ~1 KB).
- exclusions_with_reason.csv: Taxa excluded and reasons (size ~19 KB).
- county_occurrence.csv: Data on current status of taxa within counties (size ~101 KB).
- axiophytes_as_published.csv: Original axiophyte data as published (size ~103 KB).
- Additional metadata columns describe native status, county-by-county axiophyte presence, and taxon name alignment between Stace editions.

## Geographic and data-structure details
- Counties and vice-counties:
  - 24 GB counties included; some entries reflect two vice-counties per county.
- Data structure:
  - Species lists are aligned to Stace 1997/2010 names.
  - County-by-county presence/absence and status (extant vs extinct) recorded for each taxon.

## GIS applicability and usage notes
- Map-ready indicators of habitat-quality proxies:
  - Use county-level axiophyte presence as a spatial indicator of high-quality habitat.
  - Use axiophyte scores to compare relative indicator strength across species and counties.
- Data integration:
  - Join axiophyte data to GB county polygons or to a county-level raster grid.
  - Consider using both the proportion of counties with axiophytes and the extant-based proportion for more conservative estimates.
- Considerations and limitations:
  - VCCC data are historical (up to 1999); updates may alter extant/extinct statuses.
  - Taxonomic name changes between editions may affect cross-version matching.
  - Exclusions and cleaning steps mean the dataset reflects a curated subset of taxa (likely not all potential axiophytes).
- Update potential:
  - The dataset is designed to be updated as new county lists become available, enabling revision of scores and counts.

## References and context
- Hill, Mark O., et al. 2004. PLANTATT.
- Lockton, A. 2008. BSBI News.
- Stace, C.A. 1997; Stace, C.A. 2010. New flora of the British Isles.
- Stace, C.A., et al. 2003. Vice-county Census Catalogue (VCCC).