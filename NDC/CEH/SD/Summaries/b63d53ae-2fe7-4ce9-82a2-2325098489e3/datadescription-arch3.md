# EIDC dataset: Tritrophic phenology and associated data from 44 sites in Scotland, 2014-2021

## Overview
- Longitudinal dataset capturing interactions among trees, herbivores (caterpillars), and birds (blue tit) across 44 woodland sites in Scotland (Edinburgh to Dornoch).
- Data collected annually from 2014 to 2021, with nestboxes, environmental measurements, and multi-taxa phenology and breeding metrics.
- Designed to support monitoring, evaluation, and inference of environmental influences on phenology and trophic interactions.

## Study design and data collection
- Site selection and setup
  - 30 woodland sites initially, with six 26 mm Schwegler 1B nestboxes per site; expanded to 44 sites by 2017.
  - Sites spaced out and in proximity to M90 and A9 to capture environmental gradients.
- Field schedule and COVID impact
  - Regular visits every 2 days from early April to mid/late June (varying by year); 2014–2016 started mid-March; 2020 fieldwork delayed to early May with partial data collection (southern 22 sites visited regularly).
- Measurements and sampling
  - Temperature: hourly air temperature recorded at opposite ends of each site using two DS1922 L thermochron i-buttons at ~1.5 m height.
  - Tree phenology: sampling of representative deciduous taxa; phenophases recorded as first budburst, complete budburst, first leaf, complete leaf.
  - Caterpillars: branch beating on selected trees; caterpillars counted if >1 mm diameter; samples weighed from 2017 onward; weight <0.02 g recorded as such.
  - Blue tit (Nestbox-based monitoring): nestbox visits to record first egg date, clutch size, incubation, hatching, nestling weight and wing length, adult morphometrics; nestlings ringed and weighed at specific days; breeding success measured as fledging output.
- Data management and governance
  - Outputs disseminated via reports, charts, and dashboards; underlying data shared where appropriate; metadata and data provenance emphasized; quality assurance processes applied (cleaning and transformation as needed).

## Measurements and data domains
- Temperature
  - Hourly air temperatures by site and year (loggers labeled by site; data gaps indicated as NA).
- Tree phenology
  - Taxon-specific records with ordinal days for budburst and leaf onset (fbb, cbb, flf, clf).
- Caterpillars (Branch_Beating)
  - Year, site, tree ID, taxon, date, weather, counts of caterpillars, mass (g), notes, mass uncertainty flag.
- Bird phenology (Bird_Phenology)
  - Nestbox- and year-specific records: box, species, first egg date, clutch size, incubation dates, hatching, fledging, treatment for clutch swaps, and survival indicators.
- Nestlings
  - Year, site, box, nestling mass at first and second visits, wing length, mortality status, and ringer identifiers.
- Adults
  - Ring IDs, year, site, box, age, sex, wing length, mass, capture date and time, ringer identifier.

## Data structure and access
- Dataset comprises 7 CSV files, all joinable via site code and year:
  - site_details: site code, site name, latitude, longitude, elevation.
  - temperatures: site, year, hourly temperature columns (X46 to X163).
  - Tree_Phenology: year, site, TreeID, taxon, fbb, cbb, flf, clf.
  - Branch_Beating: year, site, treeID, taxon, date, weather, recorder, caterpillar count, caterpillar mass, notes, mass.uncertain.
  - Bird_Phenology: year, site, box, species, fed (first egg date), cs (clutch size), fki (first incubation), clutch_swap_treatment, hatching_first_recorded, uhe, v1date/v1alive/v1time, v2date/v2alive/v2mass/v2wing/v2ringer, fledged.
  - Nestlings: year, site, box, ring, v1date, v1mass, v1ringer, v2alive, v2date, v2mass, v2wing, v2ringer, fledged.
  - Adults: ring, year, site, box, age, sex, wing, mass, date, time, ringer.
- Coding and compatibility
  - A consistent three-letter site code is used across all files to enable integration.
  - Taxon labels and ordinal dates follow predefined conventions; some fields use NA for missing visits or non-recorded events.
  - Clutch_swap_treatment documents experimental manipulation per nestbox year.

## Data quality, gaps, and governance
- Gaps and limitations
  - 2020 data collection partially affected by COVID-19; southern sites prioritized, affecting full temporal completeness.
  - Some nest visits or measurements were not recorded (e.g., certain visits missing in Bird_Nest or Nestlings files).
  - Data sometimes require transformation or cleaning (e.g., mass values below detection, NA entries) before analysis.
- Metadata and usability
  - Detailed variable descriptions accompany each file, supporting transparent reuse and replication.
  - Data are organized to support cross-taxa, spatio-temporal analyses of phenology and breeding success in relation to environmental drivers.
- Data provenance and references
  - Datasets build on prior work cited in literature (Shutt et al. 2018, 2019; Macphie et al. 2020) and are designed to be compatible with broader environmental monitoring frameworks.

## Relevance for monitoring frameworks
- Demonstrates multi-taxa, field-based monitoring across a broad spatial and temporal scale.
- Provides a structured approach to collecting and integrating environmental data (temperature, habitat phenology) with biological responses (caterpillars, birds).
- Highlights governance considerations: metadata completeness, data sharing, data quality assurance, and handling of data gaps due to field constraints or public events (e.g., pandemics).
- Useful as a case study for designing monitoring programs that link environmental drivers to phenological and reproductive outcomes, while maintaining clear data provenance and governance.