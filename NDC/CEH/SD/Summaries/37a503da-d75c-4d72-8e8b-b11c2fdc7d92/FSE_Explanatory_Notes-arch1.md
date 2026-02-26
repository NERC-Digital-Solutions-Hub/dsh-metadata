# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Dataset Descriptions

- Crops studied: Beet, Maize, Spring-sown Oilseed Rape, Winter-sown Oilseed Rape.
- Data collected across several data areas and themes:
  - Seedbank: Seedbank counts from soil samples before planting; Seedbank Follow-up 1 (one year after initial seedbank); Seedbank Follow-up 2 (two years after initial seedbank).
  - Vegetation in the crop: First-seedling (pre-herbicide), Beet Mezzanine (between herbicide applications on conventional vs GM sides), Winter Rape Mezzanine (spring pre-herbicide), Post-herbicide (after herbicide on both sides), Final Counts (same time as Biomass sampling), Biomass (weeds) before harvest, Seed Rain (seeds produced during the season), Follow-up 1 (one year post-trial), Follow-up 2 (two years post-trial).
  - Field edge vegetation: Margin Attributes; Edge Veg Cover (June), Edge Veg Flower (April–August), Edge Veg Seed (July–August), Edge Bare Ground, Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects monthly (April–August); Pollinators (combined Bee + Butterfly counts); Crop Pests; Gastropod Search (field margin); Gastropod Trap (in crop); Pitfall (surface-active invertebrates); Vortis (arthropods on plants) in verge and crop.
  - Additional tables: Dates crops drilled; Herbicides applied; Height/Cover of weeds and crop.
- Table naming convention: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain = summary from Beet crop for seedrain; sum_b_early_pitfall = summary from Beet crop for early-season pitfalls).
- Generic table properties:
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Group totals are provided as well as individual species contributing to those groups.
  - Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Nulls appear where no verified data were collected.
  - Some counts are shown with decimals because values are calculated from only a proportion of transects.
- Specific table properties:
  - All crop_pest tables include a name suffix of 'W+' or 'W-' to indicate winged vs. wingless forms.
- Column headings (examples):
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover, crop_unit (C = conventional crop, GM = GM crop)
  - crop_height
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name)
  - site_ref (site reference number; consistent across all tables)
  - Region (Defra Government regions or aggregates)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (codes for vegetation/arthropods/gastropods/bees&butterflies)
  - weed_cover_pc (percent cover of non-crop vegetation)
- Data context:
  - The document provides a framework and glossary for how data are recorded and referenced across multiple crops and data types, enabling cross-crop analyses of weed, crop, invertebrate, and edge-vegetation dynamics under GMHT management.
  
## Additional notes and references

- For spring crops: Phil. Trans. Royal Soc. B (The Farm Scale Evaluations of spring-sown genetically modified crops), 2003, 358(1439).
- For winter rape: Bohan et al., 2005, Effects on weed and invertebrate abundance and diversity of herbicide management in genetically modified herbicide-tolerant winter-sown oilseed rape, Proceedings of the Royal Society B.