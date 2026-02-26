# PAH Concentrations and DOC Measurements Across Sites and Seasons

- **Scope of the dataset**
  - Measurements taken across five sites: Marshaw Wyre, Abbeystead, Dolphinholm, Six Arches, Garstang.
  - Occasions spread over four seasons: 19 Aug 2010; 6 Dec 2010; 6 Mar 2011; 6 Jun 2011.
  - Focus on polycyclic aromatic hydrocarbons (PAHs) in water, including different mass balance fractions.

- **Measured variables**
  - total dissolved PAHs (ng L-1)
  - freely dissolved PAHs (ng L-1)
  - DOC-bound PAHs (ng L-1)
  - DOC concentration (mg L-1)
  - log K_DOC: log-transformed water–DOC partition coefficient for PAHs

- **Calculation and interpretation of log K_DOC**
  - log K_DOC is derived from PAH and DOC concentrations to reflect the water–DOC partitioning behavior.
  - It involves the total PAH concentration (c_total), freely dissolved PAH concentration (c_free), and DOC concentration (c_DOC); the exact formula is described in the source, though the snippet provided contains a garbled representation.

- **Data structure observations**
  - Data organized by site and season, with multiple PAH-related concentration measures and DOC data for each entry.
  - Units are consistently reported: ng L-1 for PAHs and mg L-1 for DOC.

- **Data quality and metadata considerations for data leaders**
  - The excerpt lacks detailed methodological metadata (sampling methods, QA/QC procedures, detection/quantification limits).
  - The log K_DOC calculation is not fully explicit in the text; requires verification and clear documentation for reproducibility.
  - Important metadata to capture:
    - measurement methods and instruments
    - detection limits and data handling for non-detects
    - data provenance and any data cleaning steps
    - assumptions used in computing log K_DOC

- **Data management and use potential**
  - Provides a basis to analyze spatial (sites) and temporal (seasons) variation in PAH partitioning with DOC.
  - Useful for understanding PAH mobility and bioavailability in relation to DOC under different hydrological conditions.
  - To improve usability, create a data dictionary, formalize the log K_DOC calculation, and document data provenance and update cadence.
  - Identify and plan to fill data gaps: limited sites and seasons; consider expanding spatial/temporal coverage and harmonizing units and methods.

- **Considerations for stakeholders and communities**
  - Data can support policy and environmental management discussions around PAH fate in freshwater systems.
  - Co-ownership of the data product can be enhanced by releasing clear metadata, calculation methods, and data quality notes.