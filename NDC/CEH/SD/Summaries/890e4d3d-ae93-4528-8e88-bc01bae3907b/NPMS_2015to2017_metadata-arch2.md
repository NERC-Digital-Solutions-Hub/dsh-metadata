# National Plant Monitoring Scheme survey data (2015-2017)

## Overview and aims
- NPMS is a habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC.
- Purpose: provide an annual indication of changes in plant abundance and diversity; detect habitat change; understand drivers; contribute to UK Biodiversity Indicator C7.
- Volunteers collect data in fixed plots across 28 NPMS habitats (combined into 11 broad categories) to produce a statistically robust view of habitat condition over time.
- Data are stored in the NPMS database at CEH Wallingford and can be published for independent review.

## Data files provided
- locations_2015to2017.csv: unique location_id and location_type (square or linear plot).
- sampleInfo_2015to2017.csv: records of sampling events linked to locations (survey_id, date_start, entered_sref, created_on, created_by_id, etc.).
- sampleAttributes_2015to2017.csv: additional attributes linked to samples (sample_id, caption, text_value).
- occurrences_2015to2017.csv: species observations per sample (id, sample_id, taxonversionkey, preferred_taxon, domin, record_status, sensitivity_precision).

## Evidence Quality Assurance (EQA)
- NPMS data supported by peer-reviewed articles, internal reports, and project documentation.
- Data verification includes iRecord-based review for certain records; online data capture with a species dictionary and controlled fields; geographic range checks; and model-based uncertainty estimates.
- Outputs are checked by scientists; external peer review occurs when risk warrants it; data are publicly publishable for independent review.
- Version control and data tracking follow a Data Management Plan and PRINCE2 standards.

## How the survey works
- Scope: monitoring plant communities and habitat indicators in 28 fine NPMS habitats (11 broad categories) using plots within UK, Isle of Man and Channel Islands countryside.
- Plots
  - Square plots: 5x5 m (woodlands 10x10 m).
  - Linear plots: 1x25 m for certain habitats (e.g., hedgerows, margins, rivers, ponds).
- Survey frequency: two visits per year (late spring/early summer and late summer) for longitudinal tracking.
- Plot selection
  - Pre-selected plot locations within squares, aligned to habitats where possible.
  - Protocol A: self-select plots within a habitat to represent average conditions (avoid highly-supersaturated areas unless representative).
  - Relocation aids: sketches, photos, compass/ruler, GPS (where available) to recover plots in future years.
- Habitat categorization and species lists
  - 28 fine NPMS habitats, grouped into 11 broad categories.
  - For each habitat, a species list is provided; inventory level may record all vascular plants.
- Plot layout and relocation guidance
  - Field sketches with compass directions, permanent features, and photos (up to two per plot) to aid relocation.
  - Photos and sketches uploaded with data; GPS coordinates used as a support tool, not a replacement for notes.

## Survey levels and plot types
- Survey levels
  - Wildflower Level: recording a subset of species.
  - Indicator Level: recording all indicator species; robust data recommended.
  - Inventory Level: Indicator Level plus recording all other vascular plants.
- Plot types
  - Square plots: 5x5 m (10x10 m in woodlands); positioned within habitat areas.
  - Linear plots: 1x25 m; placed along linear features (e.g., hedgerows, margins, rivers); ponds counted as linear plots.
- Ponds and flushes
  - Survey as linear plots; if only one waterbody, survey that feature; if multiple, select accessible ones.

## Recording and data entry
- Recording method
  - Use the relevant NPMS species list for the habitat; conduct intensive surveys starting from a corner and moving outward.
  - For each species: estimate percent cover (Domin scale) within the plot area.
  - Also assess bare ground, litter, bare rock/gravel, and moss/lichen cover.
- Additional information (optional but encouraged)
  - Vegetation height classes, woodedness, aspect, slope, management (e.g., grazing, mowing, ditch clearance) with varying detail and intensity.
  - Tables provide guidance on levels of grazing and management practices.
- Data entry and submission
  - Enter data online at www.npms.org.uk (registration required).
  - If online entry is not possible, data can be posted to the NPMS Volunteer Coordinator.
- Documentation and forms
  - Field guidance, species lists, and monitoring forms provided; forms can be downloaded from the NPMS website.

## Data interpretation and outputs
- Data are intended to support annual reporting on habitat condition and changes in plant communities over time.
- Outputs include NPMS newsletters and peer-reviewed publications; the dataset feeds into national biodiversity indicators.
- Uncertainty, limitations, and assumptions are addressed through review processes and statistical design.

## Access, responsibilities, and governance
- Users must respect countryside access rights and landowner permissions; guidance varies by UK jurisdiction.
- Data governance includes version control, off-site backups, and adherence to project management standards.
- If participants withdraw, plots may be made available to others; ongoing surveying is encouraged to maximize longitudinal value.

## Health and safety
- Participants are responsible for their own safety; check forecasts, avoid unsafe plots (e.g., steep slopes, cliffs, unstable areas).
- Surveyors are advised to work with a partner when possible, carry a mobile phone, a first-aid kit, and wear appropriate clothing and footwear.

## Appendix: Habitat types and Domin scale (highlights)
- Habitat types cover diverse landscapes: arable field margins, bogs and wet heath, broadleaved woodlands, coastal habitats, freshwater systems, heathlands, lowland grasslands, marshes and fens, native pinewood and juniper scrub, rock outcrops and montane habitats, and upland grasslands.
- Domin scale for percent cover and abundance is a 1–10 ordinal scale (with explicit guidance on how to translate cover into percentages for 5x5 m and 10x10 m plots).
- Each habitat has associated target species lists and guidance on when to apply broad vs. fine habitat classifications.

## How to relocate plots (practical notes)
- Provide a field sketch with compass direction and permanent features.
- Mark corners with markers (retractable where possible); note GPS coordinates when available.
- Take up to two photos per plot to assist relocation.

## Summary for analysts
- NPMS provides a structured, volunteer-driven dataset capturing plant abundance and habitat condition across the UK in a standardized, quality-assured framework.
- Data architecture includes locations, sampling events, sample attributes, and species occurrences, with verification via iRecord and automated checks.
- Methods emphasize reproducibility, relocation of plots, and robust habitat-indicator design to detect change and support policy indicators.
- Key challenges include increasing data value through data integration and ensuring broad data accessibility for secondary analyses.