# UK Environmental Change Network (http://www.ecn.ac.uk) Ground Predators (IG)

## What this dataset is
- A ground predator monitoring dataset from the UK Environmental Change Network (ECN), focusing on Carabidae abundance.
- Data collected using pitfall traps, following ECN protocols.
- Managed by the ECN Data Centre with sponsorship from multiple UK government departments and agencies.

## Purpose and aims (Analysts’ perspective)
- To provide a consistent, time-series view of environmental health and policy performance related to ground-dwelling predators.
- To enable verification, quality assurance, transformation, and standardised analysis of datasets for monitoring environmental change.
- To support reporting in clear formats (reports, maps, charts) and to ensure datasets are stored/uploaded to appropriate portals for reuse.

## Protocol and data collection
- Monitoring target: abundance of ground predators (Carabidae) via pitfall traps.
- Sampling frequency: fortnightly between May and October.
- Data quality: use accompanying quality information to assess data reliability; protocol references available.

## Data structure and organization
- Data are stored in Oracle with site-specific tables:
  - D1IG_xxx: core dataset tables (one per site) containing site, location, and sampling attributes.
  - D2IG_xxx: information about when traps were set out (trap-out times).
  - D3IG_xxx: habitat information (habitat descriptions per site).
- Core metadata and structure are documented separately (metadata documentation referenced).

## Site codes and basic site details
- T01 Drayton (52°11'37.95"N, 1°45'51.95"W) — date range in dataset: 12-MAY-1993 to 28-OCT-2009
- T02 Glensaugh (56°54'33.36"N, 2°33'12.14"W) — 27-MAY-1994 to 31-OCT-2012
- T03 Hillsborough (54°27'12.24"N, 6°4'41.26"W) — 14-MAY-1993 to 31-OCT-2012
- T04 Moor House - Upper Teesdale (54°41'42.15"N, 2°23'16.26"W) — 20-MAY-1993 to 17-OCT-2012
- T05 North Wyke (50°46'54.96"N, 3°55'4.10"W) — 05-MAY-1993 to 30-NOV-2010
- T06 Rothamsted (51°48'12.33"N, 0°22'21.66"W) — 28-JUL-1992 to 03-NOV-2009
- T07 Sourhope (55°29'23.47"N, 2°12'43.32"W) — 25-MAY-1994 to 14-NOV-2012
- T08 Wytham (51°46'52.86"N, 1°20'9.81"W) — 26-MAY-1993 to 31-OCT-2012
- T09 Alice Holt (51° 9'16.46"N, 0°51'47.58"W) — 18-MAY-1994 to 31-OCT-2012
- T10 Porton Down (51° 7'37.83"N, 1°38'23.46"W) — 24-MAY-1994 to 31-OCT-2012
- T11 Y Wyddfa - Snowdon (53° 4'28.38"N, 4° 2'0.64"W) — 19-MAY-1999 to 28-NOV-2012
- T12 Cairngorms (57° 6'58.84"N, 3°49'46.98"W) — 23-JUN-1999 to 14-NOV-2012

## Data fields and structure (high-level)
- Core dataset tables (D1IG_xxx):
  - SITECODE, LCODE, SDATE (sampling date), TRAP (trap number, optional), FIELDNAME (field name or quality code), VALUE (numeric count or measurement).
- Trap timing tables (D2IG_xxx):
  - SITECODE, LCODE, FROMDATE (date traps were set out), SDATE (date traps were collected).
- Habitat tables (D3IG_xxx):
  - SITECODE, LCODE, HABDESC (habitat description).
- Metadata and core site information referenced in the ECN metadata documentation.

## Field naming and codes (key concepts)
- Fieldname entries may contain species codes or quality codes.
- Quality codes (Q1–Q8 in the data) are defined in the accompanying ECN quality codes, used to annotate data quality and field conditions.
- The QC scheme includes a broad set of standard ECN codes (examples include data loss, sample loss, weather-related effects, observer or equipment issues, and other context). A special code 999 denotes an unusual event with accompanying quality text.
- Species codes and taxonomy:
  - A comprehensive taxonomy mapping exists (species codes and genus/species names) for ground beetles (Carabidae) and related taxa, enabling detailed species-level or genus-level analyses.
  - The dataset includes hierarchical codes for many genera and species (e.g., multiple entries under a genus with species-level codes, and instances where a code maps to a higher taxonomic level).

## Data use, attribution, and access
- ECN requests acknowledgment in publications that use these data and requests one reprint of any citing publication.
- Data are designed to be stored and uploaded to appropriate data portals, enabling sharing and reuse.
- Protocols and measurement methods are standardized and documented (protocol reference provided).

## Practical considerations for analysts
- Verify data against the accompanying quality information before analysis.
- Use standardised methods to derive outputs such as environmental health indicators, species abundance, and community composition for ground predators.
- Present results in clear formats (maps, charts, reports) and ensure data are accessible through ECN portals.
- Consider combining ECN Ground Predators data with other environmental datasets to increase data utility and avoid single-use limitations.
- Acknowledge data sources in publications and share reprints as requested.

## Protocol reference
- ECN protocol: http://www.ecn.ac.uk/measurements/terrestrial/i/ig

## Summary of key challenges and opportunities
- Challenge: increasing the value of the pitfall-trap dataset by integrating with complementary environmental data.
- Opportunity: improve data accessibility for external users and enable broader reuse of the underlying datasets.