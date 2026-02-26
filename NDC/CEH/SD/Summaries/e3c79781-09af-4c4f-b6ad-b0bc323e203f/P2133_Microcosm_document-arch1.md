# Plant biomass, soil conditions and stable isotope concentrations in soil, roots and shoots from a microcosm experiment [NERC Soil Biodiversity Programme]

- Overview
  - Large-scale NERC project (Sourhope, Scotland) focused on soil biodiversity, soil biota functions, and their influence on plant–microbe competition for organic nitrogen using a controlled microcosm experiment.
  - Aimed to understand how microarthropod diversity and species composition affect microbial properties, plant biomass, and nutrient competition.

- Study context and aims
  - Site: Sourhope, Cheviot Hills, SE Scotland; soil type: humic brown (Sourhope series).
  - Plant system: Agrostis capillaris in a grassland mix; focus on interactions among soil fauna, microbial communities, and plant–microbe N partitioning.
  - Experimental objective: test effects of individual microarthropod species and diversity on soil microbial properties and short-term plant–microbe competition for organic nitrogen using a labeled glycine pulse.

- Experimental design
  - Microcosms: PVC pots (7 cm diameter, 6 cm depth) with defaunated soil inoculated with microbes; moisture kept at ~60% w/w; plants transplanted after establishing microflora.
  - Location of measurements: 190 microcosms arranged in randomized blocks within a glasshouse.
  - Faunal treatments: eight microarthropod species tested in monocultures and in diversity pools (two, four, eight species) plus a predatory mite; species chosen for field relevance and identifiability.
  - Biomass standardization: initial biomass per pot adjusted so each species contributed roughly equal biomass; higher-diversity pots included a predatory mite at 5% of total biomass.

- Isotopic labeling and sampling
  - Glycine pulse labeling after 4 months to trace glycine-derived 15N and 13C into plant and microbial biomass; label: glycine-213C-15N enriched to 5 at% 15N.
  - Labeling duration: 50 hours, followed by destructive harvest to separate plant, soil, and microbial components.

- Measurements and data collected
  - Plant metrics: shoot and root biomass; percent root length colonized by arbuscular mycorrhizal (AM) fungi.
  - Soil and microbial metrics: total soil nitrogen; extractable ammonia, nitrate, phosphate; microbial biomass carbon (MBC) and nitrogen (MBN) via fumigation–extraction; total organic carbon in extracts.
  - Isotopic analysis: 15N/14N in roots, shoots, soil; 13C/12C in roots; reported as δ values; instrumentation includes elemental analyzer and isotope ratio mass spectrometry; precision better than ±0.2‰ for 13C and ±0.3‰ for 15N.
  - AM assessment: staining and microscopic evaluation of mycorrhizal structures; presence/absence noted.
  - Data produced includes numerous derived and raw fields (e.g., MBC, MBN, ammonia, nitrate, phosphate, various isotope ratios, shoot/root biomass, AM colonization metrics).

- Data structure and access
  - Primary dataset: Dataset 1049 – Microcosm nitrogen pulse P2133_MICROCOSM_N_PULSE.csv.
  - Key fields (examples): POT_NUMBER (pot ID); GLYCENE_LABELED (labeling status: labelled vs control); WATER_TREATMENT (watered vs drought); BLOCK (experimental block); presence/absence indicators for each fauna species (e.g., ONYCH for Protaphorura armata, SCHEL for Scheloribates laevigatus, ISOT for Isotoma anglicana, MESA for Mesaphorura macrochaeta, PSEU for Pseudosinella alba, HYPO for Hypoaspis aculeifer); AM root colonization (PERCENT_RLC); shoot and root biomass (g); MBC, MBN; ammonium, nitrate, phosphate; various isotopic measures (ROOT_D15N, ROOT_D13C, SHOOT_D15N, SHOOT_PERCEN T_TOTAL_N, SOIL_D15N, etc.); and other related measurements tied to extraction, fumigation status, and lab references.
  - Documentation notes: methods and variable definitions align with the Sourhope Field Data Handbook 2003 and related methodological references; data quality checks described.

- Quality control and limitations
  - QA steps include numeric range checks, formatting checks, and logical integrity checks.
  - Caution: data provided without warranty of accuracy; not liable for fitness for a particular use; standard data-use disclaimer from NERC.

- References and supplementary information
  - Key related publications and method papers listed (e.g., functional ecology of soil fauna, carbon and nitrogen cycling, mycorrhizal assessment methods, and isotopic tracing).
  - Additional supporting information and data handbooks available via linked sources (Sourhope Field Data Handbook 2003; UK Soil Biodiversity Programme literature).

- Practical notes for analysts
  - Rich dataset for analyzing correlations between soil fauna diversity and microbial biomass, and for modeling short-term plant–microbe competition for organic nitrogen under different faunal assemblies.
  - Isotopic data enable partitioning of nitrogen and carbon flows among plant and microbial pools, under varied faunal treatments and AM associations.
  - Careful handling of complex, multi-variable fields is required; ensure alignment of labeling status, treatment codes, and sampling blocks when merging with other datasets or performing statistical modeling.