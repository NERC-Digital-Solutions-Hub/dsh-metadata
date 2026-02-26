# The Fourier Transform Infrared Spectroscopy (FTIR) spectra of poly(hydroxybutyrate)-based systems with clay additives changing crystallisation kinetics recorded at ambient temperature

## Overview
- Describes supplementary information for a dataset on PHB-based systems with clay additives, using ATR-FTIR to study crystallite formation from melt to fully formed film at ambient temperature.
- Focuses on how filler chemistry (Cloisite 25A and Cloisite 10A) influences PHB crystallisation.

## Data content and structure
- PHB polymer with two clay additives studied at 0–5 wt% to assess their effect on crystallisation.
- FTIR spectra collected at various times, with spectra averaged from 16 scans per measurement.
- Data are organized by polymer chemistry, additive, time stamp, and sample position.
- Spectra cover the 600–4000 cm⁻¹ range with a spectral resolution of 4 cm⁻¹.
- Data are presented as CSV files with two columns: wavelength (cm⁻¹) and absorbance (a.u.). No column headers are provided in the uploaded files.

## File formats and naming
- File format: CSV.
- Columns: A = wavelength (cm⁻¹); B = absorbance (a.u.).
- Naming convention: % additive, PHB, sample number, position number (example: 5pc_Clay_10A_PHB_s1_p3).
- Each file corresponds to a specific time point and polymer chemistry.

## Temporal coverage and collection details
- Data collected May–October 2021.
- Spectra recorded at multiple crystallisation times and positions within each sample.

## Experimental design and methods
- Additives: Cloisite 25A (C25A) and Cloisite 10A (C10A).
- Concentrations: 0–5 wt% additive.
- Temperature regime: Below polymer melting temperature to establish temperature-crystallisation relationships.
- Sample preparation: Melting PHB between two Kapton sheets, placed in an aluminum oval mold, then cooled/quenched in liquid nitrogen before FTIR measurement.
- Spectra collection: ATR-FTIR using a diamond crystal; measurements taken at various positions on the sample.

## Instrumentation and calibration
- FTIR instrument: Thermo Nicolet iS5 with Specac Golden Gate heated stage.
- Software: OMNIC.
- Calibration: Manufacturer’s standard protocol using polystyrene standard.

## Data processing and quality control
- Baseline correction: Applied using the airPLS algorithm (Zhang et al., 2010) via Python scripts.
- Quality control: Consistent sample preparation (same powder amount, pressure, temperature); timing controlled with a stopwatch for melting, removal, and crystallisation records.

## Metadata and provenance
- Variables described (Table 1): Wavelength (cm⁻¹) and Absorbance (a.u.).
- Each dataset entry corresponds to a specific time stamp, additive, sample, and position, enabling traceability across conditions.

## GIS-relevant considerations and potential uses
- Although no geographic coordinates are provided, sample positions (p3, etc.) enable spatial interpretation within a material, suitable for map-based visualization of spectral properties across a sample.
- Potential GIS workflow:
  - Import CSV data and attach metadata (additive type, concentration, sample, position, time).
  - Select key spectral features (wavenumbers) indicative of PHB crystallisation.
  - Create spatial layers (rasters) representing absorbance at chosen wavenumbers across sample positions.
  - Build time-enabled maps to visualize crystallisation kinetics under different additives and concentrations.
  - Integrate with temperature data to analyze temperature-crystallisation correlations.
- Data could support decision-making for material design and packaging applications by visualizing how additives influence crystallinity distribution over time.

## Limitations and caveats
- Absorbance units are arbitrary (a.u.).
- Data files contain no headers, requiring careful handling during import.
- Spatial information is limited to discrete sample positions rather than true geospatial coordinates.

## References
- Baseline correction method: adaptive iteratively reweighted penalized least squares (airPLS) as cited (Zhang et al., Analyst, 2010).