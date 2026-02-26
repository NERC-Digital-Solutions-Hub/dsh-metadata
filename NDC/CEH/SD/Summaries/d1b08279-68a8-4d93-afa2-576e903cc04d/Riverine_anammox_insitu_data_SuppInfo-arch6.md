# General information: This dataset contains results from field measurements of riverine nitrogen transformations.

## Overview
- Contains field measurements of riverine nitrogen transformations in the Hampshire Avon catchment, using 15N-nitrate tracer to quantify denitrification and related processes in different sediment types (Clay, Sand, Chalk).
- Methods include push-pull sampling with bespoke probes in permeable sediments and intact core experiments for clays; 15N-nitrate is tracked via mass spectrometry to determine production of N2 isotopologues (29N2, 30N2) and ambient processes (p14).
- Field campaign conducted in August 2013.
- Data are organized as a 13-column by 67-row table, with values marked as BDL (below detection limit) or ND (not collected).
- Sites cover six locations with precise coordinates and sediment types:
  - Clay 1 (River Sem) and Clay 2 (tributary of River Sem)
  - Sand 1 (River Nadder) and Sand 2 (west branch of River Avon)
  - Chalk 1 (River Ebble) and Chalk 2 (River Wylye)

## Data structure and key columns
- Data table: 13 columns, 67 rows (including headers).
- Primary headers and data types include:
  - Sample Label
  - Site identifier (Clay, Sand, Chalk categories; specific site names)
  - Depth (cm) – screen mid-point below riverbed
  - Injection (μM)
  - O2 (μM) – dissolved oxygen prior to 15N injection
  - O2sat (%) – saturation relative to air-equilibrated water
  - Nitrate (μM) – porewater nitrate prior to injection
  - Nitrite (μM) – porewater nitrite prior to injection
  - Ammonium (μM) – porewater ammonium prior to injection
  - SRP (μM) – soluble reactive phosphorus
  - Fe(II) (μM) – measured in porewater prior to injection
  - pH – porewater pH prior to injection
  - D14 – ambient denitrification rate (μmol N L−1 h−1)
  - A14 – ambient anammox rate (μmol N L−1 h−1) or related metric
  - ra – proportion of N2 production via anammox (percent)
- Additional column details describe site coordinates and how Clay/Sand/Chalk demarcations map to specific rivers.

## Measurements and processing
- Nitrate and nitrite measured via automated colorimetry; NOx calculated as NOx = nitrate + nitrite.
- NOx reduced to nitrite for nitrate determination using an inline cadmium column (for NOx analysis).
- O2 measured with a fast-response microelectrode; contamination corrections applied (estimated 10 μM subtracted).
- Fe(II) measured after preservation with phenanthroline; detection limit ~1 μM; precision ~1%.
- pH measured after O2 determination.
- D14, P29, P30, p14, A14, ra calculated from 15N tracer experiments and mass-spectrometry data:
  - P29 and P30 derived from linear trends of aN2 (mass spectrometry signal for 29N2 and 30N2) over time.
  - p14 calculated from ambient processes excluding tracer-affected N2 production.
  - D14 reflects ambient denitrification after accounting for tracer contributions.
  - ra determines the fraction of N2 production via anammox using 15N enrichment in N2 and N2O pools.
- Isotope pairing technique references:
  - Measures follow Nielsen (1992); Risgaard-Petersen et al. (2003); Trimmer et al. (2006); Lansdown et al. (2014); Thamdrup & Dalsgaard (2000).

## Context, quality, and limitations
- Temporal scope: data from a single field campaign (August 2013).
- Spatial scope: six sites across three sediment types within the Hampshire Avon catchment.
- Data quality indicators:
  - Some fields marked ND (not collected) or BDL (below detection limit).
  - O2 measurements include a contamination correction estimate.
  - All analyses conducted within 6 months of sampling.
- Rate measurements were not performed in shallow sediments where tracer plumes would extend above the riverbed surface.

## Potential data products for Data Support
- Self-serve dashboards by site type (Clay, Sand, Chalk) and site coordinates for quick comparison.
- Derived metrics explorer to compare D14, A14, and ra across sites and depths.
- Spatial visualization of sampling locations with associated porewater chemistry and denitrification/anammox rates.
- Data quality filters to flag BDL/ND values and highlight measurements with higher uncertainty.

## References
- Lansdown, K. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. 2014.
- Nielsen, L. P. Denitrification in sediment determined from nitrogen isotope pairing. FEMS Microbiol. Ecol. 1992.
- Risgaard-Petersen, N. et al. Application of the isotope pairing technique in sediments where anammox and denitrification coexist. Limnol. Oceanogr. Methods 2003.
- Thamdrup, B. & Dalsgaard, T. The fate of ammonium in anoxic manganese oxide-rich marine sediment. Geochim. Cosmochim. Acta 2000.
- Trimmer, M. et al. Direct measurement of anaerobic ammonium oxidation (anammox) and denitrification in intact sediment cores. MEPS 2006.