# A traits database for the species of macro-moth and micro-moth recorded by the Landscape-scale species monitoring of agri-environment schemes project: 2017-2021

## Overview
- Datasets of moth trait data from LandSpAES, addressing whether mobile taxa respond to local and landscape AES gradients beyond option/farm boundaries.
- Based on a four-year baseline survey (2017–2021) across 54 1km survey squares in England, using a pseudo-experimental design to assess AES impacts at multiple spatial scales.
- Macro- and micromoth traits were compiled from published/online sources to enable trait-based analyses of species’ responses to AES.

## Data collection and design
- Sampling: 6 light traps per survey square, surveyed twice per year; traps active for one night per occasion; nights required to meet minimum weather criteria.
- Specimens were euthanized, identified in the lab, with dissection for some species.
- The protocol is detailed in the LandSpAES project final report appendix (Staley et al. 2022).
- Trait data sources:
  - Macro-moths: Waring & Townsend (2017).
  - Micro-moths: Sterling & Parsons (2012); supplemented with Emmet & Heath (1991) and UKMoths.
- Coverage: not all moth species in England, but includes many common farmland moths due to survey locations and multi-year sampling.

## Dataset contents

### Macromoth_traits_LandSpAES_2023.csv
- Traits include: life cycle ecology and phenology, conservation status and distribution, host plant specificity and characteristics, breeding habitat, morphological traits (e.g., forewing lengths), and other ecological attributes.
- Data structure includes hierarchical categories (e.g.,Habitats and subcategories) and numerous trait columns.
- Key header areas cover residency, status, feeding, photoperiod, overwintering, voltinism, and host plant associations (HAB_XX_XXXX, HPT_XXX, Main_HP_spp_1/2/3, etc.).

### Micromoth_traits_LandSpAES_2023.csv
- Comparable trait set to macromoths, with notes on data sources (Emmet & Heath, Sterling & Parsons, UKMoths) and residency/abundance fields.
- Includes monthly timing columns for life stages (Egg_XXXX, Larva_XXXX, Pupa_XXXX, Adult_XXXX) and overwintering stages, plus host plant and habitat categories.

### Moth traits_LandSpAES project_supporting information_2023.rtf
- Detailed explanations of header meanings, data derivation, and column construction.
- Tables explain the mapping of data columns to trait definitions and the sources for each trait.
- Notes on language around merged headers and monthly representations (e.g., 12 columns for monthly data).

## Data structure and headers
- Tables describing headers provide explicit definitions for each column (scientific name, common name, various codes, residency, status, feeding, photoperiod, pupal habitat, wing measurements, voltinism, overwintering, host plant categories, and breeding habitats).
- Monthly timing is represented with dedicated columns (e.g., Egg_XXXX, Larva_XXXX, Pupa_XXXX, Adult_XXXX) across the year.
- Breeding habitats and host plants are captured at both broad and specific levels (Hab_XX_XXXX; HPT_XXXX; Main_HP_spp_1/2/3).

## Metadata, provenance, and references
- Trait data drawn from established field guides and reviews (e.g., Emmet & Heath, Sterling & Parsons, Waring & Townsend, UKMoths).
- References and project reports include LandSpAES final report (Staley et al. 2022), and related journal articles (Staley et al. 2021; final project URL provided).
- Supporting information includes sources for header definitions and data derivation criteria.

## Data quality, governance, and access
- Metadata gaps were addressed by contacting data originators and compiling from multiple sources; some metadata limitations acknowledged.
- Data governance considerations are explicit in the accompanying information, with guidance on how columns were derived and what they represent.
- Contact for queries and data access: AESspeciesmonitoring@ceh.ac.uk; project website: https://www.ceh.ac.uk/our-science/projects/landspaes

## Relevance for monitoring frameworks
- Enables trait-based interpretation of moth responses to AES gradients, supporting policy evaluations and decision-making.
- Provides a reproducible, transparent data structure with clear provenance, facilitating data sharing and cross-study comparisons.
- Demonstrates a robust approach to integrating field surveys with trait data to inform environmental health monitoring and landscape-scale policy assessment.

## Limitations and scope
- Not exhaustive of all English moth species; focused on farmland-associated and commonly encountered taxa due to the LandSpAES design.
- Micro-moth data coverage may be uneven; some header representations are merged for brevity.

## References
- Agassiz, D.J.L., Beavan, S.D., Heckford, R.J. (2013)
- Davis, A.M. (2012)
- Emmet, M. & Heath, J.H. (1991)
- Manley, C. (2021)
- Staley, J.T. et al. (2021, 2022)
- Sterling, P. & Parsons, M. (2012)
- Waring, P. & Townsend, M. (2017)