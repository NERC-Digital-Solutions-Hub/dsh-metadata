# UK Pollinator Monitoring Scheme metadata: pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

- Purpose and scope
  - Metadata for the PoMS pan-trap survey data (2017–2020, version 2), including samples, insect occurrences (bees and hoverflies to species where possible), and flowering plants within 2 m of pan-trap stations.
  - Data are used to monitor pollinator abundance and distribution across the UK and to support national pollinator strategies.
  - Version 2 corrects summed totals from the previous version and includes detailed QA processes.

- Study design and sampling strategy
  - 75 randomly allocated 1 km squares across England, Scotland, and Wales (GB total) to monitor pollinators in agricultural and semi-natural landscapes.
  - Squares stratified by habitat cover (agricultural vs semi-natural) using CEH Land Cover Map 2007; further classified as agricultural or semi-natural based on >50% cover in defined habitat classes.
  - Within each square, a diagonal transect with five pan-trap stations arranged evenly and separated by at least 100 m.
  - Pan traps: three colored bowls per station (yellow, blue, white on UV primer), placed on stakes or ground, filled with water and a drop of washing-up liquid.
  - Sampling protocol: up to 75 squares, four visits per summer (May–August), minimum two weeks between visits to a square; traps exposed for 6 hours (09:00–17:00 BST); weather thresholds for sampling days.
  - Location and access guidelines emphasize open, minimally shaded sites, avoidance of livestock disturbance, and consideration of cropping activities and landowner permissions.
  - Sampling period includes 2017 (pilot year with fewer data) through 2020, with variations due to weather, access, and covid restrictions in 2020.

- Data collection, processing, and QA workflow
  - Data collection by PoMS volunteers and staff; entered into iRecord (Indicia data warehouse) in three stages: sampling/environmental data, insect counts by trap station, and taxonomic identifications for bees/hoverflies.
  - Insects sorted at UKCEH labs; bees/hoverflies identified to species where possible; other taxa identified to higher taxonomic levels as needed.
  - QA checks include photo verification of flowering plants near traps, cross-checking identifications, and verification by multiple taxonomists for rare or out-of-range occurrences.
  - Specimen-level QA checks in 2019 and 2020 involved selecting 81 and 79 specimens, respectively, for validation across criteria (random, outside known range, rare/difficult taxa, taxonomist requests). Some identifications updated or reclassified as a result.
  - Aggregation rules: when species-level IDs are not possible, specimens aggregated into defined species groups; original taxon data is retained for reference; aggregates used to ensure consistent analysis.

- Data files and their structure
  - ukpoms_1kmPanTrapData_2017-2020_samples.csv
    - sample_id, country (England/Scotland/Wales), location_code, location_name, X1km_square, sample_projection (OSGB), land_cover (agricultural/semi-natural), date, year, digitised_by, pan_trap_station (1–5), trap_active_from, trap_active_to, trap_disturbed, temperature_start, temperature_end, cloud_cover_start, cloud_cover_end, wind_speed_start, wind_speed_end, exposure_sun, cast_shadow, vegetation_height_average, habitat_main, habitat_other, moved, sample_code_bycatch, wasps_solitary, wasps_social, wasps_parasitic, sawflies, flies, moths, butterflies, beetles_pollen, beetles_other, insects_small, insects_other, spiders, all_invertebrates_excluding_bees_hoverflies, bees, hoverflies, all_invertebrates_including_bees_hoverflies
  - ukpoms_1kmPanTrapData_2017-2020_insects.csv
    - sample_id, country, location_code, location_name, X1km_square, date, year, pan_trap_station, occurrence_id, specimen_code, taxon_group (insect– Diptera/Hymenoptera), taxon_source, English_name, source_taxon_version_key, taxon_standardised, taxon_aggregated, count (always 1), sex, stage, comment, Order, Family
  - ukpoms_1kmPanTrapData_2017-2020_flowers.csv
    - sample_id, country, location_code, location_name, X1km_square, date, year, pan_trap_station, occurrence_id, taxon_group (flowering plant), taxon_source, English_name, source_taxon_version_key, Order, Family, floral_unit, total_floral_units
  - Linkage: sample-level data links to occurrence data via sample_id; 1 km square-level data links to geographic coordinates (OSGB) and habitat attributes.

- Geographic and spatial details
  - Coordinate system: OSGB (Ordnance Survey Great Britain) grid references for 1 km squares.
  - Spatial scope: 75 GB-wide 1 km squares, with 5 pan-trap stations per square, across England, Scotland, and Wales.
  - Habitat and land-cover attributes include main/other habitats within a 2 m radius of each trap station and predominant land-cover category for each square.

- Data quality, limitations, and notes
  - Data from 2017–2020 were entered via standardized online forms; some years have incomplete sampling due to land access, weather, volunteers, or covid restrictions (notably 2020).
  - Species identifications for bees/hoverflies are taxonomist-led; some taxa are aggregated due to indistinguishability or male-only distinguishing features; full taxon details retained for reference.
  - Annex provides detailed aggregation rules for taxa not distinguishable to species level, including notes on particular genera and identification limitations (e.g., many instances require male specimens for species-level IDs).

- References and provenance
  - Cited design, testing, and program reports for PoMS and PMRP (design and testing of national pollinator framework; PMRP progress and final reports).
  - The metadata document notes the withdrawal of the previous version due to incorrect totals and provides links to PoMS and PMRP project outputs.

- Usage guidance for GIS specialists
  - Suitable for map-based analyses of pollinator abundance and distribution across GB, with the ability to join to habitat, land-cover, and environmental layers.
  - Use sample_id to join samples with insect and flower occurrences; use X1km_square and location references to map sampling sites.
  - Be mindful of year- and square-level coverage gaps; account for potential sampling bias due to weather, access, and volunteer availability.
  - Coordinate with aggregation rules when analyzing species-level data, particularly for taxa requiring male individuals or where cryptic species exist.

- Annex note
  - Aggregation schemes for taxa not distinguishable to species level are provided, detailing how recorded taxon, standardised taxon, and aggregated taxon relate, with examples across Hymenoptera and Diptera.