# Palaeoecological proxy data from the eastern Andean cloud forest of Ecuador

## Overview
- Aim: recover and analyse palaeoecological proxy data from lake sediments, surface soil, and moss pollsters to understand how ecosystem dynamics were driven by anthropogenic, physical, and climatic factors through time (late Quaternary).
- Proxies included: pollen, non-pollen palynomorphs (NPP), micro-charcoal, macro-charcoal, loss-on-ignition (LOI), and X-ray fluorescence (XRF).
- Study area: eastern Andean cloud forest of Ecuador, Napo province.
- Field period: 2012–2013; laboratory analysis: 2014–2015 at The Open University (UK).
- Sample types: fossil records from Lake Huila and Vinillos cliff section; modern reference samples from moss polsters, surface soils, and lake surface sediment.
- Data scope: 14 CSV files containing fossil and modern pollen, NPP, charcoal (micro and macro), LOI, and XRF data.

## Datasets included
- Fossil and modern data files:
  - Huila_LOI.csv
  - Vinillos_LOI.csv
  - Modern_NPP.csv
  - Huila_Macrocharcoal.csv
  - Vinillos_Macrocharcoal.csv
  - Modern_Pollen.csv
  - Huila_Microcharcoal.csv
  - Vinillos_Microcharcoal.csv
  - Huila_NPP.csv
  - Vinillos_NPP.csv
  - Huila_Pollen.csv
  - Vinillos_Pollen.csv
  - Huila_XRF.csv
  - Vinillos_XRF.csv
- Field sites and sample types:
  - Lake Huila: 128 cm core analyzed for pollen, NPP, micro- and macro-charcoal, LOI; tephra layers include major element XRF.
  - Vinillos cliff section: 325 cm exposure with samples every 5 cm; multiple sample types including pollen, NPP, charcoal, LOI, and limited XRF.
  - Modern samples: M1–M5 (moss polsters, surface soils, lake surface sediment) used as contemporary references.
- Table and figure references:
  - Figure 1 shows sample locations in the montane forest (Napo).
  - Table 1 provides sample location details (coordinates, substrate, altitude, modern vegetation).
  - Table 2 summarizes field sampling and subsampling counts for each site.
  - Table 3 describes selected metadata headings and codes.

## Field sampling regime
- Lake Huila:
  - Coring using a Livingstone corer with Colinvaux-Vohnout piston modification from a floating platform in 1.2 m water.
  - Individual cores up to 1 m; longest core Huila-E reached 2.09 m; bedrock not reached.
- Vinillos cliff section:
  - Two sections: A (upper) and B (lower); vegetation removed prior to sampling.
  - Sediment samples taken every 5 cm through organic layers; 1 cm deep cuts; discrete bulk samples from tephra layers.
  - Large wood macro-fossils recovered from organic layers.
- Modern reference samples:
  - Moss polsters (M1–M2), surface soil (M3–M4), lake surface sediment (M5).
  - Collected at ground level and stored at 4°C until processing.

## Proxy data processing and laboratory methods
- Palynology (pollen and NPP):
  - Organic sediments processed to 1 cm³ using potassium hydroxide, hydrofluoric acid, and acetolysis; tephra samples processed with density separation (bromoform) due to siliciclastic sediments.
  - Lycopodium spore tablets added to determine palynomorph concentrations (stock standard referenced).
  - Slides mounted in glycerol; counted at 400×–600×; minimum 300 terrestrial pollen grains per sample.
  - Taxonomic identification against reference material and palynology atlases; NPPs identified per literature with codes (e.g., HdV, UG, IBB).
  - New NPP morphotypes (prefix OU) recorded (published elsewhere); prefixes LH and V denote morphotypes below abundance/persistence filters.
- Micro-charcoal:
  - Counted on the same slides as palynomorphs; 200× magnification; 5–100 μm fragments counted in 50 random fields per slide; concentrations expressed as fragments per 1 cm³ of sediment using Lycopodium counts.
- Macro-charcoal:
  - Sample deflocculated in 10% KOH at 80°C; sieved at 100 μm; macro-charcoal >100 μm counted from 1 cm³ of sediment on Bogorov tray under 20×.
- LOI (Loss on Ignition):
  - ~2 cm³ sediment dried at 40°C, burned at 550°C (organic matter) for 4 h, then 950°C (carbonates) for 2 h; remaining residue weighed to determine organic carbon proportion.
- XRF (Major element analysis):
  - Tephra layers analyzed; glass discs produced; major elements (SiO2, TiO2, Al2O3, Fe2O3, MnO, MgO, CaO, Na2O, K2O, P2O5) measured using a wavelength-dispersive XRF spectrometer (ARL 8420+).

## Data codes and metadata
- Metadata schema described in Table 3:
  - Huila_XRF and Vinillos_XRF: sample_location, sample_number; description of recovery location or calibration standard.
  - NPP and Pollen: preparation_method (e.g., hydrofluoric acid, density separation).
  - Modern_NPP, Huila_NPP, Vinillos_NPP: morphotype prefixes and coding ( OU, LH, V, HdV, IBB, UG, TM) to distinguish published morphotypes and unidentified types.

## How this data can support analysis and modelling
- Enables multi-proxy correlation analyses (pollen, NPP, charcoal, LOI, geochemistry) to identify drivers of ecosystem change.
- Facilitates reconstruction of anthropogenic vs natural forcing by aligning charcoal occurrences with pollen/NPP signals and LOI.
- Useful for creating predictive models of ecosystem responses to climatic shifts and human activity in tropical montane forests.
- Provides local-scale, well-documented datasets with metadata for reproducibility and cross-site comparisons (Huila vs Vinillos; modern vs ancient records).

## Considerations and caveats for analysts
- Local-scale focus with two primary sites; depositional contexts differ (lake core vs cliff exposure).
- Varied sampling densities between sites may affect resolution of comparisons.
- Taxonomic resolution depends on reference materials and morphotype classifications (NPPs) and may require careful interpretation when integrating with pollen data.
- Tephra layers present opportunities for tephrochronology but require careful handling in stratigraphic alignments.

## References (methodological and foundational)
- Standard palynology and paleoecology references and methods cited for processing and interpretation (Faegri & Iversen; Moore et al.; Stockmarr; Heiri et al.; Thomas & Haukka; and works on NPP morphotypes and palynological databases).
- Specific studies and taxonomic keys cited for identification of pollen, NPPs, and micro-/macro-charcoal, as well as historical NPP morphotype frameworks (OU, LH, V; HdV; IBB; UG; TM).