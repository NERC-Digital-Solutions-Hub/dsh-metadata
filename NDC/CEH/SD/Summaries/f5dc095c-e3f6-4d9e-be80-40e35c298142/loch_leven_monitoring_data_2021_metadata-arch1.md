# Loch Leven long-term monitoring data

- A long-running dataset describing Loch Leven (Scotland) monitoring from 1968 onward, produced as part of the UK-SCAPE WP7 LEVEN project and managed by NERC / CEH.
- Purpose: document data, sampling and analysis methods, data processing, and output format to enable data-driven analysis of lake chemistry, biology, and related factors.

## Sampling regime and sites

- Fortnightly sampling schedule with two main sites: Reed Bower (RB) and Sluices/Outflow (L).
- Reed Bower is boat-accessible; Sluices can be sampled by boat or shore-based.
- Occasionally only Sluices can be sampled due to resource constraints, bad weather, or ice; in extreme cases, neither site is visited.
- Site identifiers and locations are provided (Harbour H, Reed Bower RB, Sluices L) with UK grid coordinates.
- Data are recorded for in situ measurements at each site, with laboratory analyses performed on collected samples.

## Measurements, sampling, and analysis methods

- In situ measurements: conductivity, pH, temperature; Secchi depth measured at Reed Bower.
- Water samples collected as duplicate 2 L samples per site; sampling methods differ by site (integrated column sample at Reed Bower; surface bottle sample at Sluices).
- Laboratory analyses include: soluble reactive phosphorus (SRP), total soluble phosphorus (TSP; filtered and frozen), soluble reactive silicate, total diatom silica, total phosphorus (TP; unfiltered and frozen), and chlorophyll a (filtered samples).
- SRP determination follows Murphy & Riley (1962); TP via persulfate digestion with acidification step; chlorophyll a via filtration and storage prior to analysis.
- Weather data recorded at Reed Bower when possible (cloud cover, wind direction, wind force using Beaufort scale); wind force table provided for interpretation.
- Water samples for chemical analyses are filtered/unfiltered as specified and stored appropriately (e.g., filtered samples refrigerated or frozen as required).

## Crustacean & Zooplankton data

- Densities of crustacean zooplankton taxa collected at Reed Bower and Sluices, expressed as individuals per liter (ind/L).
- Taxa include Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, and others (site-specific availability noted).
- Collection methods differ by site: 4 m net haul at Reed Bower; 30 L water through a 120 µm net at Sluices.
- Samples preserved in formaldehyde, later identified to the extent preservation allows, and counts converted to ind/L with standard factors.
- Data include species- or group-level densities and related counts, with non-detections coded as zeros and missing values as NA.

## Data processing, quality assurance, and transformation

- An R-based import script processes raw data before database entry.
- Wind force values may be reported as ranges (e.g., "4-5"); the first value is used in the database.
- Replicate values from probes (conductivity, pH, dissolved oxygen) are filtered using Median Absolute Deviation (MAD); values within Median ± MAD are retained. pH values are converted to 10^pH for MAD calculations and then log-transformed back; resulting values are averaged and rounded (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
- Inter-calibration between older HQ30d and newer HQ4300 probes performed; dataset columns reference HQ30d for consistency.
- Automated and manual quality checks identify and correct out-of-range or erroneous entries.
- Data are stored in a single CSV file with NA for missing values; columns include determinand, site, and units, with extensive metadata per column.

## Format and structure of the stored data

- Output format: comma-separated values (CSV) with comprehensive column names describing determinand, site, and units.
- Column examples include date, week, water level, cloud cover, wind direction/force, depth, Secchi depth, conductivity, temperature, dissolved oxygen, pH, phosphorus forms (TP, SRP, TSP), chlorophyll a, and crustacean/zooplankton densities.
- Replicate identifiers are embedded in column names (e.g., Site_RB1, Site_RB2 for replicates at Reed Bower; Site_L1, Site_L2 for Sluices replicates).
- Table 3 provides full descriptions of each column, determinand, site, and units.

## Reference material

- Methods and analyses are supported by key literature and technical references (e.g., methods for water analysis, phosphate determination, and hydrobiological taxonomic keys).
- Additional reading includes historical reports and syntheses of Loch Leven research.

## Practical use and considerations for analysts

- The dataset enables time-series analyses of lake chemistry, productivity (chlorophyll a), nutrient dynamics (phosphorus forms), and biotic responses (zooplankton densities) across two long-running sites.
- Opportunities include exploring correlations between physical conditions (wind, water level, Secchi depth) and chemical/biological variables, as well as modelling responses to environmental drivers over decades.
- Important caveats include intermittent sampling due to weather or logistics, site accessibility differences, replicates with varying availability, and the need to account for measurement method changes and QA procedures when combining across time.