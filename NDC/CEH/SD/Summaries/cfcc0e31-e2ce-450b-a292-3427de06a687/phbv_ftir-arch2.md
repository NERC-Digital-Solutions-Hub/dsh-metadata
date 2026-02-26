# Isothermal crystallisation of PHBV-based systems recorded using Fourier transform infrared spectroscopy (FTIR) at various crystallisation temperatures

- Purpose and scope
  - Provides FTIR spectra of Poly(hydroxybutyrate-co-valerate) (PHBV) with varying hydroxyvalerate (HV) content to explore crystallite formation from melt to fully formed film.
  - Targets understanding of crystallisation behavior and material properties relevant to biodegradable packaging.

- Data content
  - ATR-FTIR spectra collected for PHBV with HV contents: 0% (PHB), 7%, 12%, and 21% mol HV.
  - Spectra averaged from 16 measurements per point, recorded over 600–4000 cm^-1, with 4 cm^-1 resolution.
  - Data stored as CSV tables, one file per time point and composition, two columns: wavelength (cm^-1) and absorbance (a.u.). No column names in uploaded data.
  - Baseline-corrected cases indicated by an ending _1 in the file name.

- File naming conventions and structure
  - Naming indicates HV content, temperature, and time from measurement start (e.g., %HVcontent, 1 for 7% HV; temperature marker like tc_90, t-60, 120c; time marker like t-1min, t-2).
  - Suffixes _p2/_p3/_p4 indicate sample positions to assess uniformity.
  - _1 at end of file name signals baseline correction was applied.

- Experimental design and conditions
  - Four HV contents chosen to span a wide range of thermal and crystallisation behavior.
  - Samples melted between kapton sheets, molded, then cooled in liquid nitrogen and equilibrated at specified temperatures below melting point.
  - Measurements taken at multiple positions on each sample, every 1–1.5 minutes during crystallisation.

- Instrumentation and methods
  - Instrument: Thermo Nicolet iS5 FTIR spectrometer with Specac Golden Gate heated stage.
  - Data acquisition software: OMNIC.
  - Baseline correction performed using airPLS (Zhang et al., 2010) in Python scripts.
  - Calibration: standard polystyrene procedure per manufacturer guidelines.

- Data processing and crystallinity metrics
  - Crystallinity indices possible via FTIR peak/ratio methods, including:
    - 1227 cm^-1 (crystalline) / 1180 cm^-1 (amorphous)
    - 1380 cm^-1 reference band / 1186 cm^-1 (amorphous)
    - 1230 cm^-1 (crystalline) / 1453 cm^-1 (reference)
  - These indices enable assessment of crystallinity progression at different crystallisation temperatures and HV contents.

- Temporal and collection details
  - Data collection period: May to October 2021.
  - Location: University of Strathclyde.
  - Samples prepared with consistent protocol; timings of melting, removal, and crystallisation recorded with stopwatch.

- Quality control and consistency
  - Uniform sample preparation: identical powder mass, pressing, and temperature conditions for all measurements.
  - Repeated measurements at each condition to support reproducibility.
  - Baseline correction consistently applied where indicated.

- Relevance to environmental monitoring and policy assessment
  - PHBV is a biodegradable, bacteria-synthesized polymer with potential packaging applications as a sustainable alternative to non-biodegradable plastics.
  - The dataset provides standardized, time-resolved spectroscopic data to evaluate crystallisation behavior, informing material performance, biodegradation potential, and lifecycle implications.
  - By offering clearly defined data formats, processing steps, and crystallinity metrics, the data supports cross-study comparisons and integration with broader environmental monitoring datasets.

- Access, reuse, and references
  - Data supplied as CSV files with clearly described variables and processing steps.
  - Processing reference materials include baseline correction method (airPLS) and crystallinity peak/ratio methods cited in the document:
    - Kann et al. 2014
    - Middleton et al. 2001
    - Xu et al. 2002
    - Zhang et al. 2010 (airPLS baseline correction)
  - Instrumentation and experimental details are provided to enable replication and integration into monitoring workflows.