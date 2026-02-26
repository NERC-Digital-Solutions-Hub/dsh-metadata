# Dataset: Field measurements of riverine nitrogen transformations using 15N-nitrate (August 2013)

## Overview
- Field dataset of nitrate transformation measurements in riverbeds, comparing permeable sediments (sand, greensand, chalk) and clays.
- Uses 15N-labelled nitrate injected into the riverbed and porewater samples analyzed for 15N-N2 production via mass spectrometry to quantify denitrification and related processes.
- Background porewater measurements include nutrients, oxygen, pH, and reduced iron prior to injection.
- Samples collected in August 2013; analyses conducted within 6 months of sampling.
- Data are organized as a 13-column by 67-row table, with markers for below detection limits (BDL) and not-detected (ND). Some samples are shallow and rate measurements are not reported there due to tracer plume constraints.

## Data structure and columns
- Sample Label
- Site identifier (locations in the Hampshire Avon catchment; site types: Clay, Sand, Chalk)
- Depth (cm) - screen mid-point below the riverbed
- injection (microM) - concentration of injected 15N-nitrate
- O2 (microM) - porewater dissolved oxygen prior to injection
- O2sat (%) - oxygen saturation relative to air-equilibrated water
- Nitrate (microM) - porewater nitrate prior to injection
- Nitrite (microM) - porewater nitrite prior to injection
- Ammonium (microM) - porewater ammonium prior to injection
- SRP (microM) - soluble reactive phosphorus prior to injection
- pH - porewater pH prior to injection
- D14 - ambient denitrification rate (micromol N per L porewater per h)
- Additional derived rates and isotopic metrics (see methods)

Site keys and coordinates illustrate six sites across Clay 1/2, Sand 1/2, Chalk 1/2 with explicit latitude/longitude for each.

## Methods and QA/QC
- Nitrate tracing: 15N-labeled nitrate (300 µM, 98 atom% 15N) injected into the riverbed; 15N-N2 production tracked over time.
- Sample preservation and handling:
  - Porewater filtered to remove ambient O2; preserved for Fe(II) determination by complexation with phenanthroline.
  - Gas samples preserved with zinc chloride and stored in gas-tight vials inverted to maintain integrity.
  - All analyses performed within 6 months of sampling.
- Measurements:
  - Fe(II): absorbance at 520 nm after filtration; LOD ~1 µM; precision ~1%.
  - O2: measured with microelectrode; calibration with zero solution and known O2 solutions; potential contamination estimated (~10 µM) and subtracted.
  - O2sat: calculated from O2 and temperature using solubility coefficients.
  - Nutrients (Nitrate, Nitrite, Ammonium, SRP): automated colorimetry (Griess method for NOx/Nitrite; indophenol blue for NH4+; Mo blue for SRP); LODs and precisions specified per analyte.
  - pH: measured after O2 assessment.
- Isotopic calculations:
  - 29N2 and 30N2 production derived from mass spectrometry data; background and post-injection samples used with calibration factors.
  - p14, D14, A14, ra computations follow referenced isotope pairing technique methods; ra uses 15N-labeling of N2 and N2O pools.
- Documentation and metadata:
  - Field and travel blanks collected for nutrient and Fe(II) analyses.
  - Clear provenance through cited literature to enable reproducibility of calculations.

## Key variables and units
- Depth: cm
- Injection: µM (15N-labelled nitrate)
- O2: µM
- O2sat: %
- Nitrate, Nitrite, Ammonium, SRP: µM
- pH: unitless (pH)
- D14, A14, P29, P30, p14: µM N per L porewater per h
- ra: % (proportion of N2 production via anammox)

## Data processing and calculations
- N2 production rates (P29, P30) derived from linear trends of aN2 versus time using MS beam areas.
- p14 calculated from ambient processes using established isotope equations.
- D14 and A14 allocated to denitrification and anammox contributions, respectively, based on ra and p14.
- ra derived from 15N-labeling in N2 vs N2O pools.

## Data quality, limitations, and notes
- Data marked as BDL (below detection limit) or ND (not collected) where applicable.
- Rate measurements are not reported for shallow sediments where tracer plumes would spread above the riverbed surface.
- O2 contamination during transfer estimated and corrected; calibration and QA procedures described.
- Data are tightly tied to the original references for methodological details and calculations.

## References
- Lansdown, K. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. 2014.
- Nielsen, L. P. Denitrification in sediment determined from nitrogen isotope pairing. FEMS Microbiol. Ecol. 1992.
- Risgaard-Petersen, N. et al. Application of the isotope pairing technique in sediments where anammox and denitrification coexist. Limnol. Oceanogr. Methods 2003.
- Thamdrup, B. & Dalsgaard, T. The fate of ammonium in anoxic manganese oxide-rich marine sediment. Geochim. Cosmochim. Acta 2000.
- Trimmer, M. et al. Direct measurement of anaerobic ammonium oxidation (anammox) and denitrification in intact sediment cores. MEPS 2006.