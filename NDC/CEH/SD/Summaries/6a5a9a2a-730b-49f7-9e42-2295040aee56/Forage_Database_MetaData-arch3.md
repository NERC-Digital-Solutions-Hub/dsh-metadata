# CENTRAL ASIAN FORAGE PLANTS

## Overview
- A database compiling saiga-related forage information, including plant species, chemical composition, energy values, and edibility.
- Aims to support monitoring of environmental health measures for policy scrutiny, evaluation, and future decisions, with clear metadata and data provenance to enable transparency and reuse.

## Data structure and content
- PLANTS table
  - Contains ~1,000 desert and steppe plant species.
  - Fields include: Latin name, alternative Latin name, Russian name, local name, life form, family, and a Saiga_Food flag indicating whether the plant is recorded as saiga forage.
  - Saiga_Food_Source codes indicate the source of saiga-forage information (ACBK, FS, TB).
  - Season_Eaten and Saiga_Value provide contextual foraging information.
- VALUES table
  - For each PLANT record, multiple records of chemical composition and energy data from various sources.
  - Fields link to PLANTS via Plant_ID and include: country, location, year, season, month, number of samples, part analysed, drying method (Drying_Sample), water content (Water) and related water fields, and detailed chemical components (Crude_Protein, Ash, Cellulose, NFE, Fat, Protein, Digestible protein).
  - Energy-related fields include Feed_Units_100KG, Met_Energy_MJ_KG, and supplementary digestibility data (CD_* coefficients).
  - Growth and edibility coefficients: Coeff_Growth (seasonal growth) and Coeff_Edibility (edibility percentage of above-ground biomass).
  - Edibility field (Coeff_Edibility) ranges conceptually from 0 (inedible) to higher values indicating greater edibility.
- Quick-reference Tables 1 and 2 summarize field definitions; detailed explanations are provided within the sections below.

## Forage quality, edibility, and palatability
- Forage values based on chemical composition are not always predictive of intake or safety; some plants may be nutritious yet toxic.
- Edibility coefficients (Coeff_Edibility) quantify actual edible biomass and are used to extrapolate biomass and edibility across seasons.
- Growth coefficients (Coeff_Growth) reflect biomass abundance at different phenological stages, aiding interpretation of seasonal forage availability.

## Data harmonization and normalization
- Water content (Water) must be paired with information on how samples were dried to interpret percentages accurately.
- Drying_Sample indicates whether figures are based on undried, air-dried, absolute dry matter, or unknown basis.
- Total percentage sums (including water) can reach 100% only when water content is included; otherwise, sums assume oven-dried (no water).
- Some data report water content before drying (Water_Undried) or as residual/hydroscopic water (Water_Resid, Water_Airdried), enabling cross-source comparisons.

## Energy and nutritional metrics
- Soviet Feed Units (SFU) are converted to metabolizable energy (ME) equivalents and converted to MJ/kg for standardization.
- Digestible nutrient approach (TDN) links chemical composition to energy; conversions to EFU (Energetic Feed Unit) integrate digestible nutrients and energy factors.
- Calculations depend on species-specific digestibility coefficients (CD_*) and, where available, the coefficient of fat production; values are approximations when coefficients vary by sample.
- A typical energy equation: metabolisable energy (ME) derived from digestible nutrients (DCP, DNFE, DCF, DEE) with established conversion factors; the database standardizes to MJ/kg for comparability.

## Sources and methodologies
- Core sources include Tomme (1964); Ospanova (1996); Giprozem (1995); Nechaeva & Nikolaev (1991); Nikolaev (1994); Morozov, Morozova, Kanchaev, and others.
- Methodological notes:
  - Some data are reported on undried, air-dried, or absolute dry matter bases; others are not consistently documented.
  - Digestibility coefficients come from long-term field studies or secondary compilations; coefficients can vary between samples.
  - SFU and other energy metrics are primarily tied to the edible fraction and absolute dry matter.
- The dataset explicitly documents limitations and notes where data are minima/maxima or where totals do not add to 100% due to missing water fractions.

## Data provenance and governance
- Provenance is captured via Source_Ref and Page_Ref, with detailed metadata: country, location, year, season, month, number of samples, and part analysed.
- The database emphasizes transparency, data sharing, and clear documentation of methodologies to support reuse in monitoring frameworks.
- Acknowledgments and funding sources are listed, underscoring the collaborative, long-term nature of the data collection.

## Relevance for environmental health monitoring and policy
- Enables assessment of forage resource quality and availability across space and time, informing pastoral resilience and risk assessment for environmental health.
- Supports policy decisions related to land use, grazing management, and wildlife–livestock interactions by providing standardized metrics and transparent data lineage.
- Helps identify data gaps and standardization needs (e.g., consistent drying methods, comprehensive metadata) to improve monitoring frameworks and data governance.

## Limitations and caveats
- Data heterogeneity across sources and time periods; missing or inconsistent fields (e.g., some samples lack digestibility data or exact drying basis).
- Edibility versus palatability may not align with chemical composition across species or seasons.
- Historical Soviet-era data may carry varying measurement standards and reporting conventions.
- While extensive, the dataset may still require ongoing updates and validation to support current policy needs.

## Acknowledgements and references
- Recognizes contributors, data providers, and funding bodies enabling the compilation of this resource.
- Cites primary sources and references used to derive chemical composition, energy metrics, and foraging knowledge.