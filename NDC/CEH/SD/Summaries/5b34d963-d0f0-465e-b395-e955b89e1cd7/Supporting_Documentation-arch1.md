# Fieldwork Sampling - Experimental Design and Collection Methods

## Overview
- Seasonal field experiments conducted in Wood Brook, Staffordshire during July 2016, October 2016, February 2017, and March 2017.
- Four fluorometer sites (1–4) creating three sub-reaches: 1–2 (239.3 m), 2–3 (289.2 m), and 3–4 (165.1 m).
- Reaches 1–2 and 2–3 are sand-dominated; reach 3–4 is gravel-dominated.

## Tracers and Dosing
- Injections used: conservative fluorescein and reactive resazurin (with resorufin detection).
- Doses per season: July (2 g fluorescein + 8 g resazurin); October, February, March (1.2 g fluorescein + 8 g resazurin).
- Injection site located 180 m upstream of site 1 in July; 250 m upstream in other seasons.
- Injections performed at specific times: July 18:47, October 14:10, February 14:09, March 14:29.

## Measurements
- Breakthrough curves (BTCs) for fluorescein, resazurin, and resorufin measured at all four sites.
- Fluorometers remained in the stream for 12+ hours to adequately capture curve tails.

## Calibration
- Field calibration conducted immediately prior to tracer injections in a connected loop.
- Calibration solution concentrations: zero (stream water), 70 ppb fluorescein, 100 ppb resazurin, 100 ppb resorufin.
- Calibration repeated for 2–3 minutes until readings stabilized.

## Data Recording and Processing
- BTCs recorded in units of parts per billion (ppb).
- Corrections applied for temperature and turbidity; background corrections made when BTCs were detected but background was below zero (or above zero for non-natural tracers).
- Drift corrections applied across the breakthrough curves.

## Analytical Methods
- In-situ analysis with on-line field fluorometers (GGUN-FL30, Albillia Sàrl, Switzerland).
- Wavelengths: fluorescein (470 nm), resazurin (570 nm), resorufin (525 nm).
- Instruments configured to measure every 10 seconds; calibrated with stream water prior to injections.

## Data Structure
- Single CSV file: Fluorescein_resazurin_resorufin_breakthrough_curves_Wood_Brook_UK_2016_2017 (64 columns).
- Repeated column headings for each season/site: Date-Time (GMT), Fluorescein (ppb), Resazurin (ppb), Resorufin (ppb).
- Season and site identifiers placed above each Date-Time column.

## References
- Blaen, P. J., et al. (2017). Multitracer Field Fluorometry: Accounting for Temperature and Turbidity Variability During Stream Tracer Tests. Water Resources Research.
- Lemke, D., et al. (2013). On-line fluorometry of multiple reactive and conservative tracers in streams. Environmental Earth Sciences.