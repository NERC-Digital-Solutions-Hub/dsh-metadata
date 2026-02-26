# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2017-19

- What the data are
  - Two 1x1 km gridded datasets of Average Accumulated Exceedance (AAE) for acidity and for nutrient nitrogen critical loads due to acid and nitrogen deposition, for 2017–2019.
  - AAE summarises exceedances across multiple habitats within each grid square.

- How AAE is calculated
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × habitat area (ha).
  - Sum AE across habitats within a 1x1 km grid square.
  - AAE = total AE / total habitat area in the grid square (keq ha-1 year-1).
  - For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Acidity AAE represents a combination of sulphur and nitrogen deposition and is reported in keq ha-1 year-1; cannot be converted to kg of S or N.

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

- Data sources and validation
  - Methods aligned with UK CLRTAP processes; detailed methods report Hall et al. (2015).
  - Summary exceedance statistics published in the Trends Report (e.g., Hall et al., 2017) and as a UK Biodiversity Indicator (B5a).
  - CBED deposition data referenced from the EIDC.
  - Uncertainties documented in Hall et al. (2015) and critical loads metadata.

- Data coverage and structure
  - Files: acidhab_AAE_2017-19.csv (acidity) and nutnhab_AAE_2017-19.csv (nutrient nitrogen).
  - Coverage differs by dataset due to habitat distributions.
  - Each row includes:
    - East_m, North_m: grid square centre coordinates (OSGB grid, metres).
    - Unique1km: unique 1x1 km grid square identifier (allows linking between acidity and nitrogen files).
    - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1).
    - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.

- Use and interpretation guidance
  - National critical load maps are based on empirical/steady-state methods; exceedance indicates potential for harmful long-term effects, not necessarily current damage.
  - Habitat distribution maps and habitat areas used for critical loads may differ from other maps; totals may differ accordingly.
  - Reducing deposition below the critical load does not imply immediate ecosystem recovery; chemical and biological recovery can be time-lagged and prolonged.

- Data governance, metadata and sharing
  - Emphasises transparency, metadata availability, and the need for data governance.
  - Public sharing of underlying data may be a barrier in some cases; data provenance and metadata are provided to support verification and reuse.

- References and further information
  - Hall, J., Curtis, C., Dore, T., Smith, R., 2015. Methods for the calculation of critical loads and their exceedances in the UK.
  - Rowe, E. et al., 2019. Trends Report 2019: Trends in critical load and critical level exceedances in the UK.
  - Additional data access through the EIDC (for CBED deposition) and Defra-related outputs.