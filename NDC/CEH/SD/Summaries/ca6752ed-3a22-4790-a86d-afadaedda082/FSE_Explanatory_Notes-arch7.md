# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## GIS-relevant overview

- Data are organized around multiple crops (Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape) and across defined study areas, enabling spatial analysis by site and Defra region.
- Datasets are designed for map-based visualization and spatial exploration of habitat features, vegetation, invertebrates, and field margins in relation to GMHT management.

## Dataset scope and data domains

- Seedbank
  - Seedbank: counts of germinating plant species from pre-plant soil samples.
  - Seedbank Follow-up 1: soil sample one year after initial seedbank.
  - Seedbank Follow-up 2: final soil sample two years after initial seedbank.
- Vegetation in the crop
  - First-seedling: initial vegetation survey before herbicide.
  - Mezzanine: crop-specific vegetation survey (Beet and Winter rape) around herbicide timing.
  - Post-herbicide: vegetation survey after herbicide on both conventional and GM sides.
  - Final Counts: vegetation survey concurrent with biomass sampling pre-harvest.
  - Biomass: weeds sampled the month before harvest.
  - Seed Rain: seeds produced across the growing season.
  - Follow-up 1/Follow-up 2: vegetation surveys conducted one and two years after the trial.
- Field edge vegetation
  - Margin Attributes: physical features around field edges, margins, and verges.
  - Edge Veg Cover: percent cover of non-crop vegetation in June.
  - Edge Veg Flower: flowering from April to August.
  - Edge Veg Seed: seed setting in July and August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage from spraying.
- Invertebrates
  - Bee and Butterfly transects: monthly counts April–August in crop and margins.
  - Pollinators: combined counts of bees and butterflies.
  - Crop Pests: herbivores on the crop early and late in the season.
  - Gastropod Search/Trap: gastropods in margins and crops (spring and autumn).
  - Pitfall: surface-active invertebrates counts early, mid, and late season.
  - Vortis: arthropods on plants (early/late season) in verge and crop.
- Additional tables
  - Crop drilling dates, herbicide applications, and height/cover of weeds and crop.

## Data structure and naming

- Table naming convention: sum_[crop]_[sample date]_protocol (e.g., sum_b_seedrain for Beet seed rain; sum_b_early_pitfall for Beet early-season pitfall).
- Generic table properties
  - Rows represent half-field totals (counts/biomass/mean percent cover) for individual sites.
  - Both group totals and individual species contributions are provided.
  - Sites are geo-referenced within Defra regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Nulls indicate missing verified data.
  - Some counts use decimals due to partial transects.
- Specific table properties
  - Crop_pest tables include a suffix indicating winged ('W+') or wingless ('W-') status.

## Column headings and data codes

- conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
- crop_cover, crop_unit, crop_height
- gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
- name (species or group name)
- site_ref (site reference number, consistent across tables)
- Region (Defra government region or aggregate)
- VEG/ARTHROPOD/GASTROPOD/BB_BRC (code for vegetation/arthropods/gastropods/bees & butterflies)
- weed_cover_pc (percent cover of non-crop vegetation)

## Data provenance and references

- For spring crops: The theme issue “The Farm Scale Evaluations of spring-sown genetically modified crops” (Philosophical Transactions of the Royal Society, 2003; 358(1439)).
- For winter rape: “Effects on weed and invertebrate abundance and diversity of herbicide management in genetically modified herbicide-tolerant winter-sown oilseed rape” (Proceedings of the Royal Society Series B, 2005).

## GIS-usage considerations

- Data are organized by site with regional references, enabling spatial mapping of habitat features, crop management, and invertebrate responses.
- Temporal components (Follow-ups, seasonal surveys) support time-series visualization and change detection across years.
- Margin and field-edge data allow analysis of edge effects and habitat connectivity relative to GMHT management.

## Limitations and data quality notes

- Half-field totals and aggregated regional references may limit some site-level precision.
- Nulls indicate data gaps; some measurements carry decimals due to partial transect coverage.
- The dataset references and abbreviations may require cross-walking with Defra region codes and site identifiers for integration with otherGIS layers.

## Summary of purpose

- The compiled datasets provide a comprehensive, multi-crop, multi-year, geo-referenced data repository to assess potential wildlife and biodiversity effects of GMHT crop management, suitable for map-based analyses and decision-support in policy, consultancy, and public information contexts.