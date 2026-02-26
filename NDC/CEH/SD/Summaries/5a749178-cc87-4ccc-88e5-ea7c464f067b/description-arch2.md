# Data description Beech tree ring data from hot and dry European distribution edges, 2019

- Aim and context
  - Utilize the relationship between European Beech tree growth and environmental factors (including climate) to monitor and forecast drought-linked declines in forest growth across Europe.
  - Focus on inter-annual growth using dendroecology (ring width) to assess environmental signals.

- Study design and sampling
  - Expanded sampling to address climatic gaps in the European Beech Tree Ring Network (EBTRN).
  - 12 new sites sampled in late 2019 across Bulgaria, Albania, Kosovo, and Spain.
  - Sites are primarily at lower elevational ends to capture hot and dry edge conditions of European Beech distribution.
  - Metadata file site_meta.csv provides latitude, longitude, elevation, and nearest town for each site (as of late 2019).

- Field procedures and lab processing
  - At least 15 canopy-level trees sampled per site; two cores collected per tree.
  - Cores processed using standard dendrochronology procedures: air-dried, mounted, and sanded through progressively finer grits (80, 120, 300, 600, 1200).
  - Cores scanned at 2400 PPI for CDendro measurements with a precision of 0.01 mm.
  - Cross-dating performed virtually and statistically; COFECH used to verify cross-dating quality.

- Data products and structure
  - 12 site-specific measurement files (named by site ID) containing ring width measurements for each core by year; units in millimeters with 0.01 mm resolution.
  - Data format: first column = year; subsequent columns = ring width measurements for each core.
  - Tree core IDs are site ID + tree ID, with two cores per tree labeled 'a' and 'b'.
  - Missing values indicated by NA.

- Relevance to monitoring and analysis
  - Enhances representativeness of EBTRN by incorporating hot and dry edge environments, enabling improved monitoring of drought impacts on Beech growth across Europe.
  - Provides standardized, QA/QC’d data suitable for environmental health analyses and policy-relevant monitoring.

- Data management and accessibility considerations
  - Metadata and measurements are organized to support standardized analysis and cross-site comparisons.
  - Aligns with broader objectives to store outputs and, where possible, enable access to underlying data used to generate final outputs; data is prepared for potential deposition in appropriate data portals.