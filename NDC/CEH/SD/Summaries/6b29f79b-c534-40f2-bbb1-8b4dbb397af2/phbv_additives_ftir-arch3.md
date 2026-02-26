# The Fourier Transform Infrared Spectroscopy (FTIR) spectra of poly(hydroxybutyrate)-based systems with clay additives changing crystallisation kinetics recorded at ambient temperature

- Purpose and scope
  - Presents FTIR spectra of Poly(hydroxybutyrate) (PHB) with two clay additives (Cloisite 25A [C25A] and Cloisite 10A [C10A]) to explore how filler chemistry affects crystallisation from melt to fully formed film.
  - Aims to understand crystallite formation within PHB–additive polymer matrices over time.

- Data content
  - FTIR spectra collected using Attenuated Total Reflectance (ATR-FTIR) with a diamond crystal.
  - Spectra captured at various crystallisation times and polymer chemistries; data saved as CSV files.
  - Each CSV contains two columns: wavelength (cm−1) and absorbance (a.u.). Column names are not provided in the files.
  - Data represent an average of 16 FTIR spectra per measurement (via OMNIC) across a 600–4000 cm−1 range with 4 cm−1 spectral resolution.
  - Example file naming: 5pc_Clay_10A_PHB_s1_p3, encoding additive, PHB, sample, position.

- Methodology and instrumentation
  - Sample preparation: melt PHB with powder, pressed between two Kapton sheets using an aluminium mould; rapidly cooled in liquid nitrogen; equilibrated at ambient temperature for measurement.
  - Instrumentation: Thermo Nicolet iS5 FTIR with Specac Golden Gate heated stage; OMNIC software for data processing.
  - Calibration: standard polystyrene calibration protocol.
  - Data processing: baseline correction performed using the adaptive iteratively reweighted penalized least squares (airPLS) method; Python scripts used for processing.

- Experimental design
  - Additives: two clay types, C25A and C10A; chosen for non-toxicity and to probe effects of small chemical changes on crystallisation.
  - Composition: PHB with 0–5 wt% additive; measurements conducted at temperatures below PHB melting to establish temperature–crystallisation relationships.

- Quality control and provenance
  - Consistent preparation protocol across samples; identical melting/removal timing recorded with a stopwatch.
  - All samples prepared with the same powder, pressure, and temperature conditions prior to measurements.
  - Data includes a documented reference for baseline correction methodology (Zhang et al., 2010).

- Metadata, data governance, and reuse considerations (monitoring framework lens)
  - Strengths: explicit experimental details, instrument used, calibration approach, and baseline correction method; standardized data collection and averaging procedures.
  - Gaps and considerations for monitoring frameworks:
    - CSV files lack explicit column headers, which can hinder automated ingestion and interpretation.
    - Metadata such as exact crystallisation times, temperatures, sample IDs beyond the file name, and unit conventions should be clearly captured in a separate metadata record.
    - Underlying raw spectra are not provided (only averaged spectra per measurement); for full auditability and re-analysis, raw data and processing scripts would be valuable.
    - Data governance aspects (data sharing, versioning, and data provenance beyond the baseline method) could be strengthened to support transparent monitoring and reuse.

- Relevance to environmental health monitoring
  - While focused on polymer crystallisation, the dataset supports monitoring framework needs for material property surveillance relevant to environmental impact assessments (e.g., biodegradability performance and safe material choices in packaging).
  - Provides a reproducible measurement protocol and standardized data processing approach that could inform similar monitoring datasets in environmental health contexts.

- Reference
  - Zhang, Zhi-Min; Chen, Shan; Liang, Yi-Zeng. Baseline correction using adaptive iteratively reweighted penalized least squares, Analyst, 2010.