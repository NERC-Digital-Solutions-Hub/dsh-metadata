# Carbon and nitrogen stocks in soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

- Objective: Assess changes in total quantity and form of soil carbon (C) and nitrogen (N) stocks during afforestation of long-term grasslands, by examining different soil organic matter (SOM) fractions across grassland and Scots Pine plantations on former grasslands.

- Dataset basics:
  - File: SOM_fractions_C_N.csv
  - Location: four clusters across Scotland (Scottish Central Lowlands and Southern Uplands)
  - Sampling year: 2018 (summer)
  - Samples: 32 total (three cores per site pooled prior to analysis)

- Study design and sites:
  - Four geographical clusters (Alyth, Limerigg, Peebles, Hawick)
  - Within each cluster: grassland and Scots Pine plantation on former grasslands
  - True geographical replicates across four clusters
  - Age spectrum of Scots Pine plantations (young, middle-aged, old) with plant year recorded
  - Depths sampled: 0–5 cm and 5–20 cm

- Measurements and units:
  - Soil properties: pH, texture (sand, clay, silt in %), bulk density (BD, g/cm3), rock content (%)
  - Carbon and nitrogen stocks by SOM fractions:
    - Dissolved organic matter (DOM), free particulate organic matter (fPOM), occluded particulate organic matter (oPOM), mineral-associated organic matter (MAOM)
    - C and N stocks expressed as kg/m2 for each fraction
  - Depth-specific measurements (0–5 cm and 5–20 cm)

- Variables in the dataset (columns):
  - cluster, veg, LUT, depth, plant_year, age
  - pH, sand, clay, silt, BD, rock
  - q_DOM_C_m2, q_DOM_N_m2
  - q_fPOM_C_m2, q_fPOM_N_m2
  - q_oPOM_C_m2, q_oPOM_N_m2
  - q_MAOM_C_m2, q_MAOM_N_m2

- Data structure and interpretation:
  - 'cluster' indicates origin:
    - 1 = Alyth, 2 = Limerigg, 3 = Peebles, 4 = Hawick
  - 'veg' indicates source vegetation: Grassland (GR) or Scots pine plantation (YO, MI, OL indicating age classes)
  - 'LUT' indicates land-use type: Grassland or Scots pine forest
  - 'depth' distinguishes soil layer: 0–5 cm or 5–20 cm
  - 'plant_year' is the year when pines were planted on former grasslands
  - 'age' is the age of the Scots pines at sampling in 2018

- Location details:
  - Each cluster includes coordinates for grassland and pine plantation samples (four clusters across Scotland; example lat/long pairs provided to indicate site locations)

- Potential analyses and applications for analysts:
  - Compare C and N stocks between grassland and pine plantation plots within each cluster
  - Examine how C and N stocks and their fractions vary by soil depth
  - Assess how age of afforestation (YO/MI/OL) relates to changes in SOM fractions
  - Analyze distribution of C and N among DOM, fPOM, oPOM, and MAOM fractions
  - Aggregate across clusters to identify regional patterns in response to afforestation
  - Use SD differences to explore relationships with pH, texture (sand/clay/silt), BD, and rock content

- Limitations and notes:
  - Single sampling event (summer 2018) limits temporal trend inference
  - Sample size is 32, distributed across four clusters, which may affect statistical power for some comparisons
  - Data are provided in a single CSV file with multiple derived fraction metrics, suitable for site-level and fraction-level analyses but not longitudinal dynamics without additional data

- Practical use for decision-making:
  - Inform land-management and afforestation strategies by quantifying how conversion from grassland to Scots pine affects soil C and N storage and the distribution among SOM fractions
  - Support models predicting soil carbon sequestration potential under different afforestation timelines and soil conditions across Scotland