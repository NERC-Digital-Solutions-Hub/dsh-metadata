# Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019

## Overview
- A field experiment to assess how girdling affects soil microarthropod communities under two vegetation types: birch and willow.
- Paired subplots established in 2017; comparisons between girdled and control subplots within birch and willow vegetation.
- Soil fauna sampled in 2019 from litter and mineral soil horizons to quantify taxa counts via extraction and identification.

## Study site and experimental design
- Location: forest-tundra ecotone near the Abisko Scientific Research Station, Sweden (68°18 N, 18°49 E), ~600 m a.s.l.
- Vegetation: mountain birch forest (Betula pubescens ssp czerepanovii) and willow thickets (Salix lapponum).
- Area and layout: 0.88 km² with 5 willow and 6 birch plots; each plot divided into paired sub-plots (e.g., B1-6, W1-5) with similar pre-existing characteristics.
- Girdling treatment: one sub-plot per pair girdled between 12–15 June 2017; birch stems >1 cm diameter girdled with bark removed to the xylem (~30 cm from ground), willow stems girdled ~10–20 cm above ground.
- Post-treatment management: resprouting shoots removed as seen; birch leaves remained in 2018, willow canopies did not leaf out in 2018; willow plots trench-sealed to prevent root intrusion; birch plots not trenched.
- Pre-girdling comparability: Paired t-tests showed no significant differences in key plot characteristics before girdling (tree/stem density, canopy height, soil organic carbon stock, soil C:N, soil CO2 efflux).

## Data collection and variables
- Metadata fields (example): plot, vegetation (birch or willow), treatment (girdled or control), layer (litter or organic soil), soil (dry weight in g).
- Taxa counts (representative list): Oribatida, Prostigmata, Mesostigmata detritivores, Rhagidiidae, Bdellidae, Trombidae, Lepidocyrtus lignorum, Entomobrya nivalis, Isotoma viridis, Isotomidae sp1/sp2, Folsomia quadrioculata (and juveniles), Isotomiella minor, Ceratophysella denticulata, Hypogastrura sp, Parisotoma notabilis, Protaphorura armata, Poduromorpha sp (and juveniles), Mesaphorura sp, Anurida sp, Megalothorax minimus, Dycirtoma fusca, Arrhopalithes sp, Sminthurus nigromaculatus; Diptera, Diptera larvae, Coleoptera larvae; Arachnida; and broader groups (Thysanoptera, Staphylinidae, Coccidae, Annelid, Hymenoptera, Homoptera, Psocoptera).
- Sampling design: three soil cores per plot (4.5 cm diameter) to horizon depth within central 3 × 3 m area; litter horizon pooled per plot.
- Extraction and processing: fauna extracted with a Tullgren funnel for 10 days, then dried at 70°C for 24 hours; preserved in 70% ethanol; identified under a dissecting microscope (Collembola to species level per Hopkin 2007; Acari to order level; others to higher taxonomic levels).
- Sampling date: July 29, 2019.
- Dataset reference: Primetime_Abisko_2019_Mesofauna.csv (with corresponding metadata describing plots, vegetation, treatment, layer, and counts).

## Data structure and content (for analysis)
- Structure supports comparing girdled vs. control within and across birch and willow vegetation.
- Separate litter and soil layers enable vertical distribution analyses of fauna.
- Quantitative counts across a wide range of microarthropod taxa allow diversity and abundance analyses, as well as multivariate community assessments.

## Analysis considerations and data quality
- Paired design facilitates pre- vs post-girdling comparisons within vegetation types.
- Standardized sampling and extraction protocol reduces methodological bias across plots.
- Taxonomic resolution varies by group (species-level for Collembola, order-level for Acari, higher for others); plan accordingly for analyses requiring uniform taxonomic granularity.
- Data quality relies on accurate linking of sample IDs to plots, treatments, layers, and date; ensure consistent metadata integration.

## Practical guidance for analysts
- Potential analyses: mixed-effects models to test effects of vegetation type, girdling, and their interaction on fauna counts; layer-specific models for litter vs soil; multivariate analyses (e.g., NMDS/CCA) to explore community composition changes.
- Key predictors: plot, vegetation, treatment, layer, soil dry weight.
- Response variables: counts per taxa (both individual taxa and aggregated groups), with attention to zero-inflation and dispersion.
- Data cleaning steps: harmonize taxon names, verify sample-to-plot mappings, handle missing values, and align with pre-girdling context if available.