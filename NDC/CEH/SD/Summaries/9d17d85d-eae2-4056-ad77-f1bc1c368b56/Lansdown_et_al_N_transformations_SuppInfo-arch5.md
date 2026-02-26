# Overview of data

- A dataset from the in-stream N-cycling component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the seaward flux of C, N and P.
- Generated under the guidance of Prof. Mark Trimmer and Dr. Kate Heppell, with Dr. Katrina Lansdown as the data producer.
- Two accompanying data files:
  - Lansdown et al N transformations and porewater chemistry in permeable sediments
  - Lansdown et al N transformations in clays

## What the data cover

- Four field campaigns in the Hampshire Avon catchment to measure in situ rates of nitrogen transformations and porewater chemistry in rivers with varying land-river connectivity.
- Permeable sediments (sand or chalk geology) sampled with a push-pull technique using bespoke riverbed probes.
- Clays sampled using an intact core method due to practical challenges with push-pull in fine sediments.
- Parameters measured include porewater chemistry (O2, pH, Fe(II), CH4, nitrate, nitrite, N2O, N2 isotopes, etc.), and nitrogen transformation rates (anammox, denitrification, nitrification, and related contributions).

## Field methods and sampling details

- Permeable sediments:
  - Probes installed at depths of 3–20 cm; porewater drawn and analyzed for multiple chemical species.
  - 15N-labelled nitrate injected to measure transformation rates; multiple time points collected within 60 minutes.
- Clays:
  - Intact core incubations (3 cm diameter) with 15N-labelled nitrate added to overlying water; incubated up to 4 hours.
  - No porewater chemistry collected for clays; analyses rely on slurry sampling at the end.
- Sites include CE1 (Ebble), CW2 (Wylye), GN1 (Nadder), GA2 (Avon), and AS1/AS2 (Sem), with geographic coordinates provided.

## Data structure and content

- Data are organized into two files:
  - Permeable sediments: 241 rows × 20 columns
  - Clays: 153 rows × 7 columns
- Missing and censored data:
  - BDL: below detection limit
  - ND: not determined due to flow conditions
- Key columns (examples):
  - RecordID (unique sample identifier)
  - Season (spring, summer, autumn, winter campaigns)
  - SiteCode (CE1, CW2, GN1, GA2, AS1, AS2)
  - Vegetated (Y/N)
  - Depth (cm)
  - A14, D14 (rates of in situ anammox and denitrification; units vary by sediment type)
  - ra (contribution of anammox to N2 production)
  - Nit-15N (nitrification potential with 15N tracer)
  - Nit-pn (ambient nitrification in clays)
  - Ammonium, Chloride, Iron(II), Methane, Nitrate, Nitrite, N2O, O2, O2sat, pH, SRP (various porewater constituents and measurements)

## Measurement methods and data quality

- Analytical methods and instrumentation:
  - Automated colorimetry for ammonium and SRP
  - Ion-selective electrode for chloride
  - Spectrophotometry with phenanthroline for Fe(II)
  - Gas chromatography (GC) for CH4 and N2/N2O in headspace
  - Oxygen microelectrode for O2 with calibration against known standards
  - pH measurements with calibrated probes
- Detection limits and precision provided for each parameter
- Isotope-based calculations:
  - Isotope pairing technique for 15N-nitrogen transformations
  - Calculation of 29N2/30N2 production, correction for advective flow, and derivation of ra, p14, D14, and Nit-pn
  - Separate treatment for permeable sediments vs clays in N2 calculations
- References to established methods for calculations and calibrations are included (e.g., Risgaard-Petersen et al., Nielsen et al., Trimmer et al.)

## N2 calculations and nitrification details

- 15N-labelled nitrate introduced to quantify production of 29N2 and 30N2; 15N-N2O and 15N-N2 measured via mass spectrometry after headspace equilibration.
- For permeable sediments, p14, ra, A14, and D14 derived from 15N data; Nit-pn calculated using p14 and 14N contributions.
- For clays (impermeable sediments), N2 is derived from slurry measurements and scaled to per m2 of riverbed; similar ra, p14, A14, D14 framework applied with appropriate unit adjustments.
- Adjustments account for ambient nitrate contributions (r14) and isotopic composition to separate anammox vs denitrification contributions.

## Data quality notes and limitations

- Some sampling was not performed at certain sites in specific campaigns due to flooding or landowner restrictions.
- ND entries indicate data not possible under certain flow conditions.
- Permeable vs clay datasets have different measurement contexts and units; cross-compatibility requires careful normalization.
- The dataset includes detailed methodological descriptions and references to support reproducibility and auditability.

## References

- Lansdown, K., Heppell, C. M., Trimmer, M. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. 48, 4425-4434 (2014).
- Lansdown, K., McKew, B.A., Whitby, C., Heppell, C.M., Dumbrell, A.J., Binley, A., Olde, L. and Trimmer M. Importance and controls of anaerobic ammonium oxidation influenced by riverbed geology. Nature Geosci. Advance online publication (2016).
- Nielsen, L. P. Denitrification in sediment determined from nitrogen isotope pairing. FEMS Microbiol. Ecol. 86, 357-362 (1992).
- Smart, R. M. & Barko, J. W. Laboratory culture of submersed freshwater macrophytes on natural sediments. Aquat. Bot. 21, 251-263 (1985).
- Risgaard-Petersen, N., Nielsen, L. P., Rysgaard, S., Dalsgaard, T. & Meyer, R. L. Application of the isotope pairing technique in sediments where anammox and denitrification coexist. Limnol. Oceanogr. Methods 1, 63-73 (2003).
- Thamdrup, B. & Dalsgaard, T. The fate of ammonium in anoxic manganese oxide-rich marine sediment. Geochim. Cosmochim. Acta 64, 4157-4164 (2000).
- Trimmer, M., Risgaard-Petersen, N., Nicholls, J. C. & Engstrom, P. Direct measurement of anaerobic ammonium oxidation (anammox) and denitrification in intact sediment cores. MEPS 326, 37-47 (2006).
- Weiss, R. F. The solubility of nitrogen, oxygen and argon in water and seawater. Deep-Sea Res. 17, 721-735 (1970).
- Weiss, R. F. & Price, B. A. Nitrous oxide solubility in water and seawater. Mar. Chem. 8, 347-359 (1980).
- Yamamoto, S., Alcauskas, J. B. & Crozier, T. E. Solubility of methane in distilled water and seawater. J. Chem. Eng. Data 21, 78-80 (1976).