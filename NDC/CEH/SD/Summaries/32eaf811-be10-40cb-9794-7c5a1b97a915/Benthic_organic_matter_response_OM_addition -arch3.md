# Benthic organic matter of Welsh upland rivers in response to organic matter addition

- Purpose and design
  - A BACI (before-after-control-impact) study to assess how added organic matter affects benthic organic matter (BOM) in Welsh upland rivers.
  - Each stream includes an upstream reference (control) zone and a downstream experimental zone, with a 20–50 m gap to ensure independence.
  - Timeline:
    - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated equally.
    - After period (T2): 57–62 days (early Jan 2013 to Mar 2013); experimental zone receives leaf litter additions.
  - Leaf litter source: oak, birch, and alder from deciduous trees.
  - Manipulations:
    - One-tonne leaf litter bags emptied above the experimental zone at the start of T2, maintaining a minimum wet weight of 1.7 kg m-2 in the experimental zone.
    - Additional leaf litter (630 kg wet weight) added on Feb 12 and Mar 5, 2013 after two large storm events.
  - Sampling occurred across five occasions (Jan–May 2013).

- Study design details
  - Six random BOM samples collected per reach on five occasions.
  - Surber net sampler used: area 0.1 m2, mesh 330 µm, depth 10 cm.
  - Samples preserved on-site in 70% industrial methylated spirit; later processed in the lab.

- Collection and laboratory methods
  - Laboratory processing: macroinvertebrates removed; remaining material dried and weighed to 0.01 g.
  - BOM correction: inorganic content removed by ash combustion (550°C, 5 h) to derive ash-free organic matter.
  - Measurements reported as weights in grams.

- Data collected and units
  - Coarse and fine particulate organic matter (CPOM/FPOM) measured in grams.
  - Data captured as weight of BOM per sample, with correction for inorganic content.

- Field and laboratory instrumentation
  - Field: Surber net (0.1 m2, 330 µm mesh, 10 cm depth).
  - Laboratory: weight meter for precise mass measurements.

- Data structure and metadata
  - Primary data format: flatbed CSV.
  - Key data fields (10 columns):
    - site_code: sampling site identifier
    - landuse: basin land-use
    - region: stream basin region
    - time: before or after manipulation
    - month: sampling month
    - reach: experimental or control site designation
    - replicate: replicate code
    - surber_area: area of the Surber sampler (m2)
    - cpom: coarse particulate organic matter (g)
    - fpom: fine particulate organic matter (g)
  - Supporting site description file: DURESS_CU_site_description.csv with site metadata (site code, name, coordinates, grid refs, elevation, survey campaign, catchment).

- Data quality and limitations
  - Quality control: none specified.
  - Calibration steps: none specified beyond ash-free conversion for BOM.
  - Metadata richness: robust site and sampling metadata provided; potential gaps in formal QC documentation.

- Supporting documentation
  - Site description file accompanying the dataset, detailing coordinates and related context.
  - Campaign notation indicates Welsh Acid Waters Survey (WAWS) and Plynlimon/Llyn Brianne catchments as part of site context.

- Relevance for monitoring frameworks
  - Demonstrates a structured, transparent BACI approach to evaluate environmental health responses to controlled organic matter additions.
  - Provides a clear, machine-readable data schema suitable for integration into monitoring dashboards and future analyses.
  - Highlights practical data governance considerations: data sharing of underlying datasets and comprehensive metadata (site, reach, time, and replicate identifiers) to enable reuse and comparability across monitoring programs.
  - Identifies data and operational challenges typical in monitoring work (data gaps, access, metadata quality, and data transformation needs) that framework authors should plan for when designing monitoring initiatives.