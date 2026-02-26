# Eco-physiological data collected at Alice Holt Forest from July 2023

- Scope: Dataset on photosynthesis and gas exchange collected during a field campaign at Alice Holt Forest (July 18–20, 2023), focusing on leaf-level physiology across the site.
- Purpose for analysts: Provides leaf-level physiological measures suitable for exploring correlations, creating predictive links between environmental conditions and gas exchange, and supporting model development.

## Location, design, and sampling

- Site and design: Alice Holt Forest; a tower with six platforms (P) at two-meter intervals, positioned between two oak trees (T) with overhanging branches (B) and leaf clusters (C). Hazel understory sampled similarly.
- Taxa and scope: Measurements from oaks (Oak) and hazel understory (Haz/Haz).
- Sampling cadence: Daytime measurements only; not all branches/leaf-clusters were measured due to wind removing some branches after labeling.
- Instruments: Handy PEA+ for photosynthesis and LI-COR 6400 for gas exchange.

## Files, naming, and data structure

- File format: All data provided as CSV (.csv).
- Photosynthesis data: Single CSV file containing photosynthetic parameters.
- Gas exchange data: Multiple CSV files named using the convention 2023_07_DD_XXX_PX_BX_CX.csv, where:
  - PX indicates the tree (Oak or Haz) and
  - B and C indicate branch and leaf-cluster identifiers.
- Observations and labeling: Each observation is tagged with codes (e.g., Oak_P2_B1_C1) indicating platform, tree, branch, and leaf cluster.
- Metadata fields: Includes time stamps, sample IDs, and detailed instrument readings.

## Measurements and key variables

- Photosynthetic parameters (per leaf cluster):
  - F0, Fm, Fv_Fm: fluorescence-related metrics.
  - P_Index: vitality indicator.
  - Tfm: time to maximum fluorescence.
  - Intensity, P, T, B, C: contextual identifiers (tower platform, tree, branch, leaf cluster).
- Gas exchange parameters (per measurement):
  - Photo: Photosynthetic rate (μmol CO2 m^-2 s^-1)
  - Cond: Conductance to water vapor (mol H2O m^-2 s^-1)
  - Ci: Intercellular CO2 concentration (μmol CO2 mol^-1)
  - Trmmol: Transpiration rate (mmol H2O m^-2 s^-1)
  - VpdL: Leaf-area-based vapor pressure deficit (kPa)
  - Area: In-chamber leaf area (cm^2)
  - StmRat: Stomatal ratio estimate
  - BLCond: Boundary-layer conductance (mol m^-2 s^-1)
  - Tair, Tleaf, TBlk: Temperatures (C)
  - CO2R, CO2S: Reference and sample CO2 (μmol CO2 mol^-1)
  - H20R, H20S: Reference and sample H2O (mmol H2O mol^-1)
  - RH_R, RH_S: Relative humidity (%
  - Flow: Flow rate to the sample cell (μmol s^-1)
  - PARi, PARo: In-chamber and external light (μmol m^-2 s^-1)
  - Press: Atmospheric pressure (kPa)
  - CsMch: Sample CO2 offset (μmol mol^-1)
  - StableF, Status: Stability indicator and status string
- Measurement timing and type:
  - HHMMSS, FTime: Real-time clock and time since logging started
  - Measurement types include A/Ci (assimilation vs. intercellular CO2) and LRC (likely light response curves)
  - Details log provides start times and observation codes for each measurement event

## Data quality and limitations

- Quality control: Not all branches or leaf clusters were measured; some branches were removed by wind between labeling and measurement.
- Coverage: Data represent daytime measurements and may not capture nocturnal patterns or full canopy variation.
- Data provenance: Each gas exchange and fluorescence observation is linked to precise platform/tree/branch/leaf-cluster identifiers and time stamps, enabling traceability and reproducibility.

## Potential analyses and uses

- Correlation analyses between photosynthetic parameters (e.g., Fv/Fm, P_Index) and gas exchange metrics (e.g., Photo, Ci, Trmmol).
- Investigation of environmental drivers: assess relationships between Tair, Tleaf, RH, VpdL, PAR, and gas exchange/fluorescence responses.
- Hierarchical comparisons: platform (P) effects, tree identity (Oak vs Haz), branch (B), and leaf cluster (C) influences on physiological measurements.
- Model development: leaf-level photosynthesis models under field conditions using A/Ci data and environmental covariates, with potential predictions of gas exchange under varying conditions.

## Data access and reuse considerations

- Data are provided as CSV files with standardized naming to support programmatic access and automated analyses.
- Metadata and identifiers (P, T, B, C) enable stratified analyses by spatial context within the forest site.
- Users should account for incomplete measurements due to wind and selective sampling when designing analyses or interpreting results.