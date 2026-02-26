# Farm Scale Evaluations (FSE) Dataset Descriptions

- Purpose and aim
  - Established to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife due to management practices.
  - Data supports scrutiny and evaluation of policy and informs future decisions, aligned with environmental health monitoring objectives.

- Crops and study scope
  - Data collected for four crops: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
  - Experiments cover multiple biological levels from soil seedbank to in-field invertebrates and field-edge vegetation.

- Data collection domains and measures
  - Seedbank
    - Seedbank: germinating species from soil samples taken before planting.
    - Follow-up 1: soil sample one year after initial seedbank sample.
    - Follow-up 2: final soil sample two years after initial sampling.
  - Vegetation in the crop
    - First-seedling: initial vegetation survey before herbicide application.
    - Mezzanine (Beet and Winter Oilseed Rape): additional pre- and post-herbicide comparisons.
    - Post-herbicide: vegetation surveys after herbicide application on both conventional and GM sides.
    - Final Counts: vegetation survey coinciding with biomass sampling.
    - Biomass: weed biomass measured in the month before harvest.
    - Seed Rain: seeds collected across the growing season.
    - Follow-up 1 and Follow-up 2: vegetation surveys one and two years after the trial crop.
  - Field edge vegetation
    - Margin Attributes: data from field boundary, margin, and verge.
    - Edge Veg Cover: percent cover of ground vegetation in June.
    - Edge Veg Flower: plant flowering from April to August.
    - Edge Veg Seed: plant seed setting in July and August.
    - Edge Bare Ground: percent bare ground.
    - Edge Spray Damage: vegetation damage from spraying.
  - Invertebrates
    - Bee and Butterfly transects: monthly counts April–August in crop and field margins; Pollinators combines these counts.
    - Crop Pests: counts of herbivores on the crop early and late in the season.
    - Gastropods: Gastropod Search (field margin) and Gastropod Trap (in crop) in spring and autumn.
    - Pitfall: counts of surface-active invertebrates early, mid, and late in the crop season.
    - Vortis: arthropod counts on plants in verge and crop, early and late season.
  - Additional tables
    - Crop drilling dates, herbicide applications, height and cover of weeds and crops.
    
- Data structure and naming conventions
  - Table naming convention: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain; sum_b_early_pitfall).
  - Generic table properties
    - Rows represent half-field totals for a separate site; includes group totals and species-level details.
    - Sites are tied to Defra government regions; South-eastern and Eastern England regions often aggregated for confidentiality.
    - Nulls appear where data were not collected; some counts are decimal due to proportional transect methods.
  - Specific table properties
    - All crop_pest tables include a suffix indicating winged or wingless status: W+ or W-.
  - Column headings and data types
    - conv_count, conv_count_FL ( flowering ), conv_count_GE4TL, conv_count_L4TL, conv_count_SE (seeding)
    - crop_cover: percent cover of crop
    - crop_unit: C (conventional) or GM (GM crop)
    - crop_height: height of crop (cm)
    - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
    - name: species or group name
    - site_ref: site reference number shared across all tables
    - Region: Defra government region (or aggregates)
    - VEG/ARTHROPOD/GASTROPOD/BB_BRC: codes for vegetation, arthropods, gastropods, and Bees & Butterflies
    - weed_cover_pc: percent cover of non-crop vegetation
  - Data provenance and context
    - References to broader thematic work: spring crops theme issue and winter rape study, with listed publications for methodological and ecological context.

- Data governance and accessibility considerations
  - Emphasizes standardized data collection, clear metadata, sharing of underlying data, and consistent site-region referencing, aligning with governance and openness expectations common in monitoring frameworks.
  - Aggregation for confidentiality and regional mapping indicates balance between data transparency and privacy.

- Publications and guidance
  - The document cites related work for deeper context and validation, including:
    - The 2003 Phil. Trans. Royal Soc. paper on spring crops.
    - The 2005 Proceedings of the Royal Society (Series B) on effects of herbicide management in GMHT winter-sown oilseed rape.

- Relevance to monitoring framework authors
  - Demonstrates comprehensive, multi-tiered data collection aligned with evaluating policy-driven agricultural technologies.
  - Shows explicit data organization, provenance, and governance practices that support reproducibility, auditability, and stakeholder communication.
  - Highlights practical challenges addressed through structured protocols and standardized metadata (e.g., site references, regional aggregation, and clear naming conventions) relevant to designing robust monitoring frameworks.