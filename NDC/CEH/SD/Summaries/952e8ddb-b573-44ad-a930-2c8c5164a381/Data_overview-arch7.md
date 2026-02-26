# Palaeoecological proxy data from the eastern Andean cloud forest of Ecuador

## Scope and purpose
- Palaeoecological proxy data collected from lake sediments, surface soil and moss polsters in the eastern Andean cloud forest of Ecuador (late Quaternary).
- Aims to understand how ecosystem dynamics were driven by anthropogenic, physical and climatic factors through time.
- Data types include pollen, non-pollen palynomorphs (NPP), micro-charcoal, macro-charcoal, loss-on-ignition (LOI) and X-ray fluorescence (XRF).

## Data components (Files Included)
- 14 CSV files:
  - Huila_LOI.csv, Vinillos_LOI.csv
  - Modern_NPP.csv, Huila_Macrocharcoal.csv, Vinillos_Macrocharcoal.csv
  - Modern_Pollen.csv, Huila_Microcharcoal.csv, Vinillos_Microcharcoal.csv
  - Huila_NPP.csv, Vinillos_NPP.csv
  - Huila_Pollen.csv, Vinillos_Pollen.csv
  - Huila_XRF.csv, Vinillos_XRF.csv
- Proxies covered: pollen, non-pollen palynomorphs (NPP), micro-charcoal, macro-charcoal, LOI, major elements (XRF).
- Context includes sample locations, sampling details, and metadata codes.

## Study area and sampling sites
- Location: Napo Province, Ecuador (eastern Andean cloud forest) with sample locations shown in Figure 1 and described in Table 1.
- Lake Huila: sediment core (age ~1 ka to recent); coordinates: ~S 00° 25.405, W 78° 01.075; altitude ≈ 2608 m; current vegetation: pasture.
- Vinillos Section: cliff exposure split into Section A (upper) and Section B (lower); age ~45–42 ka; altitude ≈ 2090 m; current vegetation: secondary forest.
- Modern samples (M1–M5): moss polsters (M1–M2), surface soil (M3–M4), lake surface sediment (M5); various altitudes around 1801–2611 m; modern vegetation types include secondary and riparian forest.
- Sample scope includes sediment cores, tephra layers, and surface materials.

## Field sampling regime
- Lake Huila: coring with Livingstone corer from a floating platform; cores up to 1 m, overlapping cores, bedrock not reached; the longest core (Huila-E) to 2.09 m used for analysis.
- Vinillos cliff: sampling every 5 cm through organic layers; discrete bulk samples from tephra layers; large wood macro-fossils recovered from two organic layers.
- Modern samples: moss polsters, surface soil, and lake surface sediment collected at ground level; stored at 4°C.

## Proxy data and laboratory methods
- Palynology (pollen and NPP):
  - Organic sediments processed to 1 cm³ samples; tephra processed with density separation due to high siliciclastic content.
  - Lycopodium spores added as an exotic marker to determine palynomorph concentrations.
  - Pollen/NPP counted at 400x–600x; minimum 300 terrestrial pollen grains counted per sample.
  - Identification keyed to standard references; NPP morphotypes catalogued with codes (see metadata).
- Non-pollen palynomorphs (NPP):
  - Morphotypes identified using established literature; prefixes indicate source references and publishers (e.g., OU, LH, V, HdV, IBB, UG, TM).
- Micro-charcoal:
  - Counted on the same slides as palynomorphs at 200x within 5–100 µm range; analyzed across 50 random fields per slide; results expressed as fragments per cm³ of sediment.
- Macro-charcoal:
  - Sediment deflocculated, sieved at 100 µm; macro-charcoal >100 µm counted from 1 cm³ per Bogorov tray.
- LOI (Loss-on-ignition):
  - ~2 cm³ samples dried, combusted at 550°C (organic) and 950°C (carbonates); weight loss converted to percent organic matter.
- XRF (X-ray fluorescence) major elements:
  - Fire-pressed glass discs (tephra layers and standards) analysed for SiO2, TiO2, Al2O3, Fe2O3, MnO, MgO, CaO, Na2O, K2O, P2O5 using a wavelength-dispersive spectrometer.
- Processing standards and references provided to ensure reproducibility and comparability (e.g., Faegri & Iversen, Stockmarr, Heiri et al., Thomas & Haukka).

## Metadata and data coding
- Table 3 documents column headings and codes used in metadata files.
- NPP morphotypes are labeled with prefixes:
  - OU, LH, V: described morphotypes (Open University, local codes)
  - HdV, IBB, UG, TM: morphotypes identified per specific published schemes
- Sample and site descriptors include preparation method (e.g., HF acid, density separation), sample location, and sample numbers for cross-referencing.

## How to use in GIS (map-based data products)
- Create geospatial layers:
  - Point features for sample locations (Lake Huila, Vinillos A/B sections, M1–M5 modern samples) with coordinates, altitude, substrate, and vegetation attributes.
  - Optional polyline/polygon layers for transects or tephra layers if spatial extents are provided.
- Attach attribute tables incorporating:
  - Age ranges (e.g., Huila ~1 ka to recent; Vinillos ~45–42 ka; Modern samples: M1–M5)
  - Sample type (core, cliff, moss, soil, lake surface)
  - Proxy measurements per sample: pollen percentages, NPP morphotype abundances, micro-/macro-charcoal counts, LOI percentages, and XRF major element concentrations.
  - Tephra layer identifications and coordinates where applicable.
- Visualizations and analyses:
  - Map spatial distribution of proxies to identify regional ecological shifts and potential anthropogenic influences.
  - Time-sliced maps or profiles by layer depth/age for Lake Huila core; overlay with tephra events and major element signatures from XRF.
  - Choropleth or symbol maps for relative abundances of key pollen taxa, NPP morphotypes, and charcoal concentrations.
  - Integrate with elevation, land cover, and climate layers to assess drivers of ecological change.
- Data integration considerations:
  - Ensure alignment of sample IDs across the 14 CSV files for joined analyses.
  - Respect units and scales (e.g., charcoal fragments per cm³, LOI percentages, XRF concentrations) when combining proxies.
  - Use the provided metadata (Table 3) to interpret variable meanings and preparation methods.

## References and provenance
- Methods and proxies are grounded in established palynology and paleoecology literature, with explicit references for laboratory techniques, NPP classification, and XRF protocols.
- The dataset builds on standard palynological and geochemical procedures to support robust, GIS-ready visualization and analysis of late Quaternary ecological dynamics in a tropical Andean context.