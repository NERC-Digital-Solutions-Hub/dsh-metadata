# Overview

- The Forest of Hope is native forest creation on Highlands Rewilding's Beldorney Estate (lat 57.409, lon -2.966). Planting density: 1600 stems/ha with a mix of birch (40%), sessile oak (20%), hazel (10%), alder (10%), rowan (10%), willow (5%), hawthorn (5%).  
- Planting began Winter 2022 and is planned to complete in early 2024 after a review of the 2023 planting.  
- Experimental design includes 17 40 × 40 m unplanted plots to assess natural regeneration, stratified by distance from seed sources and an adjacent semi-natural woodland to the east, matched to planted plots for monitoring soil, biodiversity, and tree establishment.  
- Baseline soil sampling for soil carbon (C) and nitrogen (N) was collected in Autumn 2022.

# Experimental design and sampling regime

- Soil sampling occurred on a 100 m grid within the planting area in September 2022 (prior to mounding and planting) and extended into adjacent grassland for a grassland control site.  
- An additional 17 natural regeneration plots were sampled to monitor regeneration; in November 2022, samples were collected in the 40 × 40 m unplanted plots for spatial monitoring of regeneration.  
- Plot types in the study include: 40 × 40 m planted plots, 40 × 40 m natural regeneration plots. Natural regeneration plot centroids used for sampling.  
- One unplanted plot (U8) was not sampled due to a pond.

# Collection, processing, and measurements

- Soil cores were collected with a 1.9 cm diameter auger at two depths: 0–10 cm and 10–30 cm (30 cm sampling not possible at some locations; depth recorded).  
- Samples were weighed fresh, dried at 60°C for at least 48 hours, then weighed to constant mass; samples were sieved into <2 mm and >2 mm fractions.  
- A 5 g subsample of the <2 mm fraction was ball milled; approximately 10 mg analyzed for carbon and nitrogen with an elemental analyzer. The exact weight of the subsample was recorded to 0.001 mg.  
- Calculations produced: soil bulk density (based on <2 mm fraction), % C, % N, and total C and N per sample (g/cm³).

# Data quality, structure, and documentation

- A unique sampling-location numbering system was used to track samples, with processing performed by experienced lab technicians to ensure precise elemental analysis weights.  
- The dataset is stored in a single CSV file: ForestOfHope_SoilCN_Winter2022.csv. Key fields include:
  - Location_ID, Type (100 m grid planted; 100 m grid grassland; Natural regeneration plot)
  - Lat, Long, What3words
  - Date_collected
  - Top_core_cm, Bottom_core_cm, Core_height_cm, Core_diameter_cm, Core_volume_cm3
  - Fresh_weight_g, Dry_weight_g
  - More_2mm_g, Less_2mm_g
  - Bulk_density_gcm3
  - N_percent, C_percent
  - Total_N_gcm3, Total_C_gcm3
- One sampled location (U8) was excluded due to the presence of a pond.

# Purpose and expected outcomes

- The study aims to quantify how planting and natural regeneration influence soil C and N stocks over time, with baseline data established in Autumn 2022 and ongoing monitoring through planted and regeneration plots.  
- The data support comparisons between planted areas, natural regeneration, and grassland controls, and enable assessment of soil carbon and nitrogen dynamics under forest restoration.