# Supporting documentation on the patch-discovery experiment

## Objective and study design
- Investigates how changes in local population density influence the discovery of a novel resource (a new feeder) by birds.
- Conducted in Wytham Woods, Oxfordshire, UK, January–March 2021.
- Species studied: great tits, blue tits, marsh tits.
- Experimental setup includes two existing feeders per site, with an additional novel feeder placed ~40 meters away in opposite directions.
- A second patch-discovery experiment varied the locations of the novel feeders during the density manipulation period.
- Novel feeders allowed access to all PIT-tagged birds and used the same design as existing feeders to minimize neophobia.
- Data collection performed by named researchers (Keith McMahon, Sam Croft, Kristina Beck).

## Data structure and fields
- Dataset comprises a single CSV file.
- Key fields:
  - Date and Time of each individual visit to a novel feeder (logger).
  - Bto.ring: identifier for the visiting individual.
  - Site: experimental site identifier.
  - Bto.species.code: species code (greti = great tit, bluti = blue tit, marti = marsh tit).

## Data collection methods
- Birds captured during winter with mist-nets or nestboxes and fitted with metal leg-rings and a PIT tag.
- Novel feeders provided sunflower seeds and accessible to all PIT-tagged birds.
- Feeder visits recorded as part of assessing discovery time and order.

## Data governance, quality, and provenance considerations
- Source information includes contributors: Keith McMahon, Sam Croft, Kristina Beck.
- Related context references: Savill et al. 2011 (Wytham Woods ecological laboratory).
- For data management, consider cataloging:
  - Data versioning and provenance (experiment conditions, dates, sites).
  - Consistency of date/time formats and site naming.
  - Clear mapping of species codes to taxa if reused beyond the original study.
  - Documentation of any data cleaning or transformation steps.

## Potential uses and relevance for data leaders
- Supports analysis of how population density manipulation affects discovery dynamics of a resource.
- Demonstrates integration of behavioral observations with tagging and feeder-tracking data.
- Provides a compact, well-documented dataset structure suitable for time-stamped event analyses (per-individual visits to resources).
- Illustrates end-to-end data lifecycle from collection in the field to a single consumable dataset for downstream analysis.

## References
- Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press.