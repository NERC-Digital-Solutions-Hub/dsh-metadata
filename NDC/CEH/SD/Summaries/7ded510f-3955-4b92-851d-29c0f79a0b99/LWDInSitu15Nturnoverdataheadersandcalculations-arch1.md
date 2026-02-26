# General information

- This dataset contains results from in situ field measurements of riverbed nitrogen transformations in the Hammer Stream (lat 51.01085722 N, lon 0.801498333 W), a sandy tributary of the River Rother in West Sussex, UK.
- Measurements and analyses have been published in Shelley et al. (2017); the dataset uses a 15N-nitrate push-pull approach to quantify nitrate reduction processes directly in the riverbed.
- Sampling was conducted in November 2014 and February, April, and July 2015, across a main piezometer network described in Shelley et al. (2017).

- Experimental approach
  - Injected a tracer containing 15N-labelled nitrate (300 µM, 98 atom% 15N) in de-oxygenated synthetic river water with KCl into the riverbed.
  - Recovered porewater samples over time; used a helium headspace and mass spectrometry to determine 15N-labelled N2 production.
  - Measured background porewater concentrations prior to injection for multiple nutrients and parameters.
  - Pre-injection samples were analyzed for NO2, NO3, NH3, PO4, chloride, O2, pH, temperature, Fe(II), organic carbon, 15N-N2, and CH4/N2O.

- Sample handling and data flags
  - Nutrient samples filtered (0.45 µm) and frozen at -20°C until analysis.
  - Data values marked as 0 if below detection limit; marked as ND if not detected or sample lost.

- Data structure and columns (monthly sampling codes)
  - Month: Nov (November 2014); Feb, Apr (April 2015); Jul (July 2015).
  - Spatial information: lat, long; piezometer identifier (peizo); proximity to woody debris within 1 m (1m of LOW); depth and true depth below riverbed; head (vertical hydraulic gradient); water depth.
  - In situ porewater conditions: O2adj (µM), O2adj% (O2 saturation), pH, temp (°C).
  - Nutrients and related chemistry: NO2, NO3 (NOx minus nitrite), NH3, PO4, Chloride, CH4, N2O, Fe II, orgC (dissolved organic carbon).
  - Isotopic/nitrogen transformation rates and pools: p15N2 (in situ rate of total 15N2 production; nano-mol N L-1 h-1), Denitrification (p15N2 production due to denitrification), Anammox, DNRA (each in nano-mol N L-1 h-1), tot15n (sum of denitrification, anammox, DNRA).
  - Isotopic attribution metrics: qN2, qN2O (proportion of 15N labelling in produced N2 and N2O).
  - Process proportions (percent contributions): %Anammox, %DNRA, %Denitrification.

- Calculations and interpretation
  - Denitrification, Anammox, and DNRA rates are derived from 15N tracer data; tot15n is the sum of the three.
  - p15N2 is calculated by tracking 15N-N2 production over time via a linear trend; detection limits for 29N2 and 30N2 are approximately 0.003 and 0.009 µmol N2 L-1 h-1, respectively.
  - Proportions (%Anammox, %DNRA, %Denitrification) are determined by comparing 15N labelling in the produced N2 and N2O pools.

- Analytical methods (key details)
  - NOx analysis includes inline cadmium reduction to convert nitrate to nitrite; nitrite and nitrate measured by automated colorimetry (Griess method).
  - NH3 measured via indophenol blue method; SRP via molybdenum blue method.
  - Chloride measured with ion-selective electrode.
  - CH4 and N2O measured by GC with GC-FID and microECD detectors; CH4 N2O concentrations converted using solubility coefficients.
  - Fe II measured via phenanthroline complexation and UV/Vis absorbance.
  - orgC quantified by TOC analyser.

- Data quality and caveats
  - Data include background values prior to isotope injection to contextualize transformation rates.
  - Detection limits and calibration details are provided for each parameter; data include ND and 0 values as applicable.
  - Piezometer depth and head measurements were standardized by season and tool (Solinst water level meter).

- References for methods and context
  - Shelley, F., Klaar, M., Krause, S., & Trimmer, M. 2017. Enhanced hyporheic exchange flow around woody debris does not increase nitrate reduction in a sandy streambed.
  - Lansdown, K. et al. 2014. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed.
  - Sanders, I. et al. 2007; Yamamoto, S. et al. 1976; Weiss, R. & Price, B. 1980; Risgaard-Petersen et al. 1995, 2003; Thamdrup & Dalsgaard 2000; Trimmer et al. 2006.