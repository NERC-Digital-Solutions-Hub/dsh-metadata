# Supporting documentation for UK Environmental Change Network (ECN) bird data: 1995-2012 (Rennie, S. et al (2015) http://doi.org/10.5285/c616149a-fb19-4d6b-a9e5-84363538ed7e)

## Overview
- ECN bird data covering 1995–2012, managed by the ECN Data Centre (Centre for Ecology and Hydrology).
- ECN is sponsored by a consortium of UK government departments and agencies funding site monitoring and network coordination.
- Authors request acknowledgement of data use and one reprint of publications citing ECN data.

## Data collection and methodology
- Data come from a national-scale transect-based survey of birds, following the Breeding Birds Survey methodology (BTO).
- Birds are recorded on transects within 1 km squares; distance from transect to bird is noted.
- Transects are walked twice per year (early and late season).
- Site-based data are designed for national-scale monitoring and have limitations for establishing precise population–environment relationships; should be used alongside broader monitoring programmes (e.g., BTO data).
- Early ECN protocols included BTO Common Bird Census (lowland) and Moorland Bird Survey (upland); Breeding Bird Survey replaced these at ECN sites.

## Data structure and fields
- Core data (ECN_BB1-like structure):
  - SITECODE, Description: Site code
  - LCODE, Description: Location code
  - VISIT, Description: Visit (E = early, L = late)
  - SDATE, Description: Sampling date
  - TRANSECT, Description: Transect identifier
  - FIELDNAME, Description: Bird species code
  - VALUE, Description: Count value
  - DISTANCE, Description: Distance category (1 = within 25 m each side; 2 = 25–100 m; 3 = >100 m; F = bird in flight)
  - DISTANCE, Notes: Additional distance metadata
- Metadata on observations (ECN_BB2.csv):
  - FROM_HOUR/FROM_MINS, TO_HOUR/TO_MINS: Start/end times
  - CLOUD, RAIN, WIND, VISIBILITY: Weather conditions (BTO codes)
- Habitat metadata (ECN_BB3.csv):
  - FIRSTHL1/SECONDHL1, FIRSTHL2/SECONDHL2, FIRSTHL3A/SECONDHL3A, FIRSTHL3B/SECONDHL3B, FIRSTHL4A/SECONDHL4A, FIRSTHL4B/SECONDHL4B:
    - Habitat codes by levels 1–4; year; transect; and other habitat descriptors
- Habitat codes:
  - Based on the BTO habitat recording system with levels 1–4
  - Level 1 codes cover main habitat types (A–J) such as woodland, scrubland, semi-natural grassland/marsh, heathland/bogs, farmland, human sites, water bodies, coastal, inland rock, miscellaneous
  - Level 2–4 codes provide increasingly detailed subcategories (e.g., woodland: broadleaved, coniferous, mixed; shrubland characteristics; disturbance levels; shrub/field layer density; grazing status)
  - Each main habitat type includes multiple Level 2–4 codes to describe specific habitat features and management (e.g., coppice, disturbance, shrub density, grazing, hedgerows, water regime, man-made structures)

## Sites and site codes
- Site codes (example subset):
  - T01 to T12 with site names: Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Alice Holt, Porton Down, Y Wyddfa - Snowdon, Cairngorms
- Each site entry includes:
  - Geographic coordinates
  - Date range of data collection per site (e.g., 29-Apr-1995 to 14-Jun-2010 for T01)
- These site records underpin the ECN bird data across the 1995–2012 period

## Bird species codes
- A comprehensive mapping of species codes to species names is provided
- Examples (illustrative; full list included in the dataset):
  - Codes for Arctic Skua, Arctic Tern, Little Tern, Avocet, Blackbird, Blackcap, Bullfinch, etc.
  - The dataset includes a code for no birds present (XX) and a range of common and rare species
- The species code table enables standardized counting across sites and years

## Additional and supporting metadata
- ECN_BB2.csv: Weather and survey timing metadata (cloud, rain, wind, visibility; survey start/end times)
- ECN_BB3.csv: Habitat metadata for transects (Year, TRANSECT, FIRSTHL1–SECONDHL4 codes; habitat structure levels)
- These metadata tables support data quality checks, reproducibility, and context for habitat and weather influences on birds

## Habitat coding scheme details
- Level 1 codes correspond to broad habitat types (A–J)
- Level 2 codes specify subcategories (e.g., woodland: Broadleaved, Coniferous, Mixed)
- Level 3 and Level 4 codes capture finer habitat features (e.g., coppiced, disturbance levels, shrub density, grazing status)
- Examples of habitat categorization include:
  - A - WOODLAND; Level 2: Broadleaved, Coniferous, Mixed; Level 3/4: disturbance, canopy structure, shrub/field layers
  - B - SCRUBLAND/young woodland; Level 2: regenerating woodland, downland, heath scrub; Level 3/4: vegetation structure and disturbance
  - C - Semi-natural Grassland/Marsh; Level 2: downland, grassland types; Level 3/4: boundary features, grazing, disturbance
  - D–J cover heathlands, farmland, human sites, water bodies, coastal, inland rock, and miscellaneous habitats with similarly detailed subcodes

## Governance, usage, and limitations
- Data provenance and sponsorship indicate government and agency collaboration; datasets are shared to support monitoring of environmental change
- Acknowledgement and sharing of reprints are requested to demonstrate the data’s value and usage
- Limitations to note:
  - Site-based data are designed for national-scale assessment and may limit inferences about precise relationships between population levels and specific environmental changes
  - Recommend coupling ECN Bird data with broader programmes (e.g., BTO) for comprehensive analyses
- The documentation serves as a detailed guide for data structure, metadata, and habitat classification to enable proper use, integration, and governance in monitoring frameworks