# Impacts of experimental drought and plant trait diversity on floral resources and pollinator visitation

- Overview
  - Field-based study in Wiltshire, UK, using sown plant communities to test how drought and plant functional diversity affect floral resources and pollinator visitation.
  - Experiments conducted at the Winklebury Hill site as part of the Wessex BESS WP2 project; data collected in 2015 and 2016 following a drought simulation.
  - Aimed to link plant functional traits to soil carbon and nitrogen cycling, water use, and drought resistance, and to quantify effects on nectar provisioning and pollinator activity.

- Datasets included (files and core purpose)
  - NERCPropNectar.csv
    - Metadata for nectar production on racemes (standing crop and 24h accumulation).
    - Key fields: Raceme_ID, Plant_Species, Subplot_Type (D, C, R), CountWithNectar, TotalFlowersTested.
    - Notes: Links to other datasets via PlotID, Raceme_ID, SubplotID.
  - NERCNectar.csv
    - Nectar volume and sugar concentration per flower/raceme over 24 h.
    - Key fields: Volume_Absolute (μl), Concentration_Absolute (mg/μl), Concentration_AverageBlanks, Sugar_Absolute (mg), No_Floral_Units, Row, Plot_ID, Raceme_ID, ID.
    - Missing data: Concentration_Absolute missing in 144/703 values (~20%).
  - NERCFloralSurveys.csv
    - Floral surveys within subplots; species-level floral units and survey details.
    - Key fields: Plot_ID, SubplotID, FG (functional group), FG_Diversity, Date_Surveyed, Subplot_Type, SurveyID, Survey_number, IP_PlantSppRich, TotalNumberOfPollVisits, species-level floral unit counts.
    - Notes: One missing survey in subplot 14.C during first pollinator round due to observer error.
  - NERCPollinatorSurveys.csv
    - Pollinator visitation records by plant species and survey.
    - Key fields: Plot_ID, SubplotID, FG, FG_Diversity, Date_Surveyed, Subplot_Type, SurveyID, Survey_Number, Pollinator_Species_Code, Plant_Species, No_Visits.
    - Notes: Minor missing data in round 1 for subplot 14.C; some rows may contain zero visits.

- Data structure and linking
  - Datasets are linked via consistent fields: PlotID, SubplotID, Raceme_ID, SurveyID.
  - PlotID can be used to connect with Fry et al. 2017 and Fry et al. 2018 datasets; consistent with project data lineage.
  - Metadata and data dictionaries provided to aid interpretation and reuse.

- Field data collection and experimental design
  - Site: ex-arable calcareous grassland in Wiltshire (calcareous grassland typical species, CG3a community).
  - Plant communities: four arrangements with contrasting functional traits, plus high-diversity mixes; plots arranged in an 8 m x 8 m grid with 2 m gaps; six blocks for spatial control.
  - Treatments:
    - Drought (D): rain exclusion using shelters for six weeks.
    - Control (C): ambient rainfall.
    - Roofed control (R): transparent roof with openings to control for microclimate effects.
  - Drought timing: six-week period in 2015 and 2016, aligned with a one-in-100-year drought event modeled from local rainfall data.
  - Measurements:
    - Soil moisture content (SMC) measured after drought period.
    - Nectar production and quality assessed on three focal species (Lathyrus pratensis, Onobrychis viciifolia, Prunella vulgaris) using raceme sampling and 24 h nectar collection.
    - Nectar assays included nectar volume via microcapillaries and sugar concentration via refractometry; conversions used to estimate total sugar produced per flower per 24 h.
  - Floral resources and pollinator visitation:
    - Floral surveys in 1 m^2 quadrats within each subplot; identification to species level; recording of floral units.
    - Pollinator observations: 10-minute observation windows per subplot, recording visitor identity (to morphotype/typ). Two survey rounds in July; weather conditions aligned with established protocols.
  - Data quality and ethics:
    - Field protocols followed; data recorded on MS Access; missing data documented in per-file metadata.
    - Ethics approval obtained from CLES Penryn Research Ethics Committee (2016/1429).

- Field data specifics and metadata considerations
  - Field data portal includes explicit definitions for key variables and units (e.g., Raceme_ID as a categorical integer; Volume_Absolute in μl; Concentration_Absolute in mg/μl).
  - Missing data handling notes:
    - Nectar concentration data (Concentration_Absolute) missing for a portion of observations; metadata provides approach for handling blanks (Concentration_AverageBlanks).
  - Data quality notes:
    - Instance-level metadata notes missing data and data collection caveats (observer error, dates, and weather constraints).
  - Provenance:
    - Data are linked to broader ecosystem-function datasets (Fry et al. 2017; Fry et al. 2018) and to foundational pollinator/nectar methods references.

- Winklebury Hill experiment (dataset context within document)
  - A separate but related long-term experiment described in the document.
  - Aims to test functional trait groups on carbon and nutrient cycling using a grid of plant communities established on bare chalk.
  - Functional groups:
    - FG1: deep tap roots, large leaves; potential for soil carbon storage.
    - FG2: shallow tap roots, small rosettes; potential for different nutrient cycling.
    - FG3: shallow, fibrous roots; high nutrient cycling.
  - Design: 7x6 grid of plots (8 m x 8 m plots with replicates); all combinations of FG1-3 represented; drought treatment introduced via rain shelters from 2015 onward.
  - Species lists and group assignments provided; layout descriptions include plot numbering and slope/position designations.
  - Timeline: field establishment 2013–2016; drought shelters implemented in 2015–2016 to simulate extreme drought.
  - Data references:
    - Data associated with Winklebury Hill published in Fry et al. 2017 and 2018 (EIDC DOIs provided).

- Governance, provenance and references
  - Data are designed for interoperability with related datasets (explicit linking keys and cross-references to Fry et al. works).
  - Metadata and data dictionaries supplied to facilitate reuse, including explicit unit conventions and data type guidance.
  - Referenced literature for methods and context (Baldock et al. 2015; Corbet 2003; Pollard & Yates 1993; Prŷs-Jones & Corbet 1991; Rodwell 1992; Yee 2010).

- Practical implications for data stewardship
  - Ensure continued documentation of linking keys to enable integration across the Winklebury Hill and Winklebury Hill-related ecosystem datasets.
  - Maintain and update metadata to reflect any data corrections, missing data handling, or additional soil/nectar measurements.
  - Preserve clear provenance and versioning for the two drought-related datasets and for the Winklebury Hill grid experiment.
  - Consider licensing and data sharing terms consistent with NERC Environmental Information Data Centre practices and project approvals.