# Plant biomass, soil conditions and stable isotope concentrations in soil, roots and shoots from a microcosm experiment [NERC Soil Biodiversity Programme] Cole, L., Staddon, P.L., Sleep, D. and Bardgett, R.D.

## Overview and aims
- Describes a microcosm experiment from the NERC Soil Biodiversity Programme focused on integrating soil biota, plant biomass, and soil chemical properties.
- Primary objective: understand how soil microarthropod diversity and composition influence microbial properties and plant–microbe competition for organic nitrogen.
- Datasets cover aboveground biomass, soil nutrients, microbial biomass, and stable isotope tracers to trace nutrient flows.

## Experimental design and materials
- Site: Sourhope, Scottish Borders, UK; soil type: humic brown soil from Sourhope series.
- Microcosms: PVC pots with defaunated soil inoculated with microbes; Agrostis capillaris used as the plant model.
- Mycorrhizal inoculum: rough mix from Sourhope trap cultures included in the growth medium.
- Faunal treatments: eight microarthropod species tested in monoculture and in multi-species assemblages (two, four, and eight species). Included a predatory mite (Hypoaspis aculeifer) in higher-diversity treatments.
- Inoculum and setup: field-collected fauna (mostly from Sourhope) introduced; organisms counted to achieve equal initial biomass across treatments; pots arranged in a randomized block design (190 microcosms total); water maintained to original weight; barriers to prevent inter-pot movement.
- Plant management: Agrostis capillaris transplanted into each microcosm; plants cut and biomass harvested for growth and root-association analyses.

## Data collected and measurements
- Plant and root biomass: shoot and root dry weights at multiple harvest points; assessment of root length colonized by arbuscular mycorrhizal (AM) fungi.
- Mycorrhizal colonization: stained roots assessed under microscope; presence/absence of mycorrhizal structures recorded.
- Microbial measurements: microbial biomass carbon (MBC) and microbial biomass nitrogen (MBN) via fumigation-extraction; total soil organic carbon and nitrogen.
- Nutrients: soil extractable ammonia, nitrate, and phosphate measured.
- Isotopes and elemental composition: stable isotope ratios (15N/14N in soil, roots, shoots; 13C/12C in roots) and total carbon and nitrogen contents determined by IRMS and elemental analysis; glycine-213C-15N pulse labeling used to trace N flow from glycine into plant and microbial pools.
- Sampling and processing: destructive harvest after 4 months of growth following glycine pulse; multiple laboratory analyses conducted at dedicated facilities (e.g., Stable Isotope Facility, Lancaster University; Merlewood stable isotope facility).
- Quality controls: standard QA steps including range checks, data formatting, and logical integrity checks.

## Data structure and file details
- Dataset: 1049 – Microcosm nitrogen pulse P2133_MICROCOSM_N_PULSE.csv.
- Structure: CSV with a wide range of variables representing treatments, plant and soil measurements, and isotopic data.
- Key column types (illustrative): 
  - Pot metadata: POT_NUMBER, BLOCK, WATER_TREATMENT, GLYCENE_LABELLED (labelled vs. control glycine).
  - Fauna presence/absence indicators: ONYCH, SCHEL, ISOT, MESA, PLATY, PSEU, HYPO, FOLS, PRED.
  - Plant and soil measurements: PERCENT_RLC (root length colonised), SHOOT_ and ROOT biomass, MBC, MBN, AMMONIA, NITRATE, PHOSPHATE, ROOT_D15N, ROOT_D13C, ROOT_PERCENT_TOTAL_C, SHOOT_PERCENT_TOTAL_N, SHOOT_D15N, SHOOT_D13C, SOIL_D15N, etc.
  - Lab and provenance notes: analysis lab references, equipment, and units.
- Documentation indicates the dataset is linked to published handbooks and project reports (e.g., SOURHOPE FIELD DATA HANDBOOK 2003) and provides references for methods and related datasets.

## Data quality, provenance and usage notes
- Provenance: data originate from a controlled microcosm experiment with explicit treatment structures and detailed methodological documentation.
- Quality assurance: numeric range checks, formatting checks, and logical integrity checks performed; however, the NERC programme disclaims warranty of data accuracy or fitness for a specific use.
- Usage considerations:
  - Suitable for analyses of how soil faunal diversity and composition affect microbial abundance and plant–microbe nutrient competition.
  - Useful for examining relationships among diversity, biomass production, nutrient pools, and stable isotope tracers in a controlled setting.
  - Users should account for the experimental design (randomized block, fixed biomass equivalence across treatments, presence/absence codings) when modelling effects.
- References and supporting materials: project-specific methods and related data handbooks are provided for context and reproducibility.

## References and related resources
- Cole, L., Staddon, P. L., Sleep, D., & Bardgett, R. D. (2004). Soil animals influence microbial abundance, but not plant-microbial competition for soil organic nitrogen. Functional Ecology, 18(5), 631-640.
- Cragg, R.G. & Bardgett, R.D. (2001). How changes in soil faunal diversity and composition within a trophic group influence decomposition processes. Soil Biology & Biochemistry, 33, 2073-2081.
- Hopkin, S. (2000). A Key to the Springtails of Britain and Ireland.
- Kaye, J.P. & Hart, S.C. (1997). Competition for nitrogen between plants and soil microorganisms. Trends in Ecology and Evolution, 12, 139-143.
- Krantz, G.W. (1978). A Manual of Acarology.
- McGonigle, T.P. et al. (1990). A method to measure colonization of roots by vesicular-arbuscular mycorrhizal fungi. New Phytologist, 115, 495-501.
- Vance, E.D. et al. (1987). An extraction method for measuring soil microbial biomass C. Soil Biology & Biochemistry, 19, 703-707.
- Additional resources: Sourhope Field Data Handbook (2003); Understanding biological diversity in soil (Usher et al., 2006).