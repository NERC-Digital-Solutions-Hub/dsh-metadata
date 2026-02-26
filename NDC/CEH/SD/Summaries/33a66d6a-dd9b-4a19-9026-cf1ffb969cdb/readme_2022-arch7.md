# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A six-file dataset (plus ReadMe) compiling trait information for butterflies and macro-moths of Great Britain and Ireland.
- Aims to support data products and map-based analyses by providing life-cycle ecology, phenology, host plant associations, breeding habitats, morphology, distribution, and abundance trends.
- Designed to be used in GIS to create clear, explorable map visualisations for policymakers, clients, and the public.
- Data are sourced from multiple national recording schemes and literature, with explicit provenance and definitions.

## Files in the dataset
- ecological_traits.csv: core traits data covering life cycle ecology, phenology, host plant specificity, breeding habitat, morphology, conservation status, and distribution/abundance trends. Contains multiple data resolutions (broader categories with subcategories) and a wide set of columns (e.g., presence by country, red list status, grid-based occupancy, trends, diurnal/nocturnal, overwintering, phenology by month, larval/pupal/adult monthly stages, and host plant interactions).
- excluded_species.csv: Lepidoptera species excluded from the database (mainly adventive or micro-moths).
- excluded_subspecies.csv: Lepidoptera subspecies and forms excluded from the database.
- hostplant_list_stacked.csv: raw hostplant data; multiple rows per species corresponding to different hostplants (Henwood et al. 2020; Stace 2019 names).
- hostplant_list_unstacked.csv: per-species row with hostplants listed as columns (binary 1 indicates known use).
- ReadMe.docx: metadata documentation detailing data derivation, column criteria, numbering, and references.

## Key data structure and fields (high-level)
- Species identifiers: abh_number, b&f_number, wiemers_checklist_number, k&r_number; scientific_name; common_name; family.
- Distribution and status: recorded_present by country (England, Wales, Scotland, Northern Ireland, Ireland); categories for reintroduced, immigrant, resident, extinct_gb, extinct_i; red_list_gb; red_list_ireland.
- Spatial measures: gb_10_km_squares, ireland_10_km_squares (counts of grid squares with records for 2000–2016).
- Temporal trends: long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, range_long_term_distribution_trend_gb; short_term_distribution_trend_gb, sig_short_term_distribution_trend_gb, range_short_term_distribution_trend_gb; abundance_trend_gb, sig_abundance_trend_gb, range_abundance_trend_gb.
- Life-history and ecology: diurnal, nocturnal, easily_disturbed_by_day, communal_or_nest, below_ground, leaf_litter_moss_on_ground_soil_surface, hostplant_external, hostplant_internal_stem, hostplant_internal_root, other_vegetation_external, stone_inc_walls, dead_rotten_wood, wingless_reduced_wing_female, forewing_minimum, forewing_maximum, estimated_dry_mass, obligate_univoltine, obligate_multivoltine, partial_generation, phenology_shift, sig_phenology_shift_.
- Phenology and life stages: egg_stage (12-month columns), larval_stage (12 months with '?' for uncertain months), pupal_stage (12 months with possible multiple overwintering), adult_stage (12 months; months where adults are present; moths use threshold of ≥1% records), overwintering_stage.
- Habitat and hostplants: broad_host_plant_category, host_plant_section, common_hostplants, habitat (breeding habitats and subcategories), number_hostplants, hostplant_or_hostplant_category and related scientific/native status columns, Ellenberg-related values (light, moisture, reaction, nitrogen, salt_tolerance).
- Miscellaneous: body mass estimates (estimated_dry_mass), leaf/flower/parts usage by hostplant sections, and various interpretation notes (e.g., data merging, latitudinal considerations, and data sources).

## Spatial context and boundaries for GIS work
- Political boundaries used vary by data source (Great Britain: England, Scotland, Wales; United Kingdom: GB plus Northern Ireland; Ireland: island including NI and Republic of Ireland).
- Occupancy/trend data correspond to these political areas; 10 km grid square counts are provided for GB and Ireland over defined periods.
- Data sources include national recording schemes and published atlases; citations and provenance are documented in ReadMe and the References.

## Data provenance and sources
- Primary dataset provenance: Cook et al. 2021, "A traits database for the Butterflies and Macro-moths of Great Britain and Ireland."
- Data sources include Butterfly Monitoring Scheme (UKBMS), Butterflies for the New Millennium, National Moth Recording Scheme (NMRS), MothsIreland, Rothamsted Insect Survey, Hemwood/Sterling/Lewington hostplant data, and several checklists and red lists.
- ReadMe and associated references provide detailed descriptions of column derivations, data merging, and criteria for numbering and categorisation.

## How to use in GIS (practical guidance)
- Join keys: use abh_number or scientific_name to link ecological_traits.csv with species layers or grids.
- Map presence and occupancy: create layers showing recorded_present by country, 10 km squares, and trends (long/short term; abundance) with significance indicators.
- Phenology and life stages: generate monthly maps from egg_stage, larval_stage, pupal_stage, and adult_stage (with caution for uncertainties marked by '?').
- Habitat and hostplants: map breeding habitats and hostplant associations (common_hostplants; host_plant_section; broad_host_plant_category) to analyse habitat connectivity and food-web relationships.
- Hostplant networks: use hostplant_list_unstacked (binary indicators per hostplant) to build bipartite networks or species-to-hostplant maps; combine with Ellenberg-based environmental values for habitat suitability analyses.
- Native vs non-native: leverage hostplant_native_or_non_native and related fields to assess potential refugia and distribution under habitat change.
- Data quality and limitations: account for varying data resolution, cross-border data availability, and uncertainties in monthly phenology and overwintering status; note model-derived mass estimates and non-latitude-adjusted phenology.

## Data quality, limitations, and considerations
- Data are derived from multiple schemes and literature; boundaries and resolutions may differ between sources.
- Latitudinal variation in phenology is not explicitly adjusted in monthly fields.
- Some monthly indicators use thresholds (e.g., adult presence defined for moths as ≥1% of records), and certain fields include '?' to denote uncertainty.
- Mass estimates are model-derived and should be treated with caution; best suited for cross-family analyses rather than precise mass calculations.
- Excluded species/subspecies lists indicate data selection criteria; users should be aware of potential gaps in coverage for adventive or micro-moth taxa.

## Citation and licensing
- If used in publications, cite: Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.
- Acknowledgments and references provide attribution to data providers and underlying sources; permissions were granted to incorporate raw hostplant and trait data.