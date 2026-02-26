# Header Descriptions for Dataset "OH_Soil_Properties" and "NH4_NO3_OH_Soil Properties"

## Overview
- Defines the header fields and their meanings for two soil-property datasets used to capture sampling metadata, soil chemistry, and microbial indicators across sites and sampling times.

## OH_Soil_Properties – Key fields
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

## NH4_NO3_OH_Soil Properties – Key fields
- Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
- Site: Site name.
- Sample: Sample number at that site.
- Age: Site age since last wildfire (years).
- NO3.ppm: NO3- concentration, soil organic horizon (parts per million).
- NH4.ppm: NH4+ concentration, soil organic horizon (parts per million).
- mgNO3.N: NO3- concentration, soil organic horizon (mg kg -1 soil dry weight).
- mgNH4.N: NH4+ concentration, soil organic horizon (mg kg -1 soil dry weight).

## Data quality and usage considerations
- Data spans soil chemistry (NO3, NH4, P), basic soil properties (pH, CN, BD), and organic matter indicators (LOI), plus microbial markers (PLFA metrics: totPlfa, totFung, totBact, fungBact).
- Be mindful of unit consistency when combining fields across datasets (ppm vs mg kg-1; nmol g-1 for PLFA).
- Some fields may require cross-dataset mapping (e.g., Site, Age, Sample) to enable integration.
- These headers support creating self-serve data products (dashboards, pivot tables) and communicating results to non-technical end users.

## How Data Support can use and share these outputs
- Validate asks by confirming required fields (e.g., site name, sample ID, time point, and specific chemical or microbial metrics).
- Clean and transform as needed (unit harmonization, handling missing values, aligning site identifiers).
- Combine with other datasets to build dashboards showing soil chemistry, nutrient status, and microbial balance across sites and time.
- Develop and promote early prototypes (e.g., simple summaries of NO3/NH4 trends, CN vs pH relationships) and iterate with stakeholder feedback.
- Advocate for consistent data creation and metadata documentation to improve reuse.