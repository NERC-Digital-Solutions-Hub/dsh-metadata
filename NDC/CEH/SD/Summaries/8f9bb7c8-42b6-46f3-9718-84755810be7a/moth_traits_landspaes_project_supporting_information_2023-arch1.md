# A traits database for the species of macro-moth and micro-moth recorded by the Landscape-scale species monitoring of agri-environment schemes project: 2017-2021

## Overview
- Provides trait data for macro- and micro-moth species recorded in LandSpAES ( Landscape-scale Species Monitoring of Agri-environment Schemes).
- Designed to assess whether key mobile taxa respond to local and landscape AES gradients beyond farm/agreement boundaries, across multiple taxa.
- Based on a novel pseudo-experimental baseline survey conducted 2017–2021 over 54 survey squares in six English National Character Areas.
- Focuses on large spatial extents across arable, grassland, and upland agricultural systems; not a complete census of all moths.

## Data collection and scope
- Moths sampled with 6 light traps per 1 km survey square; two sampling visits per year, one night per visit, under minimum weather conditions.
- Specimens euthanized, identified in the lab; micro-moths and macro-moths included, with many micro-moths typically underrepresented in farmland studies.
- Trait data compiled for 925 moth species observed on LandSpAES squares (2017–2021) in England.
- Data sources prioritized are more recent and authoritative; macro-moth traits primarily from Waring & Townsend (2017); micro-moth traits from Sterling & Parsons (2012), with supplementary sources (Emmet & Heath 1991; UKMoths) to fill gaps.

## Data contents and structure
- Dataset comprises three files:
  - Macromoth_traits_LandSpAES_2023.csv: macro-moth trait data (410 rows, 85 KB).
  - Micromoth_traits_LandSpAES_2023.csv: micro-moth trait data (605 rows, 180 KB).
  - Moth traits_LandSpAES project_supporting information_2023.rtf: metadata on column derivation, data sources, and references.
- Additional documentation clarifies headers and the data derivation process; some trait categories are merged to save space (e.g., monthly columns represented in single rows in the header but as multiple columns in the data).
- Data cover life cycle ecology, phenology, conservation status and distribution, host plant specificity and characteristics, breeding habitat, and morphological characteristics.

## Trait variables and data design
- Life cycle and phenology: includes voltinism (univoltine/multivoltine/north/south, and variations), flight period start month, and overwintering stage (egg, larva, pupa, adult).
- Host plants: host plant type categories (HPT_XXX) and host plant parts (HPP_XXX), with up to three main host plants (Main_HP_spp_1..3) per species; diet breadth categorized as monophagous, oligophagous, or polyphagous.
- Breeding habitat: broad to specific breeding habitats (Hab_XX_XXXX) across categories like woodland, heathland, grassland, suburban, hedgerows, brownfield, wetlands, coastal, montane, synanthropic, and arable.
- Morphology: forewing length metrics for males and females (min/max and average).
- Distribution and status: England resident/immigrant indicators; conservation status references (W&T 2017 for macro; Davis 2012 for micro) and relative abundance (S&Ps 2012 for micro).
- Monthly stage data: for egg, larva, pupa, and adult stages, columns map to the 12 calendar months (e.g., Egg_XXXX, Larva_XXXX, Pupa_XXXX, Adult_XXXX).
- Data quality notes: for micro-moths, notes field captures supplementary information (e.g., first GB record, continuous-brooded status, data gaps).

## Data provenance and references
- Macro-moths: data from Waring & Townsend (2017); supplementary details from Emmet & Heath (1991) and UKMoths; LandSpAES-specific methods described in Staley et al. (2022) and final project report Staley et al. (2021, 2022).
- Micro-moths: data from Sterling & Parsons (2012); additional sources include Emmet & Heath (1991) and UKMoths; residency/immigration status and monthly life-stage data drawn from the cited literature.
- Key references include Agassiz et al. (2013), Davis (2012), Emmet & Heath (1991), Sterling & Parsons (2012), Waring & Townsend (2017), Staley et al. (2021, 2022).

## Access, use, and contact
- Project-specific contact for trait data or LandSpAES queries: AESspeciesmonitoring@ceh.ac.uk.
- Project site: https://www.ceh.ac.uk/our-science/projects/landspaes
- Final project report: https://randd.defra.gov.uk/ProjectDetails?ProjectId=20012
- Note: The dataset does not cover all moth species in England; it focuses on many common farmland species observed within LandSpAES survey zones.

## Practical considerations for analysts
- Spatial and taxonomic scope limited to LandSpAES survey squares; suitable for analyses linking traits to AES gradients but with recognition of coverage limits.
- Data compilation combines multiple literature sources; cross-checking and metadata are essential when integrating with other datasets.
- Monthly life-stage data enable analyses of seasonal dynamics and phenology in relation to AES gradients and habitat types.
- Breeding habitat and host-plant information allow testing of habitat- and diet-based vulnerability or adaptability across landscapes.
- Data provenance and header documentation are provided to support reproducibility and accurate interpretation of columns and merged fields.