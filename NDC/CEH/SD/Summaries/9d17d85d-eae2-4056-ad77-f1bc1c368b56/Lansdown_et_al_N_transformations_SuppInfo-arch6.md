# Overview of data

- This document describes a dataset from the in-stream N-cycling component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer. It comprises two accompanying data files and detailed methodology for in situ measurement of nitrogen transformations in rivers.
- Data files:
  - N transformations and porewater chemistry in permeable sediments
  - N transformations in clays
- Four field campaigns were conducted across Hampshire Avon catchment rivers with varying land-river connectivity, using push-pull sampling and intact-core methods to measure nitrogen transformations and porewater chemistry.

## Data files, structure and formats

- Permeable sediments (sands, chalk-gravels): 241 rows × 20 columns
- Clays: 153 rows × 7 columns
- Data quality indicators:
  - BDL = below detection limit
  - ND = data not available due to flow conditions
- Data are organized with a consistent column header set (see below) and include both measured values and laboratory-derived calculations.

## Sampling campaigns and sites

- Seasons and dates:
  - Spring 2013: 23/04 – 09/05/2013
  - Summer 2013: 31/07 – 16/08/2013
  - Autumn 2013: 29/10 – 11/11/2013
  - Winter 2014: 28/01 – 09/02/2014
  - Not all sites sampled in every season due to practical reasons (flooding, access, machinery).
- Site codes and locations:
  - CE1: River Ebble
  - CW2: River Wylye
  - GN1: River Nadder
  - GA2: River Avon
  - AS1/AS2: tributaries of River Sem
- Vegetation status:
  - Vegetated (Y) vs. un-vegetated (N) sediments; AS1/AS2 clays had no observed aquatic vegetation.

## Measured variables and data dictionary highlights

- Core fields (examples; permeable sediments and clays share a common structure where applicable):
  - RecordID: unique sample identifier
  - Season: campaign season (with date context)
  - SiteCode: site identifier (CE1, CW2, GN1, GA2, AS1, AS2)
  - Vegetated: Y/N
  - Depth: depth below riverbed mid-point of probe (cm)
  - A14: rate of in situ anammox (nmol N L−1 porewater h−1 for permeable sediments; μmol N m−2 h−1 for clays)
  - D14: rate of in situ denitrification (same units as A14)
  - ra: contribution of anammox to in situ N2 production (%)
  - Nit-15N: nitrification potential in permeable sediments (nmol 15N L−1 h−1) or ambient nitrification in clays (μmol m−2 h−1)
  - Nit-pn: ambient nitrification activity in clays (μmol m−2 h−1)
  - Ammonium: porewater NH4+ concentration (μM)
  - Chloride: porewater Cl− concentration (mg L−1)
  - Iron(II): Fe2+ concentration in porewater (μM)
  - Methane: dissolved methane concentration in porewater (μM)
  - Nitrate: nitrate concentration in porewater (μM)
  - Nitrite: nitrite concentration in porewater (μM)
  - N2O: nitrous oxide concentration in porewater (nM)
  - O2: dissolved oxygen in porewater (μM)
  - O2sat: O2 saturation relative to air-equilibrated water (%)
  - pH: porewater pH
  - SRP: soluble reactive phosphorus in porewater (μM)
- Units and measurement notes:
  - 15N-tracer experiments used 300 μM 98 atom% 15N-nitrate in a synthetic river water matrix with ~150 mg L−1 KCl; multiple time points within ~60 minutes.
  - N2 and N2O production quantified via mass spectrometry; N2 production corrected for chloride-driven advective flow; detection limits defined for 29N2, 30N2, and related species.
  - Nitrification in permeable sediments tracked by 15N-labelled products (NOx), later converted to N2 via nitrite, cadmium reduction, and sulphamic acid steps.
  - For clays, intact-core method (Trimmer et al. 2006) used; incubation up to 4 hours with varying 15N-nitrate labelling; core slurrified at end for analysis.
  - Analytical techniques include: automated colorimetry for ammonium and SRP; ion-selective electrode for chloride; phenanthroline assay for Fe(II); gas chromatography for CH4 and N2O; dissolved O2 measured with microelectrode; pH with calibrated probe.
  - Detection limits and precision values are specified for each parameter (e.g., NH4+ limit 0.6 μM, Fe(II) limit 1 μM, O2 limit 10 μM, etc.).

## Methods: data collection and calculations

- In permeable sediments:
  - Push-pull porewater sampling with probes at depths 3–20 cm; porewater collected for a suite of chemical measurements.
  - 15N-labelled nitrate injected into riverbed; production of 15N-N2, 15N-N2O, and 15NOx tracked to determine nitrification, denitrification, and anammox processes.
  - N2 production quantified from 29N2 and 30N2 in headspace after equilibration; corrections applied for chloride-driven advection.
  - p14, ra, A14, D14, p14, and Nit-pn derived using isotope pairing techniques and established equations (cited references included).
- In clays:
  - Push-pull rhizon sampling trialed but unsuccessful; intact-core method used instead with overlying water labelled with 15N-nitrate; short incubation (≤4 h); slurry analyzed for N2 production and related isotopic signatures.
  - Ambient nitrification (Nit-pn) calculated from p14 and pw.14 (derived from p15 and r14).
- Derived calculations:
  - ra (percent contribution of anammox to N2 production) calculated from 15N distribution in N2 and N2O pools.
  - p14 (production of ambient 14N-N2) calculated from r14 and P29/P30.
  - D14 and A14 derived from p14 and ra, representing denitrification and anammox contributions to ambient N2 production.
  - Nit-pn (ambient nitrification) computed as p14 minus pw.14.

## Data quality, limitations and availability

- Data include explicit notes on missing measurements due to environmental conditions (ND) and below-detection measurements (BDL).
- Methods and calculations are anchored by standard references (Nielsen 1992; Risgaard-Petersen et al. 2003; Trimmer et al. 2006; Lansdown et al. 2014, 2016; and related methodological papers).
- The dataset provides a rich, self-contained basis for evaluating in situ N-cycling processes in riverbed sediments, with explicit documentation of sampling campaigns, site characteristics, analytical procedures, and isotope-based calculations.

## References

- Lansdown, K., Heppell, C. M., Trimmer, M. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. 2014.
- Lansdown, K., McKew, B.A., Whitby, C., Heppell, C.M., Dumbrell, A.J., Binley, A., Olde, L., Trimmer, M. Importance and controls of anaerobic ammonium oxidation influenced by riverbed geology. Nature Geosci. (Advance online publication) 2016.
- Nielsen, L. P. Denitrification in sediment determined from nitrogen isotope pairing. FEMS Microbiol. Ecol. 1992.
- Smart, R. M., Barko, J. W. Laboratory culture of submersed freshwater macrophytes on natural sediments. Aquat. Bot. 1985.
- Risgaard-Petersen, N., Nielsen, L. P., Rysgaard, S., Dalsgaard, T., Meyer, R. L. Application of the isotope pairing technique in sediments where anammox and denitrification coexist. Limnol. Oceanogr. Methods 2003.
- Thamdrup, B., Dalsgaard, T. The fate of ammonium in anoxic manganese oxide-rich marine sediment. Geochim. Cosmochim. Acta 2000.
- Trimmer, M., Risgaard-Petersen, N., Nicholls, J. C., Engström, P. Direct measurement of anaerobic ammonium oxidation (anammox) and denitrification in intact sediment cores. MEPS 2006. 
- Weiss, R. F. The solubility of nitrogen, oxygen and argon in water and seawater. Deep-Sea Res. 1970.
- Weiss, R. F., Price, B. A. Nitrous oxide solubility in water and seawater. Mar. Chem. 1980.
- Yamamoto, S., Alcauskas, J. B., Crozier, T. E. Solubility of methane in distilled water and seawater. J. Chem. Eng. Data 1976.