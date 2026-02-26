# Invertebrate community assembly data across a natural soil temperature gradient in Iceland from May-July 2015

- Scope: dataset of environmental data, total invertebrate abundance, and mean invertebrate body mass collected from 60 soil habitat patches in the Hengill geothermal valley, Iceland, across a soil temperature gradient of 5–22 °C during May–July 2015.
- Study design: 10 geothermally heated streams, with three habitat patches sampled on each bank (left/right) of each stream; patches distributed across the gradient to capture temperature-driven variation.
- Temporal coverage: four sampling time-points on 19 May, 4 Jun, 23 Jun, and 5 Jul 2015.
- Related work: contextualized by multiple publications on temperature effects in Hengill streams (e.g., Robinson et al. 2018, 2021; O’Gorman et al. series; Friberg et al. 2009; etc.).

- Sampling regime and collection methods
  - Environmental measurements per patch:
    - Soil temperature monitored hourly using Maxim iButton DS1921G loggers buried 5 cm below the surface (13 May–3 July 2015); 49 of 60 loggers recovered; remaining data treated as NA.
    - Soil moisture measured with Imko TRIME-TDR probe.
    - Soil cores (five per patch) collected at ~10 cm depth; homogenised, dried at 60 °C for 96 h, milled for analysis.
    - Soil pH measured from 10 g of dry, milled soil using a 1:5 soil-to-water ratio with a pH meter.
    - Total carbon and total nitrogen determined via combustion (CN analyser) at a dedicated facility.
  - Invertebrate sampling:
    - Epigeal invertebrates collected with five pitfall traps per patch, left for 48 hours, at four time-points; traps are white plastic cups with glycol/water solution.
    - Collected samples combined per patch, sieved to 250 μm, stored in 70% ethanol.
    - Identification to species where possible; often higher taxonomic levels (e.g., Diptera, Hymenoptera to family level) due to identification constraints.
  - Sample handling and processing details are described comprehensively in Robinson et al. (2021).

- Data structure and content
  - Data are provided as three CSV files:
    - hengill_seasonal_environmental_data.csv
    - hengill_seasonal_abundance.csv
    - hengill_seasonal_mass.csv
  - Each row represents one sampling time-point for one of the 60 habitat patches.
  - Common header schema:
    - Columns 1–3: stream (numeric identifier), bank (left/right), patch (1–3)
    - Column 4: date of sampling (in the abundance and mass files); temperature file uses the environmental timestamp
    - Columns 5–128 in abundance and mass files: taxa names; values are:
      - Abundance file: total number of individuals per taxon per patch per sampling date
      - Mass file: mean dry weight per taxon (in milligrams) per patch per sampling date
  - Environmental data file (hengill_seasonal_environmental_data.csv) includes:
    - Columns for temperature (mean °C during study period), total carbon (g kg−1), total nitrogen (g kg−1), moisture (%), and pH
  - Taxa columns (5–128) correspond to the names of invertebrate taxa quantified in the pitfall traps
  - Data volume: for each of the four sampling dates, there are 60 patches, yielding 240 rows per file (plus environmental data rows for patches across dates)

- Data quality, limitations and governance
  - Temperature data completeness: 11 loggers not recovered; temperature data for those patches are NA, introducing gaps in the gradient measurements.
  - Taxonomic resolution: identification frequently limited to family level for groups like Diptera and Hymenoptera; species-level data are limited where feasible.
  - Metadata scope: detailed sampling protocol, measurement methods, and data file structure are described; cross-referenced with related publications for context.
  - Provenance and usage context: dataset is embedded within a broader set of studies on soil temperature effects on community structure and dynamics; suitable for secondary analyses on temperature-driven patterns in invertebrate communities.
  - Data stewardship considerations: ensure unit consistency (e.g., mg for mass, g kg−1 for carbon, percentages for moisture, NA handling for missing temperature data), maintain patch-to-location mapping (stream, bank, patch), and document any re-processing steps if reusing the data.

- Suggested governance and archival actions for Data Stewards
  - Verify and preserve measurement units and their descriptions across all files; retain the column-level metadata and taxon-names mapping.
  - Capture provenance: link to the primary publications (Robinson et al. 2018, 2021; O’Gorman et al. series) to provide methodological and contextual grounding.
  - Record data quality notes, especially the NA entries from missing temperature loggers, and consider flagging patches/dates with incomplete environmental data.
  - Ensure clear licensing and access terms are attached to the dataset and that future updates or corrections are versioned.
  - Facilitate discoverability by indexing the three CSVs under a common dataset entry with fields for study area (Hengill), temperature gradient, sampling period, and data types (environment, abundance, mass).

- Key considerations for data users and reuse
  - Use environmental data to interpret how temperature and soil properties correlate with invertebrate abundance and body mass across the gradient.
  - Be mindful of varying taxonomic resolution and potential biases in identification depth across taxa.
  - When aggregating across patches or streams, account for the hierarchical sampling design (patch within bank within stream) and four time-points.
  - Consult linked publications for methodological nuances and validation of downstream analyses (e.g., temporal dynamics and structure of communities).