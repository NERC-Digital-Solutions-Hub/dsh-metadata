# ReadMe file for AutumnCH4Flux.csv

## Purpose and scope
- Provides CH4 flux measurements from soil under three treatments (control, artificial sheep urine, nitrate + glucose) in a grazing land site.
- Data are quality-assessed flux values (not raw gas concentrations) collected to study treatment effects on CH4 emissions.

## Study context, location, and environmental details
- Location: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level; coordinates: 53°22'N, 3°95'W.
- Site description: humic gleysol soil type.

## Treatments and experimental design
- Treatments (n = 4): 
  - Control: no urine application
  - Artificial sheep urine: applied in triplicate discrete patches inside the chamber
  - C and N: nitrate + glucose treatment
- Application details:
  - ArtUrine: 200 ml per patch over 100 cm² (N 1120 kg N ha⁻¹ per patch)
  - CandN: 1 L of nitrate + glucose solution over a 40 × 40 cm square
- Treatment application date: 25/10/17
- Experimental design: randomized block design with multiple plots/chambers

## Measurements and data collection system
- Monitoring period: 45 days post-treatment
- Gas measurement system: automated greenhouse gas monitoring system (QUT, Queensland University of Technology) using a SRI 8610 GC (Torrance, USA)
- Frequency: eight CH4 flux measurements per chamber per day
  - 1 hour chamber closure per measurement
  - Four gas samples analyzed per closure
  - Calibration standard analyzed after every fourth sample
- Chamber specifications:
  - Basal area: 0.25 m²
  - Chamber dimensions: 50 cm × 50 cm × 15 cm (L × W × H)

## Data content and structure
- Data scope: CH4 flux emissions from the experimental period analyzed by the automated system (high-frequency data)
- Data type: quality-assessed CH4 flux data (µg CH4-C m⁻² h⁻¹), not raw gas concentration data
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment application
  - Columns B–M: CH4 flux values (µg CH4-C m⁻² h⁻¹)
  - Column headers indicate treatment and chamber/plot numbers
  - Treatments encoded as: Control, ArtUrine, CandN

## Data quality, curation, and limitations
- Quality assurance: inspection of raw data files and GC chromatograms for anomalies; data with issues (e.g., peak interference) were removed
- Documented QA procedures support reliability of the published flux values
- Note: Data represent processed, quality-assessed flux values, not raw concentration data

## Attribution and usage notes
- Authors must be acknowledged if data are reused or reproduced
- Metadata and data structure provided to facilitate discoverability and reuse by data users and systems

## Governance and stewardship considerations
- Clear documentation of treatments, timing, and measurement protocol supports traceability and reproducibility
- Data are suitable for integration into datasets requiring standardized CH4 flux measurements across treatments and time
- Suitable for researchers and data stewards managing large, multi-treatment, high-frequency environmental datasets