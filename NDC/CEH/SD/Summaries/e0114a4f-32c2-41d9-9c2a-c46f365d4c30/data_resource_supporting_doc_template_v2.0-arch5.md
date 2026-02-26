# Emissions of Ammonia (NH 3 ) from Agriculture in South Asia in 2015.

- Purpose and scope
  - Provides annual NH3 emissions from agricultural sources for SAARC countries in 2015.
  - Aims to better represent South Asia with region-specific information (e.g., sub-national fertiliser statistics) beyond general international inventories.

- Geographic and temporal coverage
  - Region: Afghanistan, Bangladesh, Bhutan, India, Maldives, Nepal, Pakistan, Sri Lanka (SAARC).
  - Spatial domain: 0.1° × 0.1° grid, WGS84; domain bounds xmin 60.5°–97.4°, ymin −0.7°–38.5°.
  - Temporal domain: year 2015 (annual emissions).

- Data structure and formats
  - Data format: GeoTIFF (.tif) rasters.
  - Five sub-sectors (each stored as a separate GeoTIFF):
    - NH3_CRB_SouthAsia_2015_gm2_0.1.tif – crop residue burning emissions
    - NH3_CRR_SouthAsia_2015_gm2_0.1.tif – crop residues left in field
    - NH3_GRM_SouthAsia_2015_gm2_0.1.tif – livestock grazing and manure applications
    - NH3_MNM_SouthAsia_2015_gm2_0.1.tif – livestock management (housing, storage, yarding)
    - NH3_SFA_SouthAsia_2015_gm2_0.1.tif – synthetic fertiliser application
  - Units: grams of NH3 flux per square meter per year (g m^-2 yr^-1). No-data values are NA.
  - Outside-SAARC cells are set to NA.

- Sub-sectors and methodological approach
  - Crop sector:
    - CRB: fraction of crops burnt after harvest; burnt fraction limited by crop type and country (India-specific subset).
    - CRR: fraction left in the field after harvest; emissions depend on NH3 EF tied to above-ground biomass and crop type.
  - Livestock sector:
    - GRM and MNM: nitrogen-flow approach with head-by-type excretion and stage-specific losses; emissions allocated to livestock surfaces using country- and type-specific data.
  - Fertiliser sector:
    - SFA: total N fertiliser application by type; spatially distributed to crops; emissions calculated using fertiliser-type EFs and pH-dependent factors; Urea EF updated in this dataset.
  - All sectors integrate country- or region-specific inputs (e.g., fertiliser use, livestock populations, crop areas) with standard emission factors from EDGARv6.1, IPCC guidelines, and EMEP/EEA guidebooks.

- Input data and data sources
  - Crop distributions and crop yields (EarthStat, FAOSTAT; India/Nepal-specific data)
  - Fertiliser use, nitrogen content, and type-specific data (FAOSTAT, country-level sources)
  - Livestock populations and management practices (FAOSTAT; country-specific inputs)
  - Topsoil pH and related soil data (Batjes et al., 2024)
  - Emission factors and methodological references (EDGARv6.1, IPCC 2006/2019 Guidelines, EEA guidebooks 2019/2023)
  - Additional country- and crop-specific studies and datasets cited in the methodology

- Quality control and validation
  - Checks for extreme values and NA locations; totals by sector/sub-sector verified and reconciled with non-spatial calculations.
  - Spatial distribution validated against original (non-spatial) calculations.
  - Cross-comparison with other NH3 agriculture emission estimates.

- Key methodological notes and caveats
  - Grounded in EDGARv6.1 and IPCC guidelines with region-specific data integration.
  - For crop burning (CRB), India-specific crop sets differ from other SAARC countries.
  - Livestock emissions use a nitrogen-flow approach across management stages; spatial distribution relies on country- and species-specific data.
  - Fertiliser emissions depend on total N application, crop-specific rates, and pH-sensitive emission factors; some data are reweighted to FAOSTAT totals.
  - Data produced during 2022–2023 to represent 2015 emissions.

- Governance, metadata, and reuse considerations for Data Stewards
  - Documentation includes naming conventions, spatial resolution, and sub-sector definitions to support interoperability.
  - Provenance is explicit: combines multiple data sources (EarthStat, FAOSTAT, national datasets) with EDGAR/IPCC/EEA methodologies.
  - Users should reference the underlying methodological sources (EDGARv6.1, IPCC Guidelines, EEA Guidebooks) and input data lists when aggregating or comparing.
  - Licensing and access specifics are not provided; advise verifying data use rights and including full metadata when sharing.

- References (key methodological ground)
  - EDGAR v6.1 methodology; IPCC 2006 Guidelines and 2019 Refinement; EMEP/EEA guidebooks 2019 and 2023.
  - Supporting studies and data sources listed in the document (crop, fertiliser, livestock data, and emission factor literature).