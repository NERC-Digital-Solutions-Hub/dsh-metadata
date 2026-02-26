# Collection, generation methods and quality control

- Overview
  - Describes collection, analysis methods, and quality controls for reservoir sediment cores from Cowbury Dale and Higher Swineshaw reservoirs.
  - Focuses on data generation (geochemical, mineralogical and granulometry) and how data are processed for reliability and comparability, suitable for GIS-based visualization and analysis.

- Study sites and samples
  - Reservoirs: Cowbury Dale Reservoir (Carrbrook, Tameside) and Higher Swineshaw Reservoir (Stalybridge, Tameside).
  - Sampling: five cores per site taken along the reservoir long axis from inlet to dam wall; the deepest, uninterrupted core used for analysis.
  - Collection date: Cowbury Dale core4 collected 06 August 2018; Higher Swineshaw core5 collected 11 December 2018.
  - Location references: precise OS Grid References provided for each site.
  - Core processing: gravity corer used; extrusion at 2.5 mm contiguous intervals.

- Methods and instrumentation
  - X-ray fluorescence (XRF): elemental geochemistry measured with XEPOS 3 Energy-dispersive XRF; samples prepared by light grinding, pressing, and measurement in a helium atmosphere with Pd and Co excitation radiation; daily standardization with 18 certified reference materials.
  - Loss on ignition (LOI) and organic content: LOI determined by LOI measurements (105°C overnight followed by 450°C for 4.5 h); LOI values also estimated via Near Infrared Spectrometry (NIRS) cross-calibrated against direct LOI measurements.
  - NIRS cross-calibration: NIRS reflectance measured on 1-cm depth samples using a BRUKER MPA FT-NIR spectrometer; strong correlation (r2 = 86%) between NIR-derived LOI and direct LOI measurements; LOI concentration predicted from NIRS data.
  - Particle size analysis: laser granulometry using Coulter LS 13 320; samples digested in H2O2 to remove organics, dispersed in Na6O18P6, and sonicated; three repeats per sample with outliers removed.
  - Data processing: standard geometric statistics (Folk and Ward, 1957) via GRADISTAT 8.0 to report D50 (median particle diameter).
  - Quality controls: regular calibration checks for the Coulter analyzer; replication and outlier removal to reduce intra-sample noise.

- Data structure, variables and units
  - Depth in core: depth (cm).
  - Loss On Ignition (XRF estimated): loi_xrf (%).
  - Near infrared LOI: nir_loi (%).
  - Elemental analyses: concentrations represented as d50 (element) with units mg/g or µg/g for various elements (e.g., Mg, K, Ca, Fe, Al, Si, P, S, etc.); notes indicate missing values are blank.
  - Particle size: d50 (mm) representing median particle diameter.
  - Missing values: indicated by blank spaces in the dataset.
  - Elemental data note: concentrations are provided for multiple elements with varying units (mg/g or µg/g) depending on concentration levels.

- Data acquisition workflow and quality control
  - Core selection focuses on deepest undisturbed segment per site.
  - Instrument calibration and standardization procedures are performed daily for XRF; LOI via NIRS cross-calibrated with direct LOI measurements.
  - Multiple repeats for particle size measurements; outlier reduction applied to improve precision.
  - Documentation includes references to methodological standards and calibration approaches.

- Datasets and provenance
  - Source files include:
    - cowburydale_2018_core4.csv
    - higherswineshaw_2018_core5.csv
  - References for methods and calibration approaches linked to established literature (e.g., Blott & Pye, Boyle, Folk & Ward, Schillereff et al.).

- GISa and data-usage considerations
  - Highly suitable for map-based visualization of geochemical and granulometry profiles across reservoir cores.
  - Depth-encoded data enable vertical cross-sections and 3D representations along the reservoir axis.
  - Important to standardize units (mg/g vs µg/g) and clearly handle missing values when integrating datasets into GIS.
  - Coordinate data (OS Grid References) support precise geospatial alignment and layering with other spatial datasets.