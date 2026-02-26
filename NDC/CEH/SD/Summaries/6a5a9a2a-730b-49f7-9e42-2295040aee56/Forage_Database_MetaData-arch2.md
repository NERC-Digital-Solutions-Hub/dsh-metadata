# CENTRAL ASIAN FORAGE PLANTS

- Purpose and scope
  - A database compiling desert and steppe forage plants with a focus on saiga antelope foraging. It standardizes chemical composition data from multiple sources to support environmental monitoring and policy assessment over time.
  - Two main tables: PLANTS (plant species and identification) and VALUES (multiple chemical composition records per plant from various sources).

- PLANTS table: what it contains
  - Approximately 1,000 desert/steppe species with Latin and Russian names, family, life form (e.g., annual, perennial, shrub), and local names.
  - Saiga_Food flag indicating whether a plant has been recorded as saiga food, with Saiga_Food_Source codes (ACBK, FS, TB) documenting the data source.
  - Season_Eaten and Saiga_Value (1–4 scale: 1=inedible, 2=poor, 3=edible, 4=excellent) for saiga relevance when available.
  - Life_Form and Saiga_Food_Source help relate plant type and usage to saiga for ecological analyses.

- VALUES table: what it contains
  - Records linked to PLANTS via Plant_ID, including plant name, country, location, year, season, month, phase (phenology), number of samples, and part analysed.
  - Chemical composition data: Water content, Crude_Protein, Protein, Ash, Cellulose, NFE, Fat, Digestible_Protein, and related drying information (Drying_Sample) and various water-related fields (Water_Undried, Water_Airdried, Water_Resid).
  - Energy and productivity metrics: Feed_Units_100KG (SFU), Met_Energy_MJ_KG (metabolisable energy), and Protein_PFU (grams of digestible protein per SFU). Coefficients of digestibility (CD_Crude_Protein, CD_Protein, CD_Fat, CD_Cellulose, CD_NFE) are included where available.

- Forage quality interpretation
  - Forage values based on chemical composition are not always directly indicative of quality; edibility coefficients (Coeff_Edibility) reflect actual edible biomass regardless of composition.
  - Some plants are edible in certain seasons or growth stages; growth coefficients (Coeff_Growth) indicate above-ground biomass relative to annual maximum.

- Normalization and data comparability
  - Water content and drying method crucial for cross-source comparisons. Drying_Sample indicates whether data are from undried, air-dried, oven-dried, absolute dry matter, etc.
  - Water ≠ 0 implies components are percent of total (including water). Water = 0 implies percentages are from absolute dry matter (no water).

- Energy and digestibility considerations
  - Soviet-era energy units: SFU and EFU are present, with explanations of their equivalences to digestible energy measures. Most data have been converted to MJ/kg where possible.
  - Metabolizable energy (MJ/kg) is derived from digestible nutrients (TDN-based conversions) when SFU data are present, using species- and component-specific coefficients of digestibility where available.

- Growth, edibility, and biomass context
  - Growth coefficients (Coeff_Growth) provide monthly or seasonal biomass as a percentage of annual maximum.
  - Edibility coefficients (Coeff_Edibility) indicate the proportion of above-ground biomass edible by livestock, based on multi-annual observations.

- Sources and methodologies
  - Core sources include Tomme (1964), Ospanova (1996), Giprozem (1995), Nechaeva & Nikolaev (1991), Nikolaev (1994), Kurochkina & Shabanova (1990), Mel’nik (1961), Morozova (1940), Morozov (1957), Kanchaev (1999, 2003), Gintzburger (2003), and others.
  - Methodological notes explain how raw composition data were transformed (e.g., from undried, air-dried, or absolute dry matter) and how energy and digestibility metrics were calculated or back-calculated to enable comparability.

- Table definitions (brief)
  - Table 1: PLANTS
    - Fields: PLANT_ID, Name_Latin, Name_Latin_alternative, Name_Russian, Name_Local, Life_Form, Family, Saiga_Food, Saiga_Food_Source, Season_Eaten, Saiga_Value.
  - Table 2: VALUES
    - Fields: ID, Name_Latin, Plant_ID, Source_Ref, Page_Ref, Country, Location, Year, Season, Month, Phase, Number_Samples, Part_Analysed, Drying_Sample, Water, Crude_Protein, Protein, Cellulose, NFE, Ash, Fat, Digestible_Protein, Water_Undried, Water_Airdried, Water_Resid, Water, Met_Energy_MJ_KG, Feed_Units_100KG, CD_Crude_Protein, CD_Protein, CD_Fat, CD_Cellulose, CD_NFE, Coeff_Growth, Coeff_Edibility, Protein_PFU.

- Notable caveats and considerations
  - Data are drawn from multiple decades and sources; comparability depends on consistent drying methods and biomass definitions.
  - Some entries refer to the edible fraction rather than total biomass; inferences about forage value should consider the context and available coefficients.
  - The dataset emphasizes the saiga’s foraging ecology, but users should integrate with other environmental and policy data for monitoring and decision-making.

- Acknowledgements and references
  - Acknowledges authors, data inputs, and funding sources; provides extensive references for methods and data origins, illustrating the dataset’s historical breadth and scholarly backing.

- Relevance to environmental monitoring and policy performance
  - Provides standardized, source-traceable data on plant species and their nutritional and edible properties as they relate to saiga foraging.
  - Facilitates longitudinal analyses of forage resources, seasonal dynamics, and potential impacts of environmental change or management policies.
  - Supports data accessibility and integration by detailing data provenance, transformation steps, and standardized output formats.