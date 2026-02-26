# UK Pollinator Monitoring Scheme metadata: Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Purpose and scope
- Metadata for version 2 of the Flower-insect timed count (FIT Count) dataset from the UK Pollinator Monitoring Scheme (PoMS), part of the PMRP.
- Describes two surveys: public FIT Counts and the 1 km square FIT Counts, including methodology, quality checks, and data structure.
- Aims to monitor insect pollinator populations across the UK and support national pollinator strategies.
- Notes that 2017 was a pilot year with less data; version 2 deduplicates duplicate records from the previous version.

## Data access and citation
- Data available at the provided DOI: https://doi.org/10.5285/13aed7ac-334f-4bb7-b476-4f1c3da45a13
- Licensed under the Open Government Licence; users must cite the dataset in any publications describing research that uses the data.
- Required acknowledgement: PoMS funded by Defra, devolved administrations, JNCC, and UKCEH; volunteers are acknowledged.
- © multiple organisations (UKCEH, conservation trusts, museums, universities, and government bodies).

## What is included in the dataset
- Two data files:
  - ukpoms_1kmFITCountData_2017-2020.csv (FIT Counts from the 1 km square survey)
  - ukpoms_publicFITCountData_2017-2020.csv (Public FIT Counts)
- Data cover the years 2017–2020 (with 2017 as a pilot year).
- Data are linked to PoMS squares, habitat classifications, target flowers, and counts by insect groups.

## Dataset structure and key attributes
- 1 km square FIT Count data includes: country, location_code/name, 1 km grid reference, land cover (agricultural or semi-natural), date/year, habitat, target flower (and corrections), plant family, floral unit counts/types, weather context (cloud, sunshine, wind), habitat_type, flower_structure, insect group counts (bumblebees, honeybees, solitary bees, wasps, hoverflies, other flies, butterflies/moths, beetles, small insects, others), and total insect count.
- Public FIT Count data includes: country, date/year, 1 km square grid reference, habitat, target flower (and corrections), habitat_type, flower_structure, insect group counts, and additional fields such as enjoyment and difficulty for the recorder.
- Both data files include data quality fields (e.g., corrected target flower names, photo verification where applicable, and geolocation checks).

## Data collection methodology
- Public FIT Counts:
  - Locations and dates chosen by participants; counts conducted 1 April–30 September each year.
  - Weather thresholds: minimum 13°C with clear sky or 15°C with cloudy sky.
  - Use a 50 cm × 50 cm quadrat; 10-minute counting period; 14 predefined target flowers (with options to record other flowers).
- 1 km square FIT Counts:
  - Same counting method as public counts but conducted in up to 75 randomly allocated 1 km squares.
  - Four visits per summer (May–August), aligned with PoMS pan-trap surveys.
  - Squares co-located with NPMS squares (England/Scotland) or other large-field squares (Wales); habitat stratification uses CEH Land Cover Map 2007 (LCM) to define agricultural vs semi-natural squares.
- Habitat and sampling design:
  - Stratification by habitat and landscape type (agricultural vs semi-natural) to monitor pollinator changes across different landscapes and crop contexts.

## Quality assurance and data governance
- Data entry via online forms (iRecord/Indicia) with post-season QA.
- PoMS staff review submitted photos for target flowers and correct names as needed; floral units checked against target flowers; plant family names added via lookup.
- 1 km square data validated to ensure coordinates fall within linked squares; misclassified data corrected; data outside the recording period or with missing geolocations excluded.
- Methodology documentation available on the PoMS website; guidance covers counting, target flowers, insect groups, and recording forms.

## Data provenance and collaboration
- PoMS part of the PMRP and works with other pollinator recording schemes; two large-scale surveys run with volunteer support.
- Acknowledges Defra, devolved governments, JNCC, UKCEH, and NERC funding; acknowledges volunteers for data collection.

## Practical notes for data leaders
- Version 2 dataset removes duplicates from the earlier version and provides standardized, deduplicated records.
- The dataset emphasizes data discoverability, metadata completeness, and consistent cross-year harmonization (e.g., translation of 2017 data terms to 2018–2020 term lists).
- For advanced analyses, link the FIT Count data with the PMRP literature and the National Plant Monitoring Scheme where appropriate; refer to the provided references for methodological context.

## References and further documentation
- Carvell et al. design and testing reports (Defra/UK government).
- PMRP establishment and progress reports (Defra, Scottish/ Welsh Governments, JNCC).
- PoMS reports and UKpoms.org.uk resources for methodology and field guidance.