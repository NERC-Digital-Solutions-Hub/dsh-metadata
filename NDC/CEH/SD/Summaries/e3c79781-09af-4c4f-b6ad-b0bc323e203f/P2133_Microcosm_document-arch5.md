# Plant biomass, soil conditions and stable isotope concentrations in soil, roots and shoots from a microcosm experiment [NERC Soil Biodiversity Programme]

- Overview of the programme
  - NERC Soil Biodiversity Thematic Programme (established 1999) studied soil biodiversity and functional roles in key ecological processes.
  - Site: Sourhope, Scottish Borders; large field experiment with 24 funded projects focusing on soil structure, soil processes (C and N cycles), and lives of soil fauna (micro- to macro-fauna).
  - Objectives included understanding how soil fauna diversity affects microbial properties and plant–microbial carbon and nitrogen competition.

- Study design and experimental setup
  - Microcosms created from Sourhope soil (humic brown, grassland) in PVC pots; defaunated then re-inoculated with microbes.
  - Plant system: Agrostis capillaris grown in a defined soil-sand-Terragreen mix with phosphorus source; arbuscular mycorrhizal (AM) inoculum included.
  - Faunal manipulations: eight individual microarthropod species in monoculture and diverse communities (2, 4, 8 species) plus a predatory mite; species chosen for field prevalence and Identification ease.
  - Biomass and sampling: replicated 10 times per treatment; randomized block design in a glasshouse; plants clipped and biomass measured; moisture maintained to original weight.
  - Isotopic labelling: after 4 months, microcosms received glycine with 15N and 13C, 5 at% enrichment, for 50 hours to study plant–microbe competition for organic N; destructively harvested immediately after labelling.

- Measurements and assessments
  - Plant metrics: shoot and root biomass; AM colonization of roots (stained and quantified).
  - Microbial metrics: microbial biomass C and N via fumigation-extraction; total organic C in extracts.
  - Soil chemistry: extractable ammonia, nitrate, phosphate (and Olsen phosphate); total soil N and C contents.
  - Stable isotopes: 13C/12C in roots and 15N/14N in roots, shoots, and soil fractions; δ values calculated with standard references.
  - Data processing: samples ground and analysed with isotope ratio mass spectrometry; careful QA during analysis.

- Dataset structure and contents
  - Dataset: 1049, Microcosm nitrogen pulse P2133_MICROCOSM_N_PULSE.csv
  - Key variables and data types (examples)
    - POT_NUMBER: pot identifier (Number)
    - GLYCENE_LAB_ELED: glycine labelling status (Text; labelled or control)
    - WATER_TREATMENT: watering condition (Text; watered or drought)
    - BLOCK: experimental block (Number)
    - Presence/absence indicators for fauna (e.g., ONYCH, SCHEL, ISOT, MESA, PLATY, PSEU, HYPO, FOLS) (Number; 1 = present, 0 = absent)
    - PRED: presence of predatory mite (Number)
    - PERCENT_RLC: percent root length colonised by AM fungi (Number)
    - Shoot and root biomass measurements (Number; g)
    - MBC and MBN: microbial biomass C and N (Number; mg/g)
    - AMMONIA, NITRATE, PHOSPHATE: soil inorganic nutrient concentrations (Number; mg/g)
    - ROOT_D15N, ROOT_PERCEN_T_TOTAL_C, ROOT_D13C: root isotope and elemental metrics (Number; various units)
    - SHOOT_PERCENT_TOTAL_N, SHOOT_D15N, SHOOT_D15N: shoot isotope and nitrogen metrics (Number)
    - SOIL_D15N, MGN_UNFUMIGATED_SAMPLE, D15N_UNFUMIGATED_SAMPLE, MGN_FUMIGATED_SAMPLE, D15N_FUMIGATED_SAMPLE: soil and trap isotope metrics (Number)
  - Data provenance and labs
    - Measurements performed at Soil Ecology Laboratory (Lancaster University) and Stable Isotope Facility (Centre for Ecology & Hydrology Merlewood) with detectors (IRMS, EA) and standard references.
  - Data quality and metadata
    - Quality control included numeric range checks, formatting checks, and logical integrity checks.
    - Data are provided with caveat: NERC cannot warrant accuracy or fitness for a particular use; no liability for use of data.

- Context, references, and usage notes
  - Contextual references for interpretation and methodology (e.g., Kaye & Hart 1997; Staddon et al. 1998; Cragg & Bardgett 2001; Vance et al. 1987).
  - Additional useful resources: Sourhope Field Data Handbook (2003), Understanding soil biodiversity (Usher et al. 2006).
  - Data accessibility and metadata
    - Data associated with the NERC Sourhope project; dataset noted as part of the EIDC catalogue; data users are encouraged to consult the cited references and the 2003 Sourhope Field Data Handbook for detailed context.
  - Practical notes for data stewards
    - The dataset comprises multi-modal measurements (biomass, AM colonization, microbial biomass, soil nutrients, and stable isotope data) across many treatments and species, requiring careful metadata to preserve treatment meaning and replication.
    - Metadata should capture site origin, pot-level treatments, species composition, glycine labelling details, and isotopic labelling specifics to ensure reproducibility and correct interpretation across users.