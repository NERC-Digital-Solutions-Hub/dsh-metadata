# Fieldwork Sampling - Experimental Design and Collection Methods

## Purpose and Scope
- Seasonal field experiments conducted in Wood Brook, Staffordshire (July 2016, Oct 2016, Feb 2017, Mar 2017).
- Four fluorometers deployed across four sites (1–4) creating three sub-reaches (1–2, 2–3, 3–4) to study solute tracer transport.
- Uses both conservative (fluorescein) and reactive (resazurin; with resorufin also measured) tracers to generate breakthrough curves (BTCs).

## Experimental Design
- Reaches: upstream 1–2 and 2–3 are sand-dominated; downstream 3–4 is gravel-dominated.
- Reach lengths: 239.3 m (1–2), 289.2 m (2–3), 165.1 m (3–4).
- Injections: instantaneous solute injections of fluorescein and resazurin at a site upstream of site 1 (180 m in July; 250 m in other seasons).
- Injection masses: fluorescein 1.2 g (July: 2 g), resazurin 8 g; resorufin detected as a downstream product.

## Tracers and Injections
- Tracers: conservative fluorescein; reactive resazurin with resorufin as a product.
- Timing: injections conducted in late morning across seasons (times varied: ~14:00–14:30 for most), with July slightly earlier.
- BTCs monitored at all four sites post-injection.

## Data Collection and Measurement
- Fluorometers left in the stream for 12+ hours to capture the full tail of BTCs.
- Measurements taken at each site to produce breakthrough curves.

## Calibration and Quality Assurance
- Field calibration immediately before tracer injections using a connected loop to ensure identical flow through all fluorometers.
- Two-point calibration: zero (stream water) and target concentrations (70 ppb fluorescein; 100 ppb resazurin; 100 ppb resorufin).
- Calibration solutions prepared in stream water; readings stabilized over 2–3 minutes.
- Calibration values used to drive measurements in situ.

## Data Processing and Units
- BTCs recorded in parts per billion (ppb).
- In-situ data corrected for temperature and turbidity (per Blaen et al., 2017); background drift and tail clipping applied.
- Background adjustments: zero-corrected where background appeared above zero or below zero in the tail region.
- Fluorophores do not occur naturally in streams; background concentrations adjusted accordingly.

## Analytical Methods and Instrumentation
- On-line fluorometers (GGUN-FL30, Albillia Sàrl, Switzerland) configured for in-stream measurements.
- Excitation/emission: fluorescein (470 nm), resazurin (570 nm), resorufin (525 nm).
- Sampling rate: every 10 seconds; fluorometers calibrated and deployed in the field during sampling.

## Data Structure and Availability
- Datasets stored as a single CSV file: Fluorescein_resazurin_resorufin_breakthrough_curves_Wood_Brook_UK_2016_2017.
- 64 columns; repeated column sets for each season and site: Date-Time (GMT), Fluorescein (ppb), Resazurin (ppb), Resorufin (ppb).
- Season and site identifiers provided above each Date-Time column.

## References
- Blaen, P. J., et al. 2017. Multitracer Field Fluorometry: Accounting for Temperature and Turbidity Variability During Stream Tracer Tests. Water Resources Research.
- Lemke, D., et al. 2013. On-line fluorometry of multiple reactive and conservative tracers in streams. Environmental Earth Sciences.