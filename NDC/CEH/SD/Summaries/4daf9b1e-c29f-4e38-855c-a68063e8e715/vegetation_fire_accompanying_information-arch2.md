# Plant species cover and vegetation damage from burnt and unburnt areas of the Flow Country, Scotland, autumn 2019, following wildfires in May 2019 and nearby historic wildfire sites from the years 1997, 2000 and 2011.

- Purpose and context
  - Document a vegetation survey after a large 2019 wildfire that affected wet heath and blanket bog in the Flow Country, with reference to historic fires in 1981, 1997, 2000, and 2011.
  - Aim to characterise immediate wildfire effects on blanket bog vegetation, compare open bog and drain areas, and assess long-term recovery using a chronosequence approach.

- Study sites and sampling frame
  - Four study sites within or near protected areas:
    - BH: Bighouse Estate
    - FD: Forsinard
    - CR: Croft 1
    - SH: Shurrery & Dorrery
  - Site categorisation reflects landownership and historical fire extent, not stratification by burn intensity.
  - Four plot types per site: burnt bog, burnt drain, unburnt bog, unburnt drain
  - Replication: three plots per type per site (total 48 plots)
  - Within each plot, five sampling points (U1-U5 for bog plots; D1-D5 for drain plots)

- Plot and quadrat design
  - Burnt and unburnt bog plots: 5 ha each, defined as ~125 m radius circles; boundaries adjusted to stay within blanket bog habitat.
  - Burnt drain plots: 500 m length along the nearest drain to the corresponding bog plot.
  - Unburnt bog plots matched to burnt plots by slope and comparable National Vegetation Classification (NVC) type.
  - Drain plots may lie in the same or adjacent areas; included both blocked and active drains where applicable.
  - Quadrat types within plots:
    - ST: standard quadrats
    - HU: hummock quadrats
    - HO: hollow quadrats
    - DR: drain quadrats
  - Field deployment: 356 quadrats surveyed in total (some ST data duplicated when on hummocks or hollows), conducted Sept–Dec 2019.

- Vegetation measurement and data collection methods
  - Each quadrat: 1 m x 1 m, oriented north–south; markers placed to avoid trampling.
  - Drain quadrats placed adjacent to the drain, within ~10 cm of the wall; random side placement.
  - Field forms (Wildfire Vegetation recording form) captured:
    - Plot identifiers, site, burn status, replicate, quadrat type, point number
    - Dominant species and 67 vegetation-, litter-, bryophyte-, algae-, lichen-, rock-/soil-/water-related codes
    - Measurements per quadrat for height, ground cover, microtopography, and other traits
    - Fire-impact measures for burnt plots (Sphagnum damage, moss scorch, moss survival, dwarf-shrub resprouting, ericaceous seedling frequency)
    - Oblique photographs for each quadrat
  - Vegetation metrics collected:
    - Height: maximum and obscured height at three positions (centre, ends)
    - Vertical ground height difference within a 1 m radius
    - Hummock–hollow height difference (for BH and FD)
    - Ground cover: percent cover for each category (vegetation, litter, moss, rocks, bare peat, water layers, etc.)
    - Species-level data: codes for vascular and bryophyte species; dominance at quadrat centre
    - Special notes: deer activity, seedlings (Sitka spruce, Lodgepole pine), deer dung, depth of standing water, pool presence
  - Fire-related assessments (for burnt plots):
    - Sphagnum discoloration and capitulum loss
    - Non-Sphagnum moss scorch/consumption
    - Moss survival (green tissue)
    - Vegetative resprouting of ericaceous shrubs
    - Ericaceous seedling frequency

- Data management and quality assurance
  - Field data captured on standardized forms; photos and forms stored on Forsinard server; samples ID’d in the lab as needed
  - Post-field data handling:
    - Data entry overseen by Field Officer; cross-checked by two staff
    - Quality checks on totals and covers (e.g., ensuring plausible total cover sums)
  - Training and calibration:
    - Pre-field field training to harmonise species identification and cover estimation
  - Standard reference frameworks:
    - Methods align with Forest to Bog (F2B) vegetation recording; and with National Vegetation Classification (NVC) guidance
    - Fire-impact measurements follow Davies et al. (2016) protocols for post-fire assessments

- Datasets and data structure
  - Dataset 1: Wildfire_vegetation_cover.csv
    - Contains data from 356 quadrats across 4 sites, 67 vegetation-related variables plus litter/algae/lichen/rock/water components
    - Key fields: PlotID, plot, site, fire, YR-burnt, no (point number), Qtype, Date, Dominant species, height measurements (Max_height_A/C/F and Obscured_height_*), Height_diff metrics, Ground cover by code, Deer prints, Dung, Seedlings, Water presence/depth, and detailed species/layer codes
    - Includes both alive and dead/burnt plant components where applicable
  - Dataset 2: Wildfire_vegetation_fire_impact.csv
    - Focused on burnt bog plots from the 2019 fire (116 entries)
    - Key fields: SITE, PlotID, No, Qtype, SPH_DIS, SPH_CAP_LOSS, NON_SPH_LOSS, MOSS_SURVIVAL, VEGE_RESPROUT, ERI_SEEDLING, FIELD_NOTES
  - Appendices/codes:
    - Appendix 1: Example field recording sheet template
    - Appendix 2: Code lists for species and field variables (extensive taxon code mapping)

- Temporal scope and limitations
  - Primary fieldwork conducted September–December 2019
  - Planned repeat survey in 2020 to assess one-year recovery was not completed due to COVID-19
  - Chronosequence approach combines 1997, 2000, 2011 historical fires with the 2019 fire to assess longer-term recovery dynamics

- Relevance to environmental monitoring and data use
  - Demonstrates a standardised, repeatable approach to monitor environmental health and post-fire recovery in peatland systems
  - Produces two structured datasets suitable for temporal comparisons, policy evaluation, and cross-site data integration
  - Emphasises making underlying data accessible (plots, drains, plot types, and detailed species cover) for broader use and scrutiny, aligning with the aim to increase data value and accessibility

- Key references and methodological basis
  - National Vegetation Classification (NVC) guidance and Rodwell (1991) for mire/peatland communities
  - Davies et al. (2016) for post-fire vegetation impact measurements
  - Field methods built from Forest to Bog projects and standardized SOPs (where available)