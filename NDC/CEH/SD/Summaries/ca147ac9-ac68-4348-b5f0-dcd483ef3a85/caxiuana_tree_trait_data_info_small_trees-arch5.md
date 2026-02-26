# Supporting information for Traits data from juvenile trees exposed to a 50% reducing in canopy throughfall at the Caxiuanã drought experiment, Brazil, August to September 2017

## Overview
- Data originate from the Caxiuanã through-fall exclusion (TFE) experiment in eastern Amazonia (1°43' S, 51°27' W).
- Experimental design includes two 1-hectare plots: a drought (TFE) plot that excludes 50% canopy through-fall since 2002, and a corresponding 1-hectare control plot without drought structure.
- Sampling occurred in September–October 2017 (peak dry season).

## Study design and sampling
- 76 trees were sampled across both plots: 43 on the control plot and 33 on the TFE plot.
- Trees represented a range of size classes (1 cm to 10 cm DBH).
- Sampling occurred on the most common genera present, across the plots.

## Traits measured (17 traits)
- Plot/Description: Control or Drought plot; Species
- DBH: Diameter at breast height (cm)
- Vcmax: Maximum carboxylation capacity (μmol CO2 m−2 s−1)
- Jmax: Maximum electron transport capacity (μmol CO2 m−2 s−1)
- Rleaf: Leaf respiration in the dark (μmol CO2 m−2 s−1)
- Min gs: Minimum stomatal conductance (mmol CO2 m−2 s−1)
- LMA: Leaf mass per area (g m−2)
- Nleaf: Leaf nitrogen content (g g−1)
- Pleaf: Leaf phosphorus content (g g−1)
- Thickness: Leaf thickness (mm)
- ρ: Branch wood density (g cm−3)
- Ψpd: Pre-dawn leaf water potential (MPa)
- Ψmd: Midday leaf water potential (MPa)
- P50: Xylem pressure for 50% loss of conductance (MPa)
- P88: Xylem pressure for 88% loss of conductance (MPa)
- Ksmax: Maximum lumen conductance (mol H2O m−1 MPa−1 s−1 m−2)
- PLC: Percentage loss of conductivity
- LA:SA: Leaf area to sapwood area ratio

## Data collection workflow and measurements
- Branch 1 (0430–0630): Ψpd measured; branches sealed and rehydrated for 24 hours; P50 determined using the pneumatic method (Pereira et al. 2016) by progressively drying the sample while recording air discharge and leaf Ψ.
- Branch 2 (1000–1200): Leaves used for A–Ci curve measurements with Li-Ci 6400 (to derive Vcmax and Jmax); Rleaf, Min gs, and Max gs also measured; leaves dried subsequently for Pleaf, Nleaf, and LMA measurements.
- Branch 3 (1300–1400): Ψmd measured on three leaves; then branch sealed to measure PLC and Ksmax (following Pereira & Mazzafera 2012); ρ measured on a 1 cm diameter section; LA:SA calculated by scanning all leaves on the branch and quantifying leaf area with ImageJ (v1.6.0_20).
- Data were quality controlled by excluding values where curve fits failed (for P50, P88, Ksmax, PLC, Vcmax, Jmax); such values are recorded as NA. NA also used for data lost or damaged during collection/measurement.
- Remaining data were validated to fall within ranges reported in related studies (Bartholomew et al. 2020; Giles et al. 2022).

## Data structure and metadata
- The dataset includes per-tree and per-branch measurements across the two plots, with a table of 17 measured traits (Table 1 described in the document).
- Data columns include plot designation, species, DBH, and all trait measurements with units as specified above.
- Supporting data quality and methodology references are provided for replication and validation.

## Data quality, provenance, and limitations
- QC rules: remove data that could not be fit to models/lines or did not conform to expected equations; missing values denoted as NA.
- Validation: remaining data checked against published ranges for these variables.
- Limitations: some measurements were missing due to sample loss or damage; potential variability in measurements across branches and time of day is mitigated by standardized sampling windows and protocols.

## References and methodology
- Bartholomew, D. C. et al. 2020. Small tropical forest trees and drought response (Plant Cell Environ.).
- Giles, A. L. et al. 2022. Understorey vs canopy hydraulic traits (Tree Physiol.).
- Pereira, L. et al. 2016. Plant pneumatics: stem air flow (New Phytol).
- Pereira, L. & Mazzafera, P. 2012. Low-cost xylem conductance measurement (Bragantia).
- Schneider, C. A. et al. 2012. ImageJ image analysis (Nat Methods).