# Plant biomass, soil conditions and stable isotope concentrations in soil, roots and shoots from a microcosm experiment [NERC Soil Biodiversity Programme]

## Overview
- NERC Soil Biodiversity Thematic Programme (established 1999) aimed to understand soil biodiversity and the functional roles of soil organisms.
- Large-scale field experiment at Sourhope (Scottish Borders) with 24 funded projects studying soil structure, processes (C and N cycles), and biota across micro- to macro-fauna.
- Focus of the dataset: how soil microarthropod diversity and presence influence soil microbial properties and plant–microbe competition for organic nitrogen, using a dual-labelled glycine tracer to track N partitioning between a grassland plant (Agrostis capillaris) and soil microbial biomass.

## Experimental design and materials
- Microcosms built from Sourhope soil (humic brown, Agrostis-Festuca-Galium grassland) collected from the Sourhope site.
- Soil defaunated by freezing to -80°C, then re-inoculated with microbes; plants grown in a 2:1:1 mix of defaunated soil, coarse silica sand, and Terragreen with bone meal as phosphorus source.
- AM fungal inoculum prepared from Sourhope trap cultures (≈5% Sourhope soil).
- Faunal manipulations included eight distinct microarthropod species in monoculture and diversity treatments with two, four, and eight species (plus a predatory mite). Species included two oribatid mites (Platynothrus peltifer; Scheloribates laevigatus) and multiple collembolans (Isotoma anglicana; Protaphorura armata; Folsomia quadrioculata; Pseudosinella alba; Ceratophysella denticulata; Mesaphorura macrochaeta) and a predatory mite Hypoaspis aculeifer.
- Each treatment replicated 10 times; 190 microcosms total arranged in a randomized block design in a glasshouse with 12h light/12h dark; watering to maintain original weight.
- Treatments standardized for initial biomass across species; higher-diversity pots included a proportionally small predator biomass (5% of total microarthropod biomass in eight-species pots).

## Treatments and sampling
- Plant material: Agrostis capillaris clippings; growth monitored with final harvest after 4 months.
- Isotopic labelling: pulse of glycine, either labelled glycine-213C-15N or unlabelled glycine (control); final destructive harvest after 50 hours to assess short-term plant–microbe competition for organic N.
- Sampling focused on shoot and root biomass, AM colonization, microbial biomass carbon and nitrogen, soil inorganic N and P pools, and isotopic ratios (15N/14N and 13C/12C).
- AM colonization assessed via staining and microscopy (presence/absence of mycorrhizal structures).

## Measurements and analyses
- Plant and root biomass: drying and weighing.
- AM colonization: root staining and microscopic assessment (minimum 100 intersections per sample).
- Isotopic analyses: 13C/12C and 15N/14N ratios measured by isotope ratio mass spectrometry (IRMS) after combustion, with appropriate primary standards; precision typically better than ±0.2‰ for 13C and ±0.3‰ for 15N.
- Microbial biomass: C and N by fumigation-extraction (CHCl3 fumigation 24 h) with subsequent extraction and calculation using standard factors (C: 0.35; N: 0.54).
- Other soil and plant metrics: total organic C, extractable ammonia, nitrate, phosphate; root and shoot nitrogen and carbon contents; 15N in microbial biomass; various isotopic and elemental measurements. Quality control included standard lab procedures and cross-lab verification where applicable.

## Data structure
- Data asset: Dataset 1049: Microcosm nitrogen pulse P2133_MICROCOSM_N_PULSE.csv
- Key columns and structure:
  - POT_NUMBER: pot identifier.
  - GLYCENE_LAB_ELED: whether glycine was labelled or unlabelled (glycine treatment).
  - WATER_TREATMENT: watered or drought conditions.
  - BLOCK: experimental block (1-5).
  - Presence/absence indicators for Faunal taxa: ONYCH (Protaphorura armata); SCHEL (Scheloribates laevigatus); ISOT (Isotoma anglicana); MESA (Mesaphorura macrochaeta); PLATY (Platynothrus peltifer); PSEU (Pseudosinella alba); HYPO (Hypoaspis aculeifer); FOLS (Folsomia quadrioculata); PRED (predatory mite presence).
  - PERCENT_RLC: mycorrhizal root length colonization percentage.
  - Biomass and isotopic measures: SHOOT_ and ROOT_ biomass (g or %), MBC (microbial biomass carbon), MBN (microbial biomass nitrogen), AMMONIA, NITRATE, PHOSPHATE, ROOT_D15N, ROOT_PERCEN T_TOTAL_C, ROOT_D13C, SHOOT_PERCENT_TOTAL_N, SHOOT_D15N, SOIL_D15N, etc.
  - Various timepoint-specific shoot biomass fields (e.g., CUT1_SHOOT_1, CUT2_SHOOT_1, CUT3_SHOOT_0) corresponding to harvest times.
  - References to laboratories and methods for each measurement (e.g., Soil Ecology Laboratory – Lancaster University; Stable Isotope Facility – CEH Merlewood).
- Metadata notes: dataset includes unit descriptions, data types, analysis methods, and data provenance for each field.

## Quality control and usage notes
- Quality assurance steps include numeric range checks, data formatting checks, and logical integrity checks.
- The dataset is provided with general QA but no guarantee of absolute accuracy; the data provider (NERC) disclaims liability for fitness for a particular use.
- Data and references are provided to support reproducibility and further research, including the Sourhope Field Data Handbook and related literature on soil biodiversity and plant–microbe competition.

## References and further reading
- Core methodological and background references, including:
  - Scott et al. 2003; Sourhope Field Data Handbook
  - Usher et al. 2006; Understanding biological diversity in soil
  - Key methodological sources for isotopic analyses, microbial biomass measurements, and AM fungal assessments
- Data and workflow references for interpreting and reusing the dataset.