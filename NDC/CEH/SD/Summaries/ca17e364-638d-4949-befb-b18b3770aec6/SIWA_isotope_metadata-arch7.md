# DATASET: Stable water isotopes in Western Siberian inland waters

## Overview
- Dataset part of the JPI/NERC SIWA project: Climate impact on the carbon emission and export from Siberian inland waters (grant NE/M019896/1).
- Authors and contributing institutions across Aberdeen (UK), Toulouse (France), Arkhangelsk (Russia), Tomsk (Russia), and Umeå (Sweden).
- Roles include planning sampling campaigns, coordinating isotope analysis, sample preparation, quality control, and data archiving.

## Project and Authors
- Northern Rivers Institute, School of Geosciences, University of Aberdeen (UoA): Soulsby (PI), Tetzlaff (Co-I), sampling coordination and isotope analysis oversight.
- Géosciences Environnement Toulouse (GET): Pokrovsky (PI), sampling campaign planning and logistics.
- BIO-GEO-CLIM Laboratory, Tomsk State University (TSU): Kirpotin (PI), sampling logistics; Manasypov, Lim, Krickov, Vorobyev, Kolesnichenko, Loiko (sampling and field work in various water bodies and soils).
- Department of Ecology and Environmental Science, Umeå University (UU): Karlsson (PI), Serikova (planned and performed lake sampling).

## Sampling and Sample Types
- Sample collection conducted from rivers, lakes, floodplains, and soils across Western Siberian inland waters, including permafrost zones.
- Water sampling methods:
  - Rivers: grab samples from mid-channel (preferably from a bridge) or river banks at ~0.5 m depth in active flow.
  - Lakes: boat-based sampling at ~0.5 m depth; thermokarst lakes are very shallow (1.0–0.5 m) with sampling at ~0.25 m depth for small lakes.
  - Flooded areas: grab samples from boats.
- Soil sampling: ceramic cup suction lysimeters at depths 20–50 cm (typically 10 cm above permafrost table).
- Sample handling:
  - 3.5 mL glass vials for all samples.
  - On-site filtration when water had excess organic matter using sterile syringes and acetate cellulose filters; discard first 2 mL filtrate.
- Sample types categorized as:
  - flood, lake, river, soil.

## Laboratory Analysis and Quality
- Isotope analysis performed with a Los Gatos DLT-100 laser isotope analyser.
- Instrument precision: δ2H ±0.4 ‰; δ18O ±0.1 ‰.
- Isotope ratios reported using δ notation relative to Vienna Standard Mean Ocean Water (V-SMOW).

## Sample Storage and Archiving
- Storage: samples kept in the dark at 4–6 °C and shipped to the University of Aberdeen for analysis.
- Post-analysis storage: samples archived at UoA facilities.
- Traceability: archived by analysis date and sample ID for easy back-tracing.

## Data Description and Structure
- File name: SIWA_stable_water_isotope_data.txt
- Encoding: UTF-16LE with Byte Order Mark (BOM)
- Data structure: tabular; each row represents a unique sample; each column is a data field/attribute.
- Data fields described (field-level details provided for each):
  - T_ID: sample ID linking to sample vials (text)
  - sample_ID: alternative sample ID linking to sample vials (text)
  - lat_N: Northern latitude (WGS 1984), decimal degrees (floating point)
  - long_E: Eastern longitude (WGS 1984), decimal degrees (floating point)
  - sample_type: water body type (factors: flood, lake, river, soil)
  - sample_description: detailed English or Russian description of the sample
  - name_engl: English name of the sampled water body
  - sampling_date: date of sample collection (format dd/mm/yyyy)
  - analysis_date: date of analysis (format dd/mm/yyyy)
  - d2H: Deuterium isotope ratio (δ2H), in ‰ (floating number)
  - d18O: Oxygen-18 isotope ratio (δ18O), in ‰ (floating number)

## GIS Readiness and Considerations
- Spatial data readily mappable in GIS using lat/lon coordinates in WGS 84.
- Data fields support spatial analysis and integration with other environmental datasets (water bodies, permafrost zones, hydrology layers).
- Data standards and language considerations:
  - Some sample descriptions may use Cyrillic (Russian) text; metadata and documentation may be bilingual.
  - Field formats are clearly defined (dates as dd/mm/yyyy, decimal degrees for coordinates, δ-values in ‰).
- Potential usage notes:
  - Useful for mapping isotope distributions across river, lake, floodplain, and soil environments in Western Siberia.
  - Can support investigations into water source attribution, hydrological processes, and climate-related carbon export studies.
- Limitations and data quality:
  - Availability of data at the required spatial/temporal resolution may vary.
  - Data integration may require harmonizing field categories and ensuring consistent back-tracing via IDs.