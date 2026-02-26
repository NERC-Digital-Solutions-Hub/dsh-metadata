# ReadMe file for SpringCO2Data.csv

- Overview
  - Dataset of CO2 emissions measured from control, artificial urine, and real urine treatments.
  - Study site: orthic podzol in semi-improved upland grassland, Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W), spring 2016.
  - Experimental design: randomised block with multiple plots/chambers.

- Data collection and experimental design
  - Automated greenhouse gas monitoring system in use (LI-COR LI-820).
  - Eight flux measurements per chamber per day from each 1-hour chamber closure.
  - Four gas samples analysed per 1-hour closure; calibration after every fourth sample.
  - Chamber details: basal area 0.25 m²; dimensions 50 cm × 50 cm × 15 cm (L × W × H).
  - Data reflect quality-assessed flux values, not raw gas concentrations.
  - Quality assurance involved inspecting raw files and chromatograms for anomalies; problematic data removed (e.g., gas peak interference).

- Measurements and data structure
  - Timestamp format: dd/mm/yy hh:mm.
  - Columns B–M contain CO2 flux values in mg CO2-C m⁻² h⁻¹.
  - Treatment identifiers in headers: Control, ArtUrine, Urine.
  - Each row/column corresponds to a specific chamber/plot within the randomized block design.

- Data quality and processing
  - Emphasis on quality assurance prior to release; non-qualifying data removed.
  - Data provided are the processed flux measurements suitable for analysis and visualization, not raw gas concentrations.

- Data fields and file structure (summary)
  - Timestamp: date and time of measurement.
  - Flux measurements: eight per chamber per day, across treatments.
  - Treatments: Control, ArtUrine (artificial urine), Urine (real urine).
  - Chamber/plot identifiers embedded in column headers.

- Spatial context and GIS considerations
  - Site coordinates and elevation provided to situate data spatially.
  - To map in GIS, assign plot/chamber locations using the implied plot identifiers; explicit coordinates per chamber are not listed.
  - Data are time-series per chamber; suitable for visualizing spatial variation across plots over time.
  - Units are mg CO2-C m⁻² h⁻¹, enabling standardized spatial-temporal comparisons.

- Usage notes and citation
  - Authors must be acknowledged if data are reused or reproduced.
  - Data pertain to spring 2016 emissions from specified treatments at the stated site and should be interpreted within the experimental design context.