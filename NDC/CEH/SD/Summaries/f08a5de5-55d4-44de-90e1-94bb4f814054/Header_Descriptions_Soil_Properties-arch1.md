# Header Descriptions for Dataset "OH_Soil_Properties" and "NH4_NO3_OH_Soil Properties"

## Overview
- The document lists the header fields and descriptions for two soil datasets used to capture site, sampling, and soil chemical/microbial properties.
- Data are intended to support analyses of correlations, model development, and inference on the likely impact of factors such as wildfire age on soil properties.

## OH_Soil_Properties fields
- Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
- Site: Site name.
- Sample: Sample number at that site.
- Age: Site age since last wildfire (years).
- Depth: Depth of soil organic horizon (cm).
- BD: Bulk density, soil organic horizon (g cm-3).
- CN: Ratio of total carbon to total nitrogen, soil organic horizon.
- pH: pH, soil organic horizon.
- LOI: Loss on ignition, soil organic horizon (% soil organic matter).
- P: Total phosphorous, soil organic horizon (mg g -1 soil dry weight).
- totPlfa: Total phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
- totFung: Total fungal phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
- totBact: Total bacterial phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
- fungBact: Ratio of fungal to bacterial phospholipid fatty acid content.

## NH4_NO3_OH_Soil Properties fields
- Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
- Site: Site name.
- Sample: Sample number at that site.
- Age: Site age since last wildfire (years).
- NO3.ppm: NO3- concentration, soil organic horizon (parts per million).
- NH4.ppm: NH4+ concentration, soil organic horizon (parts per million).
- mgNO3.N: NO3- concentration, soil organic horizon (mg kg -1 soil dry weight).
- mgNH4.N: NH4+ concentration, soil organic horizon (mg kg -1 soil dry weight).

## Analytical use and considerations
- The OH_Soil_Properties dataset provides physical and chemical soil properties and microbial community indicators (planktonic/cellular markers) across soil organic horizons.
- The NH4_NO3_OH_Soil Properties dataset supplies inorganic nitrogen forms (nitrate and ammonium) in the soil organic horizon, enabling nutrient availability analyses.
- Together, these headers support:
  - Exploring relationships between wildfire age and soil properties (e.g., CN, pH, LOI, P).
  - Assessing microbial community balance via totPlfa, totFung, totBact, and fungBact.
  - Linking soil chemistry with nitrogen forms (NO3-, NH4-) and their potential ecological implications.
  - Multi-source data integration by aligning on Site, Sample, and Age to track changes over time and space.