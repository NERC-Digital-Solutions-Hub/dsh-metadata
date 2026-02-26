# Generating a Soil Moisture Characteristic Using the WP4C

- The document explains how to generate a soil moisture characteristic (moisture release curve) using the WP4C dewpoint potentiometer, focusing on the wetting characteristic and noting hysteresis between wetting and drying paths.
- A moisture characteristic relates soil water potential to water content and is important for understanding water storage, plant availability, and transport of water and contaminants in soil.

## Procedure Overview

- Prepare a clean WP4C sample cup and record its mass (Mc).
- Create soil-water mixtures to achieve a range of water contents.
- Seal each sample with a disposable lid and prepare multiple samples for the same water content if made in bulk.
- For each sample: measure water potential, then quickly weigh the wet soil plus cup (Mw) to minimize moisture loss.
- Dry samples in a convection oven at 105°C for at least 16 hours; cool in a desiccator to avoid moisture uptake, then weigh the dry soil plus cup (Md).
- Calculate water content (g/g) using: (Mw - Md) / (Md - Mc).
- Plot the resulting data to form the moisture release curve; the document includes a sample figure and mentions a power-law fit line.
- Practical notes: tighten seals for better equilibration if needed; mixing soil in larger quantities (15 g or more) improves reliability and consistency; if the water content range is unknown, start with air-dry soil and incrementally add water until saturation.

## Data and Metadata to Capture

- Data to collect for each sample:
  - Sample ID, soil type, and batch information.
  - Water content target (g/g) and actual measured Mw, Md, and Mc values.
  - Measured water potential (MPa).
  - Mass measurements: Mc, Mw, Md.
  - Equilibration and measurement times and sequence (wetting path information).
  - Oven conditions (temperature, duration) and cooling/desiccation steps.
- Metadata and documentation:
  - instrument model (WP4C Dewpoint PotentiaMeter) and calibration status.
  - Date, operator, and protocol version used.
  - Any deviations from the protocol and notes on data quality.
- Output:
  - A moisture release curve dataset (water potential vs. water content) and any fitted model (e.g., power-law) with unit conventions (g/g for water content, MPa for water potential).

## Quality Assurance and Data Provenance

- Emphasize rapid sequencing of measurement and weighing to minimize moisture loss.
- Ensure seals are as airtight as practical to improve equilibration (e.g., Parafilm or sealant).
- Document mixing approach and batch preparation to support reproducibility.
- Record any anomalies or deviations and specify which portion of the curve corresponds to the wetting path.
- Maintain traceability from raw measurements (Mw, Md, Mc, MPa) to the plotted moisture characteristic and any fitted curves.
- Include notes on data cleaning, outliers, and when repeat measurements are required.

## Outputs

- A plotted soil moisture characteristic (wetting curve) showing water content (g/g) versus water potential (MPa).
- Any fitted relationships (e.g., a power-law line) with corresponding parameters.

## Governance and Documentation Considerations

- Standardize units and data formats (g/g for water content, MPa for water potential) across datasets.
- Capture comprehensive metadata to enable reproducibility and reuse by others (instrument, calibration, protocol version, conditions).
- Version control the measurement protocol and data processing steps (including the equation used for w/g calculation).
- Ensure data accessibility through appropriate portals or catalogues, with clear licensing and sharing terms.
- Document the experimental context (soil type, sources, preparation steps) to support cross-study comparability.

## Practical Challenges for Data Stewards

- Ensuring complete and consistent documentation across diverse projects and operators.
- Aligning this dataset with existing soil moisture datasets and metadata standards.
- Managing data from multiple systems or instruments and ensuring interoperability of units and formats.
- Handling large numbers of samples and maintaining data quality during rapid measurement workflows.
- Coordinating timely data entry and updates, especially when revisions or re-runs are needed.