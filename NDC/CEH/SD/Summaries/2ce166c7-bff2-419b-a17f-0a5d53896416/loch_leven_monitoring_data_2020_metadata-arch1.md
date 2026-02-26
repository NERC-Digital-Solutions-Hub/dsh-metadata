# Abstract

- The document describes a long-term Loch Leven dataset (Scotland, UK) collected as part of a monitoring programme that began in 1968 and continues under UK Centre for Ecology & Hydrology/ NERC leadership (project UK-SCAPE WP7 LEVEN).
- It details data types, sampling and analysis methods, data processing, and output format to enable reuse and interpretation.

## Sampling regime and sites

- Sampling is undertaken on a fortnightly basis at two main sites each session: Reed Bower (RB) and Sluices (L). The Reed Bower site is boat-accessible; Sluices can be sampled by boat or from shore.
- When weather, ice, or resource constraints prevent sampling, one or both sites may be missed; in extreme cases, no sampling occurs.
- The Harbour site (H) is recorded in the dataset as an alternative identifier in addition to Reed Bower (RB) and Sluices (L).

## Measurements and analyses

- In situ measurements: conductivity, pH, temperature, and Secchi depth (Secchi depth measured at Reed Bower only).
- Field sampling: two duplicate 2 L water samples per site; Reed Bower uses a weighted vertical sampler to obtain a representative column sample; Sluices uses a surface bottle sampler.
- Laboratory analyses (on returned samples): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP; filtered and frozen), soluble reactive silicate, total diatom silica, total phosphorus (TP; unfiltered and frozen), and chlorophyll a (via filtration and freezing of 400 mL samples).
- SRP measured by Murphy & Riley (1962) method; TP/TSP measured after persulfate digestion with a procedure following Wetzel & Likens (2000).
- Weather observations (cloud cover, wind direction, wind force) are recorded at Reed Bower when possible; a detailed Beaufort-scale wind force table is provided.

## Data processing and transformation

- An R-based import script processes data prior to database entry, with predefined handling rules (e.g., wind force values like "4-5" use the first value).
- Probe replicate values (conductivity, pH, DO, and respective temperatures) are included if they fall within Median Absolute Deviation (MAD) criteria; pH values are log-transformed for MAD calculation and then back-transformed, with final values rounded (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
- Automatic and manual quality assurance checks are performed to identify and correct anomalies.

## Data format and storage

- Data are stored in a single comma-separated values (CSV) file with columns detailing determinands, site conditions, lake chemistry, and crustacean/zooplankton counts; missing measurements are marked NA.
- Column naming convention combines measure, site, and units; key fields include date, week of year, wind, depth, Secchi depth, conductivity, temperature, dissolved oxygen, pH, TP, SRP, TSP, chlorophyll a, and numerous zooplankton taxa densities.

## Crustacean & Zooplankton dataset

- The dataset includes densities (ind/L) of various crustacean zooplankton taxa at Reed Bower and Sluices, collected during the monitoring programme.
- Sampling methods differ by site: Reed Bower uses a 4 m, 120 µm mesh net; Sluices uses large-volume surface water filtration (30 L, 120 µm mesh).
- Samples are preserved, processed in the lab, identified to species levels where possible, sub-sampled for counting, and counts converted to individuals per litre.
- Taxa included cover several cladocerans, copepods (adult and copepodite stages), nauplii, and other zooplankton groups; zeros indicate non-detection within the analytic resolution, and NAs indicate missing values.

## Data processing and QA (Crustacean & Zooplankton)

- Sub-samples are counted, counts are converted to per-litre densities using standard factors, and preserved samples are archived for future reference.
- References for taxonomic keys and identification guidance are provided.

## Output and references

- The document provides methodological references for analytical techniques (e.g., methods for water analysis, phosphate determination) and notes additional readings and historical reports on Loch Leven water quality and long-term research.
- Data processing and measurement methods are tied to specific laboratory and field protocols, ensuring traceability and reproducibility.

## Practical considerations and potential uses

- The dataset supports analysis of long-term trends and correlations among lake chemistry, physical properties, and zooplankton communities.
- Potential challenges acknowledged include data gaps due to sampling constraints, site accessibility, and evolving data formats across decades.
- The combination of physico-chemical data with crustacean/zooplankton densities enables exploratory and predictive analyses relevant to lake ecology, nutrient cycling, and ecosystem responses to environmental change.