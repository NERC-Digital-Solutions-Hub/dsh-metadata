# Fieldwork Sampling - Experimental Design and Collection Methods

- This document documents a multi-season field tracer study in Wood Brook, Staffordshire, using four in-stream fluorometers across four sites to generate breakthrough curves for multiple tracers (fluorescein, resazurin, resorufin).
- Objective aligned with environmental monitoring: obtain high-frequency, multi-tracer transport data to inform understanding of stream flow and contaminant transport.

## Experimental Design and Site Characteristics
- Study location: Wood Brook, Staffordshire.
- Reaches and turbidity/substrate: upstream reaches (1-2 and 2-3) sand-dominated; downstream reach (3-4) gravel-dominated.
- Reach lengths: 239.3 m (1-2), 289.2 m (2-3), 165.1 m (3-4).
- Deployments: four fluorometers at sites 1–4 to create three sub-reaches (1-2, 2-3, 3-4).
- Sampling seasons: July 2016, October 2016, February 2017, March 2017.
- Tracers used: conservative fluorescein and reactive resazurin, with resorufin measured as an additional tracer.

## Sampling Protocol and Tracer Injections
- Injections: instantaneous solute injections at the upstream site (180 m upstream for July; 250 m upstream for other seasons) prior to sampling.
- Tracer masses: fluorescein (1.2 g in Oct and Feb/Mar; 2 g in July) and resazurin (8 g); resorufin measured to complement resazurin data.
- Timing: injection times recorded per season (e.g., 18:47:00 in July; ~14:10–14:29 across other seasons).
- Measurement duration: fluorometers operated for 12+ hours to capture the tail of breakthrough curves (BTCs).

## Calibration Procedures
- Field calibration: conducted immediately prior to tracer injections in a connected loop so all fluorometers processed the same solution.
- Calibration solutions: zero (stream water) and target concentrations (70 ppb fluorescein; 100 ppb resazurin; 100 ppb resorufin).
- Procedure: each solution passed through fluorometers until readings stabilized; calibration maintained for 2–3 minutes per solution.

## Data Recording, Corrections and Units
- Recorded values: BTCs in parts per billion (ppb); in-situ measurements followed by post-processing.
- Data corrections: temperature and turbidity corrections applied (per Blaen et al., 2017); drift corrections across BTCs; baseline background adjustments to zero when background was negative or negligible.
- Data quality notes: background concentrations adjusted to zero to reflect non-natural occurrence of tracers in streams.

## Analytical Instruments and Measurement Frequency
- Instrumentation: online field fluorometers (GGUN-FL30, Albillia Sàrl, Switzerland) with LEDs and detectors for fluorescein, resazurin, and resorufin at 470, 570, and 525 nm respectively.
- Operation: configured to measure every 10 seconds; placed directly in the stream and calibrated immediately before each tracer injection.

## Data Structure and Availability
- Dataset file: Fluorescein_resazurin_resorufin_breakthrough_curves_Wood_Brook_UK_2016_2017 (CSV).
- Structure: 64 columns with four main columns repeated for each season/site—Date-Time (GMT), Fluorescein Concentration (ppb), Resazurin Concentration (ppb), Resorufin Concentration (ppb)—with season and site identified in the header above each Date-Time column.

## References
- Blaen, P. J., Brekenfeld, N., Comer-Warner, S., and Krause, S. (2017). Multitracer Field Fluorometry: Accounting for Temperature and Turbidity Variability During Stream Tracer Tests. Water Resources Research.
- Lemke, D., Schnegg, P. A., Schwientek, M., Osenbrück, K., and Cirpka, O. A. (2013). On-line fluorometry of multiple reactive and conservative tracers in streams. Environmental Earth Sciences.