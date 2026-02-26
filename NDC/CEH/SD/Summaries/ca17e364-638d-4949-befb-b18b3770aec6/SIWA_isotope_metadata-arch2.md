# DATASET: Stable water isotopes in Western Siberian inland waters

## Overview and aim
- Part of the JPI/NERC SIWA project (NE/M019896/1): "Climate impact on the carbon emission and export from Siberian inland waters".
- Purpose: generate and provide stable water isotope data (δ2H, δ18O) from Western Siberian inland waters to assess environmental condition and climate impacts over time using a consistent, standardised format.
- Supports monitoring and scrutiny of environmental health and policy performance through time by enabling cross-dataset comparisons and integration with other data.

## Collaborators and responsibilities
- University of Aberdeen (UoA, Northern Rivers Institute, School of Geosciences)
  - Soulsby (PI) and Tetzlaff (Co-I) planned sampling campaigns and coordinated isotope analysis at UoA lab.
  - Ala-aho (Postdoc) prepared samples, archived them, performed QC, and assembled the dataset.
- Géosciences Environnement Toulouse (GET)
  - Pokrovsky (PI) planned sampling campaigns and coordinated water sampling logistics with UoA, TSU, and UU.
- Tomsk State University (TSU)
  - Kirpotin (PI) planned sampling campaigns and coordinated logistics with GET, UoA, UU.
  - Manasypov, Lim, Krickov, Vorobyev, Kolesnichenko, Loiko contributed to sampling across rivers, lakes, soils (permafrost and thaw zones).
- Umeå University (UU)
  - Karlsson (PI) planned sampling campaigns; Serikova (PhD student) planned/performed lake sampling in 2016 and participated in river sampling.
- Acknowledgements for lab analysis support (Dick, Innes, UoA).

## Sampling and study coverage
- Water bodies and environments sampled:
  - Large rivers and lakes across Western Siberian inland waters; thaw ponds; suprapermafrost flow; permafrost boundary areas; soils in active layer.
- Sampling approaches:
  - Rivers: grab samples from mid-channel when possible (bridge or bank) at about 0.5 m depth; avoid stagnant water.
  - Lakes: collected from a boat at about 0.5 m depth; thermokarst lakes are very shallow (0.5–1 m).
  - Flooded areas: grab samples from boats.
  - Soil solutions: ceramic cup suction lysimeters at depths 20–50 cm (typically ~10 cm above permafrost table); filtered in the field (0.45 μm) with discard of the first 2 mL filtrate.
- Reference for soil sampling details: Raudina et al. (2017).

## Data collection, analysis, and storage
- Isotope analysis:
  - Instrument: Los Gatos DLT-100 laser isotope analyser.
  - Precision: δ2H ± 0.4 ‰; δ18O ± 0.1 ‰.
  - Reporting: δ-notation relative to Vienna Standard Mean Ocean Water (VSMOW).
- Sample storage and traceability:
  - Stored in the dark at 4–6 °C; shipped to Aberdeen for analysis; post-analysis storage at UoA.
  - Archiving linked to analysis date and sample ID for traceability.
- Data quality:
  - On-site QA during sampling; quality control of analytical results; systematic archiving and traceable storage.

## Data structure and file description
- Data file: SIWA_stable_water_isotope_data.txt
- Encoding: UTF-16LE (with BOM)
- Structure: tabular dataset; each row is a unique sample; columns capture data fields/attributes.
- Key fields described (example):
  - T_ID: sample ID linking to vial identifiers (text)
  - sample_ID: alternative sample ID (text)
  - lat_N: northern latitude (decimal degrees)
  - long_E: eastern longitude (decimal degrees)
  - sample_type: water type (flood, lake, river, soil)
  - sample_description: detailed sample description (English/Russian)
  - name_engl: English name of water body
  - sampling_date: date of collection (dd/mm/yyyy)
  - analysis_date: date of analysis (dd/mm/yyyy)
  - d2H: Deuterium isotope ratio (δ2H, ‰)
  - d18O: Oxygen-18 isotope ratio (δ18O, ‰)

## Data use, accessibility, and integration
- Outputs are prepared in clear formats (reports, maps, charts) and stored in accessible data portals as part of standardised environmental monitoring practices.
- Dataset is designed for interoperability and re-use, enabling combination with other environmental datasets to increase value and support broader environmental monitoring and policy evaluation.

## Notes and acknowledgments
- Sampling and lab analysis contributions acknowledged (notably lab analysts from UoA).
- Detailed methodology and field notes available in associated references (e.g., Raudina et al., 2017).