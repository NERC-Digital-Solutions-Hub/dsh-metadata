# Overview

- This dataset provides palaeoecological proxy data from the eastern Andean cloud forest of Ecuador, focusing on how ecosystem dynamics were shaped by anthropogenic, physical, and climatic factors in the late Quaternary.
- Proxies included: pollen, non-pollen palynomorphs (NPP), micro-charcoal, macro-charcoal, loss-on-ignition (LOI), and X-ray fluorescence (XRF).
- Field collection occurred in 2012–2013 in Napo Province; laboratory analyses were conducted in 2014–2015 at The Open University (UK).

## Data contents and structure

- 14 CSV files included (representing different proxies and sample sets):
  - Huila_LOI.csv, Vinillos_LOI.csv
  - Modern_NPP.csv
  - Huila_Macrocharcoal.csv, Vinillos_Macrocharcoal.csv
  - Modern_Pollen.csv
  - Huila_Microcharcoal.csv, Vinillos_Microcharcoal.csv
  - Huila_NPP.csv, Vinillos_NPP.csv
  - Huila_Pollen.csv, Vinillos_Pollen.csv
  - Huila_XRF.csv, Vinillos_XRF.csv
- Metadata and sample descriptions are provided through:
  - Table 1: Sample locations and information (Lake Huila and Vinillos cliff sections; ages from 1 ka to modern; various substrates and elevations)
  - Table 2: Field sampling regime details (sediment cores and discrete samples; subsampling counts for each proxy)
  - Table 3: Descriptions of selected column headings and metadata codes (data standards, preparation methods, and code prefixes)

## Sampling regime and provenance

- Lake Huila: coring with Livingstone corer on a floating platform; overlapping cores (longest: Huila-E) to 2.09 m; bedrock not reached.
- Vinillos cliff section: two sections (A and B); samples collected every 5 cm through organic layers; discrete samples from volcanic ash layers; large wood macro-fossils recovered in two organic layers.
- Modern samples: moss polsters (M1–M2), surface soil (M3–M4), lake surface sediment (M5); all stored at 4°C until required.
- Storage and handling: all field materials transported to The Open University and kept cold; detailed provenance and coordinates recorded.

## Proxy data and laboratory methods

- Palynology (pollen and NPP): standard lab processing using potassium hydroxide, hydrofluoric acid, and acetolysis; tephra samples processed with density separation; Lycopodium spores used as an external marker to determine concentrations; counts performed at 400x–600x to identify taxa to the highest possible taxonomic rank; minimum of 300 terrestrial pollen grains counted per sample.
- NPP morphotypes: identified using reference literature; new morphotypes recorded with prefixes (OU) and are described in related work (Loughlin et al., 2018); certain taxa coded as LH/V when not meeting abundance/persistence filters.
- Micro-charcoal: counted on palynology slides at 200x; fragments 5–100 μm; concentrations calculated relative to Lycopodium marker and expressed as fragments per 1 cm³ of sediment.
- Macro-charcoal: processed by deflocculation (KOH) and sieving (>100 μm); counted per 1 cm³ of sediment.
- LOI: standard loss-on-ignition protocol (drying, combustion at 550°C and 950°C) to estimate organic and carbonate contents; results expressed as percentage of dry weight.
- XRF (major elements): analysis of tephra layers and internal standards using a glass disc method on an ARL 8420+ spectrometer; elements measured included SiO2, TiO2, Al2O3, Fe2O3, MnO, MgO, CaO, Na2O, K2O, P2O5.

## Metadata, codes, and data stewardship

- Metadata includes explicit column names and codes (Table 3 describes sample locations, preparation methods, and coding conventions).
- Preparation methods documented (e.g., hydrofluoric acid vs. density separation) with references to Faegri & Iversen (1989) and Moore et al. (2001).
- NPP morphotype nomenclature references multiple databases and projects (OU, LH, V, HdV, IBB, UG, TM prefixes with corresponding literature).
- Data are organized to support discoverability and reuse, with clear provenance (field site coordinates, elevation, substrate, modern vegetation) and systematic QA/QC practices (minimum counts, cross-referenced identifications).

## Accessibility, reuse, and limitations

- The dataset comprises 14 CSV files with detailed sample-level data and comprehensive proxy measurements.
- The documentation links the dataset to published palaeoecological frameworks and morphotype references (e.g., Loughlin et al. 2018; Montoya et al.; van Geel et al.).
- Some fields show missing data for certain proxies or samples (e.g., M1–M5 macro-charcoal and micro-charcoal data not always populated in all files), and bedrock was not reached in Lake Huila cores.
- Users should consult the associated figures (e.g., Figure 1) and tables (Tables 1–3) for full context on sample locations, ages, and methodological details.
- Licensing or access restrictions are not specified in the provided documentation; users may need to refer to the publishing institution or related publications for usage rights.

## Data quality and governance considerations for Data Stewards

- Provenance and chain-of-custody are clearly described (field collection, laboratory processing, storage conditions).
- Standardized, widely cited methods are used for palynology, LOI, and XRF, facilitating comparability with other datasets.
- Metadata completeness is high, with explicit sample identifiers, locations, elevations, substrates, and modern vegetation contexts.
- Code conventions and morphotype labeling are documented, enabling consistent data interpretation and integration with related datasets.
- To enhance long-term stewardship, consider adding explicit licensing information, data access terms, and a data dictionary or README that cross-references Tables 1–3 with the CSV schemas.