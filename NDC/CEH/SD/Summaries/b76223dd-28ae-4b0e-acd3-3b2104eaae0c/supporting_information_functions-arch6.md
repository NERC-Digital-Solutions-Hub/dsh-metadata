# Does restoring native forest restore ecosystem functioning? Evidence from a large-scale reforestation project in the Scottish Highlands

## Aim and context
- Investigates ecosystem functioning in the Scottish Highlands across native reforestation sites, with comparisons to unforested and mature forest areas.
- Set in Glen Affric and Glen Moriston, central Highlands, focusing on responses to long-term reforestation (1990–2012 establishment) and grazing exclusion.
- Data collected in 2018 to assess how reforestation influences aboveground carbon, soil carbon and nitrogen, decomposition, soil fauna, tree regeneration, and ground-layer structure.

## Experimental design
- Hierarchical sampling across 14 fenced reforestation sites, each with associated unforested areas, and three sites with associated mature Caledonian pinewood (five mature-forest plots in total: grazed and ungrazed for comparison).
- Treatments represented in all combinations except reforestation × grazed (deer grazing pressure prevents this pairing).
- Plot layout: 10 × 10 m plots; treatment combinations include reforestation (ungrazed), unforested (grazed), unforested (ungrazed), and mature forest (grazed/ungrazed).
- Sampling intervals: plots 30–400 m apart within sites; mature forest plots include two grazed and two ungrazed areas per site to reflect target habitat.
- Reforestation efforts used local seed sources and varied planting methods (hand screefing or machine mounding), with heterogeneous canopy due to drainage and topography.

## Data collected and response variables
- Aboveground tree carbon (biomass and carbon conversion).
- Topsoil carbon and nitrogen (top 10 cm), including bulk density and stocks.
- Decomposition rate via Tea Bag Index (k) across plots.
- Soil invertebrate feeding using bait lamina sticks (presence/absence and proportion of feeding).
- Tree regeneration: seedling counts by height category (dbh < 2.5 cm threshold).
- Ground-layer and moss: height of ground vegetation and depth of moss layer.
- Additional data for structure: shrub layer height.

## Methods and calculations
- Aboveground biomass estimated with species-specific allometric equations; carbon content assumed at 49% for broadleaf and 50% for conifers.
- Topsoil carbon and nitrogen determined by ISO-compliant CN analysis; bulk density used to calculate stocks (kg/m²).
- Decomposition rate derived from mass loss of tea bags, using standardized 54–67 day period.
- Soil invertebrate feeding quantified via bait lamina exposure (six sticks per plot; 16 perforations per stick; 30 days total exposure).
- Seedling regeneration and ground-layer measurements collected per plot, with standardized height categories and quadrat sampling.

## Study sites and planting details
- Fourteen reforestation sites with varying size and age (years since fencing/establishment), planting intensity, and species composition:
  - Athnamulloch One and Two; River Flat; Carnach Mor; Allt Beithe (South); Fionngleann; Camban; Coille Ruigh; Ghubhais; Dundreggan WGS; Allt Fearna; Dundreggan NW; Meallan; Glac Dariach.
- Site characteristics include:
  - Year established (1990–2012), area in hectares, total trees planted, trees per hectare, species types (SP = Scots Pine, A = Aspen, BL = broadleaf, W = Willow, H = Hazel), planting method (hand screefing or machine mounding), and whether mature forest is present at the site.
  - Fenced to exclude grazing by deer and other wildlife; some sites allow low numbers of feral boar and sheep.

## Data structure and accessibility
- Data are organized into clearly labeled CSV files, each with metadata describing fields and units:
  - plot_locations.csv: plot IDs, site IDs, forest and grazing status, year established, grid references.
  - aboveground_carbon.csv: plot-level aboveground carbon (kg/m²).
  - topsoil_C_N.csv: topsoil carbon (%), nitrogen (%), bulk density, and derived stocks (kg/m²).
  - decomposition_rate.csv: Tea Bag Index decomposition constant k per plot and teabag.
  - soil_invert_feeding.csv: bait lamina feeding data per plot (six bait sticks, 16 perforations per stick) and derived feeding proportions.
  - seedling_regeneration.csv: seedling counts by species and height category per plot.
  - shrub_height.csv: mean height of shrub layer per plot.
  - moss_height.csv: mean depth of moss layer per plot.
- Each file includes identifiers for site, plot type (reforestation, unforested grazed/ungrazed, mature grazed/ungrazed) and date/stage details.
- Data are designed for self-service use (dashboards, exploratory analysis) and to support broader data sharing and re-use.

## Usage and potential applications
- Enables comparison of ecosystem functions across forest statuses and grazing regimes.
- Supports synthesis of long-term restoration outcomes and ecosystem functioning in native Scottish pinewoods.
- Useful for policymakers, land managers, and researchers assessing restoration efficacy and informing future reforestation or grazing management strategies.

## References and methodological foundations
- Core methods and context drawn from Warner et al. (2021) on plant, carabid beetle, and broader ecosystem responses to native reforestation.
- Supporting biomass and carbon conversion references (Muukkonen & Mäkipää; Zianis et al.; Matthews) for allometric calculations and carbon content.
- Contextual background on Scottish Highlands forest history, deer impacts, and habitat restoration priorities.

## Appendix 1 – Roles of authors
- Experimental design: Emily Warner, Andy Hector, Owen Lewis, Nick Brown
- Background information and fieldwork facilitation: Doug Gilbert, Alan McDonnell
- Data collection: Emily Warner, Rowan Green