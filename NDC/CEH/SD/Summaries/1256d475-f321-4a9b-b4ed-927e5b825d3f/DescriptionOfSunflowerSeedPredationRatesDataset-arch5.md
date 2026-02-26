# Sunflower seed predation rates in Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) plots, Sumatra, Indonesia

## Purpose and context
- Study of granivory (predation) on oil palm plots in Sumatra, Indonesia within the BEFTA project.
- Location: three estates in Riau Province (Ujung Tanjung, Kandista, Libo), established on mineral soils; 18 plots across estates.
- Data cover mature stands (Ujung Tanjung, Kandista) from 2014 and both mature/replanted stands from 2016–2017; replanted plots surveyed separately in 2016–2017.
- Experimental design linked to vegetation management and BEFTA objectives; coordinates and plot details provided in misc. notes.

## Experimental design and sampling regime
- Plot layout: 50 x 50 m plots with three sampling positions per plot (edge markers at 45°, 165°, 285° from north).
- Granivory measurement: 10 shelled sunflower seeds placed on a 15 cm disc, covered by a plate ~10 cm above soil.
- Treatments (per replicate): cage with grease, cage only, grease only, open (four combinations).
- Traps: metal grid boxes (≈35 x 20 x 14 cm) with holes ≤ 1 cm.
- Sampling schedule: once in mature stands (2014) and five times in mature/replants (2016–2017).
- Time in field: seeds left out for ~24 hours before assessment.
- Notes on data: includes information on seed treatment, placement times, and weather (dayrain).

## Data collected and measurements
- Primary metric: seeds remaining after exposure (out of ten; decimals may occur if fractional seeds are recorded).
- Variables captured per observation include: estate, plot, triplet, treatment, period, position, dates and times of seeding and collection, seed treatment, seeds remaining, daily rainfall, and field notes.
- Specific data fields (examples): Estate_abbrev, Plot_no, Treatment, Period, Position, Date_set, Time_set, Date_coll, Time_coll, seedstreat, seedsremaining, dayrain, allnotes.
- Special field: SAFE_distance (only in 2016–2017 data; if present near exclosure zones, data may be unreliable and should be treated with caution).

## Data formats and storage
- Three CSV files storing the data in thin format (one observation per line):
  - SunflowerSeedPredationRates_2014.csv (mature stands)
  - SunflowerSeedPredationRates_2016_2017.csv (core 2016–2017 data)
  - SunflowerSeedPredationRates_replants.csv (replanted plots)
- Data are organized with clear field descriptions and standardized column names to facilitate analysis.

## Data quality control and provenance
- Basic data checks for impossible values (e.g., more seeds remaining than available) performed.
- 50% of data entries cross-checked against original field sheets; error rate <1%; corrections recorded with an audit trail.
- Metadata and field notes retained to document data checks and any changes.

## Metadata, provenance, and provenance notes
- Funding: NE/P00458X/1.
- Data provenance: two main data groups referenced (core BEFTA plots 2016–2017 and replanted plots), plus 2014 data for mature stands.
- Plot identifiers include estate abbreviation, triplet, and three-character plot ID (e.g., C01, etc.), enabling unique data point identification.
- Miscellaneous coordinates and context provided for plots; some fields indicate potential data limitations (e.g., SAFE_distance near exclosures).

## Governance, reuse, and stewardship considerations
- Data stewardship relevance:
  - Clear, standardized metadata and thin-format csv structure support discoverability and reuse across systems.
  - Documentation of data collection methods, treatments, time points, and quality checks aids reproducibility and governance.
  - Explicit notes on data limitations (e.g., SAFE_distance caveats) inform appropriate use and prevent misinterpretation.
- Potential challenges to consider when integrating with other datasets:
  - Incomplete picture of user needs and priority alignment.
  - Timely receipt and standardization of datasets across estates and years.
  - Heterogeneous formats and large dataset sizes (especially with multi-year deployments).
  - Interoperability with legacy systems and non-interoperable solutions due to historical data formats.

## Practical takeaways for data stewards
- Maintain and publish the three CSV data files with their documented field definitions.
- Preserve the audit trail for all data corrections and data-check outcomes.
- Ensure consistent handling of decimals in seedsremaining and clearly flag measurements near data caveats like SAFE_distance.
- Facilitate data sharing by preserving provenance notes and linking to BEFTA project metadata and funding information.