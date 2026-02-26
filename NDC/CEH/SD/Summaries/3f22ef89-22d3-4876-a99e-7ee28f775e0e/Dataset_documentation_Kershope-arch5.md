# Solute concentrations in water samples from clearfelled and standing Sitka spruce ( Picea sitchensis ) forest ecosystems, Kershope Forest

- Overview
  - A dataset from Kershope Forest, Cumbria, England, examining solute concentrations in drainage water from six plots in Block 1 of a drainage experiment on a peaty gley soil.
  - Comparison between standing forest and clearfelled plots (three felled in 1983; three controls).
  - Timeframe: drainage water sampling 1981–1987; water sample collection 1981–1985 (varied by component). Site planted with Sitka spruce since 1948.
  - Research context: relates to nutrient fluxes and soil fertility changes following clearfelling; hydrological pathways analyzed to understand sources and impacts on the next forest rotation.

- Data scope and content
  - Solutes measured in drainage water: potassium, calcium, magnesium, iron, sodium, aluminium, phosphate, nitrate, ammonium, chloride, sulphate; plus pH, suspended solids (TSS), and total organic carbon (TOC).
  - Additional water sources sampled: soil solution samplers, lysimeters, rainfall, stemflow, throughfall, Knapp throughflow (note: Knapp data quality not considered reliable), and needle tray throughfall.
  - Primary data products:
    - Drainsker.csv: solute data from six main drains across the plots (with sample codes and discharge measurements).
    - Soilsker.csv: solute data from various samplers (horizons and lysimeters) associated with the plots.
    - Kershope_sampling_points.csv: sampling locations and descriptive metadata for the points listed in the datasets.
    - Kershope_codes.csv: key to sample codes mapping (plot, horizon, sample type, felled status, etc.).
    - Drain information: metadata for each plot (_Block, Felled status, Drain spacing and depth_).
  - Data fields include sampling occasion/date, sample codes, discharge (m3 s-1), ion concentrations (mg L-1), pH, TOC (mg L-1), TSS (mg L-1), and various metadata descriptors.

- Sampling design and methods
  - Study design: six plots in Block 1; three plots felled (1983) and three unfelled; drains from each plot convey drainage water to a main exit drain with a sampling point protected by a 2 m PVC pipe to capture flow; instantaneous discharge recorded with a V-notch weir; occasional flood sampling.
  - Water sources and sampling frequency:
    - Drainage water: weekly sampling (1981–1987).
    - Soil solution samplers and lysimeters: fortnightly sampling.
    - Rainfall: weekly bulk precipitation samples.
    - Stemflow and throughfall: regular collection with bulked samples every two weeks.
    - Needle trays: biweekly collection.
  - Site and soil description: upland peaty gley soils (Cambic stagnohumic gleys), shallow water table seasonally, slopes 1–5 degrees, altitude ~225 m.
  - Analysis methods: chemical analyses conducted at Merlewood Chemical Analysis Section; pH measured in sub-sample; filtration and then analysis by atomic absorption spectrophotometry (Ca, Mg, Al, Fe), flame emission (K, Na), phosphate by molybdenum blue, ammonium by indophenol blue, chloride by thiocyanate (early years) and later by ion chromatography; nitrate determined via reduction methods; sulphate by turbidimetric/barium chloride methods; TOC and TSS by standard methods.
  - Data quality notes: equivalence checks between old and new methods for some ions; Knapp throughflow data flagged as not reliable; some samples marked as no sample analysed (-1); data across methods may require harmonization for cross-year comparisons.

- Geographic and temporal coverage
  - Geographic: Kershope Forest, near Crookburn Hill Drainage Experiment, Cumbria, England.
  - Plot/block configuration: 6 plots in Block 1 with differing drain spacings and depths; three felled in 1983; overall design intended to trace nutrient flux pathways through standing vs felled forest systems.
  - Temporal: drainage water data collected 1981–1987; water samples collected through various components from 1981–1985 (depending on the sub-dataset); felled period included within the study window.

- Data governance, access, and usability considerations for Data Stewards
  - Data formats: primary data stored as CSV files (Drainsker.csv, Soilsker.csv, Kershope_sampling_points.csv, Kershope_codes.csv, Drain information).
  - Metadata provisions: detailed field descriptions, sample codes, horizons, plot/felled status, sampling dates, units, and sampling point mappings provided to support discoverability and reuse.
  - Data organization and traceability: explicit mappings between sample codes and site/horizon descriptors; sampling-point IDs linked to plots and blocks; references for further reading and provenance included.
  - Potential data management challenges:
    - Incomplete or missing samples indicated by codes like -1; some data (Knapp throughflow) deemed unreliable; multiple sampling methods and older analytical techniques may require harmonization.
    - Legacy data with varying methods over time necessitates careful metadata interpretation to ensure comparability.
  - Reuse opportunities:
    - Hydrological nutrient flux analyses related to forest management (clearfelling effects on soil fertility and drainage chemistry).
    - Cross-dataset integration of drainage, soil solution, rainfall, stemflow, throughfall, and litter/needle throughfall for ecosystem nutrient cycling studies.
  - Key references and provenance:
    - Related publications (Forestry, Journal of Hydrology) and methodological references (Allen 1989; Rowland 1983; Knapp 1973; Pyatt et al. 1985) to support data interpretation and methodological alignment.

- Constraints and notes for data users
  - Spatial coordinates available in sampling-point metadata; some tables describe complex sampling codes and horizons that must be correctly interpreted.
  - Units standardized to mg L-1 for solutes, m3 s-1 for discharge, and pH units as standard; ensure unit consistency when aggregating across components.
  - Users should consult dataset descriptions and code mappings to correctly align felled status, block, drain spacing/depth, and sample sources during analysis.