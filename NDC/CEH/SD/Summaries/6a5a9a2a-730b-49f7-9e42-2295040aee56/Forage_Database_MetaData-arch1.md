# CENTRAL ASIAN FORAGE PLANTS

- The database comprises two tables: PLANTS (desert and steppe species with taxonomic names, life form, family, and flags for saiga food) and VALUES (multiple chemical composition records per plant from various sources, with contextual metadata).
- It includes saiga-related forage information, with sources indicating whether a plant has been observed as saiga food and the season of consumption.
- Edibility and nutritional data are provided, along with methods to normalize across different sample preparations and drying methods.
- The dataset records temporal and spatial details (country, location, year, season, month, phenology) and sample-level information (number of samples, part analysed, drying method).

## Data structure and key fields

- PLANTS table
  - PLANT_ID: Unique plant species identifier
  - Name_Latin, Name_Latin_alternative, Name_Russian, Name_Local
  - Life_Form, Family
  - Saiga_Food: whether saiga has been observed grazing this plant (yes or blank)
  - Saiga_Food_Source: source codes (ACBK, FS, TB)
  - Season_Eaten: season when plant is eaten (per sources)
  - Saiga_Value: 1–4 scale for saiga palatability/edibility (1=inedible, 4=excellent)
- VALUES table
  - ID: Unique record identifier
  - Plant_ID: Links to PLANTS.PLANT_ID
  - Source_Ref, Page_Ref: Data source and page
  - Country, Location, Year, Season, Month, Phase
  - Number_Samples, Part_Analysed
  - Drying_Sample: level of drying (air-dried, undried, absolute dry matter, unknown)
  - Water, Water_Undried, Water_Airdried, Water_Resid
  - Chemical composition: Crude_Protein, Protein, Ash, Cellulose, NFE, Fat, Digestible_Protein
  - Energy and digestibility: Feed_Units_100KG, Met_Energy_MJ_KG, CD_Crude_Protein, CD_Protein, CD_Fat, CD_Cellulose, CD_NFE
  - Growth and edibility: Coeff_Growth, Coeff_Edibility
  - Other: Protein_PFU, Water content data, etc.
- Important note: Water and drying fields are used to convert results to 100% total weight; 0 in Water indicates oven-dried samples; null indicates missing data.

## Forage quality, edibility, and palatability

- Forage value is based on chemical composition, but edibility may differ due to toxicity or plant defenses.
- Coeff_Edibility indicates the proportion of a plant’s biomass that is edible by livestock (0 = inedible, higher values = more edible).
- Life form and seasonal growth influence nutrient availability and palatability; growth coefficients indicate percent annual maximum biomass by month/season.

## Energy and nutritive metrics

- Soviet Feed Unit (SFU): historical energy unit linked to fat production; conversion to modern metrics is described and used to compare with other systems.
- Digestible Nutrients: Total Digestible Nutrients (TDN) related to crude protein, NFE, cellulose, and fat; conversion to metabolisable energy (ME) via established constants.
- Metabolisable energy (ME): Reported as Met_Energy_MJ_KG or derived from SFU/TDN data; all ME values in the database are expressed in MJ/kg.
- Calculations and conversions:
  - SFU can be derived from digestible nutrients and energy coefficients, relating to oats as a reference.
  - TDN = DCP + DNFE + DCF + 2.25(DEE) (where DEE is digestible fat energy)
  - ME derived from TDN and standard conversions; in this database, values are converted to MJ/kg.
- Some records include digestible protein and other digestibility coefficients (CD_ fields) that vary by source and sample.

## Data provenance and sources

- Key sources include:
  - Tomme (1964): Forage Plants of the Soviet Union; digestibility coefficients and back-calculations from dried samples
  - Ospanova (1996): Fodder Plants of Kazakhstan; data calculated on absolute dry matter
  - Giprozem (1995), Nechaeva & Nikolaev (1991), Nikolaev (1994/ed.), Morozov (1957/1994), Morozova (1940), Kanchaev and colleagues (1999/2003)
  - Abaturov et al. (1982), ACBK reports (2012–2014)
- The dataset includes life-form, growth, and edibility coefficients drawn from long-term field studies and strategic manuals.
- Acknowledgements cite data providers, funders, and the institutions involved.

## Practical usage for analysts

- Link plant taxonomic data with chemical composition and energy metrics to assess forage quality across species, seasons, and locations.
- Identify saiga food plants and compare their edibility and seasonal availability to prioritize conservation and grazing management.
- Use edibility coefficients to adjust estimates of usable forage biomass, particularly when predicting intake.
- Normalize chemical composition data by drying method and water content to enable cross-source comparisons.
- Analyze spatial-temporal patterns:
  - Country, Location, Year, Season, Month, and Phase data allow mapping and trend analysis of forage resources.
- Build models to predict forage value (protein, ME, SFU/ME) based on life form, season, and habitat type.
- Use growth coefficients to extrapolate biomass availability through the year and its impact on grazing pressure.

## Challenges, limitations, and caveats

- Data are drawn from multiple sources with varying methodologies (drying methods, sample parts, and calculation bases), requiring careful normalization.
- Water content and drying method critical for converting percentages to 100% total weight; inconsistent reporting can introduce bias.
- SFU and TE/TDN measures require approximate coefficients of digestibility; coefficients can vary by sample and source, making exact conversion approximate.
- Not all records provide complete data (some fields are null or missing); data completeness varies by species and season.
- Edibility does not guarantee actual intake in natural settings; palatability and local availability influence consumption.
- Some plants may be listed as eaten in one source and inedible in another; seasonality and sporadic consumption must be considered.
- Administrative boundaries and local context may limit direct comparability across studies and regions.