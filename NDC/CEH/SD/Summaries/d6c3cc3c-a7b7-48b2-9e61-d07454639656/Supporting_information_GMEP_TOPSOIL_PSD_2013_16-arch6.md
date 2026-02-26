# GMEP Topsoil PSD 2013-16

## Purpose and context
- Documents the Glastir Monitoring and Evaluation Programme (GMEP) soil particle size distribution (PSD) analysis using laser diffraction.
- Aims to provide evidence on soil quality trends related to climate, pollution, land use, and Glastir interventions; supports integration with wider Welsh environmental monitoring and future analyses with GB surveys.

## Survey design and sampling
- 4-year rolling survey cycle from 2013 to 2016 to maximise site coverage while detecting spatial and temporal changes cost-effectively.
- Two components: Wider Wales (baseline estimation, national trends) and Targeted (Glastir priority areas); both use a common 1 km square spatial unit.
- 300 x 1 km squares sampled over the cycle; half are random (Wider Wales) within Land Classification strata; half are targeted to Glastir priority areas.
- Exclusions: squares with >75% urban land or >90% sea.
- Sampling within each square: five predetermined, randomly dispersed locations; soil cores collected and lab-submitted for PSD analysis.

## Methods and laboratory workflow
- PSD measured with a Beckman Coulter LS13 320 laser diffraction particle size analyser.
- Sample preparation: remove organic matter via peroxide digest; suspend in 5% Calgon solution; filtering to obtain the sand fraction (63 µm sieve) for weighting.
- Quality assurance and quality control (QA/QC):
  - Follow NERC Joint Codes of Practice; include standard soils (BS1, BS3) in each batch; instrument calibration and rinsing; duplicated samples (1 in 10) for reproducibility; cross-check sand fraction with sieve data.
  - All processing follows a documented lab QA workflow; observe that high organic matter can overestimate sand in LD measurements.
- Data validation and method comparison:
  - Compared laser diffraction (LD) results with hydrometer method (Gee and Or, 2002) using internal standards BS1 and BS3.
  - LD generally aligned with hydrometer for overall distributions but showed systematic differences in clay/silt regions; clay measurements by LD tended to be lower than sedimentation methods in some cases.
  - Adjustments explored: using a clay/silt cut-off around 8 µm (instead of 2 µm) to align more closely with sedimentation results (consistent with some literature).
  - LD demonstrated accuracy and reproducibility when tested with standards (e.g., Garnet and glass beads); LD was found to be reliable in the low particle size range.
- Data interpretation and final cut-offs:
  - Final LD-based PSD size class cut-offs established as:
    - Sand: 64.61 – 2000 µm
    - Silt: 2.42 – 63.41 µm
    - Clay: 0.04 – 2.41 µm
  - These thresholds are used to categorize particle size fractions for analysis and reporting.

## Data quality, comparability, and external benchmarking
- Inter-laboratory comparisons:
  - LD results for sandy, silty, and clay soils from Bangor compared with ADAS and BGS; results demonstrated consistency and reproducibility across laboratories.
- Cross-method considerations:
  - LD typically provides accurate low-range measurements; hydrometer method may overestimate clay due to sedimentation-related factors (e.g., Brownian motion effects on suspension). This justified LD-based cut-offs and comparison interpretations.
- Accuracy validations:
  - Reproducibility tests showed LD measurements stable across standard materials; regular calibration and internal standards supported data quality.

## Data structure and metadata
- Metadata file: GMEP_TOPSOIL_PSD_2013_16.csv
- Sample-level fields (examples):
  - SQ_ID: Unique anonymised 1 km square identifier
  - PLOT_TYPE, PLOTNUM, PLOTYEAR: sampling plot type, plot number, sampling year
  - EASTING_10km, NORTHING_10km: 10 km resolution coordinates (metres)
  - LC: Land Classification code
  - REPEATED: indicator for repeated measurements
  - BATCH: batch number within a year
  - um0.03999, …, um2000: PSD fraction percentages by size bin
  - SAND, SILT, CLAY: percentage fractions for each size class
  - TOTAL: QA total (sum of fractions)
- Purpose of metadata: to enable robust, traceable analyses and integration with other GMEP data, and to support data sharing and re-use.

## Outputs and potential data products
- PSD distributions and summaries by 1 km square and sampling year for Wales under the GMEP framework.
- QA/QC metrics and inter-lab comparability results to accompany PSD data.
- A harmonised dataset enabling integration with other Welsh environmental monitoring and with the Countryside Survey of Great Britain for cross-survey analyses.

## References and key sources
- Methodological and sampling references for PSD and soil analysis (Gee & Or, 2002; Bouyoucos, 1928; Jennings et al., 1922; Konert & Vandenberghe, 1977; Lebron et al., 1993; Bitelli et al., 2019; Rawlins et al., 2009).
- Glastir Monitoring & Evaluation Programme reports and annual summaries (2014-2017) and Welsh Government contracts.
- Land Classification references (Bunce et al., 2007) and UK EIDC data standards.

## Personnel and affiliations
- UK CEH staff overseeing QA, soil processing, data management, and analysis (including Alison, Barrett, Burden, Emmett, Garbutt, Giampieri, Hall, Henrys, Hughes, Jarvis, Lebron, Nunez, Owen, Robinson, Seaton, Sharps, Williams, Wood).
- Bangor University staff and Field Survey Teams contributing to biodiversity leadership and field operations.
- Field survey teams comprising a large roster of researchers and technicians.