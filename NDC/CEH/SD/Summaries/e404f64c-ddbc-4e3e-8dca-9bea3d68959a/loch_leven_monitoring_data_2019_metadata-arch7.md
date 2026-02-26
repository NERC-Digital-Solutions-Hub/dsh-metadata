# Loch Leven long-term monitoring dataset (UK-SCAPE WP7 LEVEN)

## Overview
- Long-term dataset from Loch Leven, Scotland (began 1968; ongoing at time of writing) covering lake chemistry, physical measurements, and crustacean zooplankton.
- Describes data, sampling/analysis methods, data processing, and output format.
- Part of the UK-SCAPE WP7 LEVEN project, designed for integration into a GIS/data-visualisation workflow.

## Sampling regime and sites
- Sampling frequency: generally fortnightly; two primary sampling sites per occasion.
- Sites:
  - Harbour (H)
  - Reed Bower (RB; Reed Bower RB5)
  - Sluices / Outflow (L / Sl8)
- Sample site coordinates (UK National Grid, epsg:27700) provided; used codes reflect Harbour, Reed Bower, and Sluices.
- Access constraints: Reed Bower boat access; Sluices accessible by boat or shore.
- Secchi depth measured at Reed Bower; other measurements taken at each site when possible.

## Measurements and analyses
- In situ measurements: conductivity, pH, temperature at most sites; Secchi depth at Reed Bower.
- Water sampling: two 2 L duplicate samples per site; integrated sampling at Reed Bower using a weighted PVC tube; surface sampling at Sluices.
- Laboratory analyses (sub-samples): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP; filtered and frozen), soluble reactive silicate, total diatom silica, total phosphorus (TP; unfiltered and frozen), chlorophyll a (filtered and frozen).
- Phosphorus methods:
  - SRP: Murphy & Riley (1962) method; phospho-molybdenum blue with absorbance at 882 nm.
  - TP/TSP: digestion with sulfuric acid and potassium persulphate; measurement as SRP; Wetzel & Likens (2000) reference.
- Weather data: cloud cover, wind direction, wind force recorded at Reed Bower when possible; wind force mapped to Beaufort scale with a provided lookup table.

## Crustacean & Zooplankton
- Densities of crustacean zooplankton taxa recorded (ind/L) at Reed Bower and Sluices.
- Taxa include Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus.
- Sampling methods:
  - Reed Bower: 4 m angled net haul (120 µm) with preservation; counts made from subsamples under a microscope.
  - Sluices: 30 L surface water passed through 120 µm net; preserved and counted similarly.
- Counts converted to ind/L; specimens identified to species level where possible; some zeros indicate non-detection, not necessarily absence.

## Data processing and quality assurance
- Processing: R-based import script standardises data for database entry; handles specific decisions to maximise sensible processing.
- Wind force handling: when a range (e.g., 4-5) is given, the first value is used.
- Probe replicates: values kept if within Median Absolute Deviation (MAD) around the median; pH values converted to 10^pH for MAD calculations, then transformed back.
- Output values: central tendency (means) computed after filtering; pH/DO to 2 decimal places; conductivity and temperatures to 1 decimal place.
- QA: automated and manual checks for data entry errors and out-of-range values; unusual values investigated and corrected as needed.

## Data format and columns
- Storage: a single comma-separated values (CSV) file.
- Column headers encode determinand, site, and units (referenceTable 3 provides full definitions).
- Key types of columns include:
  - Sampling metadata: Date, Week_of_Year, weather-related fields (cloud cover, wind direction/force).
  - Site measurements: Depth, Secchi depth, Conductivity, Temperature, DO, pH (with site-specific prefixes).
  - Chemical determinations: TP, SRP, TSP, chlorophyll a (chla).
  - Zooplankton: densities for each taxon (ind/L) at each site (RB and L).
- Missing data: represented as NA.
- Site mapping and references:
  - Table 1 lists site IDs and coordinates for H, RB, and L.
  - Table 2 provides the wind force lookup (Beaufort scale) and descriptions.
  - Table 3 provides detailed column descriptions and unit information.

## References and context
- Methods references include Golterman et al. (1978), Murphy & Riley (1962), Wetzel & Likens (2000).
- Additional reading includes Hydrobiologia special issue and related Loch Leven reports.
- Dataset serves as a long-running, multi-parameter data product suitable for GIS mapping, trend analysis, and audience-friendly map-based visualisations.