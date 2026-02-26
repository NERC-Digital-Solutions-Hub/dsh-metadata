# Overview of data

- Purpose and scope
  - A compiled dataset from the in-stream N-cycling component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the seaward flux of C, N, and P.
  - Two accompanying data files: (1) N transformations and porewater chemistry in permeable sediments; (2) N transformations in clays.

- Field campaigns and study sites
  - Four field campaigns in the Hampshire Avon catchment to measure in situ nitrogen transformations and porewater chemistry.
  - Permeable sediments (sand/chalk) vs. clays: separate data files and methodologies.

- Sampling approaches
  - Permeable sediments: push-pull sampling with bespoke stainless steel probes deployed 3–20 cm below the riverbed; porewater collected via syringe under slight vacuum; immediate measurements of O2 and pH, preservation for Fe(II) or gas analyses, and filtration for later nutrient/chloride analyses.
  - Clays: push-pull sampling with rhizons failed; used intact core method (3 cm diameter cores incubated in river water with added 15N-nitrate) for up to 4 hours; porewater chemistry not collected for clays.
  - 15N-labelled nitrate injected to trace nitrogen transformations; multiple time points collected for analysis.

- Data content and structure
  - Permeable sediments: dataset dimensions 241 rows x 20 columns.
  - Clays: dataset dimensions 153 rows x 7 columns.
  - Data coded with: BDL (below detection limit) and ND (not detected/ not possible due to flow conditions).

- Column headers and key variables
  - RecordID: unique sample identifier.
  - Season: sampling season (Spring 2013, Summer 2013, Autumn 2013, Winter 2014); note occasional site-specific access limits.
  - SiteCode: site identifiers (e.g., CE1, CW2, GN1, GA2, AS1, AS2) with geographic coordinates provided.
  - Vegetated: Y/N indicating sediment vegetation presence.
  - Depth: probe depth below riverbed (cm).
  - A14, D14: nitrification/denitrification metrics (in permeable sediments nmol N L−1 h−1 or μmol N m−2 h−1 for clays).
  - ra: contribution of anammox to N2 production (%).
  - Nit-15N, Nit-pn: labelling-based nitrification measures (ambient and nitrate-derived).

  - Key chemical and gas measurements (pre-15N injection):
    - Ammonium, Chloride, Iron(II), Methane, Nitrate, Nitrite, N2O, O2, O2sat, pH, SRP.
  - Method details and detection limits are provided for each parameter to support quality assurance.

- Analytical methods (highlights)
  - Ammonium: indophenol blue colorimetry.
  - Chloride: ion-selective electrode.
  - Iron(II): phenanthroline colorimetric method with protection from oxygen.
  - Methane and N2O: gas chromatography with headspace analysis; methane dissolved via Bunsen solubility.
  - Nitrate/Nitrite: automated colorimetry (Griess method; NOx reduction for nitrate).
  - O2: microelectrode with calibration against zero and known concentrations; oxygen contamination corrections applied.
  - pH: calibrated pH probe with temperature recording.
  - SRP: molybdenum blue method with ascorbic acid.
  - N2-related calculations: isotope pairing technique using 15N-tracer; determination of 29N2/30N2 production via mass spectrometry and correction for advective flow; nitrification via NOx/N2 conversions; separator calculations for p14, ra, A14, D14; for clays, scaling to per m2 of riverbed.

- N2 calculations overview
  - 15N-nitrate injections mixed with ambient 14N pools; production of 29N2/30N2 measured in headspace after equilibration.
  - For permeable sediments: compute aN2, correct for flow, derive p14, ra, A14, D14 using referenced equations.
  - For clays: adapted approach using slurry N2 measurements scaled to per m2 values.
  - Ambient nitrification (Nit-pn) calculated using p14 and pw.14 relationships; ra quantifies the fraction of N2 production due to anammox.

- Data quality, limitations, and gaps
  - Some samples marked as ND due to flow conditions or access constraints (e.g., flooding at GA2, CE1; AS2 spring access).
  - BDL indicates measurements below method detection limits; data interpretation uses stated limits and calibration standards.

- Data availability and references
  - Data files correspond to published and forthcoming methodologies (Lansdown et al. 2014; Lansdown et al. 2016; Nielsen 1992; Trimmer et al. 2006; Risgaard-Petersen et al. 2003; supporting methods in Lansdown 2014, 2016).
  - References provided for methodological details and isotope pairing calculations.

- Practical relevance for analysts monitoring the environment
  - Demonstrates standardized, in situ measurement of riverbed nitrogen cycling across different sediment types.
  - Produces outputs suitable for reporting environmental health and policy performance, including rates of nitrification, denitrification, anammox, and their partitioning (ra, p14, D14, A14).
  - Data are organized for integration into monitoring portals and can be combined with other data layers to enhance environmental dataset value and accessibility.