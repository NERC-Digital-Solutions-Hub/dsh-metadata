# Study sites and focal species

- Purpose and scope
  - Shade-house experiments conducted to assess how forest tree species with different mycorrhizal associations respond to varying phosphorus (P) forms, to evaluate generalisability across forest biomes (Malaysia and China).
  - Focus on interactions between mycorrhizal type (ECM vs AM) and P forms (inorganic, simple organic, complex organic, mixture, and water control) and their effects on seedling growth and root symbioses.

- Study sites and ecological context
  - Sepilok Forest Reserve, Sabah, Malaysia
    - Lowland tropical rainforest remnants; overstorey ECM-dominated, understorey AM-dominated.
    - Climate: mean annual rainfall ~2975 mm; mean annual temp ~26.7–27.7 °C.
  - Heishiding Nature Reserve, Guangdong, China
    - Subtropical evergreen broad-leaved forest; ECM-dominated overstorey, AM-associated understorey.
    - Climate: mean annual rainfall ~1744 mm; mean annual temp ~19.6 °C.

- Focal species and experimental setup
  - Eight common tree species per site selected for availability of seeds/ fruits; mycorrhizal status determined a priori.
  - Seedlings germinated and grown in shade-house conditions, transplanted into pots with sterilised soil and live soil inoculum from beneath adult conspecifics.
  - Treatments
    - Five phosphorus forms: water (control), inorganic phosphate (Na3PO4), simple organic P (AMP), complex organic P (phytic acid), and a mixture (1/3 each).
    - P supplied monthly for 6 months, with site-specific background P levels.
  - Experimental design
    - Each site used 12 blocks; each block contained all 40 pots (8 species × 5 P treatments).
    - Total pots per site: 480 (replicates across blocks and treatments).
    - Seedlings monitored and harvested after 6 months.

- Measurements and laboratory analyses
  - Growth and biomass
    - Seedling height (cm) and shoot/root dry biomass (g) at harvest.
  - Tissue and soil chemistry
    - Leaf N, P, K concentrations (N by Kjeldahl; P and K by ICP-OES after acid digestion).
    - Soil available P measured by Olsen method.
  - Mycorrhizal colonisation
    - AM: percent root length colonised via stained roots and gridline intersection method.
    - ECM: percent of ECM-colonised root tips counted under microscope.
  - Data handling
    - Specific sampling: 6 blocks sampled for root/soil analyses; one seedling per pot; 200 root intersections for AM; 30–50 ECM tips per seedling.
  - Notable outcome
    - One species (Canarium album at Heishiding) excluded from subsequent sampling due to low survival.

- Data structure and fields
  - Dataset structure includes the following fields:
    - Site: Sepilok, Malaysia or Heishiding, China.
    - Block: 1–24 (12 blocks per site; distinct blocks per site).
    - Ptreatment: 1–5 code for the five P treatments.
    - P: Descriptive label for P treatment (Water, Na3PO4, AMP, Phytic acid, Mixture).
    - Species: Codes A–H.
    - SpName: Binomial species name.
    - MycorrhizalType: ECM or AM.
    - Height: Seedling height at end (cm).
    - TotalBiomass: Total dry mass at end (g).
    - TotalBiomassStandard: Biomass scaled to species maximum for comparability.
    - RootBiomass: Root dry mass (g).
    - RootColonization: Proportion of colonised roots or root tips (AM vs ECM) per seedling; NA if not sampled.

- Data interpretation and cross-site comparability
  - The parallel design across two biomes allows assessment of general patterns in how mycorrhizal associations and P availability shape seedling performance.
  - Detailed metadata and a clearly defined data schema (including site, block, treatment, species, mycorrhizal type) support data integration, quality assurance, and potential policy-relevant synthesis.

- Relevance to monitoring and governance
  - Demonstrates structured, replicable data collection and robust documentation of treatments, species, and responses, aligning with monitoring framework needs for transparency and reproducibility.
  - Highlights the importance of metadata completeness (treatment codes, species mapping, mycorrhizal status) to enable data verification and reuse.
  - Indicates practical data management considerations for monitoring frameworks: standardised formats, cross-site comparability, and openness of underlying data and methods, while acknowledging potential barriers (e.g., data availability, alignment of metadata, and data sharing constraints).