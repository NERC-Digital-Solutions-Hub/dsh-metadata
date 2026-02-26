# CENTRAL ASIAN FORAGE PLANTS

## Overview
- A dataset comprising two tables, PLANTS and VALUES, documenting desert and steppe plant species relevant to saiga antelope foraging.
- PLANTS lists nearly 1,000 species with Latin/Russian names, family, life form, and flags indicating saiga food status with source references.
- VALUES augments each plant entry with multiple records of chemical composition (protein, ash, cellulose, fat, NFE, etc.), energy metrics (Soviet Feed Units, metabolisable energy), and contextual data (country, location, year, season, phenology).
- Includes edibility and growth coefficients to aid interpretation of chemical data for grazing; notes on the distinction between total biomass and edible fraction; and cautions about variability between sources.

## Data Model

- Table 1: PLANTS
  - Key fields include: PLANT_ID, Name_Latin (and alternative), Name_Russian, Name_Local, Life_Form, Family
  - Saiga_Food (flag indicating recorded saiga consumption), Saiga_Food_Source (code: ACBK, FS, TB), Season_Eaten, Saiga_Value (1–4: inedible to excellent)

- Table 2: VALUES
  - Key fields include: ID, Plant_ID (link to PLANTS.PLANT_ID), Source_Ref, Page_Ref, Country, Location, Year, Season, Month, Phase
  - Sampling and analysis fields: Number_Samples, Part_Analysed, Drying_Sample (air-dried, undried, absolute dry matter, unknown), Water (percent), Water_Undried, Water_Airdried, Water_Resid, Water_Resid
  - Chemical composition fields: Crude_Protein, Protein (subset), Ash, Cellulose, NFE, Fat, Digestible_Protein
  - Energy and digestibility fields: Feed_Units_100KG, Met_Energy_MJ_KG, CD_Crude_Protein, CD_Protein, CD_Fat, CD_Cellulose, CD_NFE, Coeff_Growth, Coeff_Edibility
  - Edibility and energy interpretation: Protein_PFU (grams of digestible protein per Soviet Feed Unit)
  - Additional notes: Some data are reported on undried/air-dried/absolute-dry matter with varying normalization; SFU/EFU conversions and metabolisable energy are described in-methods.

## Data Provenance and Methodologies

- Primary sources and documentation referenced for the chemical and nutritional data include:
  - Tomme (1964): Forage Plants of the Soviet Union; digestibility coefficients and calculation methods
  - Ospanova (1996): Fodder plants of Kazakhstan; absolute dry matter basis
  - Giprozem (1995); Nechaeva & Nikolaev (1991); Nikolaev (1994); Morozov (1957/1940); Kanchaev (1999/2003); Morozova (1940); Mel'nik (1961); Ivanov (1973); and others
  - Acknowledged secondary sources and field studies informing growth and edibility coefficients
- Saiga foraging data sources are coded as:
  - ACBK (Kazakh Association for Conservation of Biodiversity reports)
  - FS (Fadeev & Sludskii)
  - TB (Tables compiling saiga food plants)
- Documentation explains that field data come from diverse years, locations, and sampling methods, with explicit data lineage in Source_Ref and Page_Ref.

## Normalization, Units, and Data Quality

- Water content and drying:
  - Water field indicates water percentage for total 100% mass; if Water = 0, data are on oven-dried basis (no water).
  - Drying_Sample indicates drying status: airdried, undried, absolute dry matter, or unknown.
  - Additional fields (Water_Undried, Water_Airdried, Water_Resid) support interpretation of drying state and hydroscopic water.
- Comparability across sources:
  - Forage composition values come from sources with different drying bases (undried, air-dried, oven-dried). Normalization to 100% requires known drying method.
  - SFU and EFU calculations are described in-methods; EFU is expressed per 100 kg dry matter, with conversions to MJ/kg. Metabolisable energy (MJ/kg) is provided where available; when SFU is given without chemical data, calculations are approximate and rely on digestible nutrients (TDN) concept.
- Biomass distinctions:
  - Some sources distinguish total biomass versus edible biomass; chemical values may refer to edible fraction or whole plant, requiring careful interpretation.
- Coefficients and data reliability:
  - Growth coefficients (Coeff_Growth) and edibility coefficients (Coeff_Edibility) are long-term average values derived from multiannual observations; exact sample context may vary by source.
  - Digestibility and energy coefficients (CD_*) exist for some components, but coefficients vary between samples, so derived metrics are approximate.
- Data gaps and inconsistencies:
  - Zeros vs nulls indicate seasonality gaps or missing data for certain metrics.
  - Some tables show totals not summing to 100% due to missing water or incomplete reporting.

## For Data Stewards: Key Considerations

- Metadata and provenance:
  - Maintain clear mapping of Source_Ref to bibliographic records; capture page references and sampling details (Country, Location, Year, Season, Month, Phase).
- Data normalization rules:
  - Enforce consistent handling of drying methods and water content to allow cross-source comparability.
  - Standardize energy metrics to MJ/kg where possible; document any residual use of SFU/TDN-derived values.
- Controlled vocabularies:
  - Use consistent values for Life_Form, Drying_Sample, Season, and Saiga_Food_Source codes; align with documented definitions.
- Data quality checks:
  - Validate that numeric fields sum logically (e.g., components summing toward 100% for undried/air-dried data where applicable).
  - Flag records with incomplete or ambiguous drying information or with conflicting edibility/forage status.
- Documentation and governance:
  - Keep thorough documentation of field definitions (Tables 1 and 2), including the meaning of each field, units, and derivation notes.
  - Implement versioning and change-tracking for updates or corrections; document any recalculations (e.g., energy units) and their formulas.
- Accessibility and reuse:
  - Ensure licensing, attribution, and source integrity are preserved for derived analyses; provide guidance on appropriate use given potential measurement variability across sources.

## Practical Implications for Use

- The dataset enables assessment of forage quality and edible fraction for saiga-focused ecological studies, as well as broader ruminant nutrition contexts in Central Asian arid zones.
- Researchers and managers should interpret chemical composition alongside edibility and growth coefficients, with attention to the drying basis and the provenance of each record.
- For risk-aware decision-making, document uncertainties arising from cross-source variability and season-specific parameters.

## Summary

- CENTRAL ASIAN FORAGE PLANTS is a two-table dataset capturing plant species and their chemical composition, energy content, and saiga forage relevance across multiple sources and years.
- Data stewardship requires careful handling of drying methods, water normalization, energy unit conversions, and provenance to ensure accurate cross-source comparisons.
- Edibility and growth coefficients add practical context for interpreting nutritional data, but users must be mindful of potential variability and incomplete reporting across historical sources.