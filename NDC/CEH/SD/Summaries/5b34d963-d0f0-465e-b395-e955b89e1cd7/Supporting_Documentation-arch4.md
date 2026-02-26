# Fieldwork Sampling - Experimental Design and Collection Methods

## Overview
- Seasonal field experiments conducted in Wood Brook, Staffordshire (July 2016, October 2016, February 2017, March 2017).
- Four fluorometers positioned at four sites (sites 1–4) creating three sub-reaches: 1–2, 2–3, and 3–4.
- Reaches characteristics: upstream reaches sand-dominated (1–2 and 2–3), downstream reach gravel-dominated (3–4).

## Experimental Setup
- Reaches and lengths: 12 (1–2) = 239.3 m, 2–3 = 289.2 m, 3–4 = 165.1 m.
- Fluorometer deployment for continuous monitoring of tracer breakthrough curves (BTCs) across all sites.

## Tracers and Injections
- Injections: instantaneous solute tracer injections using conservative fluorescein and reactive resazurin.
- Injections performed before sampling at defined amounts:
  - July: fluorescein 2 g, resazurin 8 g.
  - October, February, March: fluorescein 1.2 g, resazurin 8 g.
- Injection timing and location:
  - July: injection site 180 m upstream of site 1.
  - Other seasons: injection site 250 m upstream of site 1.
  - Injection times: July 18:47:00; October 14:10:00; February 14:09:00; March 14:29:00.
- Tracers measured: fluorescein (conservative), resazurin (reactive), and resorufin.

## Measurement and Calibration
- Calibration:
  - Field calibration immediately prior to tracer injections.
  - Connected loop calibration: same solution flows through all fluorometers.
  - Two-point calibration per tracer: zero (stream water) and fixed concentrations (70 ppb fluorescein, 100 ppb resazurin, 100 ppb resorufin).
  - Calibration readings stabilized over 2–3 minutes.
- Measurement setup:
  - In-situ online fluorometers (GGUN-FL30) with appropriate LED/detector wavelengths.
  - Readings every 10 seconds; fluorometers deployed in the stream for >12 hours to capture BTC tail.

## Data Processing and Corrections
- Recorded BTCs in units of parts per billion (ppb).
- Corrections applied:
  - Temperature and turbidity adjustments following Blaen et al. (2017).
  - Drift and baseline corrections to ensure accurate tail capture.
  - Background corrections: set negative background to zero; non-natural tracers do not occur in streams, so positive backgrounds corrected to zero as needed.
- Data integrity steps ensure BTCs are detectable across sites and seasons.

## Data Structure and Content
- Single dataset file: Fluorescein_resazurin_resorufin_breakthrough_curves_Wood_Brook_UK_2016_2017.csv
- Structure:
  - 64 columns total.
  - For each season/site: Date-Time (GMT), Fluorescein Concentration (ppb), Resazurin Concentration (ppb), Resorufin Concentration (ppb).
  - Metadata indicating season and site positioned above each Date-Time column.
- Data are designed for downstream analysis of multi-tracer BTCs and cross-site comparisons.

## Data Access and References
- References informing methodology:
  - Blaen, P. J. et al. (2017). Multitracer Field Fluorometry: Accounting for Temperature and Turbidity Variability During Stream Tracer Tests.
  - Lemke, D. et al. (2013). On-line fluorometry of multiple reactive and conservative tracers in streams.
- Data provenance includes calibration protocol, measurement cadence, and post-processing steps to ensure reproducibility and comparability across seasons and sites.