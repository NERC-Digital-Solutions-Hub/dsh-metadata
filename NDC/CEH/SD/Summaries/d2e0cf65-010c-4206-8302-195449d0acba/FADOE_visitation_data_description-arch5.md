# FADOE_visitation.csv

- Overview
  - Dataset of Brassica nigra flower visitation frequencies by pollinating insects collected in 2018 and 2019.
  - Observations taken in Free-Air Diesel and Ozone Enrichment (FADOE) rings across two locations, with four pollution treatments and a control.
  - Measurements include insect counts by group, flower counts, and derived visitation rates, across observation units of six adjacent plants and over 5–10 minute observation periods.

- Experimental design and collection
  - Rings and locations: Each ring had two locations (-field shift between 2018 and 2019); rings distributed within a wheat field, moved for 2019.
  - Treatments: Four pollution treatments per year (diesel exhaust D, ozone O3, combined D+O3, and control CON).
  - Rotation: One week in 2019 where plants/treatments were rotated between rings to quantify spatial variation in pollinator foraging behavior.
  - Observation units: Each unit consists of six adjacent plants; observers recorded insect visits, durations, and plant details.
  - Timing: Year (2018 or 2019) and Date label the sampling period; observations lasted 5–10 minutes with start and finish times and calculated durations.
  - Recorder and standardization: Observations performed by trained recorders; insect groups tracked include honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth, and several others; visits defined as landing or feeding attempts.
  - Flower counts: Number of flowers recorded for each observation period to enable rate calculations.

- Data structure and variables (high-level)
  - Identifiers and metadata: Year, Ring, Location, Rotation status, Treatment, Date, Start time, Finish time, Duration, Number of plants, Plant number, Recorder.
  - Observation scope: Observation unit specifics (6 plants) and the number of flowers observed.
  - Insect counts by group: Multiple columns for various pollinator groups (e.g., honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth, and others).
  - Flower visits by group: Counts of flowers visited by the same pollinator groups.
  - Derived metrics: 
    - Insect counts per hour (insect counts scaled by flowers and time).
    - Flower visits per hour (visits scaled similarly).
    - Average visits per insect for the six focal pollinator groups.
  - Totals and rates: Totals for insect counts (total), visits (total), and visits per insect; scaled rates provided across relevant columns (including per-hour metrics).
  - Data on spatial/temporal structure: Year-location pairing, with a rotation design to assess spatial variation.

- Data quality, processing, and provenance
  - Data quality steps: Insect identification by trained recorder; subsequent quality assurance, cleaning, and transformation prior to sharing.
  - Metadata and documentation: Detailed column descriptions and measurement methods embedded in the dataset; rotation and field location data included to support interpretation of spatial effects.
  - Availability and limitations: Data are provided as a structured CSV with explicit temporal and spatial design; consider potential limitations related to observational data (e.g., observer bias, time of day, weather not specified) and any embargo or licensing constraints not described in the document.
  - Update and governance: The dataset notes a mechanism for updating each ring’s data and respecting sharing limitations; data upload and cataloguing are expected as part of the sharing process.

- Data sharing, reuse, and governance considerations
  - Format and accessibility: CSV format suitable for ingestion into data portals and catalogs.
  - Reuse guidance: Derived metrics (per-hour rates and averages) facilitate cross-study comparisons; clear mapping of columns supports reproducibility.
  - Governance needs: Ensure metadata completeness (column definitions, units, observation protocol), provenance tracking (who collected data, when, and under which treatment), and clear licensing/usage terms for downstream users.
  - Compatibility and interoperability: Document data standards used for units and nomenclature; align with existing data governance practices to minimize incompatible formats across systems.

- Key challenges and considerations for Data Stewards
  - Aligning user needs with dataset scope: Ensure the dataset’s granularity and derived metrics meet data user requirements (e.g., researchers, policy makers).
  - Timely access and data integration: Manage timely data provision from field teams and compatibility with multiple systems and formats.
  - Standardization across formats and large data volumes: Maintain consistency across years, locations, and treatments; handle potentially large per-group counts and derived metrics.
  - Handling incomplete metadata or potential biases: Address any gaps in metadata (e.g., environmental conditions during observations) and mitigate observer-related biases through documentation and data quality checks.
  - Ensuring updates and transparency: Maintain clear update processes and documentation of any changes to the dataset over time.