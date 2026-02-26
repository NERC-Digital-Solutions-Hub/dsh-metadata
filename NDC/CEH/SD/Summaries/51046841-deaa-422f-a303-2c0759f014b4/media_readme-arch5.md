# Experimental setup and flow/fraction data descriptions for CompEvo and HostAvail experiments

## Overview
- Describes two data frames (flow_data.txt and fraction_data.txt) that capture experimental setup, flow cytometry measurements, and derived cell-class fractions for two experiments: CompEvo and HostAvail.
- Documents treatment factors, replication, transfer timing, and dataset-specific measurement fields and thresholds used for gating and classification.

## Data frames and key fields (experimental setup)
- Common metadata across both data frames:
  - Experiment: Indicates one of two experiments (CompEvo, HostAvail) with distinct treatments.
  - Treatment: Specifies the starting community composition, presence/absence of mercury, and plate controls (BLANK = control).
  - Ratio: Proportion of Available vs Occupied hosts at start.
  - Replicate: Biological replicate identifier.
  - Transfer: Evolution timepoint (days) when bacteria are transferred to fresh media (every 24 hours).
- CompEvo specifics:
  - Describes multiple combinations of strains/plasmids and mercury presence across sub-conditions (e.g., A, B, C, D, F1–F4) detailing SBW25 strains with various plasmid constructs and mercury presence or absence.
- HostAvail specifics:
  - Describes host-bacteria combinations across sub-conditions (A–D; with specific host/bacteria pairings and plasmids).
  - Includes single and mixed-host scenarios with and without mercury.
- Notes:
  - The “BLANK” treatment serves as a control in plate setups.
  - The data are organized to support reproducibility and traceability of evolving communities under defined conditions.

## Flow data (flow_data.txt)
- Machine: Beckman Coulter Cytoflex.
- Measured signals (flow cytometry):
  - FSC.H (Forward Scatter height)
  - SSC.H (Side Scatter height)
  - PB450.H (PHA/Hoesch stain signal marker threshold at 10^3.5)
  - FITC (GFP/YFP detection; threshold 10^3.5)
  - ECD (detects dTomato/tdTomato; threshold)
  - PE (detects dTomato/tdTomato; threshold 10^3.4)
- Purpose:
  - Determine bacterial events vs background using threshold gates.
  - Provide per-event signal values used to classify events as bacterial.
- Context:
  - Flow data supports the calculation of fractions and totals reported in fraction_data.txt.

## Fraction data (fraction_data.txt)
- Included data:
  - Total.Count: Total events passing size thresholds per sample (from flow_data.txt).
  - Fraction_Red: Proportion of red-classified events (PE threshold exceeded, FITC threshold not exceeded).
  - Fraction_Yellow: Proportion of yellow-classified events (FITC threshold exceeded, PE threshold not exceeded).
  - Fraction_Orange: Proportion of orange-classified events (both PE and FITC thresholds exceeded).
  - Fraction_Blue: Proportion of blue-classified events (neither PE nor FITC thresholds exceeded).
- Purpose:
  - Provide color-based cellular class distributions derived from flow cytometry for each sample.

## Data governance and stewardship considerations
- Metadata completeness and consistency:
  - Ensure clear definitions for Experiment, Treatment, Ratio, Replicate, and Transfer across both frames.
  - Standardize treatment encoding to support searchable discovery and interoperability.
- Data provenance and provenance metadata:
  - Capture instrument (Beckman Coulter Cytoflex) and gating thresholds used for flow data.
  - Document the exact event thresholds and color-class definitions to enable reproducibility.
- Quality, format, and interoperability:
  - Validate that all flow_data.txt fields align with the same event-level measurement units and thresholds.
  - Confirm Total.Count and the four color fractions sum logic and edge-case handling.
  - Maintain clear linkage between flow_data.txt and fraction_data.txt via sample identifiers and replicate/transfers.
- Access, sharing, and updates:
  - Track dataset versioning and potential updates to gates, thresholds, or treatment definitions.
  - Ensure appropriate data access controls given any embargoes or sensitive components of the experimental design.
- Usability for data users:
  - Provide a data dictionary mapping each column to its meaning, data type, unit, and allowed values.
  - Include example records and any preprocessing steps (e.g., gating criteria) to aid reuse.

## Endnotes
- The document outlines a structured schema for two experimental data frames capturing both setup metadata and flow cytometry-derived measurements, enabling downstream analyses of evolving bacterial communities under defined experimental conditions.