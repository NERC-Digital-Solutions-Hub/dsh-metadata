# This dataset contains results from field measurements of riverine nitrogen transformations.

## Overview
- Field dataset of nitrate production and consumption in riverbed porewaters, using 15N-tracer push-pull and intact core methods.
- Measurements conducted in August 2013 across permeable riverbed sediments (sand, greensand/clay, chalk) in the Hampshire Avon catchment.
- Data capture ambient porewater chemistry (O2, pH, NOx/Nitrite, Ammonium, SRP, FeII) before 15N-injection and isotope-based rate calculations after injection.
- Includes derived rates for denitrification, anammox, and their respective contributions to N2 production.

## Spatial and temporal scope
- Location: Rivers within the Hampshire Avon catchment, with six site types representing substrate-dominated sub-catchments:
  - Clay 1 (River Sem), Clay 2 (tributary of River Sem)
  - Sand 1 (River Nadder), Sand 2 (west branch of River Avon)
  - Chalk 1 (River Ebble), Chalk 2 (River Wylye)
- Site coordinates are provided for each site (latitude and longitude).
- Temporal context: Sampling and analyses performed in August 2013.

## Data structure and columns
- Data organized as a table with 13 columns and 67 rows (including headers).
- Key column headers (selected):
  - Sample Label
  - Site identifier (Clay, Sand, Chalk sub-sites; specific site names)
  - Depth (cm): screen mid-point depth below riverbed
  - injection (µM): concentration of 15N-nitrate injected
  - O2 (µM): dissolved oxygen in porewater prior to injection
  - O2sat (%): oxygen saturation relative to air-equilibrated water
  - Nitrate (µM): pre-injection nitrate
  - Nitrite (µM)
  - Ammonium (µM)
  - SRP (µM): soluble reactive phosphorus
  - pH: porewater pH prior to injection
  - D14: ambient denitrification rate (µmol N L-1 h-1)
  - 14N2, 29N2, 30N2 production rates and related calculations (from isotope pairing)
  - p14: ambient production of 14N2 (not related to 15N-tracer reduction)
  - A14: ambient anammox rate (µmol N L-1 h-1)
  - ra: proportion of N2 production via anammox (percent)
- Data quality flags:
  - BDL = below detection limit
  - ND = not collected
- Pre-injection measurements and sample handling details included (filtering, preservation, storage, and blanks).

## Methods and measurements
- Permeable sediments: nitrate reduction measured via push-pull sampling with 15N-labelled nitrate (300 µM, 98 atom % 15N) in deoxygenated river water with KCl; porewater samples collected over time.
- Clays: intact cores with 15N-nitrate added to overlying water; cores homogenised post-incubation for 15N-N2 analysis.
- Porewater chemistry:
  - Fe(II) measured after preserving porewater with phenanthroline; detection limit ~1 µM; precision ~1%.
  - O2 measured with a fast-response microelectrode; calibration against zero and known O2 solutions; typical contamination correction ~10 µM.
  - Nitrate/Nitrite measured via automated colorimetry (Griess method); NOx reduced online for nitrate; LOD ~0.4 µM (nitrate) and ~0.1 µM (nitrite); precision ~1%.
  - Ammonium measured via indophenol blue method; LOD ~0.8 µM; precision ~3%.
  - SRP measured via molybdenum blue method; LOD ~0.1 µM; precision ~1%.
- Isotope-based calculations:
  - N2 isotopologues (29N2, 30N2) quantified by mass spectrometry to determine rates of denitrification and anammox.
  - p14, D14, A14, ra computed using isotope ratios and standard equations from the referenced literature (Risgaard-Petersen et al., Trimmer et al., Nielsen et al., Lansdown et al., Thamdrup & Dalsgaard).
- Quality and processing notes:
  - Analyses completed within 6 months of sampling.
  - Field blanks and travel blanks collected for nutrient and Fe(II) analyses.
  - Depths reflect measurements at different porewater screen depths.

## Data quality, limitations, and considerations for GIS work
- Spatially explicit but limited to six site types within a single catchment; coordinates provided enable mapping and spatial joins.
- Data quality flags (BDL, ND) indicate missing or below-detection data, which should be treated accordingly in analyses and visualisations.
- Detection limits and measurement precisions provided for key solutes and Fe(II) help in assessing data certainty in maps and models.
- Temporal snapshot from August 2013; may not reflect seasonal variability; suitable for comparative spatial analysis or baseline mapping.
- Calculated rate metrics (D14, p14, A14, ra) derive from isotope data and require referencing the methodology papers when interpreting spatial patterns.
- Substrate type (Clay, Sand, Chalk) and coordinates enable map-based analyses of how substrate controls denitrification/anammox and nitrate dynamics.

## Potential GIS uses and data products
- Create site-based layers showing ambient rates (D14, ra, A14, p14) by substrate type with confidence indicators from detection limits.
- Map porewater chemistry surfaces by interpolating point data (Nitrate, Nitrite, Ammonium, SRP, FeII, O2) across sampling depths where appropriate.
- Depth profiles by site to visualize vertical gradients and relate them to denitrification/anammox activity.
- Link to literature-derived methods metadata for traceability and reproducibility in GIS-enabled dashboards or data portals.
- Provide a metadata-rich layer pack including site coordinates, substrate type, depth, measured values, and derived rate metrics for policy-relevant mapping and stakeholder communication.

## References
- Lansdown, K. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. 2014.
- Nielsen, L. P. Denitrification in sediment determined from nitrogen isotope pairing. FEMS Microbiol. Ecol. 1992.
- Risgaard-Petersen, N. et al. Application of the isotope pairing technique in sediments where anammox and denitrification coexist. Limnol. Oceanogr. Methods 2003.
- Thamdrup, B. & Dalsgaard, T. The fate of ammonium in anoxic manganese oxide-rich marine sediment. Geochim. Cosmochim. Acta 2000.
- Trimmer, M. et al. Direct measurement of anaerobic ammonium oxidation (anammox) and denitrification in intact sediment cores. MEPS 2006.