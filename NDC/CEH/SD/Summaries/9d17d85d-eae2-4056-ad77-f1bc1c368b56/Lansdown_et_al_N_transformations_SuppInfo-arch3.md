# Overview of data

- Purpose and scope
  - Compilation from the NERC Macronutrients consortium study titled “The role of lateral exchange in the seaward flux of C, N and P,” focused on measuring in situ nitrogen transformations and porewater chemistry in rivers with varying land-river connectivity.
  - Four field campaigns in the Hampshire Avon catchment to compare permeable sediments (sand/chalk) and clays, aiming to quantify processes such as nitrification, denitrification, and anaerobic ammonium oxidation (anammox) and their contributions to N fluxes.

- Data collected and structure
  - Two accompanying data files:
    - N transformations and porewater chemistry in permeable sediments.
    - N transformations in clays.
  - Data files are structured as:
    - Permeable sediments: 241 rows x 20 columns.
    - Clays: 153 rows x 7 columns.
  - Column headers include:
    - RecordID, Season, SiteCode, Vegetated, Depth.
    - Rates and flux-related metrics: A14, D14, ra, Nit-15N, Nit-pn.
    - Porewater chemistry: Ammonium, Chloride, Iron(II), Methane, Nitrate, Nitrite, N2O, O2, O2sat, pH, SRP.
  - Site codes and coordinates (e.g., CE1, CW2, GN1, GA2 for permeable; AS1, AS2 for clays) with corresponding latitude/longitude.
  - Seasons covered: Spring 2013, Summer 2013, Autumn 2013, Winter 2014; some accesses were limited due to flooding or landowner constraints.

- Methods and measurements
  - Field sampling techniques:
    - Push-pull sampling with bespoke probes inserted 3–20 cm into riverbeds; porewater collected via syringe under slight vacuum.
    - Immediate measurements of O2 and pH; preservation for Fe(II) or gas analysis; filtration and freezing for nutrients and chloride.
  - Nitrogen transformation experiments:
    - Permeable sediments: injection of 15N-labelled nitrate (300 µM, ~98 atom % 15N) in a 25 mL tracer, with four time points over ≤60 minutes.
    - Clays: intact core method (Trimmer et al., 2006) with 15N-labelled nitrate added to overlying river water and cores incubated ≤4 hours.
  - Porewater chemistry and ancillary measurements:
    - Ammonium, Nitrate, Nitrite, N2O, O2, O2sat, pH, Chloride, SRP measured using automated colorimetry, Griess method, ion-selective electrodes, and microelectrodes with specified detection limits and precision.
    - Methane measured via headspace analysis after preserving porewater samples in zinc chloride; concentrations converted to dissolved concentrations with Bunsen solubility.
    - Iron(II) measured via phenanthroline complexation and UV/Vis spectrophotometry.
  - Data quality and handling:
    - BDL indicates below detection limit; ND indicates not determined due to flow conditions.
    - Calibration and reference materials used to ensure accuracy; explicit limits of detection and precision cited for each parameter.
    - O2 contamination estimated and subtracted (approximately 10 µM) with noted calibration practices.

- Calculations and analytical workflow
  - N2 isotope pairing calculations to determine production of 29N2 and 30N2 from 15N tracer data using headspace measurements and mass spectrometry.
  - Permeable sediments:
    - Calculation of p14 (14N-N2 production from ambient processes), ra (fraction of N2 from anammox), A14 (14N from ambient N2 production via anammox), D14 (14N from ambient N2 production via denitrification).
    - Nit-pn (ambient nitrification) calculated using p14 and pw.14 (p15 x r14).
  - Clays (impermeable sediments) adjustments:
    - N2 measurements scaled from slurry data to per m2 riverbed rates; similar ra, p14, A14, D14 calculations applied.
  - r14 is derived from the ratio of 14N-containing products to 15N-containing products (via 45N2O and 46N2O measurements).
  - References for methods include Nielsen (1992), Risgaard-Petersen et al. (2003), Trimmer et al. (2006), Lansdown et al. (2014, 2016), and related methodological papers.

- Data quality, limitations, and metadata considerations
  - Metadata available include site codes, geographic coordinates, sediment type (vegetated vs un-vegetated), and sampling depth.
  - Clear data qualifiers (BDL, ND) indicate data gaps and detection limits.
  - Field limitations affected data coverage: flooding and landowner access prevented core collection at some sites in certain campaigns; push-pull sampling in clays faced clogging and disruption issues; time constraints affected incubation lengths.
  - The dataset provides detailed measurement protocols, calibration steps, and analytical formulas, but users should still assess metadata completeness for cross-study harmonization and reuse.

- Accessibility and references
  - Data are accompanied by published methodological references and are designed to enable replication of in situ N-cycling measurements and isotope-based partitioning.
  - Core references include Lansdown et al. 2014, 2016; Nielsen 1992; Trimmer et al. 2006; Risgaard-Petersen et al. 2003; and foundational method papers for isotope pairing and solubility calculations.