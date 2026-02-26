# Pontbren Database Catalogue

- A comprehensive environmental health monitoring catalog designed to identify measures for scrutinising policy, evaluating outcomes, and informing future decisions.
- Aimed at managers in government departments or environmental quangos responsible for designing and implementing monitoring frameworks.

## Data Organization and Framework

- Data organized in site- and type-based directories, primarily as .txt files.
- Stored in blocks (6-month intervals) with file names indicating collection dates.
- Appendices provide metadata conventions, QA coding, and supplementary information.
- Distinct QA (Quality Assured) subset; QA status coded and clearly indicated.
- Strong emphasis on data provenance, folder structure documentation, and user guidance to aid data reuse.

## Data Types and Instrumentation

- AWS (Automatic Weather Station)
  - Minute-scale sensor sampling; daily and 10-minute averages; daily max/min; wind direction SD.
  - Sensor updates added in 2009, affecting data structure.

- Bowl study site runoff and soil water tension
  - Runoff: weirs and tipping buckets; water height converted to flow; evaporation-related anomalies treated as no-flow.
  - Tensiometers measure soil suction at multiple depths.

- Groundwater monitoring
  - Five boreholes with Diver pressure transducers; barometric pressure correction; outputs as height relative to soil surface plus temperature.

- Hillslope study site runoff and soil water tension
  - Runoff via weir boxes (drain and overland flow); tensiometers on hillslope above shelterbelts; similar QA and potential data gaps (rodent damage, evaporation effects).

- Llyn Hir study site soil water tension
  - Tensioometer arrays at multiple depths; sampling frequency varied over time.

- Land use manipulation plots
  - Four plots with three replicates; treatments: Grazed, Ungrazed, Trees.
  - Tensiometers (10/30/50 cm) and overland flow (mm/h) per replicate; detailed plot metadata and treatment allocations.

- Neutron probe soil moisture
  - Profiles up to ~120 cm across multiple areas; calibration via soil count vs water content.

- Rain gauge data
  - Tipping bucket and storage gauges across multiple sites; data reported as mm/day or storage equivalents.

- Field diaries
  - Word documents documenting field observations and data issues to aid interpretation.

- Streamflow
  - 13 sites using Starflow acoustic Doppler systems (with site-specific calibrations against manual measurements); low-flow data treated as unsuitable for calibration.

## Data Quality, Metadata, and Governance

- Appendices describe a QA coding system (Appendix A) for good data, questionable quality, calibration issues, equipment problems, and site notes.
- Metadata accompany data: origin, calibration status, sampling frequency, instrument locations, etc.
- Borehole and N-probe logs (Appendices B–C) provide drilling method, location, depth, soil descriptions, and completion details.
- Documented data quality issues include patchiness from rodent damage, sensor recalibration needs, logger power problems, and data gaps.
- Calibration relationships provided for streamflow (site-specific y = αx + β) and for soil moisture/neutron-probe relationships (site-specific parameters).

## Data Access, Sharing, and Governance

- Outputs disseminated to stakeholders; underlying data may be shared publicly, though sharing can pose barriers.
- Emphasis on metadata completeness and data provenance to support reuse and verification.
- Data governance processes in place to ensure datasets meet standards, are securely stored, and kept up to date.

## Implications for Monitoring Framework Authors

- Demonstrates a layered, credible data management approach for complex monitoring programs:
  - Structured organization with explicit QA codes, unit conventions, and rich site metadata.
  - Transparent documentation of calibration and data quality to support policy evaluation.
  - Broad coverage across meteorology, hydrology, soil moisture, groundwater, and land-use experiments enabling multi-criteria policy assessment.
  - Balance between data openness and practical governance/data quality considerations.
- Key takeaways for authors of monitoring frameworks:
  - Establish clear QA coding and metadata standards from the outset.
  - Develop site-specific calibration relationships.
  - Anticipate and document data gaps; maintain field diaries and appendices to capture context.
  - Align data governance and sharing practices with policy evaluation needs.

## Equipment & Methods (Field Documentation)

- Borehole drilling and logging procedures documented in detail:
  - Repeated use of hand augers, AQ drill rods, guide tubes, pneumatic hammers, and rotary drills.
  - Borehole logs record grid references, datum levels, soil descriptions, thickness/depths, and completion details (aluminium access tubing).
  - Site-specific entries include S3 (east, central, west), grid coordinates, dates (e.g., 14/05/06), and soil stratigraphy notes.
- Field data collection emphasizes comprehensive, standardized borehole logs to support groundwater and N-probe datasets.

## Appendix D: Streamflow Gauging and Flow Measurements

- Documented streamflow gauging sites with flow metered spot measurements:
  - Start/finish times, flow estimates, and site references across numerous measurements and dates.
  - Data illustrate calibration and validation efforts for streamflow estimates at multiple sites. 

- Overall, the Equipment & Methods and Streamflow entries exemplify the depth of field data collection and the importance of meticulous methodological documentation for monitoring frameworks.