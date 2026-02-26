# Loch Leven long-term monitoring dataset

- Part of a long-running monitoring programme for Loch Leven, Scotland, initiated in 1968 and ongoing at the time of documentation.
- Data describe nature, collection, processing, and output format for the Loch Leven dataset, produced under project UK-SCAPE WP7 LEVEN.
- Data were collected/analysed by NERC and CEH staff; includes both water chemistry measurements and crustacean/zooplankton counts.
- Data are stored as a single CSV file with extensive column metadata and provenance information.

## Scope, regime, and sites

- Sampling regime: fortnightly, with two main sampling sites per occasion.
- Sites and access:
  - Reed Bower (RB): boat-accessible; integrated water sampling using a weighted PVC sampler to capture the full water column.
  - Sluices / Outflow (L): sampled from boat or shore; sometimes sampled as “Outlet” in records.
  - Harbour (H) and site coordinates referenced, with site codes Site_H, Site_RB, Site_L used in the dataset.
- Sampling interruptions: weather, ice, or resource constraints may prevent sampling at one or both sites.
- Data coverage: includes routine in situ measurements and laboratory analyses from field-collected samples.

## Measurements and analyses

- In situ measurements at most sites: conductivity, pH, temperature; Secchi depth measured at Reed Bower.
- Water sampling and laboratory analyses:
  - Soluble reactive phosphorus (SRP) and total soluble phosphorus (TSP) from filtered/unfiltered samples.
  - Total phosphorus (TP) from unfiltered samples after digestion; SRP/TSP measured similarly to SRP method.
  - Soluble reactive silicate and total diatom silica; chlorophyll a via filtration.
- Analytical methods:
  - SRP: Murphy & Riley (1962) colorimetric method with phospho-molybdenum blue complex.
  - TP: digestion with sulphuric acid and potassium persulphate; measurement as SRP.
  - TSP: analogous to TP but from filtered samples.
  - References for methods provided (e.g., Wetzel & Likens, Murphy & Riley).
- Weather data: wind force (Beaufort scale) and basic conditions (cloud cover, wind direction/direction), where possible.

## Crustacean and zooplankton data

- Taxa counted per litre (ind/L) for a range of crustacean zooplankton, collected at RB and L sites.
- Sampling and preservation:
  - RB: 4 m net hauls (120 µm) with preservation in formaldehyde.
  - L: filtration of 30 L surface water through a 120 µm net; preserved.
- Laboratory processing:
  - Samples reconstituted, mixed, and sub-sampled for counting under a microscope.
  - Four sub-samples counted; identifications to species level where practical.
  - Counts converted to ind/L using appropriate multipliers and archived after counting.

## Data processing, quality assurance, and format

- Data processing:
  - An R import script was used to prepare data for the database.
  - Wind force values recorded as the first value when ranges (e.g., "4-5") were encountered.
  - Probe replicate values (conductivity, pH, DO and associated temperatures) validated via median absolute deviation (MAD) rules; extreme or inconsistent replicates removed.
  - pH values converted to 10^pH for MAD calculations, then back-transformed; means rounded to two decimals; other measurements rounded to one decimal.
- Quality assurance:
  - Automated and manual checks for data entry errors and out-of-range values; unusual values investigated and corrected as needed.
- Data format and metadata:
  - Data stored in a single CSV file with columns detailing determinand, site conditions, lake chemistry, and crustacean/zooplankton counts.
  - Missing values represented as NA.
  - Column naming encodes the determinand, site, and units; full column descriptions are provided in Table 3 of the documentation.
  - Example column fields include Date, Week_of_Year, weather descriptors, site-level measurements (e.g., Conductivity, Temperature, DO, pH), phosphorus measurements (TP, SRP, TSP), chlorophyll a, and zooplankton densities for multiple taxa.

## Documentation and references

- Column descriptions and dataset structure are detailed (Table 3) to serve as the core reference for understanding each column.
- References for sampling, analysis, and data processing methods provided, including classic methods for nutrient analyses and zooplankton identification keys.
- Additional reading and historical reports cited for context and replication of methods.

## Data quality, limitations, and reuse

- Strengths:
  - Longitudinal, multi-site data with clear provenance, standardized methods, and detailed metadata.
  - Explicit processing rules (MAD-based filtering, pH transformations) and QA procedures enhance reliability and reproducibility.
  - Comprehensive documentation of methods, site locations, and measurement units facilitates reuse and cross-site comparisons.
- Limitations and caveats:
  - Fortnightly sampling may yield gaps due to weather or access; some measurements may be absent at certain times or sites.
  - Data are focused on two main sites (RB and L) with harbour data described separately; spatial coverage is therefore limited to these locations.
  - Some measurements (e.g., certain zooplankton taxa) may be missing or only partially resolved due to preservation, identification difficulty, or sampling conditions.
- Reuse considerations for data leaders:
  - The dataset demonstrates robust data governance practices: end-to-end documentation, standardized CSV format, rich metadata, versioned lineage, and automated/manual QA.
  - Key governance takeaways: maintain a clear data dictionary (as Table 3), preserve method references, implement transparent outlier handling, and ensure reproducible processing pipelines (R scripts).
  - Useful for lessons on coordinating long-term multi-site environmental datasets, including integration of chemistry and biota measurements across time.