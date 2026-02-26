# What has been recorded and what form does the data take?

## Overview and study context
- Data originate from a study examining whether sewage-associated plastic waste acts as reservoirs for faecal bacteria, potential human pathogens, and antimicrobial resistance genes.
- Tied to UKRI NERC grants: "Microbial hitchhikers of marine plastics: the survival, persistence & ecology of microbial communities in the Plastisphere" and the SPACES project.
- The dataset comprises multiple CSV files capturing various biological and chemical measurements across field sites.

## Data collection locations and timing
- Data collected in December 2021.
- Locations are indicated by black dots (geographic context provided visually, not in the text).

## Sampling and laboratory methods
- Field sampling: At each site, a transect of 100 m × 10 m along the high-tide strandline was surveyed; all sewage-associated plastic waste within the transect was collected into sterile bags.
- Replicate composite samples for wipes, cotton bud sticks, and seaweed were pre-enriched in non-selective LB broth or Vibrio-selective broth (37 °C, 18 h).
- Post-enrichment, samples were serially diluted and plated on selective media:
  - E. coli: MLGA
  - Vibrio: TCBS
  - Intestinal Enterococci: SB
- CFUs were enumerated to determine target bacteria concentrations.
- Minimum Inhibitory Concentrations (MIC): Representative colonies of E. coli, Enterococcus, and Vibrio were tested against five antibiotics (amoxicillin, ampicillin, streptomycin, cephalexin, tetracycline) across ten concentrations (256 mg/L to 0.5 mg/L) to assess resistance.

## Data files and contents
- Water_Background_Sewage_Pathogens.csv
  - Concentrations of bacteria in water at field sites
  - Variables include: Site, Rep, E.coli_CFU_per_25ml, Vibrio_CFU_per_25ml, Enterococcus_CFU_per_25ml
  - ND indicates no data
- Plastic_Waste_Sewage_Pathogens.csv
  - Data on the weight of plastic collected at each site
  - NP indicates no plastic collected
- Sand_Background_Bacterial_Concentrations_Sewage_Pathogens.csv
  - Bacterial concentrations in sand at each site
- Wipes_Dry_Weight_Sewage_Pathogens.csv
  - Dry weight of the wet wipes
- Sand_Dry_Weight_Sewage_Pathogens.csv
  - Dry weight of the sand
- Seaweed_Dry_Weight_Sewage_Pathogens.csv
  - Dry weight of seaweed
- Enterococcus_Concentrations_Sewage_Pathogens.csv
  - Concentrations of Enterococcus on plastic at each site
- E_coli_Concentrations_Sewage_Pathogens.csv
  - Concentrations of E. coli on plastic at each site
- Vibrio_Concentrations_Sewage_Pathogens.csv
  - Concentrations of Vibrio on plastic at each site
- Minimum_Inhibitory_Concentrations_Sewage_Pathogens.csv
  - MIC data for bacteria isolated from plastic
  - Includes per-site/replicate MIC values for Amoxicillin, Ampicillin, Streptomycin, Cephalexin, Tetracycline (µg/mL)
  - Also includes CFU presence/absence indicators for bacteria and related material metrics (e.g., weights)

## Data completeness and quality
- Data were checked for anomalous values and bounded by upper/lower limits.
- Missing data are recorded as 'ND'.

## GIS and data integration considerations
- The dataset is site-based with multiple matrices (water, sand, wipes, seaweed, and plastic-associated bacteria), suitable for spatial analysis and mapping of pathogen presence and resistance patterns.
- Units vary by file (CFU per volume/weight, grams, etc.), and ND values exist; careful unit harmonization and metadata interpretation are required when integrating datasets.
- Some data describe physical weights (dry/wet weights) and others describe microbial concentrations, enabling multi-factor spatial visualization (e.g., pathogen load vs. material type).
- Data provenance on responsibilities and exact site coordinates is limited in the text; integrating with GIS would require linking site identifiers to spatial coordinates.