# General information:

- This dataset contains results from in situ field measurements of riverbed nitrogen transformations in the Hammer Stream (51.01085722 N, 0.801498333 W), a sandy tributary of the River Rother in West Sussex, UK. The results have been published in Shelley et al. (2017).
- Study design: nitrate reduction measured by a 15N-labelled nitrate push-pull technique, conducted directly in the main piezometer network described in Shelley et al. (2017). 15N-nitrate (98 atom % 15N) was injected into the riverbed in a de-oxygenated synthetic river water plus KCl matrix; samples recovered over time via a helium headspace, with 15N-labelled N2 determined by mass spectrometry.
- Sampling campaigns: measurements performed in November 2014 and February, April, and July 2015.
- Pre-injection background sampling: porewater was collected to measure NO2, NO3, NH3, PO4, chloride, oxygen, pH, temperature, Fe(II), organic carbon, 15N-N2, CH4, and N2O. Samples for nutrients were filtered (0.45 µm) and frozen at -20 ºC until analysis.
- Data coding and handling: values below detection limits are coded as 0; ND indicates no data collected or a sample lost.
- The dataset contains a mix of field measurements, laboratory analyses, and in situ calculations, with multiple derived rates and isotopic-tracer calculations described below.

## Data scope and location

- Location: Hammer Stream, a sandy tributary of the River Rother, West Sussex, UK.
- Coordinates provided for piezometer locations (lat/long).
- Variables cover porewater chemistry before injection, hydraulic conditions, and in situ nitrogen transformation rates during and after 15N-nitrate injections.

## Measurement methodology (key procedures)

- 15N-nitrate push-pull in riverbed sediments, using a tracer in de-oxygenated synthetic river water with KCl.
- Porewater sampling and background measurements collected prior to injection.
- Sample handling and storage:
  - Nutrients filtered (0.45 µm) and frozen at -20 ºC until analysis.
  - Oxygen measurements via fast-response microelectrode; calibration with zero solution and known concentration; contamination estimated and subtracted.
- Instrumentation and analyses:
  - Mass spectrometry (Delta Plus Thermo Finnigan) for 15N2 production (29N2/30N2) following 15N-nitrate injection.
  - GC-FID for CH4 and N2O after gas-tight headspace equilibration.
  - Automated colorimetry for NO2, NO3 (NOx), NH3, and SRP; inline Cd reduction for NOx analysis.
  - ISE for chloride.
  - UV/Vis spectrophotometry with phenanthroline for Fe(II) and total inorganic analyses.
  - TOC analyzer for dissolved organic carbon.
- Calculations and standards:
  - Rates of p15N2 production derived from time-series isotope data.
  - Denitrification, Anammox, and DNRA rates calculated in situ from isotope measurements.
  - Totals and isotopic fractions (qN2, qN2O) computed from mass spectrometry data.
  - Performance metrics and detection limits described for each analyte.

## Data fields and units (core headers)

- Spatial and sample identifiers:
  - lat, long: coordinates of each piezometer (degrees north/west).
  - peizo: numeric piezometer id.
  - 1m of LOW: yes/no indicator if piezometer is within 1 m of large woody debris.
  - Depth (cm): screened midpoint depth below riverbed (cm).
  - True depth (cm): actual screened depth below riverbed (cm).
  - head: vertical hydraulic gradient (m).
  - water depth: depth from river surface to riverbed interface (m).
- Physicochemical state:
  - O2adj: dissolved oxygen in porewater before injection (µM).
  - O2adj%: dissolved oxygen saturation (%).
  - pH, temp: porewater pH and temperature (units as stated in document).
- Nutrients and solutes (pre-injection porewater):
  - NO2, NO3, NH3, PO4: concentrations (µM for NO2/NO3/NH3; SRP in µM for PO4).
  - Chloride: Cl- concentration (mM).
- Gas and redox compounds (pre-injection porewater):
  - CH4, N2O: concentrations (CH4 and N2O in µM/nM as specified).
  - Fe II: Fe(II) concentration (µM).
  - orgC: dissolved organic carbon (mg/L).
- Isotopic and reaction rates:
  - p15N2: in situ rate of total 15N2 production (nM N per L per h).
  - Denitrification: rate of 15N2 production due to denitrification (nM N per L per h).
  - Anammox: rate of 15N2 production via anammox (nM N per L per h).
  - DNRA: rate of 15N-NH3 production via DNRA (nM N per L per h).
  - tot 15n: sum of denitrification, anammox, DNRA (nM N per L per h).
  - qN2: proportion of 15N labeling in produced N2.
  - qN2O: proportion of 15N labeling in produced N2O.
  - %Anammox: percentage of total N2 production from anammox.
  - %DNRA: percentage of total N production attributed to DNRA.
  - %Denitrification: percentage of total N production due to denitrification.
- Notes on data quality:
  - Detection limits and precision are provided for each analyte (e.g., NO2, NO3, NH3, SRP, FeII, O2, etc.).
  - Values marked 0 indicate below detection limit; ND indicates missing or lost data.

## Data quality, flags, and provenance

- Detection limits and precision are explicitly stated for key measurements (e.g., NO2 detection limit 0.04 µM; NO3 detection limit 0.1 µM; NH3 limit 0.8 µM; SRP 0.1 µM; Fe(II) limit 1 µM; O2 measurement uncertainty ~10 µM contamination).
- Data handling conventions:
  - 0 used for below detection limits.
  - ND used when data are not collected or sample lost.
- Isotopic calculations rely on established methods and calibrations (mass spectrometry and calibration factors) and refer to specific literature for isotope pairing techniques.
- Derived rates (denitrification, anammox, DNRA) are calculated from time-series isotopic data with defined detection thresholds (e.g., micro-mole levels per L per h for 29N2/30N2).
- Background pre-injection measurements provide context for interpreting injection-derived transformations.

## Derived metrics and interpretation

- Denitrification: in situ rate of 15N2 production attributed to denitrification.
- Anammox: in situ rate of N2 production via anammox pathway.
- DNRA: in situ rate of 15N-NH3 production via DNRA.
- tot 15n: aggregate rate combining denitrification, anammox, and DNRA.
- qN2 and qN2O: isotopic labeling fractions for produced N2 and N2O, used to derive %Anammox, %DNRA, and %Denitrification.
- Percentage contributions inform pathway partitioning of nitrogen removal in the riverbed sediments.

## Temporal and publication context

- Sampling windows: November 2014; February 2015; April 2015; July 2015.
- Related publications establishing methods and context:
  - Shelley et al. 2017
  - Lansdown et al. 2014
  - Supporting methodological references for isotopic techniques and solubility corrections (Yamamoto et al. 1976; Weiss & Price 1980; Risgaard-Petersen et al. 1995, 2003; Thamdrup & Dalsgaard 2000; Trimmer et al. 2006; Sanders et al. 2007).

## Data governance, storage, and reuse considerations for Data Stewards

- Provenance: clearly documented measurement and calculation workflow, with explicit references to original methods and publications.
- Metadata completeness: spatial coordinates, sensor depths, hydraulic conditions, pre-injection background chemistry, and all derived nitrogen transformation metrics are included.
- Standardization: consistent units, explicit column headers, and data-flag conventions (0, ND) support interoperability and reuse.
- Data sharing and access: dataset references peer-reviewed publications; ensure alignment with repository requirements and include the cited literature in data dissemination.
- Data quality management: document detection limits, calibration procedures, and potential contamination estimates to inform downstream users of uncertainty.
- Versioning and updates: the dataset spans multiple seasons; maintain versioned records as updates or corrections arise, ensuring traceability to original sampling events.
- Curation notes for user needs: to support data discoverability for data stewards, provide clear mappings between field measurements, laboratory analyses, and derived rates; consider user education on interpreted isotopic fractions and their implications for nitrogen cycling studies.

## References

- Shelley, F., Klaar, M., Krause, S., & Trimmer, M. Enhanced hyporheic exchange flow around woody debris does not increase nitrate reduction in a sandy streambed. Biogeochemistry (2017).
- Lansdown, K. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. (2014).
- Sanders, I. et al. Emission of methane from chalk streams has potential implications for agricultural practices. Freshwater Biology (2007).
- Yamamoto, S., Alcauskas, J.B. & Crozier, T.E. Solubility of methane in distilled water and seawater. J. Chem. Eng. Data (1976).
- Weiss, R. & Price, B. Nitrous oxide solubility in water and seawater. Mar. Chem. (1980).
- Risgaard-Petersen et al. 1995; Risgaard-Petersen et al. 2003; Thamdrup & Dalsgaard 2000; Trimmer et al. 2006 (isotope pairing and related methods).