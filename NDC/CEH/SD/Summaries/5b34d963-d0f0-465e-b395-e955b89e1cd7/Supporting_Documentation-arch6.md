# Fieldwork Sampling - Experimental Design and Collection Methods

- Seasonal tracer experiments conducted in Wood Brook, Staffordshire (July 2016, Oct 2016, Feb 2017, Mar 2017)
- Four fluorometers deployed at four sites (1-4) creating three sub-reaches (1-2, 2-3, 3-4)
- Upstream reachs: sand-dominated (1-2, 2-3); downstream reach: gravel-dominated (3-4)
- Reach lengths: 239.3 m (1-2), 289.2 m (2-3), 165.1 m (3-4)

## Experimental Design

- Tracer injections immediately before release: conservative fluorescein and reactive resazurin
- Injection site located 180 m upstream of site 1 (July) and 250 m upstream (other seasons)
- Reaches sampled via breakthrough curves at all four sites

## Tracers and Injections

- Tracers used: fluorescein (conservative), resazurin (reactive), and resorufin (metabolite)
- Injections: instantaneous solute injections with 1.2 g fluorescein and 8 g resazurin (July) vs 2 g fluorescein and 8 g resazurin (other seasons)
- Breakthrough measured for fluorescein, resazurin, and resorufin at all sites

## Data Collection and Calibration

- Field fluorometers calibrated immediately before tracer injections
- Calibration in a connected loop with equal flow through all fluorometers
- Two-point calibration per tracer: zero (stream water) and fixed concentrations (70 ppb fluorescein; 100 ppb resazurin; 100 ppb resorufin)
- Calibration measurements run for 2–3 minutes per solution
- Fluorometers configured to measure every 10 seconds; left in stream for 12+ hours to capture tail

## Data Processing, Corrections, and QA

- Recorded units: parts per billion (ppb)
- BTCs corrected for temperature and turbidity (per Blaen et al., 2017)
- Data clipped at baseline before/after tail; drift corrected across BTC
- Background corrections: set to zero when background would otherwise be negative; corrected to zero for non-natural tracer values

## Data Structure and File Details

- Single CSV dataset: Fluorescein_resazurin_resorufin_breakthrough_curves_Wood_Brook_UK_2016_2017 (64 columns)
- Four column headings repeated for each season/site: Date-Time (GMT), Fluorescein Concentration (ppb), Resazurin Concentration (ppb), Resorufin Concentration (ppb)
- Season and site identifiers located above each Date-Time column
- References: Blaen et al. 2017; Lemke et al. 2013

## Instrumentation and Analytical Methods

- On-line fluorometers: GGUN-FL30 (Albillia Sàrl, Switzerland) with LEDs/detectors for excitation/measurement of the three tracers
- Excitation/emission wavelengths: fluorescein (470 nm), resazurin (570 nm), resorufin (525 nm)
- Measurement cadence: every 10 seconds; data streamed during the experiment

## References

- Blaen, P. J. et al. 2017. Multitracer Field Fluorometry: Accounting for Temperature and Turbidity Variability During Stream Tracer Tests. Water Resources Research.
- Lemke, D. et al. 2013. On-line fluorometry of multiple reactive and conservative tracers in streams. Environmental Earth Sciences.

## Data Use and Integration Considerations

- Multi-season, multi-site BTC dataset suitable for cross-season comparisons and integration with other hydrological or tracer data
- Enables self-serve exploration of tracer breakthrough behavior, with QA/QA-adjusted values and clear metadata about calibration and corrections
- Beneficial for data-support tasks such as verifying data quality, aligning with other datasets, and creating dashboards or analyses of tracer dynamics across reaches and seasons