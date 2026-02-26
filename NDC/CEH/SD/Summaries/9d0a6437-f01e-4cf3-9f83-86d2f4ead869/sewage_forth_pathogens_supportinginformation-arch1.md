# Data collected for a study looking at the ability of sewage associated plastic waste to act as reservoirs for faecal bacteria, potential human pathogens and genes for antimicrobial resistance

## Purpose and scope
- Investigates whether sewage-associated plastic waste can act as reservoirs for faecal bacteria, potential human pathogens, and genes for antimicrobial resistance.
- Supports UKRI Natural Environment Research Council (NERC) grants related to microbial hitchhikers of marine plastics.

## Data files (10 CSVs) and what they contain
- Water_Background_Sewage_Pathogens.csv: concentrations of bacteria in water at field sites (E. coli, Vibrio, Enterococcus per 25 mL).
- Plastic_Waste_Sewage_Pathogens.csv: weight of plastic collected from different sites.
- Sand_Background_Bacterial_Concentrations_Sewage_Pathogens.csv: bacterial concentrations in sand at each site.
- Wipes_Dry_Weight_Sewage_Pathogens.csv: dry weight of wet wipes collected.
- Sand_Dry_Weight_Sewage_Pathogens.csv: dry weight of sand.
- Seaweed_Dry_Weight_Sewage_Pathogens.csv: dry weight of seaweed.
- Enterococcus_Concentrations_Sewage_Pathogens.csv: Enterococcus concentrations colonising plastic at each site.
- E_coli_Concentrations_Sewage_Pathogens.csv: E. coli concentrations colonising plastic at each site.
- Vibrio_Concentrations_Sewage_Pathogens.csv: Vibrio concentrations colonising plastic at each site.
- Minimum_Inhibitory_Concentrations_Sewage_Pathogens.csv: MIC data for bacteria isolated from plastic; antibiotics tested and concentrations.

## Study locations and timing
- Data collected at multiple field sites along the high-tide strandline (locations indicated by black dots in the original).
- Sewage-associated plastic waste collection occurred in December 2021.
- Site-specific sampling included replicates and site identifiers (Site_Name, Site_Number).

## Sampling design and laboratory methods
- Field sampling:
  - Transect: 100 m × 10 m along the high-tide strandline.
  - All sewage-associated plastic waste within the transect collected into sterile bags.
  - Replicate composite samples: wipes (30 g in 100 mL), cotton buds (four sticks in 20 mL), seaweed (3 g in 20 mL).
- Pre-enrichment:
  - In non-selective LB broth or Vibrio-selective broth (1% peptone, 0.5% Taurocholic acid, 1% NaCl, pH 9.0) at 37 °C, 18 h.
  - For sites with limited material (e.g., <30 g wipes), adjusted to 3 g in 10 mL broth.
- Bacterial isolation and enumeration:
  - Serial dilutions (10^-4 to 10^-7) plated on selective media:
    - MLGA for E. coli, TCBS for Vibrio, SB for intestinal Enterococci.
  - Incubation: MLGA and TCBS at 37 °C for 24 h; SB first at 37 °C for 4 h, then 44 °C for 44 h.
  - Presence/absence determined by colony-forming units (CFUs).
- Minimum Inhibitory Concentrations (MIC):
  - Representative colonies of E. coli, Enterococcus, and Vibrio isolated from seaweed, wipes, and cotton buds.
  - MIC testing against five antibiotics (amoxicillin, ampicillin, streptomycin, cephalexin, tetracycline).
  - Antibiotics tested at ten concentrations spanning 256 to 0.5 µg/mL in two-fold serial dilutions.
  - Growth measured via OD600 after overnight incubation.

## Why the data were collected
- To assess whether sewage-associated plastics serve as reservoirs for bacteria, potential human pathogens, and antimicrobial resistance genes.
- To fulfil grant requirements for the Plastisphere and related projects.

## Data quality, completeness, and governance
- Data checked for anomalies; upper/lower limits examined.
- Missing data are recorded as ND (No Data).
- Some field limitations noted in collection (e.g., variable sample sizes: NP for no plastic, <4 cotton buds at certain sites, fewer sticks at a site).
- Responsibility for data collection and interpretation is not specified in the document.

## Data contents and variable descriptions (summary)
- Site-level data include Site_Name/Site_Number and Replicate (Rep).
- Concentration measurements:
  - Water: E. coli, Vibrio, Enterococcus per 25 mL.
  - Plastic-colonising bacteria: E. coli, Vibrio, Enterococcus per 5 mL, per 1 g (wet weight) and per 100 g (dry weight) where applicable.
  - Sand and wipes: bacterial concentrations and dry weights; moisture changes (before/after drying) and percentage changes.
- Material weights:
  - Wet wipes, dry weight of wipes, sanitary products, cotton bud sticks, total weight collected.
  - Dry weights for sand and seaweed.
- Microbiological presence/absence:
  - CFU data indicating presence (1) or absence (0) for each material type.
- MIC data:
  - For each bacterial species and material, minimum inhibitory concentrations for five antibiotics (amoxicillin, ampicillin, streptomycin, cephalexin, tetracycline) in µg/mL.

## Notes for analysts
- Data can support analyses of correlations between plastic waste weight or dry mass and microbial loads in environmental matrices (water, sand) and on plastics themselves.
- Cross-material comparisons (wipe, seawater, sand) can reveal habitat- or material-specific microbial colonisation patterns.
- MIC data enable investigation of antibiotic resistance patterns across bacteria isolated from different plastics and source materials.
- Remember to account for ND and NP entries and site-specific sampling limitations when performing analyses.