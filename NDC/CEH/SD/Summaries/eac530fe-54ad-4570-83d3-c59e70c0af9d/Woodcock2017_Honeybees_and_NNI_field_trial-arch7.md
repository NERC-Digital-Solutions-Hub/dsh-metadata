# Data describing population responses of honeybees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Multi-country field study examining effects of three neonicotinoid seed treatments (clothianidin, thiamethoxam, and a control) on wild pollinators, focusing on honeybees (Apis mellifera).
- Datasets linked to the Science 2017 paper by Woodcock et al.; expanded with individual hive-level information.
- Data describe EFSA primary endpoints (colony strength, overwintering success) and secondary endpoints, plus neonicotinoid exposure via pollen/nectar, diseases, foraging, and landscape context.

## Experimental design and sampling
- 33 commercial oilseed rape sites: UK (12), Hungary (12), Germany (9).
- Large continuous crop blocks (~63 ha avg); sites grouped into blocks (three sites per block) with randomised treatment within each block; blocks separated by >10 km.
- Six honeybee hives per site placed centrally to crop; hives later moved to country-specific overwintering sites.
- Flowering period Apr–Jun 2015; assessments during flowering (4–7 day intervals) and again post-winter (Mar 2016).
- Median values across six hives per site used for many analyses to address non-independence among hives.

## Data collection and endpoints
- Colony metrics via Liebefeld counts: worker bees, eggs, larvae, pupae, brood stages, nectar/pollen storage; overall colony strength and overwintering status.
- Disease and health covariates: Nosema spp., Varroa mite infestation, and assorted disease loadings; sampled pre-exposure, during exposure, and post-exposure.
- Foraging and pollen analyses: pollen traps to assess foraging breadth; pollen grain identification to OSR and other taxa; plant taxon richness and Shannon diversity.
- Considerations of hive weight and timing of sampling to capture peak responses.

## Residue and exposure analyses
- Neonicotinoid residues measured in pollen and nectar from free-flying bees and in crop-exposed samples.
- Target compounds: clothianidin, thiamethoxam, and imidacloprid (not applied in study but detected in soils); residue quantification with ISO-accredited methods; LoQ ~0.53 ng/g.
- Derived composite exposure metric: nnI (neonicotinoid index) adjusted using LD50 values to combine TMX, CTD, and IMI toxicity.
- Crop-expression assessment using caged honeybee colonies to collect pollen/nectar directly from treated vs. control crops; day 2 and day 9 sampling; recognition of potential crop depletion effects.

## Landscape context
- Within a 1.5 km radius of each hive: land parcels classified into crops (including OSR), cereals, legumes, vegetables, grassland, woodland, scrub, water, urban.
- Landscape metrics include broadleaf cover, semi-grass cover, urban cover, arable share, OSR share, and OSR pollen-grain abundance.

## Datasets and metadata
- apis_median.csv: site-level medians (six hives per site) with country, site, block, treatment, sampling dates, hive metrics, overwintering results, disease metrics, foraging/pollen data, landscape context, and residue metrics; end values rounded to whole numbers.
- apis_allhives.csv: all-hive data (six hives per site) with detailed per-hive measurements, dates, weights, brood and foraging metrics, and disease metrics.
- apis_tent.csv: residue expression data from crop-tent experiments; includes ctd, tmx, imi concentrations in nectar/pollen collected in tunnels; event counts and sampling details; days 2 and 9.
- trial metadata: descriptive fields for each dataset, including treatment, country, site, hive, block, dates, exposure days, and sample counts.

## GIS-ready attributes and usage
- Spatial linkage: site locations, block structure, and central hive placements enable map-based visualization of treatment effects and landscape context.
- Landscape layering: ready-to-map land-use classes and landscape metrics around hives (1.5 km radius) for spatial analyses.
- Multiscale data: integrates site-level summaries with hive-level measurements and detailed residue data for spatially explicit modeling of exposure and responses.

## Data quality, limitations, and notes
- Some imbalance and missingness due to logistical constraints (e.g., crop depletion in tent experiments; incomplete hive counts at some sites).
- Within-site hive data not fully independent; median hive values used to mitigate drift between hives.
- Deployed index nnI is LD50-corrected and should be interpreted as a toxicity-adjusted exposure metric rather than a direct concentration.
- Temporal alignment varies by country with flowering windows differing slightly between sites.

## Propriety and provenance
- Funded by Syngenta Ltd. and Bayer CropScience; dataset extends the referenced 2017 Science paper.
- Data collection and analysis carried out across the UK, Hungary, and Germany with standardized methods (Liebefeld, residue analyses, pollen/grain analysis, disease assays).

## Potential applications for GIS Specialists
- Map site-level colony outcomes by treatment and country to identify spatial patterns.
- Overlay landscape context with residue exposure and colony health metrics to explore habitat-pesticide interactions.
- Visualize temporal dynamics of colony strength and overwintering success across sites and blocks.
- Integrate residue data with foraging and pollen diversity layers for habitat quality assessments.