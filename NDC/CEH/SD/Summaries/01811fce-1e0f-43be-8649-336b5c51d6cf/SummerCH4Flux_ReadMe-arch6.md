# ReadMe file for SummerCH4Flux.csv

## Purpose and scope
- Provides CH4 flux data from control (no urine) and two urine treatments (artificial and real sheep urine) applied to patches on a dystric histosol in unimproved grazing land.
- Aims to support analysis of how urine amendments affect methane emissions over time, with high-frequency measurements post-treatment.
- Includes data quality notes and metadata to aid reuse and proper attribution.

## Study site and context
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK.
- Site features: unimproved grazing land; soils described as dystric histosol; elevation ~556 m above sea level; coordinates 53°22'N, 3°95'W.
- Experimental context: sheep excluded from plots starting 15/05/2017 to avoid recent excretal effects.

## Experimental design
- Treatments (n = 4): 
  - Control: no urine application.
  - Artificial sheep urine: 200 ml applied per patch (0.25 m2 area per patch) totaling N = 920 kg N ha-1 per patch, in triplicate patches.
  - Real sheep urine: 200 ml applied per patch (0.25 m2 area per patch) totaling N = 930 kg N ha-1 per patch, in triplicate patches.
- Application/date: 24/07/2017.
- Design: randomised block experimental design with patch-level applications within chambers.
- Each treatment is represented by triplicate discrete patches per chamber/plot.

## Data collection and instrumentation
- Emissions monitoring: automated greenhouse gas monitoring system (Queensland University of Technology) paired with a SRI 8610 GC (Torrance, USA).
- Measurement cadence: eight CH4 flux measurements per chamber per day.
  - 1 hour chamber closure period per measurement cycle.
  - 4 gas samples analysed per closure period.
  - Calibration standard analysed after every fourth gas sample.
- Chamber specs: basal area 0.25 m2; chamber dimensions 50 cm x 50 cm x 15 cm (l x w x h).
- Timeframe: emissions monitored for 80 days following treatment application.

## Data content and format
- Data type: high-frequency flux data (not raw gas concentration data); quality-assessed emissions included.
- Headers and columns:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment application
  - Columns B to M: CH4 fluxes (µg CH4-C m-2 h-1)
- Column labeling: 
  - Control = Control treatment
  - ArtUrine = artificial urine treatment
  - Urine = real urine treatment
  - Chamber/plot numbers encoded in headers

## Quality assurance and data quality
- QA procedures: inspect raw data files and GC chromatograms for anomalies; remove problematic data (e.g., interference in gas peaks) as needed.
- Data included represents validated flux measurements; not raw gas concentration data.

## Spatial and temporal coverage
- Temporal span: 80 days of post-treatment monitoring (treatment date: 24/07/2017).
- Spatial/experimental scope: measurements across multiple chambers/plots under three treatment conditions with triplicate patches per treatment.

## Usage notes and considerations
- Data are presented as CH4 fluxes (µg CH4-C m-2 h-1); units and time-relative to treatment are provided for analysis of treatment effects and temporal dynamics.
- Notable considerations include patch-level data within a randomized block design and the exclusion of sheep prior to treatment to avoid confounding emissions.

## Attribution and authorship
- Authors must be acknowledged if data are reused or reproduced.