# General information: This dataset contains results from field measurements of riverine nitrogen transformations.

## Overview and scope
- Field measurements of riverine nitrogen transformations in permeable sediments (sands, chalks) and clays.
- Locations: Hampshire Avon catchment; sites represent clay, greensand (sand), and chalk-dominated sub-catchments.
- Purpose: quantify nitrate reduction and nitrogen cycling processes in riverbeds using isotope tracing.

## Data collection timeline
- Sampling and measurements conducted in August 2013.

## Methods and instrumentation
- Permeable sediments: push-pull sampling with bespoke stainless steel probes; injection of 15N-labelled nitrate (300 μM, 98 atom% 15N) in deoxygenated river water with KCl; porewater samples recovered over time.
- Clays: intact cores with 15N-nitrate added to overlying water; after incubation, cores homogenised and a slurry sub-sample retained for 15N-N2 analysis.
- Gas analysis: 15N-N2 measured by mass spectrometry with a helium headspace.
- Pre-injection porewater sampling: measured background nutrients, O2, pH, reduced iron (Fe(II)).
- Sample preservation and handling:
  - Nutrients and Fe(II) filtered through 0.45 μm filters; nutrients frozen until analysis.
  - Gas samples preserved with zinc chloride and stored in gas-tight vials inverted.
  - All analyses performed within 6 months of sampling.
- Blanks: field and travel blanks collected for nutrient and Fe(II) analyses.

## Dataset structure and data quality
- Data organized as a table with 13 columns and 67 rows (including headers).
- Data flags:
  - BDL indicates below detection limit.
  - ND indicates data not collected.
- Depths: porewater sampling depths referenced as screen mid-points below the riverbed (in cm).
- Shallow sediments: not used for rate measurements due to tracer plume reaching the surface.

## Site and sample metadata
- Site identifiers include:
  - Clay 1 (River Sem) and Clay 2 (tributary of River Sem)
  - Sand 1 (River Nadder) and Sand 2 (west branch of River Avon)
  - Chalk 1 (River Ebble) and Chalk 2 (River Wylye)
- Geographic coordinates provided for each site.
- Depths correspond to mid-point of the porewater probe’s screen.

## Key headers and measured parameters (highlights)
- Sample Label, Site, Depth (cm), injection (μM)
- O2 (μM), O2sat (%)
- Nitrate (μM), Nitrite (μM), Ammonium (μM)
- SRP (μM)
- pH
- D14: Rate of ambient denitrification (μmol N L−1 h−1)
- p14: Production of ambient 14N2 (μmol 14N L−1 h−1)
- A14: Ambient anammox rate (μmol 14N L−1 h−1)
- ra: Proportion of N2 production via anammox (%)
- 29N2 and 30N2 production calculations (mass spectrometry data) used to derive D14, p14, A14, ra

## Calculations and isotope analysis (conceptual)
- 15N-nitrate injection followed by production of 29N2 and 30N2 quantified via mass spectrometry.
- Isotope pairing technique used to separate denitrification from anammox contributions.
- Calculations reference established methods (e.g., Thamdrup & Dalsgaard; Risgaard-Petersen et al.; Trimmer et al.; Lansdown et al.).

## Data governance, provenance, and reuse considerations
- Detailed description of sample collection, preservation, and analysis methods supports reproducibility and auditability.
- Clear documentation of detection limits and data quality flags (BDL, ND) aids data interpretation and quality assessment.
- Metadata links to site coordinates and river subcatchments enable spatial analyses and data discovery across datasets.

## Limitations and considerations for users
- Some data are flagged as not detected (BDL) or not collected (ND).
- Rate measurements limited to certain sediment types; shallow sediments were not used for rate calculations due to tracer plume behavior.
- Data reflect a specific temporal window (August 2013) and may require provenance checks for longitudinal studies.

## References and methodological background
- Lansdown et al. (2014) on fine-scale riverbed nitrate production and consumption.
- Nielsen (1992); Risgaard-Petersen et al. (2003); Thamdrup & Dalsgaard (2000); Trimmer et al. (2006) for isotope pairing technique and related denitrification/anammox analyses.