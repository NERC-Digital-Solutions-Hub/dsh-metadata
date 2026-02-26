# DATASET: Stable water isotopes in Western Siberian inland waters

## Overview
- This dataset is part of the SIWA project funded by JPI/NERC (grant NE/M019896/1), focused on climate impact on carbon emission and export from Siberian inland waters.
- Authors and affiliations include researchers from the University of Aberdeen (UoA), GET Toulouse, Tomsk State University (TSU), and Umeå University (UU).
- The dataset documents stable water isotopes in Western Siberian inland waters, including rivers, lakes, thaw ponds, soil solutions, and related sampling across permafrost and non-permafrost zones.

## Data generation and governance
- Roles and collaboration:
  - UoA (Northern Rivers Institute): planned sampling campaigns, coordinated isotope analysis, performed quality control, and compiled results into a database (Ala-aho contributed to sample preparation and archiving).
  - GET Toulouse: planned sampling campaigns and coordinated water sampling logistics.
  - TSU: planned sampling campaigns and coordinated water sampling logistics.
  - UU: planned sampling campaigns and conducted lake water sampling (2016).
- Quality assurance:
  - Rigorous quality control of analyses; results aggregated into a centralized database.
- Data scope and provenance:
  - Large geographic coverage including major rivers and lakes in the Western Siberian inland water system; collaboration among multiple institutions ensured standardized sampling and coordination.

## Sample collection and handling
- Sample types and collection:
  - River water: grab samples from the middle of the channel or banks at about 0.5 m depth.
  - Lakes: collected from a boat at ~0.5 m depth (thermokarst lakes shallower, sampling at ~0.25 m).
  - Flooded areas: grab samples from boats.
  - Soil solutions: collected with ceramic cup suction lysimeters at depths 20–50 cm (typically ~10 cm above permafrost).
- Filtration and handling:
  - On-site filtration using sterile acetate cellulose filters when organic matter was present; first 2 mL of filtrate discarded.
  - Soil solutions filtered in the field (0.45 μm filters).
- Sample preparation and archiving:
  - Samples prepared, stored, and archived for analysis; detailed field protocols are referenced (Raudina et al. 2017).
- Sample scale:
  - Rivers and lakes across large geographic areas, including permafrost and non-permafrost zones.

## Data analysis and measurements
- Instrumentation:
  - Isotope analyses performed with a Los Gatos DLT-100 laser isotope analyser.
- Precision:
  - δ2H: ±0.4 ‰; δ18O: ±0.1 ‰.
- Isotope notation:
  - Ratios reported in δ-notation relative to Vienna Standard Mean Ocean Water (VSMOW).

## Sample storage and archiving
- Storage conditions:
  - Samples stored in the dark at 4–6 °C and shipped to the University of Aberdeen for analysis.
  - Post-analysis storage maintained at UoA facilities.
- Traceability:
  - Samples archived by analysis date and sample ID to enable traceability.

## Data structure and metadata
- File details:
  - File name: SIWA_stable_water_isotope_data.txt
  - Encoding: UTF-16LE (with BOM)
  - Structure: tabular data where each row represents a unique sample; columns describe data fields/attributes.
- Data fields and metadata descriptions:
  - T_ID: Sample ID linking to vial name; text format.
  - sample_ID: Alternative sample ID linking to vials; text format.
  - lat_N: Northern latitude (WGS 1984); floating point; decimal degrees.
  - long_E: Eastern longitude (WGS 1984); floating point; decimal degrees.
  - sample_type: Type of sampled inland water; text/factor (e.g., flood, lake, river, soil).
  - sample_description: Detailed English/Russian sample description (e.g., river/lake name, flood context); text.
  - name_engl: English name of the water body ( rivers/lakes ); text.
  - sampling_date: Date of sample collection; text (dd/mm/yyyy).
  - analysis_date: Date of analysis; text (dd/mm/yyyy).
  - d2H: Deuterium isotope ratio (δ2H); numeric; unit ‰.
  - d18O: Oxygen-18 isotope ratio (δ18O); numeric; unit ‰.

## Acknowledgements
- Laboratory analysis performed by Jonathan J. Dick and Audrey Innes (UoA).