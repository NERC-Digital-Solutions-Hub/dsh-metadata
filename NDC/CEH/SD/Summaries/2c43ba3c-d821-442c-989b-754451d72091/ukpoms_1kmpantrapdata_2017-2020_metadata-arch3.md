# UK Pollinator Monitoring Scheme metadata: pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview and purpose
- Provides metadata and description for the pan-trap survey data from PoMS (2017–2020, version 2).
- PoMS aims to monitor pollinator populations across the UK and inform national pollinator strategies; data support environmental health monitoring and decision-making.
- Data are part of a wider PMRP effort to understand changes in insect pollinator populations and are associated with large-scale surveys and public engagement.

## Scope and survey design
- Survey network: 75 randomly allocated 1 km squares across England, Scotland, and Wales; aims to monitor pollinator abundance in agricultural and semi-natural landscapes.
- Co-located sampling: 1 km squares aligned with other biodiversity monitoring schemes (e.g., NPMS in England/Scotland; Wales squares aligned with other natural resources data).
- Habitat stratification: squares characterized as agricultural or semi-natural based on CEH Land Cover Map 2007; sampling positions selected to cover habitat diversity and land-use types.
- Sampling within squares: five pan-trap stations per square, placed diagonally with minimum 100 m separation; traps set on open ground and oriented to minimize disturbance.
- Temporal design: up to four visits per summer (May–August) per square, weather permitting; minimum two weeks between visits; data gaps possible due to land access, weather, or COVID-19 restrictions in 2020.
- Target power: prior analyses suggested 75 sites provide >80% power to detect ~30% change in common pollinator groups over 10 years.

## Data collection and protocol
- Pan traps: three colored bowls per station (yellow, blue, white; water plus a few drops of detergent) to capture insects over a 6-hour exposure (09:00–17:00 BST).
- Weather thresholds: at least part of trapping period under specific conditions (temperature and cloud/wind thresholds) to ensure suitable sampling.
- Specimen handling: insects returned to UKCEH labs; bees and hoverflies identified to species where possible; other groups identified to taxonomic groups.
- Flower data: flowering plants within 2 m of each trap station counted and linked to floral units; separate Flower-Insect Timed Count dataset exists.
- Data collection team: PoMS volunteers and staff; data entry via iRecord/Indicia data warehouse; QA checks implemented at multiple stages.

## Data files and attributes
Three CSV data files are provided:
- ukpoms_1kmPanTrapData_2017-2020_samples.csv
  - Contains sample-level data: sample_id, country, location_code/name, 1 km square, land_cover, date/year, trap details, weather variables, habitat, movement, ground conditions, trap counts by taxonomic groups (insects, bees, hoverflies, flowers-related fields, etc.).
- ukpoms_1kmPanTrapData_2017-2020_insects.csv
  - Contains occurrence-level data for bees and hoverflies linked to samples: occurrence_id, specimen_code, taxon information (group, name, source, standardised/aggregated taxon), count, sex, life stage, etc.
- ukpoms_1kmPanTrapData_2017-2020_flowers.csv
  - Contains occurrence-level data for flowering plants within 2 m of traps: occurrence_id, taxon group/order/family, floral_unit information, and counts.

- Data attributes include: country, location codes/names, grid references, sampling date/year, trap station, environmental variables (temperature, cloud cover, wind, exposure, vegetation height), land cover, habitat codes, and multiple taxonomic detail levels (including aggregated and standardised taxa for consistent analysis).

## Quality assurance, data governance, and versioning
- Versioning: metadata document is version 2; previous version was withdrawn due to incorrect summed totals for insect specimens and has been corrected.
- Data capture and QA: online recording via iRecord; three-stage data entry (field data, lab counts, taxonomic identifications); species identifications validated by taxonomic experts; cross-checks by a second taxonomist in 2019–2020 for certain specimens.
- Verification for problematic records: specimens flagged for difficulty, out-of-range distribution, or random checks; corrections and re-classifications recorded in the database.
- Aggregation approach: when species-level identification is not possible, specimens are aggregated into defined species groups for consistent analysis; original taxon identifications retained for reference.
- Metadata completeness: extensive attribute metadata provided to support data use and verification; quality checks include photo verification of flowering plants near pan-traps and lookup-table enrichment for plant families/types.

## Data governance and sharing
- Data are part of a publicly accessible monitoring framework; underlying data should be shared in accordance with governance processes described by PoMS and PMRP partners.
- Acknowledgement requirements specify funders and collaborating organizations; PoMS is funded by Defra, devolved administrations, JNCC, and UKCEH, with UKCEH contribution supported by NERC.
- Data are intended to inform policy and management decisions, and are connected to broader national pollinator strategies and monitoring initiatives.

## References and Annexes
- Key references detailing the design and testing of the monitoring framework and the PMRP evolution are listed (Defra reports and PMRP progress documents).
- Annex: Aggregate species groupings for taxa not distinguishable to species level; defines how recorded taxon, standardised taxon, and aggregated taxon relate for multiple taxa (Hymenoptera, Diptera, etc.), with notes on when male specimens are required for species-level identifications and other taxonomic caveats.

## Practical notes for users (from the document)
- The dataset includes both sample-level and occurrence-level data, with linkages across the three files via sample_id and other keys.
- The project encourages engaging volunteers and communities in pollinator monitoring and provides a framework that supports data-driven policy decisions.
- For more information, see the PoMS website and referenced reports.