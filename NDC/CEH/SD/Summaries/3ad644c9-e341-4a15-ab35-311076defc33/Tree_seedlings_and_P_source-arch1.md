# Study sites and focal species

- Purpose: shade-house experiments to test how soil phosphorus (P) form preferences interact with mycorrhizal type (ECM vs AM) across two forest biomes, aiming to generalise findings beyond a single site.
- Locations:
  - Kabili-Sepilok Forest Reserve, Malaysia (lowland tropical rainforest; ECM-dominated overstorey, AM-dominated understorey)
  - Heishiding Nature Reserve, China (subtropical evergreen broad-leaved forest; ECM overstorey with diverse AM understorey)
- Climate and habitat context:
  - Sepilok: mean annual rainfall ~2975 mm, temperatures ~26.7–27.7 °C
  - Heishiding: mean annual rainfall ~1744 mm, temperatures ~10.6–28.4 °C range
- Focal species:
  - Sepilok (Malaysia): eight ECM-associated species (Shorea multiflora, S. argentifolia, S. parvifolia, Dryobalanops lanceolata, Parashorea tomentella, Vatica sp., Mangifera sp., Adenantera pavonina)
  - Heishiding (China): eight AM- or mixed-AM/ECM-associated species including Castanopsis fissa, Castanopsis faberi, Engelhardtia fenzelii, Schima superba, Cryptocarya concinna, Cinnamomum porrectum, Ormosia glaberrima, Canarium album
- Seedling preparation: experimentally germinated seedlings used to assess soil P form preferences by mycorrhizal type
- Mycorrhizal status: determined for each focal species prior to experiments

## Shade-house experiments

- Timeline and setup:
  - Sepilok, Malaysia: Nov 2015 – May 2016
  - Heishiding, China: Sep 2015 – Apr 2016
- Seed and soil handling:
  - Seeds collected Oct–Dec 2014 (Heishiding) and Aug 2015 (Sepilok); surface-sterilised and germinated
  - Seedlings transplanted after 3 months into pots with sterilised field soil-sand mix (1:1) and 20 g live soil from under adult trees
  - Replacements made for early transplant injuries
- Experimental treatments:
  - Five phosphorus (P) forms: inorganic P (Na3PO4), simple organic P (AMP), complex organic P (phytic acid), a 1/3–1/3–1/3 mixture of the three, and a water control
  - P dosing: 0.24 mg P per g soil (Heishiding) or 0.27 mg P per g soil (Sepilok)
  - Treatments replicated monthly for 6 months
- Experimental design:
  - 12 blocks per site; each block contains an entire treatment unit
  - 8 species × 5 P treatments per site (40 pots per block) → 480 pots per site
  - Randomised treatment arrangement within blocks; blocks separated by 0.5 m
- Growth and harvest:
  - Seedlings watered regularly; height measured monthly
  - 6-month growth period; harvest included shoot and root separation for dry weight
  - Canarium album at Heishiding excluded from final sampling due to low survival

## Laboratory analyses

- Biomass and tissue nutrients:
  - Dry weights: shoot and root measured after drying at 60 °C for 72 h
  - Leaf analysis: N, P, K concentrations via Kjeldahl (N) and ICP-OES after acid digestion
  - Soil available P via Olsen method
- Mycorrhizal assessment:
  - AM fungi: root amputation and staining (trypan blue); percent colonisation determined on 200 root intersections per seedling
  - ECM fungi: counting ECM root tips (live, swollen roots) under stereomicroscope; 30–50 tips per seedling
  - Colonisation expressed as proportion (AM) or proportion of ECM tips
- Data handling:
  - Seedlings with no sampling for root colonisation marked as NA

## Data structure and fields

- Structure: site-level, block-level, treatment-level, and species-level measurements
- Key fields:
  - Site: Sepilok (Malaysia) or Heishiding (China)
  - Block: 1–24, with 1–12 Sepilok and 13–24 Heishiding
  - Ptreatment: 1–5 coded for water, Na3PO4, AMP, phytic acid, Mixture
  - P: combined descriptor (Water, Na3PO4, AMP, Phytic acid, Mixture)
  - Species: coded A–H
  - SpName: binomial species name
  - MycorrhizalType: ECM or AM
  - Height: seedling height at end (cm)
  - TotalBiomass: total dry mass (g) at end
  - TotalBiomassStandard: biomass scaled to species maximum
  - RootBiomass: root dry mass (g) at end
  - RootColonization: proportion of root length (AM) or root tips (ECM) colonised; NA if not sampled

## Table 1: focal species by site

- Sepilok, Malaysia (ECM): Shorea multiflora (SMUL), Shorea argentifolia (SARG), Shorea parvifolia (SPAR), Dryobalanops lanceolata (DLAN), Parashorea tomentella (PTOM), Vatica sp. (VASP), Mangifera sp. (MASP), Adenantera pavonina (APAV)
- Heishiding, China (AM): Castanopsis fissa (CFIS), Castanopsis faberi (CFAB), Engelhardtia fenzelii (EFEN), Schima superba (SSUP), Cryptocarya concinna (CCON), Cinnamomum porrectum (CPAU), Ormosia glaberrima (OGLA), Canarium album (CALB)

- Notes:
  - Canarium album at Heishiding excluded from final sampling due to low survival
  - Data enable comparisons of growth and nutrient status across P forms and mycorrhizal types, with site-specific soil and climate contexts

Key takeaway for analysts
- A robust, block-randomised, multi-factor design links P form availability and mycorrhizal associations to seedling performance and mycorrhizal colonisation, across two distinct forest biomes, with detailed measurements enabling cross-site comparisons and standardised biomass normalization.