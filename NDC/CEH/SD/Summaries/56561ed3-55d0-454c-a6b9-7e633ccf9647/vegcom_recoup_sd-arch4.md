# RECOUP-Moor Vegetation Community data: Methodology

- Field site and context
  - Stalybridge estate on Saddleworth Moor, a blanket bog near Manchester, UK.
  - Vegetation dominated by Calluna vulgaris and Eriophorum vaginatum.
  - June 24, 2018: wildfire event burned the area for six weeks, affecting 18 km² and removing surface vegetation.

- Experimental design
  - 10 plots established in October 2018, each 10 m × 10 m.
  - 5 plots designated as shallow (less severe) burn, 5 as deep (more severe) burn.
  - All plots had surface vegetation removed, exposing bare peat.
  - Two vegetation surveys per plot using 1 m × 1 m point quadrats with 1 cm intervals; surveys conducted at random positions and results averaged to yield one community per plot per survey.

- Soil seed-bank sampling
  - Peat samples collected from three random locations within each plot.
  - Each sample taken from two depths: 0–5 cm (top layer) and 5–10 cm (bottom layer).
  - Three samples per plot aggregated to one soil sample per plot per depth.
  - A neighboring unburned reference site (<2 km away) sampled with the same procedure (n=5 plots).

- Post-collection processing and germination experiment
  - Samples transported to the University of Southampton and stored at approximately 5 °C for 21 days.
  - Frost treatment: -20 °C for 48 hours.
  - Samples mixed with ~1 L of horticultural peat and spread on trays in a greenhouse.
  - Seedlings that emerged identified and removed; experiment continued for 12 weeks or until no new seedlings emerged.
  - Total number of species adjusted to account for differences in initial soil weight; each sample equivalent to 1 L of extracted peat soil.

- Data structure and variable key
  - Plot_number / Plot_ID: identifies the plot and burn type (S1–S5 shallow, D1–D5 deep, R1–R5 reference).
  - Survey: vegetation or seed-bank abundance data.
  - Soil_layer: top (T) or bottom (B) layer (seed-bank only).
  - Sample_group: Reference or Post-Fire.
  - Weight_soil: weight of extracted peat soil (g) (seed-bank only).
  - Date: sampling date.
  - Species_Latin: Latin species name.
  - Abundance / Raw_Abundance: counts per sample; seed-bank abundances adjusted for soil weight, vegetation abundances unchanged.
  - Notes: seed-bank values are standardized to 1 L of extracted peat soil; raw abundances are not weight-normalized for seed-bank data.

- Species list (selected taxa observed)
  - Betula pubescens (Moor birch)
  - Calluna vulgaris (Common heather)
  - Epilobium angustifolium (Rosebay willowherb/Fireweed)
  - Epilobium hirsutum (Great willowherb)
  - Erica tetralix (Bog heather)
  - Eriophorum vaginatum (Hare's-tail cottongrass)
  - Festuca rubra (Red fescue)
  - Holcus lanatus (Yorkshire fog)
  - Juncus bufonius (Toad rush)
  - Juncus effusus (Soft rush)
  - Rumex acetosa (Common sorrel)
  - Vaccinium myrtillus (European blueberry)

- Data quality and reuse considerations
  - Explicit replication across burn severities and a nearby unburned reference site enables comparisons of post-fire recovery and seed-bank dynamics.
  - Standardized sampling protocol (plot size, quadrats, depths, and greenhouse germination conditions) supports reproducibility.
  - Clear metadata on soil weight normalization and differentiation between seed-bank and vegetation data facilitates correct analysis and integration with other datasets.