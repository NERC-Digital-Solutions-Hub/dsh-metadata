# For both data frames, the following columns describe the experimental set up and conditions:

- The document describes two data frames capturing experimental setups and conditions:
  - Experiment types: CompEvo (first experiment) and HostAvail (second experiment)
  - Treatment field with starting community composition and mercury presence; blank (BLANK) indicates a control with no bacteria
  - Ratio: Proportion of Available vs Occupied hosts at the start point
  - Replicate: Biological replicate identifier for treatments
  - Transfer: Timepoint (in days) when bacteria are transferred to fresh media, every 24 hours

- CompEvo (where $Experiment = CompEvo)
  - Multiple sample configurations labeled A, B, C, D, and F1–F4, describing combinations of bacterial strains, plasmids, GFP/tdTomato/YFP markers, and mercury presence
  - Example structure notes:
    - A, B, C, D blocks specify combinations of SBW25 strains with various plasmids and mercury conditions
    - F1–F4 denote additional individual sample configurations with specific marker combinations
  - Overall emphasis: diverse starting conditions and genetic constructs to explore evolving communities

- HostAvail (where $Experiment = HostAvail)
  - Subsets A–D describe hosts arranged as nested groups with SBW25.GmR and other strains/plasmids (e.g., pWBR57d0059.GFP, pQBR57)
  - Examples indicate different pairings of a host strain with an available partner and, in some cases, mercury presence
  - D line references an alternative host (KT2440.KmR) paired with SBW25.GmR and related constructs
  - Overall emphasis: different host availability scenarios and preparations for interaction studies

- Flow_data.txt (measurement context)
  - Instrument/machine: Beckman Coulter Cytoflex
  - Channels/parameters:
    - FSC.H: Forward Scatter signal (threshold 10^3)
    - SSC.H: Side Scatter signal (threshold 10^3)
    - PB450.H: Hoechst-stained signal (threshold 10^3.5)
    - FITC: GFP/YFP signal (threshold 10^3.5)
    - ECD: PE signal (for red/yellow/blue gating; threshold not explicitly stated)
    - PE: PE signal (threshold 10^3.4)
  - Purpose: determine which events are bacterial signals and classify signals via gating thresholds

- fraction_data.txt (derived metrics per sample)
  - Total.Count: total events sampled from flow_data.txt that pass basic thresholds (size gates)
  - Fraction_Red: proportion of counts classified as red (PE-threshold satisfied, FITC-threshold not)
  - Fraction_Yellow: proportion classified as yellow (FITC-threshold satisfied, PE-threshold not)
  - Fraction_Orange: proportion classified as orange (both PE and FITC thresholds surpassed)
  - Fraction_Blue: proportion classified as blue (neither PE nor FITC thresholds surpassed)

- Data provenance and context
  - Flow data collected with specific cytometry thresholds and channel mappings
  - Replicate and transfer timing provide temporal structure for evolution experiments
  - The data frames and measurement files together describe experimental design, population composition, and cytometric characterization

- Notes on data quality and standardization (relevant for GIS-like data products)
  - Some inconsistencies and formatting irregularities (e.g., varying spellings such as “Treament” vs “Treatment,” and mixed notation for sample identifiers)
  - Lack of explicit spatial attributes; data are non-spatial experimental observations, so GIS mapping would require deriving or adding spatial metadata (e.g., lab/location, plate positions) if mapping to geospatial contexts
  - Clear data dictionary and consistent coding would aid interoperability, reproducibility, and potential spatial-temporal analyses or visualization of experimental conditions across replicates and treatments