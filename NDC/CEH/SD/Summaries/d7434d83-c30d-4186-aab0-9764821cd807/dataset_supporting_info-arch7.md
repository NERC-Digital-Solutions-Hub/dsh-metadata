# Ecological, dietary, and socio-economic data from 10 smallholder farming villages in Jumla District, Nepal, 2021-2022

- A comprehensive transdisciplinary dataset from 10 smallholder farming villages in Jumla District, Nepal, collected across 2021–2022 to explore diets, nutrition, farming practices, pollination, and climate-related impacts.
- Includes both ecological (plant–pollinator interactions, flowering density, pollen loads) and socio-economic/dietary data (household census, participant dietary recalls, anthropometry, farming and beekeeping practices, cooks’ and lead farmers’ questionnaires).
- Spatial design features: study area around village centers (600x600 m) with 9 plots per village across three habitat types (village, crop, semi-natural); a separate altitudinal field experiment along a 2400–3100 m gradient with 15 sites.

## Spatial coverage and geospatial context

- Location: Patarasi Rural Municipality, Jumla District, Nepal; 10 study villages mapped (Figure 1 reference).
- Ecological datasets are tied to fixed plots within 600x600 m study areas, categorized into habitat types and surveyed at multiple biweekly intervals.
- Field experiments conducted along an altitudinal gradient (15 sites, 2400–3100 m) with standardized crop plots and insect visitation measurements.
- Several datasets provide hierarchical spatial summaries (plot, habitat, village) suitable for GIS aggregation and visualization.

## Datasets included (structure, content, and GIS relevance)

- Plant-pollinator interactions
  - 11,107 interactions recorded across 10 villages (Apr–Nov 2021).
  - Two CSVs: data and metadata.
  - Each row documents a plant–insect interaction with location/place within plots.
  - Useful for network mapping, pollination risk maps, and habitat-type comparisons.

- Flower density data
  - Metadata + raw flower data plus plot-, habitat-, and village-level summaries.
  - Floral abundance scored per quadrat (0–4 scale) with additional 0.1/0.2/0.3 scale for undetected flowering plants.
  - Enables spatial layers of flowering resource availability for pollinators.

- Pollen analysis data
  - Pollen loads from 1,928 insect specimens (subset of pollinator list).
  - Species/genus/family/order-level summaries plus metadata.
  - Supports spatial overlays of pollinator foraging & crop dependence.

- Farmer questionnaire data
  - 200 lead farmers across 10 villages; land ownership, practices, income, crops (6 pollinator-dependent crops), climate awareness.
  - Spatial use may be limited, but can be linked to village-level GIS polygons for regional patterns.

- Field experiment data
  - Pollinator exclusion, open pollination, and hand pollination treatments across 15 sites and multiple crops (apple, beans, pumpkin, slipper gourd).
  - Yields recorded per plant/branch/node and insect visitation data per crop-site.
  - Site_info and multiple crop-yield sheets enable site-level and crop-level mapping of pollination effects along the altitude gradient.

- Beekeeper questionnaire data
  - 116 beekeepers across 10 villages; honey yield, hive counts, perceived drivers of change.
  - Individual beekeeper data that can be aggregated to village-level honey-production maps.

- Household census data
  - Village-wide census at HH and individual levels; detailed household composition for sampling frames.
  - Enables creation of village-level demographic and socio-economic maps; supports linking with dietary and anthropometry data.

- 24-hour dietary recall data
  - 12-month, fortnightly recalls for 721 individuals from 200 households.
  - Ingredient-level dietary data with geographic linkage to participant residence; supports nutrient intake mapping.

- Anthropometry data
  - Monthly anthropometric measurements for 721 participants; linked to households.
  - Spatially mappable at village level to investigate nutritional status patterns.

- Participant information data
  - Demographics and household characteristics; anonymized.
  - Supports cohort-level GIS analyses when linked to household locations.

- Cook questionnaire data
  - Household cooking practices, fuel use, and food security (two files).
  - Village-level summary potential for mapping cooking-energy access trends.

## Data structure and access

- Data collection platform: CommCare-based mobile data entry with anonymization prior to sharing.
- Data can be linked via household or participant identifiers to produce multi-layer GIS-ready datasets (points for plots, sites, households; aggregated polygon-level summaries for villages).
- Metadata provided for each dataset to interpret columns and units; some columns may contain NA values due to conditional questioning or zero responses, retained to preserve question provenance.

## Quality, limitations, and harmonization notes

- Quality controls include botanist/insect taxonomist verifications, regular monitoring visits, and field-based standardization training.
- Some NA values observed in columns where questions were conditional or inapplicable; dataset retains these for completeness.
- Spatial resolution varies by dataset (plot- and site-level data vs. household- and village-level summaries); integration requires careful alignment by village, plot, or site identifiers.

## Potential GIS products and analyses

- Pollination and ecological risk maps:
  - Plant–insect interaction networks by village and habitat type.
  - Spatial distribution of pollinator activity intensity across crops and landscapes.
- Resource availability mapping:
  - Flower density and flowering abundance heatmaps at plot, habitat, and village scales.
  - Overlay with pollinator visitation data to identify high/low resource areas.
- Altitudinal gradient analyses:
  - Yield and visitation patterns across the 2400–3100 m gradient; site-level choropleth maps.
- Nutrition and livelihoods mapping:
  - Diet diversity and nutrient intake indicators linked to household locations.
  - Household honey yields, beekeeping activity, and farming practices mapped at village scale.
- Integrated dashboards:
  - Multi-layer GIS views combining ecological, dietary, and socio-economic dimensions for policy briefs or stakeholder engagement.

## Summary of practical considerations for GIS specialists

- Ready-to-use geospatial anchors: village polygons, site coordinates, and plot locations enable robust map-based storytelling.
- Rich multi-omics and socio-economic context: enables cross-domain spatial analyses (e.g., how pollination resources relate to diet or household economics).
- Harmonization opportunities: align datasets via village/site/plot and household IDs to produce cohesive maps and models.
- Data provenance and reproduction: complete metadata and clear data lineage support reproducible GIS workflows and future updates.