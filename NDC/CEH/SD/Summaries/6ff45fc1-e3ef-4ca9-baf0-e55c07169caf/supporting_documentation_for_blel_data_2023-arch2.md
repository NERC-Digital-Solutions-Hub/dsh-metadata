# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2023. Feuchtmayr, H., Dodd, B.A., Guyatt, H., Hunt, A.G., Le Quesne, K., McShane, G., Moorhouse, H., Rankin, G., Rhodes, G., Thackeray, S.J. (2025)

## Scope and purpose
- Long-term, fortnightly monitoring dataset from Blelham Tarn, Cumbria, England.
- Covers surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, nutrients (NH4N, TON, PO4P, TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA) for 2023 (Jan–Dec).
- Aimed at providing standardized environmental health indicators and enabling trend analysis over time.

## What is included
- Variables and units:
  - TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 L−1), pH, NH4N (µg N L−1), TON (µg N L−1), PO4P (µg P L−1), TOTP (µg P L−1), SIO2 (µg L−1), TOCA (µg L−1).
- Sampling regime:
  - Water samples integrated from 0 to 5 m; collected from the deepest lake location (buoy). If buoy access failed, shore samples were taken (Flag 2).
- Timeframe:
  - January 2023 to end of 2023; dataset is part of an ongoing long-term monitoring program.

## Data and quality control
- Data status:
  - Raw data presented; not yet quality controlled or calibrated.
- Verification and QA:
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA double-entered and validated by a database manager.
  - Visual checks of line graphs performed; missing data attributable to weather, equipment issues, or staff shortages.
- Structure and flags:
  - Data delivered as CSV with columns: sdate, Description (variable), value, sign(if<LOD), flag.
  - sign indicates below-detection-limit (<); flag indicates sampling location (1 = buoy, 2 = shore).

## Methods (analytical approaches)
- Instrumentation:
  - Temperature and dissolved oxygen: YSI ProODO; DO% calibration daily; biweekly and bimonthly calibrations.
  - Secchi depth: Secchi disk with measured rope.
- Chemical analyses:
  - Alkalinity and pH: integrated water sample sealed; Gran titration with Radiometer electrode; calibration before sampling.
  - NH4N and TON: SEAL AQ2 colorimetric analyzer after filtration; detailed reagent chemistry and calibration; UKAS accredited methods.
  - Total Phosphorus (TP): persulfate digestion with molybdenum blue colorimetry; absorbance at 880 nm; calibration and QC samples.
  - Dissolved reactive silicon (SIO2): silicomolybdenum blue colorimetry; absorbance at 880 nm; QC samples included.
  - Phytoplankton chlorophyll a (TOCA): methanol extraction after filtration; spectrophotometric analysis.
- Quality controls:
  - Calibration ranges and internal QA/QC checks (duplicates, standards, reference materials) described for each method; methods reference established protocols.

## Data use and accessibility
- Outputs and monitoring use:
  - Designed to demonstrate environmental condition and support interpretation of ecological health and policy performance over time.
- Data management considerations for analysts:
  - Raw data require quality control and calibration before final use.
  - Potential to couple with other datasets to enhance value and enable broader analyses.

## Limitations and considerations
- Current dataset is raw with ongoing quality control; results should be interpreted with awareness of potential calibration and detection-limit considerations.
- Occasional sampling from shore when buoy access was not possible; metadata flags clarify sampling context.

## Funding and references
- Data collection supported by Natural Environment Research Council (award NE/R016429/1) as part of UK-SCaPE National Capability; data validation supported via UKCEH National Capability NE/Y006208/1.
- References include standard methods for water analysis (Mackereth et al., Mortimer, Talling) cited for method protocols.