# Isothermal crystallisation of PHBV-based systems recorded using Fourier transform infrared spectroscopy (FTIR) at various crystallisation temperatures

## Overview
- Studies isothermal crystallisation of Poly(hydroxybutyrate-co-valerate) (PHBV) with varying hydroxyvalerate (HV) content, using ATR-FTIR to track crystallite formation from melt to fully formed film.
- Data supports analysis of how HV content and crystallisation temperature influence crystallisation dynamics.

## Data content and structure
- Data consists of FTIR spectra saved as CSV files, each representing a time stamp and polymer chemistry.
- Files contain two columns: wavelength (cm-1) and absorbance (a.u.); there are no column names in the data.
- File naming convention encodes: HV content, temperature, and time from the start of measurement; a suffix indicates baseline correction (_1 indicates correction applied).
- Distinctions in samples: phb (0% HV) and phbv samples with various HV contents; _p2, _p3, _p4 indicate different sample positions to reflect uniformity.

## Experimental design and sampling
- HV contents studied: 0% (PHB), 7%, 12%, and 21% HV.
- Experiments conducted at temperatures below the melting point to establish temperature-crystallisation relationships.
- Sample preparation: melt between kapton sheets, pressed in an aluminum mould, then quenched in liquid nitrogen and equilibrated at the target temperature.
- Spectra collection: every 1–1.5 minutes at multiple sample positions; data saved as CSV files; baseline correction performed via airPLS.

## Data processing and crystallinity measures
- Baseline correction applied using the airPLS algorithm (Python-based).
- Crystallinity index can be calculated using established peak ratios, for example:
  - 1227/1180 cm-1 (crystalline vs. amorphous)
  - 1380/1186 cm-1 (reference vs. amorphous)
  - 1230/1453 cm-1 (crystalline vs. reference)
- The dataset provides a framework for time-resolved crystallisation analysis across HV contents and temperatures.

## Temporal coverage and instrumentation
- Data collection period: May to October 2021.
- Instrumentation: Thermo Nicolet iS5 FTIR spectrometer with Specac Golden Gate heated stage; spectra processed with OMNIC software.
- Spectra collected over time during crystallisation at defined temperatures.

## Calibration and quality control
- Calibration performed per manufacturer protocol using polystyrene standards.
- Quality control ensured by uniform sample preparation (consistent powder amount, pressure, and temperature) and precise timing (stopwatch-based records for melting, removal, and crystallisation).

## Metadata and data discoverability
- File naming provides traceability for HV content, temperature, time, and sample position, facilitating reproducibility and cross-study comparison.
- Data range: 600–4000 cm-1 with a spectral resolution of 4 cm-1; 16 FTIR spectra per measurement averaged by OMNIC software.

## Reuse and governance considerations for data leaders
- Standardised data capture, time-resolved sampling, and baseline-corrected spectra support reproducibility and cross-study integration.
- Availability of derived crystallinity indices enables meta-analyses of crystallisation behaviour across HV contents and processing conditions.
- Clear naming conventions and documented processing steps (baseline correction method, sample preparation protocol, and calibration approach) enhance data governance and discoverability.
- Potential for integration with complementary polymer datasets to broaden understanding of biodegradable polymer crystallisation for packaging applications.

## References
- Kann, Y., M. Shurgalin, R.K. Krishnaswamy, FTIR spectroscopy for analysis of crystallinity of poly(3-hydroxybutyrate-co-4-hydroxybutyrate) polymers and its utilization in evaluation of aging, orientation and composition, Polymer Testing, 2014.
- Middleton, A.C., et al., Real-Time FTIR and WAXS Studies of Drawing Behavior of Poly(Ethylene Terephthalate) films, J. Appl. Polym. Sci., 2001.
- Jun Xu, et al., In situ FTIR study on melting and crystallization of polyhydroxyalkanoates, Polymer, 2002.
- Zhang, Z.-M., et al., Baseline correction using adaptive iteratively reweighted penalized least squares, Analyst, 2010.