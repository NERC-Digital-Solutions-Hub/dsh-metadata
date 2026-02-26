# National Plant Monitoring Scheme (NPMS)

## Purpose and scope
- A habitat-based plant monitoring scheme designed to track changes in plant abundance and habitat quality across the UK, Isle of Man, and Channel Islands.
- Aims to detect habitat change, understand drivers/pressures, and contribute to UK Biodiversity Indicator C7.
- Provides annually updated data and feedback to volunteers; data managed by CEH, BSBI, JNCC, and Plantlife.

## Data files provided (2015–2018)
- locations_2015to2018.csv: unique location_id and location_type (square or linear) describing survey plots by location.
- sampleInfo_2015to2018.csv: sample-level information including id, survey_id, date_start, location_id, entered_sref and entered_sref_system (spatial reference), created_on/by.
- sampleAttributes_2015to2018.csv: additional attributes linked to samples via sample_id (sample_attribute_id, caption, text_value).
- occurrences_2015to2018.csv: species occurrences linked to samples (id, sample_id), with taxon data (taxonversionkey, preferred_taxon), domin (Domin scale) for cover, record_status, and sensitivity_precision (blurring when needed).
- npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.

## Spatial data and GIS considerations
- location_id links to samples; each sample has spatial reference (entered_sref) and system (OSGB 27700, Irish National Grid 29902, or WGS84 4326) for GIS integration.
- Domin scale provides percent cover for species within plots; supports map-based visualization of habitat condition.
- Some records may be spatially sensitive and blurred (sensitivity_precision = 10000 implies 10 km blur).

## Survey design and habitat classification
- 28 fine NPMS habitats, aggregated into 11 broad NPMS categories (Appendix 1).
- Plots: fixed 5x5 m square plots (10x10 m for woodland) and 1x25 m linear plots.
- Plots are selected within kilometre squares; pre-selected locations and Protocol A self-selection options available to ensure representative coverage.
- Habitat assignments may change over time due to management or environmental change; plots can be reclassified to appropriate habitat lists as needed.

## Data collection and recording methods
- Three survey levels: Wildflower Level (fewer target species), Indicator Level (robust indicator species), Inventory Level (full vascular plant list).
- Plot layout and relocation: use pre-selected plot locations when possible; if not feasible, self-select plots but ensure they are relocatable in future years; record plotting details (sketches, photos, GPS).
- Recording protocol: identify species using habitat-specific lists; estimate percent cover (Domin scale); record bare ground, litter, moss/lichen, and other optionally recorded attributes (vegetation height classes, woodedness, aspect, slope, management).
- Data entry: online via NPMS portal (www.npms.org.uk). If online entry is not possible, submit printed forms by mail.
- Documentation: field sketches, up to two photos per plot, GPS as support; ensure plots can be relocated in subsequent years.

## How to record in plots (key methods)
- Record species present using the applicable habitat-specific species list; search efficiently within plots.
- Abundance: estimate percent cover for each species (Domin scale). Consider layering and cover beneath larger plants.
- Additional measures: percent bare ground, litter, moss/lichen, bare rock/gravel; optional vegetation height, woodedness, aspect, slope, and management details (with defined categories).

## Data quality assurance and governance (EQA)
- EQA supported by peer-reviewed publications and project documentation.
- Data verification through iRecord for certain records; review and oversight by a project Steering Group; external expert inputs for design and QA.
- Uncertainty estimation via models; outputs checked by scientists; data publication aims for transparency and public availability.
- Documented data management practices, version control, and off-site backups following CEH standards (PRINCE2).

## Access, rights, safety, and withdrawal
- Access rights vary by country; follow local codes (e.g., Countryside/Outdoor Access Code; landowner permissions).
- Surveyors are responsible for safety; assess weather, terrain, and access risks; do not risk safety and consider surveying with a buddy.
- Withdrawal possible; efforts made to reallocate plots to other surveyors if withdrawn.
- Data sharing and support: data submission support via NPMS contact; support email provided.

## How to use NPMS data in GIS
- Use location_id to join locations with samples, then join sampleAttributes and occurrences to build a full spatial dataset of habitat plots and species.
- Utilize entered_sref and entered_sref_system to project data into a common coordinate system for mapping.
- Visualize habitat condition and species indicators over time; account for uncertainty and verification status where applicable.
- Respect data sensitivity where present (blurring) and follow data sharing guidelines.

## Appendix: Habitat types (summary categories)
- 1) Arable field margins
- 2) Bog and wet heath (blanket bog, raised bog, wet heath)
- 3) Broadleaved woodland (dry deciduous woodland, native hedgerows, wet woodland)
- 4) Coast (coastal saltmarsh, dunes, vegetated shingle, machair, maritime cliffs)
- 5) Fresh water (nutrient-poor/ nutrient-rich lakes, ponds, rivers and streams)
- 6) Heathland (dry heathland, dry montane heathland)
- 7) Lowland grassland (dry acid grassland, dry calcareous grassland, neutral damp grassland, neutral pastures and meadows)
- 8) Marsh and Fen (acidic and base-rich fens/flushes/mires/springs)
- 9) Native pinewood and juniper scrub (conifer woods, juniper scrub)
- 10) Rock outcrops, cliffs and screes (inland and montane rocks and scree)
- 11) Upland grassland (montane acid and calcareous grasslands)

## Notes for mapping and analysis
- The dataset is designed for long-term change detection; ensure consistent plot relocation and habitat classification across years.
- Consider the three survey levels when interpreting species richness and abundance; Inventory Level provides the most comprehensive data.
- Use the NPMS HabitatLookup for alignment between broad and fine habitat classifications in GIS analyses.