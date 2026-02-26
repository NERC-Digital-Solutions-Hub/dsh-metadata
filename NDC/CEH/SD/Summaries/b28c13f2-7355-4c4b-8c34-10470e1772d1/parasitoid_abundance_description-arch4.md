# Description, Experimental Design and Collection

- Overview
  - Data describe the abundance of parasitoid wasps collected from sticky traps placed in Brassica napus plants subjected to Free-Air Diesel and Ozone Enrichment (FADOE) ring experiments.
  - Focus on two parasitoid groups: Diaeretiella rapae and others; counts are recorded per sticky trap and summarized by various experimental factors.
  - Two-year study with field conditions, capturing environmental and treatment effects on parasitoid communities.

- Experimental design
  - Location: field in 2018 and moved to an adjacent field in 2019; fields are in proximity with precise latitude/longitude provided.
  - Treatments: four pollutant conditions—diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and a control (CON; natural air).
  - Aphid inoculation: plants received either 50 aphids, 10 aphids, or no aphids (Treatment).
  - Replication and runs: each FADOE ring is assigned a number; two rings per pollutant treatment across four treatments (total rings per year); sticky traps deployed once per run among plant groups; three experimental runs over the two years.
  - Sampling timeline: sticky traps collected after seven weeks, replaced with a second set, and collected after an additional week; traps stored at -20 °C prior to analysis.

- Data collected and structure
  - Counts recorded for each trap: D. rapae (D_rapae_counts) and other parasitoids (Others_counts).
  - Derived metric: Percentage_D_rapae = percentage of total parasitoids identified as D. rapae.
  - Data are pooled for each Treatment per Ring per Year from week seven and eight collections.
  - Key identifiers in the dataset include Year, Ring, Pollutant, Treatment, Run, D_rapae_counts, Others_counts, and Percentage_D_rapae.
  - Geospatial and procedural metadata: field locations, Ring numbering, and cross-year field movement.

- Data processing and quality control
  - Parasitoid identification performed under a microscope and categorized into two groups (D. rapae vs. others).
  - Full FADOE configuration and quality-control measures are described in the referenced methodology.
  - The study references a detailed methodology: Ryalls et al. 2022 (Environmental Pollution), which documents how anthropogenic pollutants affect insect-mediated pollination services.
  - Data handling includes freezing of samples (-20 °C) and pooling across specified weeks and runs for analysis.

- Data quality, provenance, and reuse considerations for data leaders
  - Clear linkage between experimental factors (Pollutant, Treatment) and biological responses (D. rapae vs. others) enabling system-level analysis of data flows and outcomes.
  - Metadata supporting discoverability includes explicit stage of collection, trap timing, and pooling rules, aiding reproducibility and auditability.
  - Potential considerations:
    - Granularity: trap-level counts with pooling by Year, Ring, Treatment; researchers may need to reconstruct per-run or per-week details if required.
    - Cross-year comparability: field movement between years and environmental variability may influence counts; appropriate stratification needed.
    - Metadata completeness: ensure inclusion of processing steps, identification criteria, and any excluded data for full data stewardship.
  - Suitable reuse applications include examining how air pollutants influence parasitoid abundance and composition, and integrating with broader networked data on pollination-servicing insects.