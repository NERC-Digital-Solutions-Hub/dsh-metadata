# Hyetographs and statistics of annual-maximum rainfall events in Great Britain, from historical rain gauge records Supporting Documentation

- Purpose and scope
  - Documents the collection and processing of rainfall data to build a dataset of annual-maximum (AMAX) rainfall events in Great Britain.
  - Produces dimensionless hyetographs and statistical properties for ~70,000 AMAX events, enabling analysis of temporal rainfall characteristics and GB climatology.
  - Data source: sub-hourly rainfall records from Environment Agency (EA), Natural Resources Wales (NRW), and Scottish Environment Protection Agency (SEPA), prior to summer 2018.

- Data and outputs
  - AMAX values at multiple durations (5, 10, 15 minutes; 0.5–24 hours) forming the basis for each rainfall event.
  - 72,094 cumulative rainfall hyetographs and 207,084 AMAX values, with accompanying statistics.
  - Dataset components:
    - UK_AMAX.csv: all AMAX values (about 207k rows).
    - UK_AMAX_Hyetographs.csv: 72,094 cumulative rainfall profiles corresponding to AMAX values.
    - UK_AMAX_Hyetographs_Statistics.csv: metadata and summary statistics for profiles.

- Data collection and provenance
  - Original data: mixed temporal resolutions (mainly 15-minute accumulations or time-of-tip records) and measurement resolutions (0.2 mm per tip; some 0.5 mm).
  - Time span varies by gauge; no unified period to maximize long-running records; median record length ~20.5 years; total ~27,600 station-years.
  - Data were harmonised to common gauge identifiers and coordinates; spread across different agencies.

- Quality control (QC) and data integrity
  - Two-tier QC: Global SubDaily Rainfall-Quality Control (GSDR-QC) on hourly data, followed by Sub-Hourly Quality Control (SHQC) on original resolution.
  - GSDR-QC uses station metadata tests, 25 time-series tests, and a rule-base; ETCCDI indices (Climdex) as reference; GPCC daily data used where accessible (omitted here due to access restrictions for UK usage).
  - Local UK adaptations of GSDR-QC:
    - Excluded GPCC in local QC; retained ETCCDI references.
    - UK-specific adjustments: UKMO-based 1-hour and 24-hour records used for thresholding; 24-hour rolling totals assessed against UKMO record.
    - Streaks threshold adjusted to a fixed 20 mm/hour for large events; minor tweaks to reflect UK rainfall behavior.
  - SHQC focuses on sub-hourly resolution checks, including thresholds that vary by month to reflect seasonal extremes; spike and drift checks implemented with rolling sums and tipping-bucket data where available.
  - Limitations and caveats:
    - GPCC data not accessible for this UK-focused QC; spatial consistency tests were adapted accordingly.
    - Internal consistency and spike tests limited by data availability; multi-instrument consistency not tested.

- Independent rainstorm identification
  - Independent events identified by isolating rainfall bursts using a per-gauge minimum inter-arrival time to ensure statistical independence.
  - Each event may contain multiple AMAX values at different durations; care taken to remove duplicates across durations within the same event.
  - Result: ~70,000 independent rainfall events containing ~200,000 AMAX values.
  - Event boundaries are determined locally (per gauge); spatial independence across gauges not enforced.

- Data format and semantic structure
  - Event_id and Burst_id are central identifiers:
    - Burst_id links to a specific AMAX value and duration.
    - Event_id links multiple AMAX values within the same independent rainfall event.
  - Compound AMAX events: Event_id may include a non-zero part indicating long-duration AMAX totals composed of multiple independent storms.
  - Key fields include station identifiers, geographic coordinates (latitude/longitude), timestamps, cumulative rainfall profiles, and AMAX depths.

- Relevance for monitoring frameworks and policy evaluation
  - Provides high-resolution, long-running records of extreme rainfall behavior suitable for:
    - Flood risk assessment and infrastructure design analyses.
    - Calibration and validation of hydrological and climate impact models.
    - Evaluation of drought and extreme rainfall indices at sub-hourly to daily scales.
  - Enables construction of indicators around AMAX frequency, duration distribution, and event magnitudes to scrutinise policy outcomes and inform adaptation decisions.

- Practical considerations for implementation in monitoring programs
  - Data governance and accessibility:
    - Data are derived from UK government agencies; openness is balanced with governance requirements; some external reference datasets had restricted access, impacting full reproducibility of QC against those datasets.
  - Metadata and data transformation:
    - Extensive metadata is embedded in the dataset structure (Event_id, Burst_id, timing, location); however, users may need to perform careful data handling to interpret event-part relationships and compound events.
  - Temporal coverage and representativeness:
    - No unified time window across gauges; reliance on all available records maximizes information but introduces non-uniform observation periods.
  - Data quality and updates:
    - QC methods are robust and UK-tuned but rely on continued data sharing from agencies; updating the dataset would require reapplication of QC and storm-separation procedures.

- Observations on challenges aligned with monitoring framework archetype
  - Data gaps and variable data quality across sources (lack of data at ideal standards).
  - Access constraints to external reference datasets for QC.
  - Siloed data sources and governance barriers to data sharing beyond agencies.
  - Metadata completeness and consistency challenges; transformation requirements to harmonize formats.
  - Communicating complex, high-resolution rainfall outputs in policy-friendly formats.

- References and methodology base
  - QC methodologies and references include WMO guidelines, ETCCDI/Climdex indices, UK climate extreme records (UKMO), and related rainfall QC literature.
  - Key methodological works: development of the GSDR-QC, SHQC, and independent rainstorm identification approaches; details provided in the cited papers.