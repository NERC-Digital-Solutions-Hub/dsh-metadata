# General information: This dataset contains results from field measurements of riverine nitrogen transformations

## Overview
- Field study measuring riverine nitrogen transformations in the Hampshire Avon catchment.
- Permeable sediments (sand, greensand, chalk-dominated) assessed for nitrate reduction using 15N-tracer methods; clays assessed with intact-core incubations.
- Focus on in situ rates of denitrification and anammox, plus ambient N and O chemistry prior to tracer injection.
- Measurements conducted in August 2013.
- Includes pre-injection porewater data (nutrients, oxygen, pH, Fe(II)) and post-injection isotope analyses.
- Data structure allows construction of solute depth profiles and comparison across sediment types.

## Methods and procedures
- Permeable sediments (sands/chalks): push-pull sampling with 15N-labelled nitrate (300 μM, 98 at% 15N) in deoxygenated synthetic river water + KCl. 15N-nitrate injected into the riverbed; porewater samples collected over time.
- Clays: intact core incubations with 15N-nitrate added to overlying water; after incubation, cores homogenised to slurry and a sub-sample analysed for 15N-N2.
- Gas analysis: 15N-N2 measured by mass spectrometry; includes calculations to convert beam areas to concentrations.
- Background porewater sampling prior to injection: measure nutrients, oxygen, pH, reduced iron (Fe(II)).
- Filtration and preservation: nutrients and Fe(II) filtered; nutrient samples frozen; gas samples preserved with zinc chloride and stored in gas-tight vials.
- Analysis timeline: all analyses performed within 6 months of sampling.
- Quality controls: field and travel blanks for nutrient and Fe(II) analyses.

## Data structure and column headers
- Data are organized as a table with 13 columns and 67 rows (including headings); values below detection are marked as BDL; data not collected are marked as ND.
- Sample Label: unique identifier for each sample.
- Site identifier: rivers within the Hampshire Avon catchment; lithology codes indicate clay, sand, or chalk-dominated sub-catchments.
- Lithology and site details: Clay 1 (River Sem) and Clay 2 (tributary of River Sem); Sand 1 (River Nadder) and Sand 2 (west branch of River Avon); Chalk 1 (River Ebble) and Chalk 2 (River Wylye); with latitude/longitude coordinates provided.
- Depth: depth to the mid-point of the porewater probe in cm.
- Injection: 15N-nitrate injection concentration in μM.
- Fe(II): concentration of ferrous iron in porewater (μM); detection limit 1 μM; precision ±1%.
- O2: dissolved oxygen in porewater prior to injection (μM); measurement via microelectrode; detection limit 10 μM; precision ~2%; contamination correction applied.
- O2sat: oxygen saturation (%) relative to air-equilibrated water at sample temperature.
- Nitrate: porewater nitrate concentration prior to injection (μM); calculated from NOx and nitrite.
- Nitrite: porewater nitrite concentration prior to injection (μM).
- Ammonium: porewater ammonium concentration prior to injection (μM).
- SRP: soluble reactive phosphorus in porewater prior to injection (μM).
- pH: porewater pH prior to injection.
- D14: ambient denitrification rate in the riverbed (μmol 14N L−1 h−1) derived from 15N-labeling and isotope pairing data.
- A14: ambient anammox rate in the riverbed (μmol 14N L−1 h−1).
- ra: proportion of N2 production via anammox (%).
- p14: ambient production rate of 14N2 by processes other than 15N-nitrate reduction (μmol 14N L−1 h−1).
Notes:
- Some columns report derived isotopic metrics (D14, A14, ra, p14) based on isotope pairing and 15N labeling.
- Rates are calculated using established isotope-pairing methodologies and mass-spectrometry data.

## Key measurements and calculations
- D14: ambient denitrification rate calculated from production of 29N2 and 30N2 after 15N-nitrate addition; expressed in μmol 14N L−1 h−1.
- P29 and P30: production rates of 29N2 and 30N2 derived from mass-spectrometry data; limits of detection ~0.003 μmol 29N2 L−1 h−1 and ~0.009 μmol 30N2 L−1 h−1.
- p14: ambient production of 14N2 by processes not driven by the tracer, computed from measured N2 isotopologues.
- ra: fraction of N2 production attributed to anammox, calculated from 15N-labeling patterns in N2 and N2O pools.
- A14: ambient anammox rate, estimated as ra × p14.
- Data processing uses equations from Risgaard-Petersen et al. (2003) and Trimmer et al. (2006) with isotopic measurements (N2 and N2O) to partition nitrogen transformation pathways.
- Nutrient analyses: NOx and nitrite measured by automated colorimetry (Griess method); nitrate derived by subtracting nitrite from NOx; Fe(II) quantified via phenanthroline colorimetry; pH via calibrated probe.
- Oxygen measurements corrected for potential contamination; oxygen saturation calculated from temperature and solubility coefficients.

## Data quality, handling, and storage
- Field blanks and travel blanks collected for nutrient and Fe(II) analyses as part of QA.
- All analyses performed within 6 months of sampling to ensure sample integrity.
- Data flags indicate non-detects (BDL) or not-collected data (ND).
- Measurements and calculations rely on standard, well-documented laboratory methods and calibration materials, with accuracy checks against standard reference materials.

## Site locations and lithologies
- Clay sites: Clay 1 (River Sem; 51.045826°, -2.1104425°) and Clay 2 (tributary of River Sem; 51.055413°, -2.1568407°).
- Sand sites: Sand 1 (River Nadder; 51.043849°, -2.1118158°) and Sand 2 (west branch of River Avon; 51.318289°, -1.8600020°).
- Chalk sites: Chalk 1 (River Ebble; 51.027499°, -1.9217089°) and Chalk 2 (River Wylye; 51.142475°, -2.2033140°).

## References and methodological grounding
- Lansdown et al. 2014: Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed.
- Nielsen 1992; Trimmer et al. 2006: Isotope pairing techniques for denitrification/anammox in sediments.
- Risgaard-Petersen et al. 2003: Isotope pairing technique in sediments with coexisting anammox and denitrification.
- Thamdrup & Dalsgaard 2000; Measured mass-spectrometry procedures for N2 isotopologues.

## Potential uses and relevance for environmental monitoring
- Enables cross-site comparisons of denitrification and anammox in different riverbed lithologies under standardised isotope-based methods.
- Provides QA-focused data (background porewater chemistry, detection limits, blanks) suitable for dataset integration into environmental health dashboards and policy performance assessments.
- Supports data fusion with other environmental datasets to enhance understanding of nitrogen cycling in fluvial systems.
- Useful for trend analyses and monitoring program evaluations aimed at reducing nitrate loads and improving riverine water quality.