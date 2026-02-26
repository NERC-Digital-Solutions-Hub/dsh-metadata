# What has been recorded and what form does the data take?

- Study goal: examine whether sewage-associated plastic waste acts as reservoirs for faecal bacteria, potential human pathogens, and antimicrobial resistance genes.
- Data scope: ten CSV files containing concentrations of bacteria, weights of plastic-related materials, and antibiotic resistance data; linked to UKRI/NERC grants on microbial hitchhikers of marine plastics.
- Data collection timing: December 2021.
- Data collection location: sites indicated by black dots; transect-based sampling along the high-tide strandline (100 m × 10 m).

## What was collected and how it is structured

- Sample collection approach:
  - Transect (100 m × 10 m) along the high-tide strandline; all sewage-associated plastic waste within the transect collected.
  - Replicate composite samples from each site: wipes (30 g in 100 mL), cotton bud sticks (four sticks in 20 mL), seaweed (3 g in 20 mL).
  - Pre-enrichment in LB broth or Vibrio-selective broth; incubated at 37 °C, then serial dilutions plated on selective media.
  - Target organisms: E. coli (MLGA), Vibrio (TCBS), Enterococcus (SB).
  - CFU enumeration to determine presence/absence of target bacteria on plastic waste samples.
- Antibiotic resistance testing (MIC):
  - Bacteria isolated from seaweed, wipes, and cotton buds tested for resistance to five antibiotics (amoxicillin, ampicillin, streptomycin, cephalexin, tetracycline).
  - MICs determined using two-fold dilutions (256 mg/L to 0.5 mg/L) in LB broth; OD600 read after incubation.
- Data completeness:
  - Missing data labeled as ND; some samples had varying quantities of wipes or cotton buds (noted in the method).

## What each data file contains (data file contents)

- Water_Background_Sewage_Pathogens: concentrations of bacteria in water at each site; CFU per 25 mL for E. coli, Vibrio, and Enterococcus.
- Plastic_Waste_Sewage_Pathogens: data on the weight of plastic collected per site.
- Sand_Background_Bacterial_Concentrations_Sewage_Pathogens: bacterial concentrations in sand at each site.
- Wipes_Dry_Weight_Sewage_Pathogens: dry weight of the wet wipes collected.
- Sand_Dry_Weight_Sewage_Pathogens: dry weight of the sand collected.
- Seaweed_Dry_Weight_Sewage_Pathogens: dry weight of seaweed collected.
- Enterococcus_Concentrations_Sewage_Pathogens: concentrations of Enterococcus on plastic at each site.
- E_coli_Concentrations_Sewage_Pathogens: concentrations of E. coli on plastic at each site.
- Vibrio_Concentrations_Sewage_Pathogens: concentrations of Vibrio on plastic at each site.
- Minimum_Inhibitory_Concentrations_Sewage_Pathogens: MIC values for bacteria isolated from plastic for multiple antibiotics; includes site, replicate, CFU presence/absence data, and MICs (µg/mL) for Amoxicillin, Ampicillin, Streptomycin, Cephalexin, Tetracycline.

## Data structure details and variable examples

- Site and replication: Site_Name/Site_Number; Rep (replicate).
- Bacterial concentrations: CFU per 25 mL (water), per 5 mL (some water/measurements), per 1 g (wet wipe), per 100 g (dry weight), and presence/absence (CFU = 1/0) for specific materials.
- Material weights: Wet weight (g) and Dry weight (g) for wipes, sand, seaweed, and sanitary materials; moisture-change metrics where applicable.
- MIC data: Minimum inhibitory concentrations for each bacteria-antibiotic pair (µg/mL).

## Data quality and provenance

- Data checked for anomalies; ND indicates missing data.
- NP indicates no plastic collected for a given sample.

## Responsibility

- The document includes a section for responsibility but does not specify individuals or teams responsible for data collection and interpretation.

## How this aligns with data support practice

- Rich, multi-sensor dataset enabling cross-cutting analysis:
  - Link CFU data with material type and site context to assess contamination risk across environments.
  - Combine concentrations (water, sand, wipes, seaweed) with plastic waste weights to understand reservoir potential.
  - Integrate MIC results with CFU/matrix data to explore antimicrobial resistance patterns by site and material.
- Data product opportunities (self-serve tools):
  - Dashboards showing site-level contamination by material and organism.
  - Maps of sampling sites with associated CFU densities and MIC profiles.
  - Reports comparing pre- and post-enrichment or drying metrics for wipes/sand/seaweed.
- Data quality considerations:
  - Standardize units; handle ND/NP consistently.
  - Document site metadata and data provenance for reproducibility.
  - Consider audience needs for simplifying complex microbiology results into clear visualizations.

## Gaps and notes for users

- The document does not specify who was responsible for data collection and interpretation.
- Some sites had incomplete representative samples (e.g., fewer wipes or sticks); note variability when analyzing across sites.
- The exact spatial distribution of the sampling sites is indicated by black dots but not enumerated here; users may want to align site codes with a map.