# CENTRAL ASIAN FORAGE PLANTS

## Overview
- A database of desert and steppe forage plants focused on saiga antelope feeding. Includes two main tables: PLANTS and VALUES, covering nearly 1000 species with scientific and local names, family, life form, and whether saiga is recorded to eat them.
- For each plant, multiple chemical composition records from various sources, including protein, ash, cellulose, fat, and, where available, digestible protein, metabolisable energy, and Soviet Feed Units (SFU).
- Each chemical record is linked to metadata such as country, location, season, month, and phenological phase, enabling context-specific analysis.
- Additional fields capture edibility and growth information to help translate composition into actual forage use by livestock and saiga.

## Data structure and fields

### PLANTS (Table 1)
- Plant_ID: Unique species identifier
- Name_Latin / Name_Latin_alternative: Primary and alternative Latin names
- Name_Russian / Name_Local: Russian and local language names
- Life_Form: Growth form (annual, perennial, shrub, etc.)
- Family: Plant family
- Saiga_Food: Flag if plant is recorded as saiga food (Yes) or NA if unrecorded
- Saiga_Food_Source: Source code for saiga foraging information (ACBK, FS, TB)
- Season_Eaten: Season(s) when plant is eaten (from sources)
- Saiga_Value: Saiga palatability/edibility rating (1–4 per Abaturov et al. 1982)

### VALUES (Table 2)
- ID: Unique record identifier
- Name_Latin / Name_Russian: Latin and Russian names (matching PLANTS)
- Plant_ID: Link to PLANTS table
- Source_Ref: Reference source for the data
- Page_Ref: Page/table number in the reference
- Country / Location / Year / Season / Month / Phase: Context of sampling
- Number_Samples: How many samples underpin the composition values
- Part_Analysed: Part of plant analysed
- Drying_Sample: Drying method level (air-dried, undried, absolute dry matter, unknown)
- Water / Water_Undried / Water_Airdried / Water_Resid: Water content notes and related hydroscopic water
- Crude_Protein / Protein: Total nitrogenous content (and the amino-acid–containing subset)
- Ash: Mineral matter
- Cellulose: Cellulose content
- NFE: Nitrogen-free extract
- Fat: Fat content
- Digestible_Protein: Digestible protein (if provided)
- Digestible protein / Met_Energy_MJ_KG: Digestible protein and metabolisable energy (where available)
- Met_Energy_Unit_KG_DM: Metabolisable energy unit per kg dry matter
- Feed_Units_100KG: Soviet Feed Units per 100 kg dry matter
- CD_Crude_Protein / CD_Protein / CD_Fat / CD_Cellulose / CD_NFE: Coefficients of digestibility for components
- Coeff_Growth: Growth coefficient (seasonal percentage of maximum above-ground biomass)
- Coeff_Edibility: Edibility coefficient (percentage of green biomass edible to livestock)

## Forage values, edibility, and saiga relevance
- Forage values are derived from chemical composition, but high nutritive value does not guarantee safe or palatable intake (edibility coefficients account for palatability and potential toxicity).
- Edibility Coeff_Edibility indicates how much of the above-ground biomass is actually edible by livestock.
- Saiga_Eaten flag and Saiga_Value provide a structured view of saiga foraging records, aiding ecological and forage-use analyses.

## Normalization and energy metrics
- Water content varies by source and drying method; Water and related fields are essential to normalize to 100% total mass.
- Drying_Sample indicates if figures are based on air-dried, undried, absolute dry matter, or unknown samples.
- Values may be reported per undried, air-dried, or absolute dry matter; researchers must apply the appropriate normalization to interpret percentages correctly.
- Energy metrics:
  - SFU (Soviet Feed Units): Historical energy metric converted from digestible fat production, related to TDN, and used in several Soviet-era sources.
  - TDN (Total Digestible Nutrients): Sum of digestible components, provides a relative measure of feed value.
  - EFU (Energetic Feed Unit): Introduced in 1985, linked to metabolisable energy (ME); data converted to MJ/kg in the database.
  - Met_Energy / Met_Energy_MJ_KG: Metabolisable energy expressed in MJ/kg; conversion relies on digestible nutrients and component-specific coefficients.
- Important note: Metabolisable energy cannot be precisely calculated from raw components without species- and component-specific digestibility coefficients; existing coefficients (CD_*) are used where available but are approximate and sample-dependent.

## Growth and edibility coefficients
- Growth Coeff_Growth: Seasonal percentage of maximum above-ground biomass, used to adjust nutritional estimates across the year.
- Coeff_Edibility: Percentage of above-ground biomass edible by livestock, derived from multi-year field observations and literature.

## Data sources and methodologies
- Primary sources include: Tomme (1964), Ospanova (1996), Giprozem (1995), Nechaeva & Nikolaev (1991), Nikolaev (1994), Kurochnkina & Shabanova (1990), Mel'nik (1961), Morozova (1940), Morozov (1957), Kanchaev (1999, 2003), Gintzburger (2003), and others.
- The Saiga dataset references specific sources for saiga foraging data (ACBK reports, Fadeev & Sludskii 1982, TB compilation).
- The table of field definitions and the accompanying tables summarize and standardize terms to enable cross-source comparisons.

## Data quality, caveats, and best practices
- Data come from a mix of undried, air-dried, and oven-dried samples; normalization is necessary to compare records.
- Some records may list edibility or composition inconsistently across sources; use Coeff_Growth and Coeff_Edibility to infer year-round usability.
- The Saiga_Food flag indicates recorded saiga consumption but is not a definitive absence of consumption (null implies no written record).
- Coefficients of digestibility and energy conversions vary by sample and source; treat them as approximate and cite the original source when applying them.

## How to use this data (Data Support perspective)
- Build dashboards or reports enabling end users to explore plant species by family, life form, and saiga relevance, with adjustable filters for season, location, and year.
- Self-serve analyses of forage quality by comparing chemical composition, digestible protein, ME, and SFU/EFU across sources and drying methods.
- Develop guidance tools that translate chemical composition into palatability and edible biomass using Growth and Edibility coefficients.
- Validate outputs by tracing analyses back to Source_Ref and Page_Ref, ensuring provenance and enabling reproducibility.
- Identify data gaps (patchy records, missing seasons, or incomplete edibility data) to prioritize data collection or targeted literature review.