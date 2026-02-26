# Study site

- Location and scope: Study conducted in the unlogged primary forest of Danum Valley Conservation Area (DVCA) and adjacent selectively logged forest of Ulu Segama Forest Reserve (USFR) in Sabah, Malaysia (DVCA: 4˚ 58' N, 117˚ 52' E). DVCA covers 438 km2 with lowland dipterocarp forest and lower montane rainforest; USFR region sampled was logged between 1981–1993 with subsequent restoration trials and natural regeneration in different coupes.
- Climate and landscape: DVCA experiences mean annual rainfall ~2305 mm and mean daily temperature ~25.8°C. The adjacent USFR experienced high-intensity logging with varying harvest methods; Reduced Impact Logging (RIL) trial initiated in 1993; silvicultural restoration to restore carbon stocks in some areas.

- Data purpose: Collect seedling trait data to compare primary vs logged forest conditions and assess effects of active restoration versus natural regeneration on seedling traits.

# Study design and sampling

- Seedling plots and timing: Seedling plots (1 m2) established in Sep–Oct 2019 during a mast fruiting event. In DVCA (primary forest) there were 87 plots within a 50 ha forest dynamics plot; in USFR (logged forest) there were 96 plots (52 actively restored; 44 naturally regenerating).

- Seedling sampling: Measured traits on 399 seedlings from 15 species (195 in primary, 204 in logged). Seedlings germinated during the mast event ~6 months prior to sampling (Jan–Feb 2020).

- Plot selection and replication: Seedlings sampled from 75 plots (46 primary, 26 logged). In logged plots, 19 within actively restored areas and 7 in naturally regenerating areas. Where seedlings were unavailable due to high mortality or access issues, additional seedlings were collected up to 20–40 m away from the plot to improve replication and trait estimates.

- Species coverage: Mixed approach to ensure species representing >80% of seedlings on the plots were included; several species sampled in both forest types, with some species unique to either primary or logged forest.

# Traits measured and method

- Traits measured per seedling (14 total): 
  - Leaf mass fraction (LMF) and root mass fraction (RMF)
  - Leaf mass per area (LMA) and leaf thickness
  - Leaf force to punch (LFP)
  - Leaf area to shoot area ratio (LA:SA)
  - Root length to shoot length ratio (RS) and Specific Maximum Root Length (SMRL)
  - Foliar nutrients: leaf nitrogen (N leaf), phosphorus (P leaf), calcium (Ca leaf), potassium (K leaf), magnesium (Mg leaf)
  - Leaf nitrogen to phosphorus ratio (N:P)

- Sampling and processing workflow:
  - Field: Three seedlings per plot (outside the permanent seedling plot) were collected; an additional ten seedlings per seedling plot were collected for foliar analyses.
  - Measurements: Seedlings measured for root and shoot length, shoot diameter; leaf area scanned and calculated with ImageJ; leaf thickness measured on up to three leaves; LFP measured with a force gauge; leaves, shoots, and roots dried and weighed after oven-drying at 50°C.
  - Calculations: Proportions (LMF, RMF), LMA (dry leaf mass / leaf area), LA:SA (leaf area / shoot cross-sectional area), RS (root length / shoot length), SMRL (max root length / dry root mass), N:P (N leaf / P leaf).
  - Foliar chemistry: Leaves dried, ground, digested with H2O2–H2SO4; N and P measured colorimetrically; Ca, K, Mg measured spectroscopically; moisture content used to convert to oven-dry basis.

- Data collection logistics: Seedlings collected in morning, transported to DV Field Centre, processed promptly; leaves combined with additional samples for foliar analysis.

# Data structure and fields

- Dataset name: Danum_Valley_Seedling_Traits.csv

- Key fields and descriptions:
  - Date: Date of seedling sampling
  - Forest: Forest type (primary or logged)
  - Management: Management regime (Natural Regeneration or Active Restoration)
  - Species: Scientific species name
  - Family: Plant family
  - Seedling.Plot: Identifier for the 1 m2 seedling plot
  - Individual: Seedling identifier
  - Biomass: Total dry biomass (g)
  - RL:SL: Root length to shoot length ratio (mm/mm)
  - LMF: Leaf mass fraction (g g-1)
  - RMF: Root mass fraction (g g-1)
  - LMA: Leaf mass per area (g m-2)
  - Leaf.Thickness: Leaf thickness (mm)
  - LFP: Leaf force to punch (N)
  - LA:SA: Leaf area to shoot area (cm2 per mm2)
  - Leaf.N: Leaf nitrogen concentration (mg g-1)
  - Leaf.P: Leaf phosphorus concentration (mg g-1)
  - Leaf.Ca: Leaf calcium concentration (mg g-1)
  - Leaf.K: Leaf potassium concentration (mg g-1)
  - Leaf.Mg: Leaf magnesium concentration (mg g-1)
  - Leaf.N:P: Leaf nitrogen to phosphorus ratio (g g-1)
  - SMRL: Specific Maximum Root Length (mm g-1)

- Units and methodology notes: Each field includes explicit units (e.g., g, mm, mg g-1). The dataset describes measurement methods and the field collection workflow, including instruments used and calculation formulas for derived traits.

# Data quality, limitations, and governance

- Coverage and representativeness: Data encompass 15 species across both primary and logged forests, with a mix of actively restored and naturally regenerating logged plots. Some species appear only in one forest type due to availability of seedlings.

- Sampling limitations:
  - High seedling mortality in logged plots reduced sample availability in some locations.
  - Some plots inaccessible or requiring off-plot sampling (20–40 m away) to maintain monitoring continuity.
  - Species representation varied by forest type, with certain species absent in one forest type due to sampling constraints.

- Processing consistency: Standardized field and lab protocols described (e.g., 50°C oven-drying, ImageJ leaf-area calculations, specific digestion and measurement techniques), enabling comparability across plots and forest types.

- Data governance implications for Data Stewards:
  - Dataset highlights the importance of robust metadata (collection date, forest type, management regime, plot and species details) for discoverability and reuse.
  - Clear documentation of measurement methods, units, and data fields supports data quality assurance, interoperability, and future data integration with other forest trait datasets.
  - The dataset structure supports intra- and inter-species comparisons, as well as assessments of the impacts of forest management and restoration on seedling trait expression.

# Summary of relevance for data governance and reuse

- Provides a well-documented, multifactorial seedling trait dataset comparing primary and logged forests, including active restoration effects.
- Includes comprehensive trait suite (morphological, structural, and foliar chemistry) across plots with explicit sampling design and replication details.
- Clear data dictionary (Danum_Valley_Seedling_Traits.csv) and detailed methods enable reliable data discovery, provenance tracking, quality assurance, and reuse in meta-analyses or comparative studies of forest management effects on seedling physiology.