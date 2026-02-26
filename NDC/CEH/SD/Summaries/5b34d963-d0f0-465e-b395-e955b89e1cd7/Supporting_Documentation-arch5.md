# Fieldwork Sampling - Experimental Design and Collection Methods

- Seasonal tracer experiments conducted in Wood Brook, Staffordshire during July 2016, October 2016, February 2017 and March 2017.
- Four fluorometers deployed at sites 1–4, creating three sub-reaches: 1-2, 2-3, and 3-4.
- Reaches: upstream reaches (1-2, 2-3) sand-dominated; downstream reach (3-4) gravel-dominated.
- Reach lengths: 239.3 m (1-2), 289.2 m (2-3), 165.1 m (3-4).
- Tracer injections: instantaneous solute tracer (conservative fluorescein and reactive resazurin) dissolved in stream water.
  - Injections: 1.2 g fluorescein + 8 g resazurin (October, February, March); 2 g fluorescein + 8 g resazurin (July).
  - Injection sites: 180 m upstream of site 1 (July) and 250 m upstream (other seasons).
  - Injection times: 18:47 (July) and 14:10–14:29 (other seasons).
- Measured breakthrough curves for fluorescein, resazurin, and resorufin at all four sites.
- Fluorometers left operating for 12+ hours to capture curve tails.

- Calibration steps and values
  - Field calibration performed immediately before tracer injections in a connected loop (same solution through all fluorometers).
  - Two-point calibration per tracer: zero concentration (stream water) and target concentrations (70 ppb fluorescein, 100 ppb resazurin, 100 ppb resorufin).
  - Calibration solutions diluted with stream water; readings stabilized before recording for 2–3 minutes.

- Nature and units of recorded data
  - Breakthrough curves stored in parts per billion (ppb).
  - In-situ measurements corrected for temperature and turbidity (per Blaen et al., 2017).
  - Data clipped at baseline around the tail; drift corrections applied between start and end of the curve.
  - Background corrections applied when necessary (set negative backgrounds to zero; fluorescein, resazurin, resorufin are not naturally present in streams).

- Analytical methods and instrumentation
  - On-line field fluorometers (GGUN-FL30, Albillia Sàrl) with LEDs/detectors for 470 nm (fluorescein), 570 nm (resazurin), 525 nm (resorufin).
  - Calibration performed immediately before tracer injection; data captured every 10 seconds.
  - Instruments configured for continuous measurement during the experiment.

- Data structure and contents
  - One CSV file: "Fluorescein_resazurin_resorufin_breakthrough_curves_Wood_Brook_UK_2016_2017" containing 64 columns.
  - Four column headers (Date-Time GMT, Fluorescein Concentration ppb, Resazurin Concentration ppb, Resorufin Concentration ppb) repeated for each season/site.
  - Season and site identifiers provided above each Date-Time column.

- Provenance and references
  - Methodological basis for temperature and turbidity corrections: Blaen et al., 2017.
  - On-line fluorometry approach for multiple tracers: Lemke et al., 2013.

- Data governance considerations for reuse
  - Ensure complete, consistent metadata including site identifiers, reach names, injection details, calibration parameters, and processing steps.
  - Maintain traceability of corrections (temperature, turbidity) and baseline/background adjustments.
  - Document any deviations from protocol (e.g., injection amounts by season) and instrument configurations.
  - Provide versioned data access and clear licensing to enable discovery and reuse by other researchers and data users.