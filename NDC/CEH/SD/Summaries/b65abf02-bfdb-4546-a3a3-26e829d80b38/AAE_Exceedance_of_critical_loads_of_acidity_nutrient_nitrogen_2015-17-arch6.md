# 1x1 km AAE data sets for acidity and nutrient nitrogen 2015-17

- Purpose: Provide 1x1 km grid-based averages of exceedance above critical loads (Average Accumulated Exceedance, AAE) for acidity and nutrient nitrogen, enabling assessment of potential long-term impacts across habitats in the UK.

- What AAE measures
  - AAE is the sum of exceedances (per habitat) multiplied by the habitat area within a grid square, divided by the total habitat area in that square.
  - Formulae:
    - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha)
    - AAE (keq ha-1 year-1) = AE (keq year-1) / total habitat area (ha)
  - Values are zero when deposition is below the corresponding critical load.

- Habitats included
  - Acidity (for AAE): acid grassland; calcareous grassland; dwarf shrub heath; bog; montane; managed productive coniferous woodland; managed productive broadleaved woodland; unmanaged coniferous woodland; unmanaged broadleaved woodland.
  - Nutrient nitrogen (for AAE): acid grassland; calcareous grassland; dwarf shrub heath; bog; montane; managed productive coniferous woodland; managed productive broadleaved woodland; unmanaged beech woodland; unmanaged oak woodland; unmanaged Scots pine woodland; other unmanaged woodland; dune grassland; saltmarsh.

- Data and methodology references
  - Based on methods agreed under CLRTAP; detailed description in Hall et al. (2015).
  - Summary exceedance statistics published annually (Trends Report) and as UK Biodiversity Indicator B5a.

- Units and interpretation
  - AAE units: keq ha-1 year-1.
  - Acidity AAE can only be expressed as keq ha-1 year-1 (no kg S or N conversion).
  - Nutrient nitrogen AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Exceedance indicates potential for long-term harm; may not reflect current damage or immediate recovery.

- Data files and structure
  - Two files (UK coverage differs by habitat distribution):
    - acidhab_AAE_2015-17.csv (AAE for acidity)
    - nutnhab_AAE_2015-17.csv (AAE for nutrient nitrogen)
  - Common schema features
    - East_m and North_m: centre coordinates (OSGB grid, metres)
    - Unique1km: unique 1x1 km grid square identifier (to link acidity and nitrogen datasets)
    - AAE_keq: the AAE value
    - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland

- Data coverage and linkage
  - Datasets cover differing UK regions due to habitat distribution; the Unique1km code enables cross-linking where data exist for both datasets.

- Quality control and uncertainty
  - Methods conform to national/international standards via CLRTAP; transparency provided in Hall et al. (2015) and related metadata.
  - Note on habitat mapping: mapped areas may differ from other habitat maps; differences can affect total habitat areas used in each dataset.
  - Uncertainty in habitat mapping and critical loads is acknowledged; users should consult the referenced meta-data.

- Use and interpretation guidance
  - Critical load maps reflect long-term steady-state concepts; exceedances indicate potential harm but not immediate damage.
  - Recovery after reducing deposition below critical loads can be slow; chemical and biological recovery timescales may be lengthy, especially for sensitive ecosystems.
  - Freshwater (1752 sites) exceedance statistics are published separately and are not included in these AAE calculations since freshwater data are catchment-based, not 1x1 km grid-based.

- Access and related data
  - Data and metadata available via the EIDC (Environmental Information Data Centre).
  - Related information on the CBED deposition and critical loads available from the EIDC.
  - For further context on methods and trends, refer to the UK Trends Report (Rowe et al., 2019) and the 2015 Methods Report (Hall et al., 2015).

- Summary notes
  - The two AAE datasets enable cross-habitat comparisons at a fine spatial scale and support self-service analysis through a linked grid framework.
  - They provide a standardized, QA-supported basis for assessing potential habitat sensitivity to acidification and eutrophication across the UK.