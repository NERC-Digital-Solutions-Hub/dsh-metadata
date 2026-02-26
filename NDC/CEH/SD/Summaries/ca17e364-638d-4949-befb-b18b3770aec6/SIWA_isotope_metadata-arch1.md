# DATASET: Stable water isotopes in Western Siberian inland waters

## Overview
- Part of the JPI/NERC SIWA project: “Climate impact on the carbon emission and export from Siberian inland waters” (grant NE/M019896/1).
- Multinational collaboration across the University of Aberdeen (UK), GET Toulouse (France), TSU Tomsk (Russia), and Umeå University (Sweden).

## Authors and affiliations
- P. Ala-aho, C. Soulsby, D. Tetzlaff (University of Aberdeen, UK) and colleagues from GET Toulouse, TSU Tomsk, and UU Umeå.
- Roles included planning sampling campaigns, coordinating logistics and analyses, preparing samples, quality control, and data archiving.

## Responsibilities in dataset generation
- Planning sampling campaigns and coordinating isotope analyses.
- Sample preparation, quality control, and database compilation.
- Logistics coordination for field campaigns across multiple sites and landscape scales.

## Sample collection and sampling strategy
- Water samples collected in 3.5 mL glass vials.
- River sampling: grab samples from the middle of the channel (bridge or banks) at about 0.5 m depth.
- Lake sampling: from a boat at ~0.5 m depth; thermokarst lakes sampled at 0.25 m due to shallow depths.
- Floodplain sampling: grab samples from inundated areas.
- Soil solutions: collected with ceramic cup suction lysimeters at 20–50 cm depths (typically ~10 cm above permafrost).
- On-site filtration for water samples with 0.45 μm filters; initial 2 mL of filtrate discarded.
- Soil samples filtered in the field; details provided in Raudina et al. (2017).

## Data analysis and instrumentation
- Isotope analysis performed with a Los Gatos DLT-100 laser isotope analyzer.
- Instrument precision: δ2H ± 0.4 ‰; δ18O ± 0.1 ‰.
- Isotope ratios reported in δ notation relative to Vienna Standard Mean Ocean Water (VSMOW).

## Sample storage and archiving
- Store samples in the dark at 4–6 °C and ship to the University of Aberdeen for analysis.
- Post-analysis storage in UoA facilities.
- Archiving by analysis date and sample ID to enable traceability.

## File and data description
- File name: SIWA_stable_water_isotope_data.txt
- Encoding: UTF-16LE (with BOM)
- Structure: tabular, each row represents a unique sample; columns are data fields/attributes.
- Data fields are described with:
  - Field description
  - Field format
  - Unit
  - Explanation of variables (if applicable)

## Detailed data fields (example fields)
- T_ID: Sample ID to link to vial; text format.
- sample_ID: Alternative sample ID; text format.
- lat_N: Latitude (WGS 1984); floating point; decimal degrees; Northern latitude.
- long_E: Longitude (WGS 1984); floating point; decimal degrees; Eastern longitude.
- sample_type: Type of inland water sampled; text/factor; values include flood, lake, river, soil.
- sample_description: Detailed English/Russian description; text (may include Cyrillic).
- name_engl: Name of the water body in English; text.
- sampling_date: Date of collection; text; format dd/mm/yyyy.
- analysis_date: Date of analysis; text; format dd/mm/yyyy.
- d2H: Deuterium isotope ratio (δ2H); floating number; unit ‰.
- d18O: Oxygen-18 isotope ratio (δ18O); floating number; unit ‰.

## Notes for users
- The dataset captures stable water isotopes across Western Siberian inland waters, including rivers, lakes, floodplains, and soils, with detailed metadata to support site- and sample-specific analyses.
- Clear provenance and traceability are provided through sample IDs, collection/analysis dates, and storage/archive practices.