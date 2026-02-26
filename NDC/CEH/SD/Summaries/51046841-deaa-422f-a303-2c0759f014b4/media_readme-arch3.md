For both data frames, the following columns describe the experimental set up and conditions:

- Experiment
- Treatment
- Ratio
- Replicate
- Transfer

Overview
- The document documents two related experiments, CompEvo and HostAvail, including how treatments are defined, how data was collected, and how flow cytometry data are structured and labeled.
- It provides concrete metadata for experimental design, including the starting composition, presence of mercury, and timepoints when transfers occur.

Experimental design and conditions
- CompEvo
  - Two runs (experiments) with distinct treatments.
  - Treatments describe starting community composition and mercury presence.
  - Example groupings show combinations of SBW25 strains with plasmids (e.g., pQBR57d59.GmR.GFP, pQBR57d59.GmR.dTomato) and mercury conditions.
  - Experimental labels include A, B, C, D, F1–F4, and corresponding representative strain configurations.
- HostAvail
  - Two groups of conditions with different host and plasmid combinations.
  - Example configurations include SBW25.GmR paired with SBW25.GmR pWBR57d0059.GFP and SBW25d4242.dTomato pQBR57, sometimes with Mercury or additional hosts (KT2440.KmR).
  - Experimental labels include A, B, C, D with specific host/plasmid pairings.
- Time and replication
  - Transfer is a timepoint concept representing when bacteria are transferred to fresh media; units are days.
  - Replicates (biological) are identified to capture variability across treatments.
  - Ratio indicates the proportion of available vs occupied hosts at the start point.
  - Transfers occur approximately every 24 hours.

Flow cytometry data (flow_data.txt)
- Machine: Beсkman Coulter Cytoflex
- Measured signals (columns)
  - FSC.H (Forward Scatter height)
  - SSC.H (Side Scatter height)
  - PB450.H (PB450 height; Hoescht-stained)
  - FITC (detects GFP and YFP)
  - ECD (detects dTomato/tdTomato for PE filtering)
  - PE (detects dTomato/tdTomato)
- Thresholds
  - Threshold values are provided for each signal (e.g., FSC.H, SSC.H, PB450.H, FITC, ECD, PE) to distinguish bacterial events from background.
- Purpose
  - Used to classify events as bacterial and to determine color categories through signal channels (GFP/YFP vs. red fluorophores).

Fraction data (fraction_data.txt)
- Key metrics
  - Total.Count: total events sampled from flow_data.txt that pass basic size thresholds (determine bacteria vs background).
  - Fraction_Red: proportion classified as red (surpassing PE threshold but not FITC).
  - Fraction_Yellow: proportion classified as yellow (surpassing FITC but not PE).
  - Fraction_Orange: proportion classified as orange (surpassing both PE and FITC).
  - Fraction_Blue: proportion classified as blue (neither surpassing PE nor FITC).
- Purpose
  - Provides summarized color-class fractions to quantify composition of signals after gating, enabling downstream ecological or evolutionary inferences.

Measurement and data processing considerations
- Data provenance and metadata
  - Explicit experiment names, treatment descriptions, and timepoints enable reproducibility and auditability for monitoring frameworks.
  - Flow cytometry gating relies on defined signal thresholds and channel mappings, facilitating transparent data processing steps.
- Data quality and transformation
  - Metadata gaps can impede reuse; the documentation emphasizes the need to verify data originators and metadata completeness.
  - Data transformation (e.g., gating, event classification) is inherent to producing fraction_data from flow_data, highlighting the importance of clear, shareable processing steps and thresholds.
- Data governance implications
  - The structure supports traceability of data from raw flow data to summarized fractions, aiding governance, openness, and accountability.
  - The collaborative, multi-treatment design illustrates how data silos can be avoided with consistent schemas and explicit metadata.

Relevance for environmental health monitoring and policy
- Demonstrates a structured approach to monitoring microbial ecosystem responses under different treatments and stressors (e.g., mercury), with time-resolved data and replicates.
- Highlights the importance of:
  - Detailed experimental metadata (treatments, start conditions, transfer timing)
  - Transparent measurement protocols (flow cytometry signals, thresholds, and color classifications)
  - Clear data products (Total.Count and color fractions) for interpretation and policy-relevant decision-making
  - Data governance practices (data provenance, shareability of underlying data, and metadata quality)

Key challenges and considerations for authors of monitoring frameworks
- Ensuring data are complete, well-documented, and easily linkable across experiments to avoid silos.
- Providing sufficient metadata to verify whether data meet standards for timely sharing and reuse.
- Balancing the need to share underlying data with potential barriers related to privacy, sensitivity, or proprietary information.
- Clear communication of complex analytical steps (gating strategies, threshold choices) to enable replication and comparability.