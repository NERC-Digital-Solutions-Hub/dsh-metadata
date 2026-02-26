# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Crops and data domains

- Four crops studied: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.
- Data collected across multiple ecological domains:
  - Seedbank: counts of plant species germinating from soil samples taken before planting; Follow-up 1 (one year after initial sample); Follow-up 2 (two years after initial sample).
  - Vegetation in the crop: first-seedling (pre-herbicide); Mezzanine surveys (Beet: between herbicide applications on conventional vs GM side; Winter rape: spring before any herbicide); Post-herbicide; Final vegetation survey; Biomass of weeds prior to harvest; Seed rain during the growing season; Follow-ups 1 and 2 years after trial.
  - Field edge vegetation: Margin attributes around field edges; Edge Veg Cover (June); Edge Veg Flower (April–August); Edge Veg Seed (July–August); Edge Bare Ground; Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects monthly (April–August); Pollinators (combined Bee/Butterfly counts); Crop Pests; Gastropod Search (verges) and Gastropod Trap (in crop, spring and autumn); Pitfall traps; Vortis (arthropods on plants) in verge and crop.
  - Additional tables: Date crops were drilled; Herbicides applied; Height/Cover of weeds and crop.

## Data collection timing and measures

- Systematic, time-staggered surveys aligned to herbicide application and crop development to capture potential GMHT effects on wildlife and vegetation across the growing season and into post-harvest periods.

## Data organization and identifiers

- Table naming convention: abbreviatedprefix_crop_(sample date)_protocol, e.g., sum_b_seedrain (Beet, seed rain) or sum_b_early_pitfall (Beet, early pitfall).
- Each row represents half-field totals (counts/biomass/mean percent cover) for a single site.
- Datasets include both group totals and species-specific contributions.
- Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
- Nulls appear where data were not collected; some counts are decimal due to partial transects.

## Column headings and key variables

- Crop and GM indicators:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - crop_cover (percent cover), crop_unit (C = conventional crop, GM = GM crop)
  - crop_height (cm)
- Species and site identifiers:
  - name (species or group)
  - site_ref (site reference number)
  - Region (Defra Government region or aggregate)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC codes for classification
  - weed_cover_pc (percent cover of non-crop vegetation)

## Data quality, outputs and sharing

- Data are intended to be verified, quality assured, cleaned, and transformed for analysis.
- Outputs are presented in clear formats (reports, maps, charts) to enable standardized assessment of environmental health and policy performance over time.
- Datasets are stored and uploaded to appropriate data portals to facilitate access to underlying data for broader use.

## References and context

- Additional information on spring crops: Phil. Trans. Royal Soc., 2003; 358(1439).
- Additional information on winter rape: Bohan et al., 2005, Proc. R. Soc. B, 272:463-474 (Effects on weed and invertebrate abundance and diversity under GMHT management).