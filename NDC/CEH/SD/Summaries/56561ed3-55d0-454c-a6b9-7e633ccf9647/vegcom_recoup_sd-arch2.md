# RECOUP-Moor Vegetation Community data: Methodology

- Purpose and context
  - Assess environmental condition and vegetation recovery following wildfire on Saddleworth Moor (Stalybridge estate, blanket bog, UK).
  - Compare recovery between shallow (less severe) and deep (more severe) burns, with an unburned reference site for contrast.
  - Include a greenhouse seed-bank experiment to evaluate potential vegetation regrowth from soil seed-bank.

- Field site and burn context
  - Location: Saddleworth Moor near Manchester, UK; dominant vegetation includes Calluna vulgaris and Eriophorum vaginatum.
  - Event: June 24, 2018 wildfire affected 18 km² over six weeks, removing surface vegetation.

- Experimental design
  - Plots: 10 plots total, each 10 m × 10 m.
  - Burn severity: 5 plots shallow burn (S1–S5) and 5 plots deep burn (D1–D5); all plots exposed bare peat surface.
  - Reference: Nearby unburned plots (R1–R5) within 2 km, using the same sampling protocol.

- Vegetation data collection (post-fire recovery)
  - Method: 1 m × 1 m point quadrats with 1 cm intervals.
  - Replication: two surveys per plot at random positions; results combined to produce one community profile per plot per survey time.
  - Timing: surveys conducted at specified intervals following the fire to track recovery trajectory.

- Seed-bank data collection (soil seed-bank)
  - Sampling: peat extracted from three random locations within each plot.
  - Depths: 0–5 cm (top layer) and 5–10 cm (bottom layer).
  - Aggregation: samples combined to yield one soil sample per plot per depth; included a neighboring unburned reference site (n=5) with identical procedure.
  - Processing: samples transported to University of Southampton, stored at ~5°C for 21 days, then frost-treated at -20°C for 48 hours.
  - Germination experiment: peat mixed with ~1 L horticultural peat and spread in greenhouse trays; seedlings identified and removed over 12 weeks, then total species counts adjusted for initial soil weight.
  - Outcome: seed-bank species composition and abundance linked to post-fire vegetation recovery potential.

- Data structure and variable key
  - Plot/Tier identifiers:
    - Plot_number, Description: Plot number
    - Plot_ID, Description: Plot feature/replicate (S1–5 shallow burn, D1–5 deep burn, R1–5 reference)
  - Survey type and abundance:
    - Survey, Description: Abundance data from seed-bank surveys (SB) or vegetation surveys (Veg)
  - Soil and seed-bank specifics:
    - Soil_layer, Description: Top (T) or Bottom (B) soil layer for seed-bank data
    - Sample_group, Description: Reference or Post-Fire
    - Weight_soil, Description: Weight of extracted peat soil (g) for seed-bank data
    - Date, Description: Sampling date
  - Species data:
    - Species_Latin, Description: Latin species name
    - Abundance, Description: Total individuals per sample (seed-bank values adjusted to 1 L of soil; vegetation abundances left unadjusted)
    - Seed-bank only: Raw_Abundance, Description: Raw seed-bank individuals per sample (not standardized by weight)
  - Data purpose: Enables comparison of post-fire vegetation recovery and seed-bank contribution across burn severities and reference conditions.

- Species tracked (examples)
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

- Data handling, QA, and sharing (monitoring relevance)
  - Standardised data collection across plots and depths to ensure comparability over time.
  - Seed-bank data standardized to per-liter soil basis; vegetation data retained in raw units for direct abundance comparisons.
  - Tacit emphasis on documenting data descriptors (plots, surveys, depths, burn severity) to support data quality assurance and cross-study comparability.
  - Methodology implies storage and processing steps suitable for integration into broader environmental monitoring datasets, with clearly defined outputs (vegetation composition per plot, seed-bank composition per depth, and seed-bank viability potential).

- End notes on applicability for environmental monitoring
  - Provides a replicable framework for monitoring post-disturbance vegetation recovery and assessing the role of the seed-bank in recolonisation.
  - Facilitates temporal comparison (pre/post-fire and across burn severities) and integration with other environmental datasets.
  - Aligns with monitoring objectives to improve data value and accessibility by standardising formats, variables, and outputs for broader scrutiny and reuse.