# pasture fed livestock farms across Great Britain, 2019

- A dataset from UK Centre of Ecology & Hydrology (funded by BBSRC) assessing the impacts of pasture-fed livestock practices on grassland ecology in Great Britain during 2019 (the second year of sampling).
- Focuses on farms that are members of, or aligned with, the Pasture Fed Livestock Association (PFLA) and includes both fully certified farms and those intending certification.
- Data collected include vegetation composition and biomass, soil chemistry and physical properties, and farm/field management practices, with an emphasis on mob grazing and herb-rich leys.

## Spatial scope and units

- 17 farms distributed across Great Britain (GB); fields sampled to compare mob-grazed vs set-stocked or ley vs traditional pasture systems.
- Fields sampled in pairs per farm when possible; fields anonymised and assigned IDs to protect landowner confidentiality.
- Location references include:
  - FARM_NO and FIELD_ID for relational joins
  - A5KM_REF: Ordnance Survey 5km grid reference for field locations
  - LC2007 and LC2007_CODE: ITE land classification codes
- Data structure designed for GIS use, enabling field- and farm-level mapping and analysis.

## Data collection design

- Sampling period: May–September 2019 (second year of the study).
- On each farm: two paired fields (mob-grazed vs comparable set-stocking; or ley-based vs traditional ley-based).
- Sampling units:
  - Vegetation: 3 quadrats per field (2 m x 2 m) plus a W-shaped soil transect across the field with 10 sampling locations.
  - Soils: soil cores at depths representative of the field (including 15 cm cores) and bulked samples along the transect (0–5 cm, 5–15 cm, 15–30 cm).
- Data collected on management practices via on-site farmer questionnaires (historic and current practices, grazing management, inputs).

## Data tables (data structure)

Seven CSV files, anonymised by farm.

- SEEGSLIP_PLOTS_2019.csv: Vegetation data per 2x2 m plot (plots attributes, sampling dates, slope/aspect/shade, canopy/ground layer heights, biomass indicators, etc.).
- SEEGSLIP_SPECIES_2019.csv: Species-level vegetation data per plot (species name, cover, flowering, land classification codes).
- SEEGSLIP_BIOMASS_2019.csv: Dry biomass weights by plant groups (grass, dicot, cereal) per field/plot.
- SEEGSLIP_SOIL_2019.csv: Soil chemistry and physical properties by field/depth (pH, conductivity, moisture, LOI, bulk density, texture, C/N, P metrics, Olsen P, CaCO3, total C/N, etc.).
- SEEGSLIP_FARMDATA_2019.csv: Farm- and field-level management information (grazing type, set-stocking, rest periods, fertiliser use, etc.).
- SEEGSLIP_FIELDS_2019.csv: Field-level management and site characteristics (field size, number of sub-units, shade, rest, management controls, stocking patterns, etc.).
- SEEGSLIP_STOCK_2019.csv: Stocking information (livestock types, supplementary feeding, bales rolled).

- Key join keys: FARM_NO and FIELD_ID across tables; A5KM_REF and LC2007/L C2007_CODE provide spatial-context attributes.

## Methods and quality control (QC)

- Vegetation and soil sampling followed standardized survey protocols; quadrats and W transects designed to cover field variation.
- Soil analyses included:
  - LOI and SOC by loss-on-ignition and elemental analysis
  - Total P and Olsen P; pH in water and CaCl2
  - Electrical conductivity, field moisture, bulk density, stones content, particle-size distribution (PSD via laser diffraction and hydrometer methods)
  - Aggregate stability and calcium carbonate content
- QA/QC procedures:
  - Internal standards and duplicates for soil and chemical measurements
  - Repetition if QC criteria exceeded (e.g., LOI standards, pH, EC)
  - Calibration and cross-checks for instrumentation (e.g., TGA, elemental analyzer, LD instrument)

## Data characteristics relevant for GIS users

- Spatially anchored at field level with grid references (A5KM_REF) and land classification codes (LC2007/LC2007_CODE), enabling GB-wide mapping of soil and vegetation attributes across paddocks.
- Rich attribute set per field/plot, including:
  - Sward composition indicators (plant groups, species cover, flowering status)
  - Soil properties linked to carbon stocks and nutrient status (SOC, TOTC, TOTN, Olsen P, pH, CaCO3, PSD, bulk density, aggregate stability)
  - Management regimes (mob grazing vs set stocking, duration of rest, field size, shade, fertility practices)
- Anonymised farm identifiers allow aggregate-level GIS analyses (e.g., comparing management regimes with soil/vegetation outcomes) while protecting landowner privacy.

## Potential GIS applications

- Map distribution of pasture types, sward diversity, and soil health indicators across GB.
- Assess relationships between grazing strategies (mob grazing vs set-stocked) and soil carbon, nutrient availability, and soil structure.
- Visualize spatial patterns of ley types, biodiversity proxies, and management intensity.
- Combine with ENA-submitted environmental DNA (data from sub-samples) for integrated ecological mapping (data deposited under PRJEB46195).

## Limitations and considerations

- Sample size is limited (17 farms), which may constrain generalizability at national scale.
- Data are anonymised; field boundary geometries are not provided in the summary (locations are reference-based), potentially requiring access to field-level coordinates for precise GIS mapping.
- Temporal scope is a single-year snapshot (2019); longitudinal analyses would require additional years.

## References and metadata

- Data collected by UKCEH; funded by BBSRC; related to pastoral management and biodiversity/soil health research.
- Related publications and background literature cited within the dataset (e.g., soil manual references, ITE land classification, and methodological standards).
- Sub-sample soil data include eDNA analyses deposited in European Nucleotide Archive (PRJEB46195).

- Note: The dataset includes future-reading references and additional context for researchers seeking to cross-link with related studies on mob grazing and soil microbial communities.