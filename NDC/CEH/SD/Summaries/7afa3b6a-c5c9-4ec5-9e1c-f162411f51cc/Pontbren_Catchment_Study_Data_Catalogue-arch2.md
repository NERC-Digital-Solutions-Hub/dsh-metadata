# Introduction to the Database Catalogue

- Purpose and audience: Describes the Pontbren Database, its instrumentation, data structure, quality assurance, and supporting documentation to monitor environmental conditions consistently over time. Aimed at researchers and analysts evaluating environmental health and policy performance using standardized monitoring data.
- Core aim for analysts: support examining environmental health over time through consistent, comparable data outputs and transparent data quality information.

## Overall structure and data organization

- Data organized into descriptive directories representing dataset families and sites; 6-month data blocks (January–June, July–December) for handling, with some exceptions for sampling frequency or file size.
- Data points carry quality assurance (QA) codes; QA framework and related notes are provided in appendices.
- Hierarchical folder structure examples: Quality Assured data; AWS; Bowl study site; Groundwater; Hillslope study site; Llyn Hir; Land use manipulation plots; Neutron probe soil moisture; Rain gauge data; Streamflow; Field diaries.
- Data are primarily plain text (.txt) files to facilitate reuse and interoperability.

## Data quality assurance and QA coding

- A comprehensive QA coding system (Appendix A) marks data quality and issues across all measurement types (e.g., tensiometers, rain gauges, overland flow, groundwater, Starflow, site manipulations).
- QA codes distinguish data quality categories such as good quality, calibration issues, logger failures, sensor problems, animal damage, and site-specific reliability concerns.
- Supporting materials include borehole logs (Appendices B–C) to aid interpretation and QA.

## Data categories and instrumentation

- Automatic Weather Station (AWS)
  - Location: bowl within instrumented hillslope.
  - Measurements: incident radiation, wind speed/direction, soil temperature, relative humidity, air temperature, net radiation.
  - Sampling: sensors log every minute; data delivered as daily and 10-minute averages; 2009 updates added columns for improved RH and temperature accuracy.
- Bowl study site - runoff and soil water tension
  - Subfolders for bowl runoff and tensiometers; runoff tracked via weirs and tipping buckets; pressure transducers estimate flow (L/s).
  - Tensiometers at multiple depths (10, 30, 50 cm) in arrays; data consolidated, with logger changes in 2008.
- Groundwater
  - Monitored at five boreholes using Diver pressure transducers with barometric correction (BaroDiver); outputs include water height and groundwater temperature.
  - Sampling frequency changed from 10 minutes to 30 minutes in Oct 2006; borehole logs provide location, depth, lithology, and completions.
- Hillslope study site - runoff and soil water tension
  - Tree shelterbelt hillslope data (excluding boreholes/neutron probes); weirs and tensiometers; overland flow captured by traps and converted to continuous tipping-bucket data.
- Llyn Hir study site - soil water tension
  - Tensiometers at 10, 30, and 50 cm; initial 10-minute cadence with later adjustments; data expressed as cm H2O.
- Land use manipulation plots
  - Four plots with three replicate treatments: Ungrazed, Trees, and Grazed; randomized across replicates.
  - Data include tensiometer readings (10/30/50 cm) and overland flow (mm/h) for isolated plots; dedicated subfolders (M1–M4) describe layout and treatments.
- Neutron probe soil moisture
  - Profiles across bowls, hillslope, plots, tree areas, and Llyn Hir; measurements typically every 10 cm down to 120 cm where possible.
  - Calibration uses site-specific relations; CEH-derived parameters (alpha ≈ 0.96, beta ≈ -0.01) with notes on peat/organic-rich surfaces affecting top layers (e.g., Llyn Hir).
- Rain gauge data
  - Tipping bucket and storage gauges; rainfall reported as mm/day (tipping buckets) or mm (storage data); locations listed (Bowl, Llyn Hir, Penllwyn, etc.).
- Field Diaries
  - Word documents containing field notes on locations and instrumentation; used to document data issues and interpret anomalies.
- Streamflow
  - Multiple gauging sites with Starflow bed-mounted acoustic Doppler systems; outputs include stage height, velocity, and derived flow; data logged every minute and averaged every 15 minutes.
  - Calibration relations (y = alpha x + beta) connect Starflow estimates to manual spot measurements; low-flow data (<50 mm depth) flagged as unsuitable for calibration at several sites.
  - Site-specific calibration parameters provided (Table 3).

## Calibration and site-specific notes

- Starflow vs. manual calibration: site-by-site calibration curves provided (Table 3) with alpha and beta values and standard deviations.
- Low-flow data: readings with very low water depths may be excluded from calibration.
- 2009 updates: AWS relative humidity and temperature readings include additional columns for improved accuracy.

## Data accessibility, reuse, and storage

- Emphasizes clear access, traceability, and quality assurance to support reuse.
- Data are stored in text-based formats and uploaded to appropriate portals as part of the data lifecycle, enabling broad data access for analysis and policy evaluation.

## Appendices and supporting materials

- Appendix A: Detailed QA coding system covering tensiometers, rain gauges, overland flow, groundwater, Starflow, and site manipulations.
- Appendix B: Borehole logs detailing drilling equipment, methods, soil descriptions, lithology, and completions.
- Appendix C: Neutron probe access tube logs detailing locations and logs for N-probe sites.
- Additional items include a Table of Tables and a Table of Figures to aid catalog navigation.

## Endnotes and references

- The Catalogue provides a comprehensive, multi-site, multi-parameter environment monitoring dataset with standardized QA, calibration approaches, and documentation to support robust long-term environmental monitoring and analysis.

## Implications for analysts

- A single, standardized dataset framework enabling cross-site comparisons and longitudinal analyses of environmental health and policy outcomes.
- Transparent QA and calibration metadata are integral for robust interpretation and reuse in research, reporting, and decision-making.
- The structure supports data integration and broader reuse by external researchers and policy evaluators, addressing the challenge of increasing data value and data accessibility.