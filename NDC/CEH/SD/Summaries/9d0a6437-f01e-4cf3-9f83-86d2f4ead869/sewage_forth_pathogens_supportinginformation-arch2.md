# Data collected for the study looking at the ability of sewage associated plastic waste to act as reservoirs for faecal bacteria, potential human pathogens and genes for antimicrobial resistance

## Overview
- A dataset from a study examining whether sewage-associated plastic waste acts as reservoirs for faecal bacteria, potential human pathogens, and antimicrobial resistance genes.
- Ten CSV files capture various biological, chemical, and physical measurements from field samples collected in December 2021.
- Data quality checks noted: anomalous values reviewed; missing data marked as ND.

## Study location and timing
- Data collected at multiple field sites along transects defined by black dots on a map.
- Sampling period: December 2021.

## Sampling design and data collection methods
- Field sampling:
  - At each site, a transect of 100 m x 10 m along the high-tide strandline was established.
  - All sewage-associated plastic waste within the transect was collected into sterile zip-lock bags.
  - Replicate composite samples were prepared for wipes (30 g in 100 mL), cotton bud sticks (four sticks in 20 mL), and seaweed (3 g in 20 mL).
- Laboratory processing:
  - Pre-enrichment in non-selective LB broth or Vibrio-selective broth at 37 °C for 18 h.
  - Serial dilutions in PBS (10^-4 to 10^-7) plated on selective media (MLGA for E. coli, TCBS for Vibrio, SB for intestinal enterococci).
  - Incubation times: MLGA and TCBS at 37 °C for 24 h; SB at 37 °C for 4 h then 44 °C for 44 h.
  - CFU enumeration to determine presence/absence of target bacteria on plastic waste.
- Antimicrobial resistance testing (MIC):
  - Representative colonies of E. coli, Enterococcus, and Vibrio from seaweed, wipes, and cotton buds were tested.
  - Five antibiotics examined: amoxicillin, ampicillin, streptomycin, cephalexin, tetracycline (ten concentrations from 256 mg/L to 0.5 mg/L).
  - MIC testing performed in LB broth in 96-well plates with optical density adjusted to OD600 of 0.1.

## Purpose and funding context
- Primary aim: assess whether sewage-associated plastic waste can harbor faecal bacteria, human pathogens, and antimicrobial resistance genes.
- Funding and grants: UKRI NERC grants for “Microbial hitchhikers of marine plastics: the survival, persistence & ecology of microbial communities in the 'Plastisphere'” (NE/S005196/1) and the NERC-GCRF SPACES project (NE/V005847/1).

## Data management and responsibility
- Section on who was responsible for data collection and interpretation is not provided in the document.
- Data storage and portal submission are implied as standard practice, with an emphasis on ensuring datasets are stored and uploaded to appropriate portals.

## Data completeness and quality notes
- Data checked for anomalies; upper and lower bounds reviewed.
- ND indicates missing data in the records.

## Data files and what they contain
- Water_Background_Sewage_Pathogens
  - Concentrations of bacteria in water at field sites.
  - Variables include E. coli, Vibrio, and Enterococcus CFU per 25 mL.
- Plastic_Waste_Sewage_Pathogens
  - Data on the weight of plastic collected from the sites.
  - NP indicates no plastic collected.
- Sand_Background_Bacterial_Concentrations_Sewage_Pathogens
  - Bacterial concentrations in sand at each site.
- Wipes_Dry_Weight_Sewage_Pathogens
  - Dry weight of the wet wipes collected.
- Sand_Dry_Weight_Sewage_Pathogens
  - Dry weight of sand collected.
- Seaweed_Dry_Weight_Sewage_Pathogens
  - Dry weight of seaweed collected.
- Enterococcus_Concentrations_Sewage_Pathogens
  - Concentrations of Enterococcus on plastic at each site.
- E_coli_Concentrations_Sewage_Pathogens
  - Concentrations of E. coli on plastic at each site.
- Vibrio_Concentrations_Sewage_Pathogens
  - Concentrations of Vibrio on plastic at each site.
- Minimum_Inhibitory_Concentrations_Sewage_Pathogens
  - MIC data for bacteria isolated from plastic (E. coli, Enterococcus, Vibrio) against antibiotics.
  - Antibiotics measured: Amoxicillin, Ampicillin, Streptomycin, Cephalexin, Tetracycline.
  - MIC values reported as µg/mL, with per-site replicate (Rep) details and CFU presence/absence data in related columns.

## Variable and data structure highlights
- Site and replicate identifiers are included across datasets.
- Concentration measurements expressed as CFU per defined sampling unit (per 25 mL, per 5 mL, per 1 g, etc.) or weight measurements in grams.
- Presence/absence data captured as CFU (1 = present, 0 = absent) in MIC-related datasets.
- Unit descriptions and data columns explicitly defined to support standardised interpretation and cross-dataset integration.