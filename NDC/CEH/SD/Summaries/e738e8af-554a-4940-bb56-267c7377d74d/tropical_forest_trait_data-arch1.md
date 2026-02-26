# Study site

- Location and environment
  - Conducted in Danum Valley Conservation Area (DVCA) primary forest and adjacent Ulu Segama Forest Reserve (USFR) logged forest, Sabah, Malaysia (4˚ 58' N, 117˚ 52' E).
  - DVCA: 438 km2 of lowland dipterocarp forest and lower montane rainforest; climate ~2305 mm annual rainfall; mean daily temperature ~25.8°C.
  - USFR region adjacent to DVCA was selectively logged 1981–1993; logging intensity historically high with varying coupe-level practices.

- Logging history and restoration
  - Logging in USFR occurred in annual coupes (≈27 km2 each); most trees >60 cm DBH removed.
  - 1993 Reduced Impact Logging (RIL) trial established to minimize damage; silvicultural interventions included in a subset of coupes aiming to restore forest carbon stocks (Innoprise-FACE Foundation Rainforest Rehabilitation Project).

- Seedling plots and sampling design
  - Seedling plots (1 m2) established during mast fruiting in Sep–Oct 2019 in both forest types.
  - Primary forest: 87 seedlings within ForestGEO Danum Valley 50 ha plot.
  - Logged forest: 96 seedlings within INDFORSUS plots (52 actively restored; 44 naturally regenerating).
  - Overall: 75 plots sampled (46 primary; 26 logged). Logged plots included 19 actively restored and 7 natural regeneration plots.

- Species and sampling coverage
  - 399 seedlings from 15 species measured (January–February 2020): 195 in primary forest; 204 in logged forest.
  - Species selection aimed to represent >80% of seedlings on plots and allow intraspecific comparisons between forest types.
  - Several species sampled across forest types; some species sampled only in primary or only in logged forests due to distribution or sampling constraints.
  - Seedlings mostly originate from canopy or emergent trees; exceptions include smaller species such as Buchanania sessifolia and certain lianas.

- Seedling sampling details and replication
  - For each plot, three seedlings were collected just outside the permanent seedling plot; an additional ten seedlings per plot were combined with the three for foliar analyses.
  - Where seedlings were unavailable due to mortality or access, samples were taken ~20–40 m from the plot to improve mean trait estimates.
  - Mortality and access limitations reduced sampling in some logged plots.

- Traits measured (14) and data collection
  - Morphological and chemical traits per seedling:
    - Leaf Mass Fraction (LMF), Root Mass Fraction (RMF)
    - Leaf Mass per Area (LMA), Leaf Thickness
    - Leaf Force to Punch (LFP)
    - Leaf Area:Shoot Area (LA:SA)
    - Root Length:Shoot Length (RS)
    - Specific Maximum Root Length (SMRL)
    - Foliar nutrients: Leaf Nitrogen (N leaf), Phosphorus (P leaf), Calcium (Ca leaf), Magnesium (Mg leaf), Potassium (K leaf)
    - Leaf Nitrogen to Phosphorus ratio (N:P)
  - Calculation details:
    - Biomass: total seedling dry mass after oven-drying (50°C, 48 h)
    - LMF/RMF: dry leaf/root mass / total dry mass
    - LMA: dry leaf mass / leaf area (from scanned leaves analyzed with ImageJ LeafArea)
    - LA:SA: leaf area / shoot cross-sectional area (derived from shoot diameter)
    - RS: root length / shoot length
    - SMRL: max root length / dry root mass
    - N:P: N leaf / P leaf
  - Foliar nutrient analyses
    - Leaves ground and digested (H2O2–H2SO4); N and P via colorimetric analysis; Ca, K, Mg via spectrophotometry; moisture correction for oven-dry basis.

- Data structure and fields
  - Data file: Danum_Valley_Seedling_Traits.csv
  - Key fields (with examples)
    - Date (seedling sampling date)
    - Forest (Primary or Logged)
    - Management (Natural Regeneration or Active Restoration)
    - Species, Family
    - Seedling.Plot, Individual
    - Biomass (g)
    - RL:SL (root length : shoot length; mm:mm⁻¹)
    - LMF, RMF (g/g)
    - LMA (g/m²)
    - Leaf.Thickness (mm)
    - LFP (N)
    - LA:SA (cm² per mm²)
    - Leaf.N, Leaf.P, Leaf.Ca, Leaf.K, Leaf.Mg (mg/g)
    - Leaf.N:P (g/g)
    - SMRL (mm/g)
  - Descriptions and units for each field are provided in the CSV documentation, with measurement methods summarized above.

- Overall aims and considerations
  - Compare seedling functional traits between primary and logged forests and between natural regeneration and active restoration.
  - Address responses of seedling traits to disturbance and restoration interventions, contributing to understanding of forest recovery and carbon dynamics.
  - Note challenges: higher mortality in logged plots affecting sample size; some plots inaccessible or not fully sampled; data capture relies on combining multi-plot replication to estimate species-mean trait values.