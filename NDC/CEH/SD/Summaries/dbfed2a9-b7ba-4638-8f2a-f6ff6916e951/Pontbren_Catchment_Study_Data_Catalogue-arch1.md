# Pontbren Database Catalogue

- A comprehensive, QA-controlled, multi-site environmental dataset designed for correlations, pattern detection, and predictive modeling.
- Data organized into directories and six-month blocks; includes metadata, site descriptions, and QA codes to support reuse and discovery.

## 1) Purpose, scope, and intended use

- Aimed at identifying correlations, reporting findings, and predicting impacts of actions.
- Combines topic expertise with statistical analysis to inform practical decisions in government/environmental contexts or academic work.
- Supports cross-dataset analyses across hydrology, soil moisture, weather, rainfall, groundwater, and streamflow, subject to data quality and site caveats.

## 2) Data structure and organization

- Data stored as text files (.txt) in a hierarchical directory structure.
- Major directories include: AWS, Bowl study site, Groundwater, Hillslope study site, Llyn Hir, Land use manipulation plots, Neutron probe, Rain gauge data, Streamflow, Field Diaries, plus Appendices.
- Quality Assured (QA) data are flagged within subfolders; appendices provide QA coding, borehole logs, neutron probe logs, and site logs.
- Data blocks are typically six months (Jan–Jun, Jul–Dec) with filenames indicating covered dates.

## 3) Data categories and instrumentation

- Automatic Weather Station (AWS)
  - Located at the bowl site; minute- to daily-averaged data; variables include radiation, wind, temperatures, humidity, etc.
  - Sensor changes from 2009 introduced additional fields.

- Bowl study site
  - Runoff: weir boxes and tipping buckets; overland flow measurements; drainage data.
  - Soil water tension: tensiometers at 10, 30, 50 cm.

- Groundwater
  - Monitoring at five boreholes with Diver pressure transducers; barometric correction; groundwater height and temperature; data cadence from 10 to 30 minutes.

- Hillslope study site
  - Tree shelterbelt runoff and tensiometer data; multiple weirs and data quality notes (e.g., rodent damage affecting data).

- Llyn Hir study site
  - Tensiometer arrays at 10, 30, 50 cm; sampling cadence similar to other sites.

- Land use manipulation plots
  - Four plots with replicates; treatments include Grazed (control), Ungrazed, and Trees; tensiometers and overland flow measurements; plot locations documented.

- Neutron probe soil moisture
  - Profiling across bowl, hillslope, plots, tree areas, and Llyn Hir; typically 10 cm increments to 120 cm; site-specific calibration notes.

- Rain gauges
  - Tipping bucket and storage gauges; site-specific folders (Bowl, Llyn Hir, Penllwyn, Quarry, Rhos1, etc.); units in mm/day.

- Field diaries
  - Word documents with monitoring notes and data-quality issues.

- Streamflow
  - Flow monitoring across multiple sites; Starflow acoustic Doppler; site-specific calibrations linking Starflow outputs to manual measurements; notes on low-flow reliability.

## 4) Equipment & methods (N-probes and borehole logging)

- Borehole logging conducted with hand augers, AQ drill rods/guide tubes, pneumatic hammer, Atlas Copco RAB/Leopard air-flush drills; borehole logs compiled by Centre for Ecology and Hydrology.
- N-probe boreholes NP20–NP23 described in detail across sites (Pen-tal-y-cein, Llanfair Caereinion, COED CWM-Y-LLWYNOG, Tyn y Fron Trees, etc.).
- Logs include grid references, datum levels, lithology (e.g., silty/clay soils, mottling), thicknesses, depth to completions, and aluminum access tubing completions.
- Samples collected at various depths; depths typically recorded as 0.25–1.60 mBGL with detailed soil descriptions and stratigraphy.
- Data emphasize traceability: borehole numbers, dates (e.g., 14/05/06), and site-specific notes.

## 5) Data quality, QA, and governance

- Appendix A defines a comprehensive QA coding system covering data quality, logger status, sensor calibration/operation, and site-specific issues (rodent damage, power, calibration integrity, etc.).
- QA codes differentiate good versus questionable or unusable data across tensiometer, rain gauge, overland flow, groundwater, Starflow, and other components.
- Data quality notes and caveats (e.g., low-flow calibration reliability, data gaps, site-specific problems) are documented to guide analysts.

## 6) Appendices, logs, and data support

- Appendix B: Groundwater borehole logs (equipment, drilling, stratigraphy, depth, completions, groundwater LVD notes).
- Appendix C: Neutron probe access tube logs (location, depth, soil types, calibration notes, access-tube details).
- Appendices also include QA coding details, site logs, and field notes to support interpretation and reproducibility.

## 7) Data accessibility, discoverability, and usage guidance

- Metadata and directory descriptions are designed to aid discoverability and reuse.
- Site maps and figures illustrate instrument locations and data collection schemes.
- Suitable for exploring correlations, patterns, and predictive relationships, with attention to QA codes and site-specific caveats (rodent damage, calibration differences, low-flow limitations, data gaps).
- Integration across multiple datasets requires standardization of scales, careful handling of missing values, and consideration of data provenance.

## 8) Practical implications for analysts

- Expect diverse data formats tied to multiple measurement types and sites; robust QA filtering is essential before analysis.
- Use neutron probe, tensiometer, groundwater, streamflow, and rainfall datasets in combination to model hydrological processes and land-use effects.
- Cross-site calibration and contextual notes (e.g., site-specific calibrations for Starflow) are critical for reliable modeling and interpretation.
- Maintain dataset discoverability and reuse by referencing QA codes, site metadata, and appendices.