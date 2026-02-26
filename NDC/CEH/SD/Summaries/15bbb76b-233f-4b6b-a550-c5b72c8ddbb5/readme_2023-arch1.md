# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A six-file dataset compiling life-cycle traits, host-plant associations, habitat, distribution, and abundance information for butterflies and macro-moths of Great Britain and Ireland.
- Intended to support data-driven analysis of ecological patterns, correlations, and potential impacts of actions; suitable for government, environmental bodies, and academic research.
- Dataset is citable (Cook et al., 2021) and aggregates numerous primary sources with metadata to enable reproducibility.

## Dataset contents
- ecological_traits.csv: Core traits including life cycle ecology, phenology, host-plant specificity, breeding habitat, morphology; presence/absence data by political boundaries; conservation status and distribution/abundance trends; extensive monthly phenology and life-stage indicators; overwintering and pupation details; host-plant and habitat classifications.
- excluded_species.csv: Lepidoptera species excluded from the database (mostly adventive or micro-moths).
- excluded_subspecies.csv: Lepidoptera subspecies and forms excluded from the database.
- hostplant_list_stacked.csv: Raw stacked host-plant data from Henwood et al. 2020; multiple rows per species for multiple hostplants; hostplants named per Stace (2019).
- hostplant_list_unstacked.csv: Unstacked, single-row-per-species representation of hostplants; binary indicators for hostplant use.
- ReadMe.doc: Detailed descriptions of column derivations, data provenance, numbering criteria, and references.
- Table 1–6 in ReadMe summarize files, formats, and sizes (ecological_traits: 970 rows; hostplant lists: ~5k rows; etc.).

## Key data fields and structure
- Identifiers and taxonomy: abb_number (ABH), b&f_number, wieders_checklist_number, k&r_number, scientific_name, common_name, family.
- Occurrence and status: recorded_present by England, Wales, Scotland, Northern Ireland, Ireland; reintroduced, immigrant, resident, extinct_gb, extinct_i, red_list_gb, red_list_ireland, 10km_squares counts (gb/ireland), rarity indicators, long_term and short_term distribution trends with significance flags and ranges.
- Phenology and life stages: diurnal/nocturnal; easily_disturbed_by_day; communal_or_nest; overwintering_stage; larval_stage; pupal_stage; adult_stage (monthly indicators); overwintering details; egg_stage (12 months, months BA-BL); larval_stage (BM-BY) with potential uncertainty markers; pupal_stage (BZ-CK, with multiple overwintering notes); life-stage timing not adjusted for latitudinal variation in phenology.
- Host-plant ecology: hostplant_specificity (monophagous/ oligophagous (genus or family)/ polyphagous); number_hostplants; hostplant_and_category fields; hostplant_species and hostplant_names from stacked/unstacked lists; native/non-native status; Ellenberg-based environmental values for hostplants (light, moisture, reaction, nitrogen, salt_tolerance); broad_host_plant_category and host_plant_section classifications; common_hostplants indicators.
- Habitat and breeding: habitat columns with broad and specific categories; breeding habitat details; upland associations; definitions for specific categories (e.g., scrub, wetland, montane upland, etc.).
- Morphology and mass: forewing_minimum/maximum; estimated_dry_mass (model-based, caution advised); wingedness traits (wingless_reduced_wing_female).
- Pupal and overwintering strategies: various positions and substrates (below_ground, leaf_litter_moss_on_ground_soil_surface, hostplant_external/internal_root/internal_stem, other_vegetation_external, stone_in_walls, dead_rotten_wood), and multiple overwintering strategies when applicable.
- Data provenance and quality: merged headers with notes; some columns describe data ranges or notes about data scope; data sources and verification procedures summarized in ReadMe.

## Data sources and provenance
- Primary source: Cook et al., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland (Butterfly Conservation & Centre for Hydrology and Ecology, UK).
- Underlying data drawn from: Agassiz et al. (2013); Emmet & Heath (1991, 1992); Henwood et al. (2020); Waring & Townsend (2017); Fox et al. (various); Rothamsted Insect Survey; UKBMS; NMRS; MothsIreland; and others.
- ReadMe and metadata explain column derivations, data boundaries (e.g., political regions vs administrative units), and references used to collate the dataset.
- Dataset should be cited when used in publications; acknowledgement of data contributions from many authors and institutions.

## Usage notes and considerations
- Boundary definitions: distribution data are provided according to specified political boundaries (Great Britain, United Kingdom, Ireland) with explicit metadata clarifying scope.
- Temporal and phenology caveats: monthly egg/larval/pupal/adult stages are provided, but phenology may not be latitudinally adjusted; ranges and trends rely on occupancy and recording effort corrections where available.
- Data gaps and scale: potential lack of local-level data; some fields rely on modeled estimates (e.g., estimated_dry_mass) or expert-derived categories; users should consider scale and uncertainty when combining datasets.
- Data integration: stacked vs unstacked hostplant lists require careful merging; ensure consistent species identifiers (abh_number) when linking hostplants to traits.
- Reproducibility: extensive metadata and ReadMe documentation to facilitate traceability and reuse.

## Citation
- Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.

## Access and format
- Six CSV/Doc files: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.doc.
- ReadMe contains header notes, data definitions, and a detailed table of contents for the dataset.