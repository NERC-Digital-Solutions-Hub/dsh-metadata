# DATASET: Stable water isotopes in Western Siberian inland waters

- A part of the SIWA project funded by JPI/NERC (grant NE/M019896/1) focusing on climate impact on carbon emission and export from Siberian inland waters.
- Authors and affiliations span the University of Aberdeen (UK), GET Toulouse (France), Tomsk State University (Russia), and Umeå University (Sweden); collaborative leadership for sampling, analysis, and logistics.

## What the dataset covers and aims

- Stable water isotope data (δ2H and δ18O) collected from Western Siberian inland waters (rivers, lakes, soil solutions) to understand hydrological and carbon-related processes in permafrost and non-permafrost zones.
- Data intended for integration into broader studies of water cycling, with potential use in cross-site comparisons and modeling.

## Responsibilities and data generation governance

- Northern Rivers Institute, UoA (PI Soulsby; Co-I Tetzlaff) planned sampling and coordinated isotope analyses at UoA lab.
- GET Toulouse coordinated sampling logistics in collaboration with UoA, TSU, and UU.
- TSU coordinated sampling campaigns and logistics; team members collected samples from large rivers, lakes, permafrost zones, thaw ponds, suprapermafrost flow, and small rivers across the north-south gradient.
- UU planned sampling campaigns; Serikova contributed to lake sampling in 2016.
- Acknowledgements note contributions for laboratory analysis.

## Sample collection and study design

- Sampling sites include large (>10,000 km²) rivers and lakes in the permafrost and surrounding zones; soil pore waters north of the permafrost boundary.
- Sample types:
  - River water, lake water, floodplain water (flood samples during spring floods)
  - Soil solution from active layer (20–50 cm depth; 10 cm above permafrost)
- Field procedures:
  - River and lake samples collected as grab samples from mid-channel or bank; depth ~0.5 m; shallow thermokarst lakes sampled at ~0.25 m depth.
  - On-site filtration for waters with excess organic matter using sterile filters; initial 2 mL filtrate discarded.
  - Soil samples collected with ceramic cup suction lysimeters; field-filtered to 0.45 μm.
- Sample management:
  - Collected in 3.5 mL glass vials; samples stored in the dark at 4–6°C; shipped to Aberdeen for analysis; archived at UoA after analysis.

## Data analysis and quality control

- Instrument: Los Gatos DLT-100 laser isotope analyzer.
- Precision: ±0.4 ‰ for δ2H and ±0.1 ‰ for δ18O.
- Isotope ratios reported in δ-notation relative to Vienna Standard Mean Ocean Water (VSMOW).
- Quality control performed by Ala-aho; results compiled into a database and traced through the analysis date.

## Data storage, provenance, and traceability

- Samples stored at UoA facilities post-analysis; full archival maintained with sample ID and analysis date.
- Detailed provenance: sample collection dates, analysis dates, and processing steps are recorded to enable traceability.

## Data structure and metadata

- Data file: SIWA_stable_water_isotope_data.txt
- Encoding: UTF-16LE with BOM
- Structure: tabular, one row per unique sample; columns include:
  - T_ID: sample ID associated with vial
  - sample_ID: alternative sample ID
  - lat_N: latitude (WGS84, decimal degrees)
  - long_E: longitude (WGS84, decimal degrees)
  - sample_type: river, lake, flood, soil
  - sample_description: detailed English/Russian description
  - name_engl: English name of water body
  - sampling_date: date of collection (dd/mm/yyyy)
  - analysis_date: date of analysis (dd/mm/yyyy)
  - d2H: δ2H isotope ratio (‰)
  - d18O: δ18O isotope ratio (‰)
- Field descriptions provide:
  - field format (text or numeric), units (e.g., degrees, ‰), and explanations of variables
- The dataset supports geospatial and isotope data integration, with clear data-field semantics and traceable lineage.

## Practical implications for data strategy and usage

- Clear data provenance and cross-institution collaboration support co-ownership and accountability for data products.
- Metadata and structured data file enable discoverability, reproducibility, and interoperability for researchers studying hydrological and biogeochemical processes in Siberian inland waters.
- The explicit documentation of sampling methods, analysis precision, and storage ensures data quality assessment and appropriate use in regional/global comparisons.