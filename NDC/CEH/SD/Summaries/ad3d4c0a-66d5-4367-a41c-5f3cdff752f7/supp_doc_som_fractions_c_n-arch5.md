# Carbon and nitrogen stocks in soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Dataset Overview
- Provides carbon (C) and nitrogen (N) stocks in soil organic matter (SOM) fractions across grassland-to-forest conversion chronosequences in Scotland.
- Stocks expressed in kg per m2 for two mineral soil depths: 0-5 cm and 5-20 cm.
- Focuses on grasslands and Scots Pine plantations established on former grasslands, collected in four areas across Scotland.
- Aims to quantify changes in total C and N and in the forms (fractions) of C and N following afforestation.

## Data Content and Structure
- Dataset comprises one CSV file: SOM_fractions_C_N.csv.
- Columns cover: cluster, veg, LUT, depth, plant_year, age, pH, sand, clay, silt, BD (bulk density), rock, and C/N stocks in fractions:
  - q_DOM_C_m2, q_DOM_N_m2
  - q_fPOM_C_m2, q_fPOM_N_m2
  - q_oPOM_C_m2, q_oPOM_N_m2
  - q_MAOM_C_m2, q_MAOM_N_m2
- Units:
  - Stocks in kg/m2
  - Fractions include dissolved organic matter (DOM), free particulate organic matter (fPOM), occluded particulate organic matter (oPOM), and mineral-associated organic matter (MAOM).

## Study Design and Sampling
- Four clusters across Scotland (Alyth, Limerigg, Peebles, Hawick) sampled as geographical replicates.
- For each cluster, samples from grassland (GR) and Scots Pine plantations (young, middle-aged, or old) established on former grasslands.
- Three soil cores per site pooled, yielding a total of 32 samples.
- Samples collected in summer 2018.
- Soils were fractionated into four fractions and analyzed for pH, texture (sand, clay, silt), bulk density, and rock content.

## Geography and Sampling Locations
- Four clusters with paired habitat types (grassland and Scots pine plantation) and precise coordinates:
  - Cluster 1: Grassland (56.633827, -3.2410629)
  - Cluster 1: Scots pine plantation (56.735279, -3.2706253)
  - Cluster 2: Grassland (55.896026, -3.8524698)
  - Cluster 2: Scots pine plantation (55.914748, -3.7977104)
  - Cluster 3: Grassland (55.646448, -3.1281129)
  - Cluster 3: Scots pine plantation (55.613873, -2.9536157)
  - Cluster 4: Grassland (55.366159, -3.0258238)
  - Cluster 4: Scots pine plantation (55.37448, -3.0053828)

## Variable Details and Metadata
- Key identifiers:
  - cluster: origin cluster (1–4)
  - veg: vegetation type (GR = grassland; YO/MI/OL = young/middle-aged/old Scots pine)
  - LUT: land use type (grassland or Scots pine forest)
  - depth: soil layer (0-5 cm or 5-20 cm)
  - plant_year: year Scots pines were planted on former grasslands
  - age: age of Scots pines at sampling (2018)
- Soil properties included:
  - pH, sand (%), clay (%), silt (%), BD (bulk density, g/cm3), rock (%)
- C and N stocks by SOM fractions:
  - DOM, fPOM, oPOM, MAOM for C and N (values in kg/m2)

## Data Quality and Stewardship Considerations
- The dataset is authored by the study researchers who collected and interpreted the data.
- Sampling provides a single timepoint (summer 2018) across four clusters, with pooling of three cores per site.
- Fractionation and measurements (pH, texture, BD, rock) are described, enabling reproducibility and cross-study comparisons.
- For reuse, ensure consistent interpretation of depth, fraction nomenclature, and units; the dataset is organized as a single CSV with explicit column definitions to aid discoverability and interoperability.