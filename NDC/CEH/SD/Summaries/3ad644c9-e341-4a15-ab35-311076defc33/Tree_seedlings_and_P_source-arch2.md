# Study sites and focal species

- Purpose and scope
  - Shade-house experiments to test how generalisable the findings are across different forest biomes.
  - Focus on ectomycorrhizal (ECM)–dominated overstorey and arbuscular mycorrhizal (AM)–dominated understorey communities.
  - Eight common tree species per site with determined mycorrhizal status; seeds collected for experimentation.

- Study locations and climatic context
  - Sepilok, Malaysia (Kabili-Sepilok Forest Reserve)
    - Lowland tropical rainforest remnant; coordinates 5°49'N, 117°57'E.
    - Climate: mean annual rainfall ~2975 mm; temperatures ~26.7–27.7 °C.
    - Forest types include lowland dipterocarp, heath, and mangrove ecosystems.
  - Heishiding Nature Reserve, China
    - Subtropical evergreen broad-leaved forest; coordinates 111°53'E, 23°27'N, elevation 150–927 m.
    - Climate: mean annual temperature ~19.6 °C; ~1744 mm annual rainfall with a pronounced dry season Oct–Mar.
  - Seeds collected Oct–Dec 2014 (Heishiding) and Aug 2015 (Sepilok); surface-sterilised for germination.

- Experimental design
  - Seedlings germinated in controlled shade-house conditions, then transplanted into pots.
  - Pots: 8 cm diameter x 10 cm height; sterilised field soil mixed 1:1 with sterilised sand.
  - Live soil inoculum: 20 g per pot, collected 0–30 cm depth beneath adult focal trees to convey associations with adult-tree microbiomes.
  - Experimental units: 12 blocks per site; each block contains a full treatment unit (8 species × 5 P treatments; total 40 pots per block; 480 pots per site).
  - Randomization: treatments within blocks; blocks separated by ~0.5 m.
  - Harvest: after 6 months of growth; Canarium album excluded at Heishiding due to low survival.

- Focal species and mycorrhizal status
  - Eight focal species per site listed in Table 1; species codes (A–H) correspond to binomial names.
  - Mycorrhizal type determined a priori as ECM or AM (ECM at Sepilok; AM represented among some species at Sepilok; ECM at Heishiding; AM present in Heishiding species list).

- Phosphorus (P) treatments and application
  - Five P treatments to evaluate inorganic and organic P preferences and their interaction with mycorrhizal types:
    - Water (control)
    - Na3PO4 (inorganic P)
    - AMP (simple organic P)
    - Phytic acid (complex organic P)
    - Mixture (1/3 Na3PO4 + 1/3 AMP + 1/3 phytic acid)
  - Treatment dosing: monthly for 6 months, with site-specific background soil P concentrations.
    - Heishiding: 0.24 mg P per g soil
    - Sepilok: 0.27 mg P per g soil

- Seedling handling and data collection
  - Seedlings transplanted one week after survival check; dead/poorly growing individuals replaced.
  - Growth monitoring: monthly height measurements; final harvest for biomass.
  - Biomass and tissue analyses:
    - Shoot and root dry weights (60 °C, 72 h).
    - Leaf N, P, K concentrations (N via Kjeldahl; P and K via ICP-OES after acid digestion).
    - Soil available P measured via Olsen method.
  - Mycorrhizal colonisation assessment:
    - AM: roots stained with trypan blue; 200 root intersections checked per seedling; percent AM colonisation calculated.
    - ECM: act by counting ECM root tips (30–50 tips per seedling); colonised tips expressed as a percentage.
  - Extractions and sample processing were conducted on samples from the first 6 blocks for deeper root/soil analyses.

- Data structure and fields
  - Dataset fields (A–L) describe the structured data collected:
    - A: Site (Sepilok or Heishiding)
    - B: Block (1–24; 1–12 Sepilok, 13–24 Heishiding)
    - C: Ptreatment (1–5; coded for five P treatments)
    - D: P (descriptive P treatment names corresponding to C)
    - E: Species (codes A–H)
    - F: SpName (binomial species names)
    - G: MycorrhizalType (ECM or AM)
    - H: Height (seedling height in cm)
    - I: TotalBiomass (total dry biomass in g)
    - J: TotalBiomassStandard (biomass scaled to species maximum)
    - K: RootBiomass (root dry biomass in g)
    - L: RootColonization (proportion of colonised roots or tips; NA where not sampled)

- Notes on data and interpretation
  - The design enables cross-site comparisons of mycorrhizal associations, P forms, and seedling performance.
  - Seedling performance was assessed under controlled soil inoculation to mimic field conditions around adult trees.
  - One species (Canarium album at Heishiding) was removed due to low survival, affecting the Heishiding dataset for that species.