# UK Pollinator Monitoring Scheme metadata: Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

- Purpose and scope
  - Metadata and description for the Flower-insect Timed Count (FIT Count) data from the UK Pollinator Monitoring Scheme (PoMS) for 2017–2020 (version 2; deduplicated from the previous version).
  - PoMS aims to monitor pollinator populations across the UK and engage volunteers; FIT Count data contribute to national pollinator strategies.
  - PoMS comprises two surveys: the Flower-Insect Timed Count (FIT Count) and a 1 km square survey (co-located with pan-trap data in a separate dataset). The current dataset includes FIT Count data from both the public (volunteer) counts and the 1 km square survey counts (technically aligned with PoMS sampling).

- Data access, licensing, and attribution
  - Data accessible at the provided DOI/URL.
  - Open Government Licence; dataset must be cited in publications describing work that uses it.
  - Acknowledgement required for PoMS funding and volunteers; multiple institutions contribute to PoMS.
  - Copyright © multiple UK institutions and partners.

- About PoMS and the FIT Count datasets
  - PoMS is part of the Pollinator Monitoring and Research Partnership (PMRP) to track UK pollinators’ changes; two large-scale surveys support national monitoring.
  - Datasets described:
    - ukpoms_1kmFITCountData_2017-2020.csv: FIT Counts from the 1 km square survey.
    - ukpoms_publicFITCountData_2017-2020.csv: Public FIT Counts collected by citizen scientists.
  - Data for 2017 are a pilot year with fewer records; 2017 data have been harmonised to align with 2018–2020 methods.

- FIT Count methodology (key features)
  - Public FIT Counts:
    - Occur at user-selected locations/dates from 1 April to 30 September, under weather thresholds (13°C with clear skies; 15°C with cloudy skies).
    - Count insects visiting a target plant within a 50 cm × 50 cm quadrat for 10 minutes.
    - 14 target flower types are provided; participants may use other flowers if needed.
  - 1 km square FIT Counts:
    - Follow the same methodology as public counts.
    - Conducted in up to 75 randomly allocated 1 km squares (England, Scotland, Wales) for four visits per summer (May–August), with potential gaps.
    - Squares co-locate with PoMS pan-trap surveys and align with the National Plant Monitoring Scheme (NPMS) sampling framework in England/Scotland and with a UK-wide pool in Wales.
  - Habitat stratification:
    - GB 1 km squares matched to habitat coverage using the CEH Land Cover Map 2007 (LCM) to define agricultural (AG) vs semi-natural (SN) squares.
    - Sampling excludes squares that are predominantly urban/coastal or not meeting AG/SN criteria.

- Data collection, quality assurance, and entry
  - Data entry via online forms (iRecord/Indicia) with season-end QA checks.
  - QA steps include:
    - Photo verification of target flowers; corrections to plant identifications as needed.
    - Cross-checking floral units with the target flower; applying corrections to floral unit counts.
    - Adding plant family names to target flowers via lookup tables.
    - Location verification for 1 km square counts; correction of misclassified data between public and 1 km datasets.
    - Exclusion of counts outside the recording period (1 April–30 September) and records with missing geolocations.

- Data files and key attributes (high-level)
  - ukpoms_1kmFITCountData_2017-2020.csv
    - Attributes cover: sample ID, country, location code/name, 1 km square grid reference, date/year, land cover (AG vs SN), habitat, target flower and corrected identifications, flower context and structure, weather indicators (cloud cover, sunshine, wind), habitat type, flower cover, floral units counted, counts by insect groups (bumblebees, honeybees, solitary bees, wasps, hoverflies, other flies, butterflies/moths, beetles, small insects, other insects), and total insects.
  - ukpoms_publicFITCountData_2017-2020.csv
    - Attributes cover similar fields as the 1 km dataset, plus additional fields for public-reported metadata: enjoyment and difficulty of taking part, and recorder confidence-related details; includes counts by insect groups and total insects, with similar target flower and habitat fields.
  - Common data themes across files:
    - Sample identifiers, geographic location (country, location code/name, grid reference), date and year, habitat and land-cover classifications, target flower identifications (with corrected fields), context of the floral patch, weather and environmental conditions during the count, and detailed insect group counts plus totals.

- Data interpretation notes and caveats
  - 2017 data are considered pilot data with fewer records; subsequent years provide more complete coverage.
  - Some 2017 terms and data entries have been harmonised to match 2018–2020 term lists for consistency.
  - Northern Ireland data in the public dataset may include NA values for certain target flower fields; corrected columns exist to align identifications where photos were submitted.
  - The dataset includes translations of older terminology to standardized categories to enable consistent analysis across years.

- Data provenance, governance, and references
  - Metadata and design references to Defra/Scottish/Welsh Government projects and PMRP reports.
  - Key sources include:
    - Carvell et al. design and testing of national monitoring framework (2016).
    - Establishing and progress reports for PMRP (2020).
  - Documentation and guidance for FIT Count methodology are available on the PoMS website.

- How to use the data (practical implications for data work)
  - Suitable for creating self-serve dashboards or reports on pollinator visitation by insect groups to target flowers across UK habitats and years (2017–2020).
  - Can be joined with habitat classification and 1 km square context data to analyze spatial patterns of pollinator activity and habitat associations.
  - QA notes provide a workflow for data cleaning when integrating counts from public and 1 km square datasets.
  - Licensing and citation requirements should be followed to ensure reuse is compliant and properly acknowledged.