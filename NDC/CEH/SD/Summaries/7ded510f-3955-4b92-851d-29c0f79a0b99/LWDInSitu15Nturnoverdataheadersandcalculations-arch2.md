# General information

- This dataset contains in situ field measurements of riverbed nitrogen transformations in the Hammer Stream, a sandy tributary of the River Rother in West Sussex, UK (lat 51.01085722 N, long 0.801498333 W). Findings published in Shelley et al. (2017).
- Objective: quantify nitrate reduction in permeable sandy sediments using a 15N-labelled nitrate tracer, conducted within the main piezometer network described in Shelley et al. (2017).
- Methodology (high level):
  - 15N-nitrate tracer injected into the riverbed in de-oxygenated synthetic river water with KCl; samples collected over time.
  - Pre-injection porewater samples for background nutrients and other parameters.
  - Helium headspace used; 15N-labeled N2 produced measured by mass spectrometry.
  - Porewater nutrients filtered, frozen, and analyzed with established protocols.
- Sampling timetable: November 2014; February, April, and July 2015.

- Data structure and field descriptions:
  - Spatial and installation data: lat, long, peizo (piezometer ID), 1m of LOW (whether within 1 m of woody debris), Depth, True depth.
  - Hydraulics and sampling context: head (vertical hydraulic gradient), water depth.
  - Baseline porewater conditions (before injection): O2adj, O2adj% saturation, pH, temp, NO2, NO3, NH3, PO4, Chloride, CH4, N2O, Fe II, orgC.
  - Isotopic and transformation metrics: p15N2 (in situ rate of total 15N2 production), Denitrification, Anammox, DNRA, tot15n, qN2, qN2O.
  - Fractional/process indicators: %Anammox, %DNRA, %Denitrification.
  - Temporal marker: month (Nov, Feb, Apr, Jul).

- Data quality and handling:
  - Values labeled 0 indicate concentrations below detection limit; ND indicates not collected or sample lost.
  - Background concentrations and calibration details documented (e.g., O2 calibration, detection limits, precision).

- Analytical methods and calculations:
  - p15N2 derived from 15N2 production rates from injected tracer; linked to total N2 production and sample volumes.
  - P29 and P30 production rates used to quantify denitrification pathways; limits of detection defined.
  - Denitrification, Anammox, and DNRA rates derived from p15N2 and related measurements; DNRA quantified via hypobromite oxidation of NH3.
  - Totals and ratios: tot15n, qN2, qN2O, and percent contributions of each pathway (%Anammox, %DNRA, %Denitrification).
  - Calculations anchored to established methods and references (Thamdrup & Dalsgaard 2000; Risgaard-Petersen et al. 2003; Trimmer et al. 2006; and related methodological papers).

- References and provenance:
  - Shelley, Klaar, Krause, & Trimmer (2017) on enhanced hyporheic exchange and nitrate reduction.
  - Lansdown et al. (2014); Sanders et al. (2007); Yamamoto et al. (1976); Weiss & Price (1980); Risgaard-Petersen et al. (1995, 2003); Thamdrup & Dalsgaard (2000); Trimmer et al. (2006).

- Alignment with Analysts Monitoring the Environment objectives:
  - Uses standardised data collection and documentation to enable comparison over time and integration with other datasets.
  - Emphasizes data quality assurance, provenance, and transparent, replicable calculations for environmental health assessment.
  - Provides a rich, multi-parameter dataset suitable for combining with other monitoring data and enabling broader environmental policy evaluation.