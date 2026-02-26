# UK water chemistry and greenhouse gas emissions study, LOCATE, 2021-2022: Supporting information

- Objectives and scope
  - LOCATE is a multidisciplinary NERC project to understand carbon flow from land into the ocean.
  - Aims: characterise diurnal greenhouse gas emissions from inland water bodies and assess how water body type and seasonality affect emissions.
  - Methods: deploy floating chambers on selected UK waterbodies for 24 hours to quantify emitted GHGs; compare initial and 24-hour gas samples.

- Sampling campaign and locations
  - Fieldwork conducted across the UK from July 2021 to March 2022.
  - Sampling sites included ponds, streams, lochs, dykes, broads, and wetlands chosen for geographical and land-type variation.
  - Detailed site information available in Table 1 and Figure 1 (site names, types, dates, coordinates).

- In-field collection and sample handling
  - Water samples collected for DOC/TdN, TP, and SRP using a 60 ml syringe; filtration and storage specifics for each analyte described.
  - Physicochemical measurements taken in the field: pH, conductivity, DO, temperature using calibrated probes; multiple readings taken for temperature to compute an average.
  - Floating chambers
    - Constructed from inverted basins with floats; covered to minimize temperature effects.
    - Chambers deployed in duplicate or triplicate at sites to trap air above water; gas collected after 24 hours via a syringe and stored in Exetainer vials.
  - Dissolved gas sampling (headspace)
    - Gas samples collected at time zero using a water-air equilibration method and stored for laboratory analysis.
  - Sample storage timelines
    - TP, SRP, and filtered samples: stored at -18°C.
    - DOC/TdN/UV-Vis samples: stored at 4°C and analyzed within a week.
    - GHG samples: stored at room temperature until batch analysis.

- Laboratory analytics and methods
  - DOC and TdN
    - Analyzed with Shimadzu TOC-LCPH (with TNM L unit) using 680°C combustion, acidification, and sparging.
    - NPOC measured as DOC; quality controls included standards, blanks, and duplicate measurements with CV checks.
  - UV/Vis and SUVA
    - Absorbance measured from 230 to 800 nm; SUVA254 calculated to indicate DOC aromaticity.
  - Total Phosphorus (TP) and Soluble Reactive Phosphorus (SRP)
    - TP: digestion with potassium persulfate, followed by acid molybdate-blue colorimetric assay; AQ2 analyzer calibrated with multiple standards.
    - SRP: filtered samples analyzed with the same colorimetric method on AQ2.
  - Greenhouse gases
    - Dissolved GHGs analysed with Agilent 7890B GC (μECD for N2O; FID for CH4 and CO2).
    - Concentrations derived from peak areas and calibrated with multi-point standards; results reported as ppmv and converted to µg L⁻¹ using Henry’s law.
  - Data products and units
    - Data structured in MERLIN 2022-2023 format: sampling information (columns A–F), field physicochemical data (G–M), and laboratory results (O–AD).
    - Column descriptions and units provided (e.g., Conductivity in µS/cm, pH, DO in mg/L, CH4_C/CO2_C/N2O_N in µg/L or ppmv, etc.).
  - Example data points
    - Chambers presence (Yes/No), CH4_C, CO2_C, N2O_N concentrations, and chamber-specific averages (0 h and 24 h) where available.

- Data structure, metadata, and quality controls
  - Dataset organization includes site name, type, date, location (latitude/longitude), time, and a comprehensive suite of measured parameters.
  - Table 3 provides detailed column headings, decimal places, and units for all variables.
  - Quality assurance
    - Calibration curves and blanks included for each analytical run.
    - Replicates and duplicate measurements used to ensure precision; outliers handled by averaging the best two measurements.
  - Dataset completeness and exclusions (Table 4)
    - Documented excluded measurements with dates, determinants (e.g., time, DO_temp, pH, CO2_2), and reasons (e.g., not recorded, sample contamination, missing samples).
    - Exclusions illustrate data quality management and rationale for omitting incomplete or compromised data.

- Acknowledgments and references
  - Acknowledges permissions and sampling access from Norfolk Wildlife Trust, Historic Environment Scotland, Scottish Wildlife Trust, and Dŵr Cymru Welsh Water.
  - References methods for SUVA and downstream CO2 calculations used in the analyses.