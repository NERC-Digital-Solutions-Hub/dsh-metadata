# Collection of water samples

- Purpose and scope
  - Autumn fieldwork (September–November) 2018–2020 to identify environmental health measures for monitoring policy and decision-making.
  - International collaboration with the Faroese Geological Survey; sites across England, Scotland, Wales, Northern Ireland, and the Faroe Islands.
  - Focus on water bodies with peat or organic soils; sampling from multiple locations within each catchment (pools, headwaters, streams, inlets, reservoirs, lakes, outlets).

- Sampling design and field practices
  - In situ site variables recorded: pH, conductivity, dissolved oxygen, water temperature; air temperature, pressure, humidity.
  - Grab water samples (50 mL) collected at each site; filtration in the field through a 0.45 µm syringe filter; samples kept cold (in cool bag/box) and stored at 4 °C in the lab.
  - Sampling types include diverse catchment locations and multiple sites per catchment, subject to access constraints.

- Analytical methods
  - Water chemistry analyses on filtered grab samples: dissolved inorganic and organic carbon, absorbance at eight wavelengths, dissolved nutrients, cations, metals, and anions.
  - Organic matter processing: at about one third of sites, concentrate particulate organic matter (POM) and dissolved organic matter (DOM) for CHNO analysis after filtration and evaporation.
  - DOM/POM analysis: elemental composition (total C, N, H, O) with inorganic C removal (acid treatment); derived metrics include Cox, OR, DBE/C, C/N, H/C, O/C, and proportion of organic carbon.
  - Instrumentation: Elementar Vario MICRO cube used for CHNO analyses.

- Data quality assurance (QA) and data handling
  - Lab QA: 10% of samples analysed in replicate; instrument calibration at start and during runs.
  - Data QA: replicate data compared; averages used if replicates agree within 95%; otherwise re-analysis.
  - Derived metrics restricted by physical-property constraints (e.g., CHNO-derived metrics limited by bonding considerations).
  - Data management emphasizes data cleaning, transformation, and clear presentation of findings (reports, charts, dashboards).

- Datasets and data descriptions
  - UK_FI_Water_Chemistry (N = 448)
    - Site metadata: site code; sampling type; sampling locations within catchments.
    - Environmental conditions at sampling: air temperature, humidity, air pressure, bank soil temperature, water temperature.
    - Field/lab water chemistry: pH, electrical conductivity (EC), dissolved oxygen (DO), dissolved organic carbon (DOC), SUVA254, E4/E6, DON, Proportion of organic N, DOP, Proportion of organic P; concentrations of Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li.
  - UK_FI_DOM_CHNO
    - Elemental content in dissolved organic matter (N, C, H, O; organic carbon content after acid treatment).
    - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C; percent organic carbon (prop C).
  - UK_FI_POM_CHNO
    - Elemental content in particulate organic matter (N, C, H, O; organic carbon content).
    - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C; percent organic carbon (prop C).
  - UK_FI_SITES
    - Site metadata and observations; anonymized locations due to access constraints.
    - Land use descriptions (e.g., moorland peat extraction, felled forest, grazing, moorland, plantation, renewable energy sites, restored moorland, shooting, woodland).
    - Vegetation cover categories (based on CEH Land Cover maps) and catchment area (km², calculated from DEM and QGIS).
    - Country identifiers: ENG, SCO, WAL, NIR, FAROE.

- Accessibility, governance, and policy relevance
  - Data governance considerations include anonymization of certain site locations and the need for open data sharing versus access limitations.
  - The dataset structure supports cross-site comparability and policy-relevant monitoring of peat-dominated catchments and DOM/POM dynamics.
  - Highlights typical barriers for monitoring frameworks: data availability, metadata completeness, and data sharing constraints; nevertheless, the comprehensive QA and clear metadata support robust evaluation and reporting to inform environmental health decisions.