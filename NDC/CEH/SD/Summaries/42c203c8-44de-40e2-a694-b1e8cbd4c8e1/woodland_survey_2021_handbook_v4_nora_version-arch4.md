# Field Handbook

## Overview
- Field protocol for the 1971 baseline broadleaved woodland survey of Great Britain, amended and expanded (notably 2021) with procedures for soil sampling, understorey plant recording, DBH measurements, and plot attribute capture.
- Focus on building a longitudinal data set across woodland sites, enabling updates to original survey data and assessment of change over time.
- Data are intended to be collected primarily electronically (Survey123) with paper backups, and to be dispatched to CEH Lancaster for soil analyses.

## Data collection framework and instruments
- Primary data tool: Survey123 (ArcGIS) with offline capability; supports electronic field forms and automatic geo-location; backup paper forms provided.
- Data forms and scope:
  - Site Description and Habitats (site-level attributes and context)
  - Plot Description and Habitats (plot-level attributes within each site)
  - Vegetation Plot: Ground Flora (four nested quadrats within each 14.14 x 14.14 m plot, assessing vascular plants and common bryophytes)
  - Trees, Saplings and Shrubs (DBH, species, multi-stemmed entries, dead trees)
  - Soil Sampling (center of each plot; 15 cm depth; labelling and chain-of-custody)
- Data integrity: defined attribute definitions in Appendix IV; bryophyte recording restricted to a common set (Appendix I/Ib); careful handling to avoid double counting bryophytes (Total Bryophyte vs species-level bryophyte covers).

## Sampling design and plot layout
- Site contains 16 random sampling points (plots) per site, with a 14.14 x 14.14 m plot area (200 m2).
- Plot center and corners defined by physical markers; four nested 2 x 2 m to 14.14 x 14.14 m plots allow gradient sampling of ground flora.
- Ground flora sampling sequence:
  - Start with Nest 1 (innermost 2 x 2 m) to record presence of all vascular plants and common bryophytes; estimate % cover to the nearest 5% for each species within each nest.
  - Proceed to Nest 2–Nest 5, recording additional species and covers for each successive nested area.
  - Record total plot cover for all vascular plants plus seedling trees/shrubs and the six extra categories (litter, wood, rock, bare ground, water, total bryophytes).
- Trees, saplings, and shrubs are sampled by plot quadrants (NE and SW quarters for saplings/shrubs as per protocol); DBH measurements follow specific inclusion criteria and multi-stemmed configurations.

## Metadata, standards, and data quality
- Species handling:
  - Use dropdown lists; if unknown, use “Other” with free-text entry and replace later once identified.
  - Avoid duplicate entries; ensure accuracy of species lists per nest and per plot.
- Measurements and units:
  - Ground flora cover estimated for each nest; total percent cover can exceed 100% due to layered vegetation.
  - Bryophyte recording limited to common species and to understorey habitats (not on tree bases or rocks), per Appendix I.
  - DBH thresholds: trees ≥ 5 cm DBH; saplings > 130 cm height but < 5 cm DBH; shrubs defined by species and typically in diagonally opposite quarters (1 and 3).
- Bias minimization: avoid subjective bias by knowingly bypassing non-representative microhabitats; use prior DBH data as a locator to re-find plots, but interpret changes with caution.
- Site vs plot consistency: cross-check attributes on plot forms against site forms for logical consistency.

## Access, permissions, and governance
- Permissions managed by XSG Ltd; CEH issues permission letters and site maps; surveyors must carry permission details and contact info.
- Avoid recording on land with insufficient permission; sites may have changed land use since 1971 (e.g., gardens, motorways) and should be noted in site notes if applicable.
- Safety and due diligence stressed: contact landowners and managers as required; maintain awareness of land-use changes and access constraints.

## Data handling, submission, and lifecycle
- Electronic data submission prioritized:
  - Online submission to central database via Survey123 when connected; offline data stored in drafts/outbox and uploaded later.
  - Automatic data saving reduces loss risk; QA checks recommended before submission.
- Soil samples:
  - 16 soil cores per site (one per plot), labeled and dispatched to CEH Lancaster (or partner institution) within the same week if possible.
  - Cold chain and labeling procedures emphasized to prevent data loss.
- Site-level data collection:
  - A separate Site Description and Habitat form is completed for the whole site in addition to the 16 plot forms per site.
  - Ensures context and landscape-scale attributes accompany plot-level measurements.
- Appendices and protocols:
  - Appendix IV details attribute definitions and recording guidance.
  - Appendix V lists field equipment and per-site provisioning (permissions, mapping, sampling tools, labeling).
  - Appendix VII provides soil analysis laboratory protocols (pH, loss on ignition, sample preparation).
  - Appendix VIII outlines Survey123 navigation and data management workflows.

## Practical takeaways for data leadership and strategy
- Standardization and comparability: rigorous, predefined data schemas (site vs plot; nested plots; DBH conventions) enable robust longitudinal analysis and cross-site comparability.
- Data quality controls: constrained bryophyte lists, explicit handling of unknown species, and cross-form consistency checks promote data integrity across repeated surveys.
- Data lifecycle and governance: centralized data submission to CEH; documented permissions; robust metadata and site history notes support traceability and network-wide data sharing.
- Technology-enabled data capture: Survey123 and offline GPS reduce transcription errors, improve location accuracy, and streamline data delivery to central repositories.
- Risk management: explicit guidance on access permissions, land-use changes, and safety considerations helps mitigate data gaps and field risks.
- Community and ecosystem: facilitation of data collection across multiple sites with standardized protocols supports broader environmental monitoring initiatives and inter-organizational collaboration.