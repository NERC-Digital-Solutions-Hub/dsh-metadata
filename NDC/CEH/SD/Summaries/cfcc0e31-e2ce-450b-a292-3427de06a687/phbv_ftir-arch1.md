# Isothermal crystallisation of PHBV-based systems recorded using Fourier transform infrared spectroscopy (FTIR) at various crystallisation temperatures

## Overview
- A dataset exploring the formation of PHBV crystallites from melt to film using ATR-FTIR, across different HV contents (degree of hydroxyvalerate) and temperatures, with time-resolved measurements.

## Sample types
- Four HV contents studied: 0% HV (PHB), 7% HV, 12% HV, 21% HV.

## Data and format
- ATR-FTIR spectra collected and averaged (16 spectra per measurement) using OMNIC, across 600–4000 cm-1 with 4 cm-1 resolution.
- Data saved as CSV files with two columns: wavelength (cm-1) and absorbance (a.u.).
- Each file corresponds to a specific time point and polymer chemistry; baseline correction applied in some files.

## File naming and structure
- Naming encodes: HV content, crystallisation temperature, and time from start of measurement.
- End with _1 indicates baseline correction; _p2/_p3/_p4 indicate different sample positions to assess uniformity.

## Experimental procedure
- Sample prep: melt between two kapton sheets, quench in liquid nitrogen, place on heated FTIR stage.
- Spectra collected every 1–1.5 minutes from multiple positions on the sample.
- Instrumentation: Thermo Nicolet iS5 with Specac Golden Gate heated stage; data processed with OMNIC.

## Calibration and quality control
- Calibrated per manufacturer protocol using a polystyrene standard.
- Consistent preparation: identical powder amounts, pressure, melting times, and temperatures; timing tracked with a stopwatch.
- Baseline correction performed using airPLS (Zhang et al., 2010) in Python.

## Data processing and crystallinity assessment
- Baseline-corrected data enabling crystallinity index calculations via peak/line ratios:
  - 1227/1180 cm-1 (crystalline vs amorphous) Kann et al., 2014
  - 1380/1186 cm-1 (reference vs amorphous) Middleton et al., 2001
  - 1230/1453 cm-1 (crystalline vs reference) Xu et al., 2002

## Experimental design
- Temperature range below melting point examined to establish temperature–crystallisation relationships.
- Temporal span from May to October 2021 at the University of Strathclyde.

## Potential analyses for data-driven insights
- Derive crystallinity versus time at each HV content and temperature.
- Compare crystallisation kinetics across HV contents.
- Explore spatial uniformity using multiple sample positions (p2/p3/p4).
- Assess impact of baseline correction on derived metrics.
- Build predictive models of crystallisation behavior as a function of HV content, temperature, and time.

## References (used in the dataset)
- Kann, Y., et al. 2014. FTIR for crystallinity in PHBV.
- Middleton, A.C., et al. 2001. Real-time FTIR studies in polymers.
- Xu, J., et al. 2002. In situ FTIR on melting/crystallization of polyhydroxyalkanoates.
- Zhang, Z.-M., et al. 2010. Baseline correction via airPLS.