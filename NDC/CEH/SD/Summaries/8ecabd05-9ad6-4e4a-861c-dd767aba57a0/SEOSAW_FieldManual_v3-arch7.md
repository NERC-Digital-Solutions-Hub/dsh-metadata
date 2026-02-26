# SEOSAW Field Manual

## Overview
- Describes a method for establishing long-term plots in savannas, woodlands, and forests, with a focus on southern Africa.
- Aims for compatibility with SEOSAW protocols and global comparisons; complements with data entry forms (Android/ODK and Excel).
- Emphasizes sharing experience to avoid repeating mistakes; notes that alternative designs may exist but this is a robust, broadly applicable approach.

## Plot design and location (GIS-focused)
- Locate plots in homogeneous soils and with consistent land-use history; obtain informed consent from landowners and users.
- Long-term plots: 0.25–1.0 ha, with 1.0 ha squares preferred.
- For each stem (alive or dead, standing or fallen) record measurements above a defined minimum diameter.
- Random or pre-determined placement within strata to reduce bias; regularly spaced plots (e.g., on a grid) can aid analyses.
- Determine random plot locations using GIS to place points within strata; keep extra points as reserves.
- Consider drones for site assessment (disturbance proximity, drainage) and to aid in planning; use free drone-capture tools and post-processing software (e.g., Pix4D Capture, DJI GS Pro; Pix4D, Agisoft for mosaics).
- Record planimetric and topographic context: bearings, latitude, longitude, elevation; adjust for slope to enable comparisons with planar-area plots.

## Plot shape, orientation, and size
- Plot shapes: circular, square, or rectangular; square generally preferred for 0.1 ha+ plots due to perimeter:area considerations.
- Principal axes: align with cardinal directions when possible; document bearings, location, and altitude.
- Size considerations: 1 ha is standard for long-term monitoring; smaller plots (0.75, 0.5, 0.25 ha) acceptable where vegetation structure is homogeneous and tree density is high; ensure enough stems (≥25) for diversity metrics.

## Plot establishment timing
- Aim to measure in the same season each year to minimize stem-water-content effects on diameter.
- Dry season preferred for easier measurements; rainy season valuable for voucher collection and flowering/fruiting identifications.

## Visibility and plot markers
- Mark corners/center for long-term relocation, or use cryptic methods if markers may bias sampling.
- Durable markers: concrete posts, steel droppers, or buried markers; consider cryptic approaches where necessary.
- Use a 20 cm offset above the POM for tagging; maintain marker durability against corrosion, fire, termites.
- When marking risks bias, use alternative relocation methods (maps, buried markers) and/or a 20 m grid within the plot for re-measurement accuracy.

## Data recording and metadata
- Use SEOSAW plot data sheet for plot-level metadata.
- Record: plot design (shape/size), location (lat/long, altitude, slope, aspect), sampling within plot, environmental conditions (rainfall, canopy, termites), land-use history, fire history, herbivore exposure, and other contextual factors.

## Tree stems: what to measure and how (Section 5)
- Measure all stems meeting inclusion criteria (base inside plot ≥50% and diameter above the threshold).
- Minimum diameter threshold commonly 5 cm or 10 cm; for recruitment analysis, measure smaller stems as needed.
- Optional sub-plots: separate sections for poles, saplings, and seedlings.

### 5.2 Diameter and point of measurement (POM)
- Measure diameter at a defined POM: 1.3 m or 0.3 m above ground along a straight line (not vertical height).
- Default POM is 1.3 m; if few stems reach 1.3 m, use 0.3 m (and measure a subset at both POMs for conversion).
- Adjust POM for forks, resprouts, buttresses, or lean; for each stem, record exact POM and note any deviations.
- Use a stick with a mark or a tag for re-measurement; if necessary, move POM to a new position (and record) for accurate diameter representation.
- For difficult stems (climbers, deformations), use half-diameter methods or measure at multiple points as described.

### 5.3 Marking and mapping stems
- Mark stems with metal tags or painted numbers; attach 20 cm above POM for re-measurement ease.
- If tagging may affect plot use, bury tags at the base as an alternative.
- Map stem locations to enable re-measurement and spatial analyses; record coordinates by dividing the plot into 10 m strips or use a center-based approach for circular plots.
- GPS can be used but ensure sufficient accuracy; standard handheld GPS may require supplementary methods for precise relocation.

### 5.4 Damage and topkill
- Record full-cut/breakage height, cambium exposure, bracket fungi, and whether stems have fallen.
- Exclude non-rooted stems from stem inventory; fallen but rooted stems are included if contiguous to the POM.

### 5.5 Alive / Dead and topkill
- Record each stem as alive or topkilled; topkilled means no signs of life above POM.
- Use codes to document mode of death (e.g., uprooted, snapped, standing, vanished) and probable cause (neighboring tree, elephant, fire, human, termites, wind).
- For uncertain causes, use “Q” and add notes.

### 5.6 Species identification
- Assign species or morphospecies; involve a botanist/parataxonomist; collect vouchers when possible.
- Photograph living and dried specimens; ensure voucher export complies with Nagoya protocol and permits.
- Use local names or morphospecies where needed; standardize determinations across sites.

### 5.7 Height
- Height is time-consuming; develop site-specific height–diameter relationships (roughly 50 trees across DBH ranges) to estimate height if needed.
- If height data are essential, use trigonometry or height-measuring devices; otherwise, estimate via height–diameter relationships.

### 5.8 Stems on termite mounds
- Note stem location relative to termite mounds, as mound-associated flora differs.

### 5.9 Data recording
- Use separate data sheets for live stems, topkilled stems, recruits, and stumps to support clear demographic analyses.

## Small stems, stumps, and coarse woody debris (Sections 6–8)
- 6 Small stems: Poles (≥5 cm and <10 cm), Saplings (height-based thresholds), Seedlings; count rather than measure in a 2 m x 50 m transect within each 0.25 ha plot; two such transects per plot.
- 7 Stumps: Measure diameter at top, height, diameter at 0.3 m, decay class, species where possible, and cause of break if known.
- 8 Coarse woody debris: Measure intersecting pieces along perpendicular transects radiating from plot center; record diameter at intersection, length, decay class, and species; apply standard biomass equations to estimate density, volume, and biomass.

## Plot re-measurement (Section 9)
- Re-measure approximately every 5 years, with a shorter initial period to resolve early census issues.
- Compare with previous censuses; keep all prior data on the same data sheets (insert blank rows for each stem to maintain consistency).
- Recruits should be documented on a separate recruit sheet; do not reuse tag numbers.
- Track mortality and topkill by maintaining base IDs across stems; update tagging as needed; if a stem dies in two censuses, removal from field sheets is acceptable.
- Re-measure all stems, re-locate POMs, and note any changes; if POM becomes unreliable, measure at both old and new POM to adjust biomass.

## Annexes and data sheets
- Annex 1: Plot data sheet – comprehensive plot-level metadata including design, location, sampling, environmental conditions, land use, fire history, canopy, termites, etc.
- Annex 2: Stem data sheet – stem-level records (subplots, X, Tag No, Base Tag No, species, POM, DBH, alive/dead, stand/fall type, mode, cause, decay, height, notes, etc.).
- Data sheets are designed to facilitate consistent data entry, cleaning, and analysis across censuses.

## Tools, standards, and references for GIS specialists
- Data integration: designed to produce geospatially explicit plot and stem data suitable for GIS visualizations and global comparisons (e.g., RAINFOR-compatible formats).
- Allometry and biomass: specify recommended allometry (e.g., Chave et al. 2014) for biomass estimation; choose local/allometric options when available.
- Data management: consistent use of IDs (stem and base IDs) across censuses enables demographic analyses (recruitment, resprouting, topkill, mortality).
- Ethics and legality: obtain land-use consent; follow Nagoya protocol for voucher specimens; maintain proper permissions for specimen export and data sharing.
- Outputs for GIS: geolocated plot boundaries, plant locations (stem coordinates), POM-based diameter data, and multi-layer attributes (species, status, height, canopy context) suitable for map-based data products and spatial analyses.