# Farm Scale Evaluations (FSE)

## Aim
- Determine whether genetically-modified herbicide-tolerant (GMHT) crops have any significant effects on farmland wildlife due to management practices.

## Datasets and measurement domains
- Crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data domains and specific measures:
  - Seedbank: counts of germinating plant species from pre-plant soil; Follow-up 1 (1 year later) and Follow-up 2 (2 years later).
  - Vegetation in the crop: First-seedling; Mezzanine (Beet) or Spring-sown oilseed rape; Post-herbicide; Final Counts; Seed Rain (throughout the season); Follow-ups 1 and 2.
  - Field edge vegetation: Margin Attributes; Edge Veg Cover (June); Edge Veg Flower (April–August); Edge Veg Seed (July–August); Edge Bare Ground; Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects (monthly Apr–Aug); Pollinators (combined Bee & Butterfly counts); Crop Pests; Gastropod Search (field margin) and Gastropod Trap (in crop); Pitfall (early/mid/late season); Vortis (arthropods on plants; early/late).
  - Additional tables: Crop drilling date; Herbicide applications; Height/Cover of weeds and crop.
- Documentation and naming: Tables follow a consistent naming convention (e.g., sum_b_seedrain for Beet seed rain; sum_b_early_pitfall for Beet early-season pitfalls).

## Data structure and conventions
- Each row represents half-field totals for a separate site; sites are referenced within Defra Government regions.
- Regions: South-eastern and Eastern England are aggregated due to farmer confidentiality.
- Data completeness: Nulls appear where no verified data were collected.
- Measurements and units: Columns capture counts, biomass, and percent cover; crop_unit differentiates conventional vs GM crops; weed/crop height and cover are recorded.
- Species and groups: Column name "name" indicates species or group name (scientific or common British name); region and site_ref link tables across crops.
- Special table properties: Pest tables use suffixes W+ (winged) or W- (wingless).

## Data governance, quality, and sharing
- Data standards are embedded in the dataset design (explicit table properties, site referencing, regional aggregation to protect confidentiality).
- Metadata and provenance are structured through defined table conventions and naming rules.
- Data sharing considerations: underlying data are linked and described to enable transparency, with confidentiality shaping regional aggregation.
- Data lifecycle and quality: information is organized to support quality assurance, transformation, and analysis, with notes on data presence/absence and potential need for further metadata.

## Endnotes and context
- References for further information on related studies include a Royal Society Proceedings B paper (2005) on effects on weed and invertebrate abundance for winter-sown oilseed rape and related crops.