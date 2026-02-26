# RECOUP-Moor Vegetation Community data: Methodology

- Field site: Stalybridge estate on Saddleworth Moor (blanket bog near Manchester, UK). A wildfire began June 24, 2018, lasting six weeks and affecting 18 km2, with large-scale removal of surface vegetation.

- Study design and burn severity:
  - 10 plots established in October 2018 at the post-fire site, each 10 m x 10 m.
  - 5 plots in shallow (less severe) burns and 5 plots in deep (more severe) burns.
  - Surface vegetation removed by fire, exposing bare peat.

- Vegetation surveys:
  - Conducted using 1 m x 1 m point quadrats with 1 cm intervals.
  - Two surveys performed at random positions within each plot; results combined to yield one overall community for each plot at each survey time.

- Soil seed-bank sampling and germination experiment:
  - Soil samples collected from three random locations within each plot, at two depths: 0–5 cm (top layer) and 5–10 cm (bottom layer), with an additional reference sample from a nearby unburned site (<2 km away, n=5).
  - Samples stored at ~5°C for 21 days, then frost-treated at -20°C for 48 hours.
  - Seedlings germinated in greenhouse: soil mixed with ~1 L peat, trays set up and monitored for 12 weeks, after which emerging seedlings were identified and removed.
  - Seed-bank data adjusted to account for initial soil weight; seed-bank values standardized to 1 L of extracted peat soil. Vegetation abundances remained unchanged.

- Data collection and processing details:
  - Each sample is associated with metadata such as plot ID (S1–S5 for shallow burn, D1–D5 for deep burn, R1–R5 for unburned/reference) and survey type (SB for seed-bank, Veg for vegetation).
  - Weight of extracted soil (Weight_soil) and date of sampling (Date) are recorded.
  - Seed-bank data include species names (Latin) and abundances; raw abundances are recorded for vegetation data (Raw_Abundance vs standardized Seed-bank Abundance).

- Variable key (data structure overview):
  - Plot_number / Plot_ID: identifies plot and burn category (S1–S5, D1–D5, R1–R5).
  - Survey: indicates data type (SB = seed-bank, Veg = vegetation).
  - Soil_layer: top (T) or bottom (B) layer (seed-bank only).
  - Sample_group: Reference or Post-Fire.
  - Weight_soil: weight of extracted soil (g) (seed-bank only).
  - Date: sampling date.
  - Species_Latin: scientific name.
  - Abundance: total individuals per sample (seed-bank data adjusted by soil weight; vegetation data unchanged).
  - Seed_bank / Vegetation: indicates data source.
  - Raw_Abundance: total individuals per sample (unadjusted for soil weight for seed-bank).

- Species list (selected taxa observed in methodology):
  - Betula pubescens (Moor birch)
  - Calluna vulgaris (Common heather)
  - Epilobium angustifolium (Rosebay willowherb / Fireweed)
  - Epilobium hirsutum (Great willowherb)
  - Erica tetralix (Bog heather)
  - Eriophorum vaginatum (Hare's-tail cottongrass)
  - Festuca rubra (Red fescue)
  - Holcus lanatus (Yorkshire fog)
  - Juncus bufonius (Toad rush)
  - Juncus effusus (Soft rush)
  - Rumex acetosa (Common sorrel)
  - Vaccinium myrtillus (European blueberry)

- Purpose and relevance for monitoring frameworks:
  - Combines post-fire vegetation recovery assessment with seed-bank dynamics across burn severities.
  - Uses standardized, replicable field and laboratory procedures to generate comparable data over time.
  - Emphasizes data transparency and comparability, with explicit metadata, soil-weight adjustments for seed-bank data, and reference sites to contextualize post-fire recovery.