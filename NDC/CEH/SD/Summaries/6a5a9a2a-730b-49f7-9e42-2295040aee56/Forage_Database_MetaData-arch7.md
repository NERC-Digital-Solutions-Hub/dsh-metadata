# CENTRAL ASIAN FORAGE PLANTS

- A biogeographically focused database combining plant species data with chemical composition and energy values, intended to support understanding of forage resources for saiga and other livestock.

## What the database contains

- Two main tables:
  - PLANTS: about 1000 desert and steppe plant species with Latin/Russian names, family, life form, and a flag for saiga foraging (Saiga_Food) with source codes (Saiga_Food_Source) and seasonality (Season_Eaten).
  - VALUES: per-plant chemical composition records linked to PLANTS (Plant_ID), including multiple sources, geography (Country, Location), time (Year, Season, Month, Phase), sample size, and details of the sample analysis.
- Each PLANTS record can have multiple VALUE records giving different chemical/energy measurements for different times/locations.

## Key fields and concepts (GIS-relevant)

- Plant-level identifiers and taxonomy:
  - Plant_ID, Name_Latin, Name_Russian, Family, Life_Form
- Forage relevance:
  - Saiga_Food (Yes/NA), Saiga_Food_Source (codes ACBK, FS, TB), Season_Eaten, Saiga_Value (1–4)
- Spatial and temporal context (to map distributions and seasonal patterns):
  - Country, Location, Year, Season, Month, Phase
- Chemical composition and related metrics (for thematic mapping and modeling):
  - Drying and normalization: Drying_Sample, Water, Water_Undried, Water_Airdried, Water_Resid
  - Key composition: Crude_Protein, Protein, Ash, NFE, Cellulose, Digestible_Protein
  - Energy and digestibility: Feed_Units_100KG, Met_Energy_MJ_KG, Coeff_Growth, Coeff_Edibility
  - Digestibility coefficients: CD_Crude_Protein, CD_Protein, CD_Fat, CD_Cellulose, CD_NFE
  - Growth/edibility context: Growth_Coefficient per season, Edibility_Coefficient (Coeffs) for edible biomass

- Table 2 includes mirrored/parallel fields for multiple records per Plant_ID with detailed Page_Ref, Source_Ref, and sampling metadata.

## How the data is normalized and used

- Water and drying matters:
  - Water field indicates whether values are on a 100% basis or exclude water (0 means oven-dried, 100% dry basis implied by totals).
  - Drying_Sample indicates whether data are undried, air-dried, absolute dry matter, or unknown; essential for cross-source comparability.
- Forage energy concepts:
  - Soviet Feed Unit (SFU) and Energetic Feed Unit (EFU) are units historically used; EFU is converted to MJ per kg dry matter in this dataset.
  - Metabolizable energy (ME) is normalized to MJ/kg DM; SFU/TDN-based conversions are outlined, with TDN and ME related through established coefficients.
- Composition and edibility:
  - Protein, Ash, NFE, Cellulose, Digestible_Protein fields capture the chemical basis.
  - Coeff_Edibility indicates the practical edible fraction of green biomass, independent of chemistry.
  - Growth_Coeff links biomass amount to growth stage (e.g., peak biomass month 100).

## How this supports GIS data products

- Joinable data:
  - PLANTS <-> VALUES via Plant_ID to create species-level thematic maps of forage quality, edibility, and energy content across space and time.
- Map-ready attributes:
  - Presence of saiga food plants (Saiga_Food), seasonality (Season_Eaten), and edibility/growth coefficients enable choropleth and symbol maps by country, location, or season.
- Temporal analyses:
  - Year, Season, and Month fields support time-series visualizations (e.g., seasonal forage availability across regions).
- Data layering potential:
  - Overlay with saiga distribution data, pastoralist zones, or grazing calendars to assess forage sufficiency and risk periods.

## Considerations and caveats for GIS use

- Data heterogeneity:
  - Multiple sources with different drying methods and biomass bases (undried vs air-dried vs absolute dry matter) require careful normalization before comparatives.
- Gaps and incompleteness:
  - Some records have zero (indicating non-consumption in a season) or nulls (no data); interpret accordingly in maps.
- Edibility vs chemical composition:
  - Do not assume high nutritional value equates to high forage intake; edibility coefficients are crucial for real palatability.
- Biomass vs edible fraction:
  - In some sources, data refer to total biomass, others to edible fraction; use Coeff_Growth and Coeff_Edibility to estimate usable forage.
- Spatial precision:
  - Location is provided as textual fields (Location, Country); geolocating may be required for precise GIS analyses.

## Data sources and provenance

- Primary sources include Tomme (1964), Ospanova (1996), Nechaeva & Nikolaev (1991), Nikolaev (1994), Morozova (1940), Morozov (1957), Kanchaev et al. (1999, 2003), Giprozem (1995), and others; data are compiled to support forage assessments in Central Asia.
- Acknowledgements note contributors, funders, and related projects.

## Practical guidance for creating GIS products

- Data preparation:
  - Link PLANTS to VALUES via Plant_ID; standardize drying basis and Water interpretation to a common 100% DM basis where feasible.
- Visualization ideas:
  - Map saiga-food plant frequency by region (Saiga_Food) with seasonality (Season_Eaten) as time-enabled layers.
  - Create risk/quality maps using Edibility_Coefficient and Met_Energy_MJ_KG (along with Growth_Coefficient) to show seasonal forage value.
  - Use Protein/NFE/Cellulose/Coefficients to derive nutrient profiles for ecological or pastoral planning.
- Data handling notes:
  - When interpreting SFU/EFU and RT ME values, document the species- and component-specific coefficients used for any derived metrics.
  - Be explicit about the drying method and water content when aggregating across records.

## Acknowledgements

- Author: Sarah Robinson; data input: Louise Köhler and Bibiana Dobosova; various data providers and funders acknowledged.

## References (selected)

- Abaturov et al. 1982; ACBK reports; AFRC 1993; Gintzburger et al. 2003; Ivanov 1973; Johnstone et al. 1999; Kalashnikova et al. 2003; Tomme 1964; Ospanova 1996; Nikolaev 1994; Morozov 1957; Kanchaev et al. 1999, 2003; and others.