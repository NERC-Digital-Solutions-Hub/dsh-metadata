# Pontbren Database Catalogue

- A comprehensive data platform documenting hydrological and environmental data across multiple study sites, with an emphasis on data discovery, quality assurance (QA), and reusability.
- Aims to support correlational analyses, modeling, and impact assessment by organizing data with metadata and QA codes to enable robust analysis and reproducibility.

## Data structure and contents

- Data organized into theme- and site-based directories, including:
  - AWS (Automatic Weather Station)
  - Bowl study site runoff and soil water tension data
  - Groundwater (boreholes)
  - Hillslope study site runoff and soil water tension data
  - Llyn Hir study site soil water tension data
  - Land use manipulation plots
  - Neutron probe soil moisture data
  - Rain gauge data
  - Field diaries
  - Streamflow
  - Appendices (QA coding, borehole logs, neutron probe logs)
- Each data type is subdivided by location and instrument; files predominantly .txt, organized by collection periods (e.g., January–June, July–December); QA codes documented in Appendix A.
- QA and provenance metadata accompany datasets to explain data issues, instrumentation changes, and site conditions; datasets are designed for cross-site comparisons and portal discoverability.

## Instrumentation and data details (key themes)

- AWS (Automatic Weather Station)
  - High-frequency measurements (1-minute; daily and 10-minute averages) with sensor upgrades influencing data structure post-2009.
- Bowl, Hillslope, Llyn Hir, and Groundwater datasets
  - Runoff and drainage measurements (weirs, tipping buckets), tensiometers at multiple depths, groundwater monitoring via boreholes with transducers and barometric compensation.
  - Multi-site installations with site-specific calibration and data quality notes.
- Neutron probe soil moisture
  - Multi-site measurements (0–120 cm depth), site-specific calibration acknowledging peat and soil variations.
- Rainfall and streamflow
  - Rain gauges at multiple locations with tipping-bucket and storage measurements.
  - Streamflow mainly via Starflow acoustic Doppler systems; depth/velocity measurements at newer sites with linear calibrations to convert to flow (L/s).
- Field diaries and appendices
  - Field notes documenting issues and data quirks; appendices provide QA codes and borehole/neutron probe logs for provenance.

## Quality assurance, metadata, and provenance

- QA: Data flagged with QA codes (Good quality and various issue types such as logger failures, calibration problems, etc.) outlined in Appendix A.
- Provenance: Borehole logs and neutron probe logs (Appendices B–D) provide site-specific details and calibration context to support reproducibility.
- Metadata: Emphasizes tracking data sources and making datasets discoverable with descriptive metadata in data portals.

## Calibration and data processing notes

- Streamflow calibration uses site-specific linear relationships (y = αx + β) to align Starflow estimates with spot measurements; low-flow data are often excluded from calibration.
- AWS sensor changes and post-2009 data columns reflect improved measurement accuracy.
- Neutron probe data require counts-to-moisture-content conversion with site-specific parameters, including peat adjustments where applicable.

## Practical considerations for analysts

- Rich, multi-site, multi-system dataset enabling analyses of rainfall, soil moisture, runoff, groundwater, and streamflow, with land-use treatments aiding causal inferences.
- QA metadata enables robust data cleaning, filtering, and reproducibility across analyses and models.
- Designed to support cross-site comparisons, multi-scale modelling, flood-risk evaluation, and hydrological responses to land management.
- Challenges include data gaps, sensor/logger failures, animal damage to equipment, and harmonization across varying sampling frequencies and formats.

## Access and reuse

- Catalogue provides a structured framework to locate and reuse data, with metadata-rich organization supporting portal upload and provenance.
- Emphasizes careful interpretation with QA flags and site-specific calibrations to ensure robust analyses.

## Equipment & Methods (borehole logs excerpt)

- Methods and site details for borehole logging:
  - Equipment: hand auger with AQ drill rod/guide tube, pneumatic hammer, Atlas Copco RAB hand-held air flush rotary drill; logging performed under Centre for Ecology and Hydrology.
  - Sites and probes: N-probes associated with Manipulation plots 3.1–3.3 at Site S3 (Eastern, Central, Western); grid references provided (e.g., SJ 07360 06833; SJ 07341 06821; SJ 07323 06807).
  - N-probe logs NP20–NP23:
    - Depths and diameters: Depth measurements from ground level with depth mBGL; apparatus completion using 16 gauge aluminium tubing.
    - Soils: Descriptions include dark yellow brown silty clays, clays with mottling, peat/inclusions, gravelly clays, and various weathering materials; logs detail soil horizons, moisture, and mottling.
    - Datums and levels: Datum levels and reduced levels recorded; multiple logs document different depths and horizons.
    - Sampling: Sample intervals commonly 0.25–1.60 m, with ranges noted (e.g., 0.85–1.50 m, 1.20–1.55 m).
  - Documentation cadence: Example dates shown (e.g., 14/05/06) with repeated entries across NP20–NP22 and a separate borehole NP23 at another location (COED CWM-Y-LLWYNOG, LLANFAIR CAEREINION).
- The borehole logs provide detailed provenance for groundwater-related data and are integrated into the broader Pontbren data framework to support calibration and interpretation.