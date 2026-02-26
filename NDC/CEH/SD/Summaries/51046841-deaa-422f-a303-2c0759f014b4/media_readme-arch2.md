# Experimental Setup and Data Description for CompEvo and HostAvail Data

## Overview
- Describes two data frames containing experimental setup and observational data from evolving microbial communities.
- Includes flow cytometry data (flow_data.txt) and derived fraction data (fraction_data.txt) collected under defined treatments and transfer schedules.

## Experimental design

- Experiments
  - CompEvo: two separate runs with distinct treatments; includes various SBW25 strains carrying plasmids (GmR, GFP, dTomato, tdTomato, YFP) and mercury-related conditions.
  - HostAvail: defined host configurations with available vs occupied hosting contexts and plasmid variants; includes a KT2440.KmR line in one configuration.
- Treatments
  - BLANK/CONTROL in plate (no bacteria) and starting community compositions with or without mercury.
  - Mercury addition is included in certain treatments for CompEvo.
- Ratio
  - Proportion of Available vs Occupied hosts at the start point.
- Replicate
  - Biological replicates of each treatment.
- Transfer
  - Timepoint (in days) when bacteria are transferred to fresh media, every 24 hours.

## Data contents and fields

- For both data frames
  - Experiment: identifies whether data come from CompEvo or HostAvail.
  - Treatment: describes starting community composition and mercury presence (including controls).
  - Where Experiment = CompEvo: multiple detailed treatment rows (A–D) and F1–F4 variants with specific strain/plasmid combinations and mercury conditions.
  - Where Experiment = HostAvail: multiple configurations (A–D) describing host availability pairings and plasmid constructs.
  - Ratio: starting proportion of Available vs Occupied hosts.
  - Replicate: biological replicate identifier.
  - Transfer: evolution timepoint in days for transfers.

- flow_data.txt (machine and gating information)
  - Machine: Beckman Coulter Cytoflex.
  - FSC.H: Forward Scatter height threshold (10^3).
  - SSC.H: Side Scatter height threshold (10^3).
  - PB450.H: Hoescht-stained signal threshold (10^3.5).
  - FITC: GFP/YFP signal threshold (10^3.5).
  - ECD: dTomato/tdTomato signal confirmation (height).
  - PE: dTomato/tdTomato signal threshold (10^3.4).

- fraction_data.txt (summary statistics per sample)
  - Total.Count: total events passing basic thresholds (size-based gating).
  - Fraction_Red: proportion of red-classified events (pass PE threshold, not FITC).
  - Fraction_Yellow: proportion of yellow-classified events (pass FITC threshold, not PE).
  - Fraction_Orange: proportion of orange-classified events (pass both PE and FITC thresholds).
  - Fraction_Blue: proportion of blue-classified events (neither PE nor FITC thresholds).

## Data quality and processing

- Data collection and processing
  - Data are drawn from established experiments with verification, quality assurance, cleaning, and transformation to standard outputs.
- Outputs
  - Standardised deliverables include reports, maps, and charts.
  - Datasets are stored and uploaded to appropriate data portals to enable sharing and reproducibility.

## Practical considerations for Analysts

- Valuing datasets by combining with other relevant data to avoid “single use.”
- Facilitating access to underlying data used to create final outputs to support transparency and reanalysis.

## Relevance to environmental monitoring

- The data illustrate how microbial ecosystems respond to environmental variables (e.g., mercury presence, host availability) over time, providing a framework for monitoring environmental health and evaluating policy-relevant performance through standardized, auditable datasets.