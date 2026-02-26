# CENTRAL ASIAN FORAGE PLANTS

- The database comprises two tables: PLANTS and VALUES, focused on desert and steppe plant species and their chemical composition as it relates to saiga foraging.
- PLANTS lists nearly 1,000 species with Latin and Russian names, family, life form, and a flag indicating whether a plant is recorded as saiga food, plus a source for that information and seasonal context.
- VALUES contains multiple records per plant sourcing chemical composition (protein, ash, cellulose, fat), and where available, digestible protein, metabolisable energy, and Soviet Feed Units (SFU). Each record includes metadata on country, location, year, season/month, phenology, sample size, and how the sample was analyzed.
- The dataset emphasizes that forage quality based on chemistry is not a perfect predictor of palatability or intake; edibility coefficients and growth coefficients are included to reflect actual usefulness to livestock.
- The document provides detailed definitions and explanations of fields, data normalization issues, and methodologies used across primary sources.

## Data Model and Key Tables

- PLANTS
  - Plant_ID: Unique ID for each plant species.
  - Name_Latin, Name_Latin_alternative, Name_Russian, Name_Local: Taxonomic and local names.
  - Life_Form: Growth form (e.g., annual, perennial, shrub, etc.).
  - Family: Plant family.
  - Saiga_Food: Yes if recorded as saiga food; otherwise blank.
  - Saiga_Food_Source: Code indicating source of saiga-foraging information (ACBK, FS, TB).
  - Season_Eaten: Season in which the plant is eaten (per sources).
  - Saiga_Value: A value (1–4) indicating palatability/edibility from cited literature.

- VALUES
  - ID: Unique record ID.
  - Plant_ID: Link to PLANTS.
  - Source_Ref, Page_Ref: Source citation and page/table reference.
  - Country, Location, Year, Season, Month, Phase: Where and when the sample was collected and its phenology.
  - Number_Samples: Number of samples underpinning the chemical data.
  - Part_Analysed: Part of the plant analysed for composition.
  - Drying_Sample: Drying method baseline (air-dried, undried, absolute dry matter, unknown).
  - Water, Water_Undried, Water_Airdried, Water_Resid: Water content and related hydroscopic/undried data to standardize to 100% total.
  - Crude_Protein, Protein, Ash, Cellulose, NFE: Core chemical components (protein-related measures, mineral matter, fibre, carbohydrates).
  - Digestible_Protein: Digestible protein content (if provided).
  - Met_Energy_MJ_KG: Metabolisable energy measured or derived (MJ/kg).
  - Feed_Units_100KG: Soviet Feed Units per 100 kg of dry matter.
  - CD_Crude_Protein, CD_Protein, CD_Fat, CD_Cellulose, CD_NFE: Coefficients of digestibility for components.
  - Coeff_Growth: Growth coefficient as percent of maximum above-ground biomass for the season.
  - Coeff_Edibility: Edibility coefficient indicating the edible proportion of biomass (percentage).

## Key Concepts and How They Are Used

- Saiga_Food and Saiga_Food_Source
  - Indicates whether a plant is documented as saiga food and the source codes (ACBK, FS, TB) for that claim.
- Edibility and Growth Coefficients
  - Coeff_Edibility reflects the actual proportion of the plant’s biomass edible by livestock.
  - Coeff_Growth indicates seasonal biomass availability, aiding interpretation of when a plant is most useful.
- Chemical Composition and Energy Metrics
  - Core components: Crude_Protein, Ash, Cellulose, NFE, Fat; Digestible_Protein.
  - Energy metrics include SFU (Soviet Feed Units), Met_Energy_MJ_KG, and the implied Total Digestible Nutrients (TDN) concept through related calculations.
  - SFU calculations and conversions to comparable energy units are described, linking historically used units to modern MJ/kg.
- Data Normalization and Drying Context
  - Water content and Drying_Sample determine how percentages relate to total weight (100%), with notes on how undried, air-dried, and oven-dried baselines affect interpretation.
  - Some values may not sum to 100% due to incomplete water data or missing components; some data derive from edible biomass rather than total plant biomass.

## Data Provenance, Sources, and Methodologies

- Primary sources include Tomme (1964), Ospanova (1996), Giprozem (1995), Nikolaev (1994, 1980), Nechaeva & Nikolaev (1991), Morozov/Morozova (1957, 1940), Kanchaev et al. (1999, 2003), Kurochkina & Shabanova (1990), Mel’nik (1961), Morozova (1940), Ivanov (1973), and others.
- The dataset provides explicit notes on how different sources calculated or reported composition, energy, and digestibility (e.g., percent of absolute dry matter, undried/air-dried baselines, and how SFU/TDN relate to these figures).
- Acknowledgments credit data provision from multiple researchers and institutions; funding acknowledgments are included.

## Data Normalization and Calculations

- Water and drying
  - Water content is recorded to enable normalization to 100% weight; Drying_Sample indicates the drying baseline.
  - When Water > 0, percentages include water and sum to 100%; when Water = 0, figures are based on oven-dried (absolute dry matter) weight.
  - Some records include Water_Undried, Water_Airdried, and Water_Resid to capture pre-drying water and hygroscopic water.
- Energy and digestibility
  - SFU is tied to fat production calculations using component digestibility coefficients and a fat-production factor; results relate to a normalized comparison with 1 kg of oats.
  - TDN is computed from digestible nutrients (DCP, DNFE, DCF, DEE) with a fixed conversion to energy units.
  - EFU (metabolisable energy) values are derived from TDN and standardized to 10,000 kJ per EFU, then converted to MJ/kg for reporting.
  - Met_Energy_Unit_KG_DM provides MJ per kg dry matter; notes explain that exact calculation of EFU/ME requires species- and component-specific digestibility coefficients, which may be approximate.
- Growth and edibility coefficients
  - Coeff_Growth and Coeff_Edibility are derived from multiannual observations and field studies, providing seasonally varying context for biomass availability and edibility.

## Practical Implications for Data Leaders

- Holistic view of the forage data system
  - Enables cross-plant and cross-season assessment of forage resources for pastoral systems and saiga habitat considerations.
  - Supports co-ownership of data products by aligning with user needs (policy colleagues, field ecologists) by providing both chemical composition and practical usefulness (edibility, growth).
- Data quality and stewardship
  - Highlights need to standardize baselines (drying method, water normalization) when aggregating across sources.
  - Identifies gaps in data (e.g., granularity of location/year/season, complete energy/digestibility data for all records) and potential biases from older Soviet-era measurements.
- Cross-network collaboration potential
  - The dataset’s provenance and diverse sources make it suitable to link with broader rangeland, biodiversity, or saiga-management datasets to support coordinated stewardship and policy decisions.
- Actionable outputs
  - Edible biomass estimates and seasonal palatability signals can inform grazing planning, habitat management, and transboundary forage assessments.

## Limitations and Considerations

- Heterogeneity across sources
  - Different drying methods, baselines (undried vs. air-dried vs. oven-dried), and reporting units require careful normalization.
- Incomplete or approximate data
  - Not all records include digestible protein, ME, SFU, or energy conversions; coefficients of digestibility vary by source and sample.
- Edibility vs. chemical composition
  - Edibility coefficients provide a practical lens but depend on long-term observations and may not capture short-term variability or seasonal toxicity in some species.
- Documentation depth
  - While Tables 1 and 2 define fields, some records may lack complete metadata (e.g., precise location or year), affecting reproducibility of energy or digestibility calculations.

## References and Acknowledgements

- Comprehensive references accompany the dataset, detailing sources for chemical composition, digestibility, energy calculations, and edibility.
- Acknowledgements recognize data providers, collaborators, and funding support enabling the Central Asian Forage Plants database.