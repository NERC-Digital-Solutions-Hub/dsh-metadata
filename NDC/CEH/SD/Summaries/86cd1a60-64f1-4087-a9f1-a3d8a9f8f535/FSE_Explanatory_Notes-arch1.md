# Explanatory notes

- Objective: The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

- Datasets and Crops
  - Four crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
  - Data collected across multiple domains:
    - Seedbank: Seedbank (pre-plant), Seedbank Follow-up 1 (one year after initial), Seedbank Follow-up 2 (two years after initial).
    - Vegetation in the crop: First-seedling; Mezzanine (Beet) or Winter Rape Mezzanine; Post-herbicide; Final Counts; Biomass of weeds; Seed Rain; Follow-up 1 (one year after); Follow-up 2 (two years after).
    - Field edge vegetation: Margin Attributes; Edge Veg Cover (June); Edge Veg Flower (April–August); Edge Veg Seed (July–August); Edge Bare Ground; Edge Spray Damage.
    - Invertebrates: Bee and Butterfly transects (Pollinators); Crop Pests; Gastropod Search; Gastropod Trap; Pitfall; Vortis (arthropods on plants).
    - Additional tables: Date drilled; Herbicides applied; Height/Cover of weeds and crop.

- Data organization and naming
  - Table naming convention: All tables are named and referenced using the format abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain for Beet crop seed rain; sum_b_early_pitfall for Beet early-season pitfall).
  - Generic properties:
    - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
    - Group totals plus individual species contributions are included.
    - Sites are linked to Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
    - Nulls indicate missing verified data.
    - Some counts are shown with decimals due to using a proportion of transects.
  - Specific properties:
    - crop_pest tables use a name suffix of 'W +' or 'W-' to denote winged vs. wingless.

- Key columns and metadata
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE: conventional crop counts at various plant categories.
  - crop_cover: percent cover of the crop (C) or GM crop (GM).
  - crop_unit: C or GM indicating conventional or GM crop.
  - crop_height: height of the crop in centimetres.
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE: GMHT crop counts at various plant categories.
  - name: species or group name (scientific or common British name).
  - site_ref: site reference number (consistent across all related tables).
  - Region: Defra Government region or aggregated region.
  - weed_cover_pc: percent cover of non-crop vegetation.
  - Regional and site metadata are maintained; data portals may provide dataset discoverability with metadata.

- References and context
  - The work is linked to broader research on GMHT impacts; cited publications include:
    - Phil. Trans. Royal Soc. B (2003/2005) on spring crops.
    - Proceedings of the Royal Society B (2005) on effects on weed and invertebrate abundance and diversity of herbicide management in GMHT winter-sown oilseed rape.

- Notes on scope and intent
  - Data are intended to support analyses of potential wildlife effects arising from GMHT crop management.
  - The dataset emphasizes standardized protocols across crops, timepoints, and regions to enable cross-site comparisons and statistical analysis.