# What has been recorded and what form does the data take?

## Overview
- Study aim: examine whether sewage-associated plastic waste acts as reservoirs for faecal bacteria, potential human pathogens, and antimicrobial resistance genes.
- Data comprises ten CSV files, each describing different aspects of samples collected from field sites.
- Data collection occurred in December 2021, with site locations indicated by black dots.
- Data completeness notes: missing data flagged as ND where applicable; some samples had incomplete components (e.g., cotton bud sticks at certain sites).

## Data holdings (files and purposes)
- Water_Background_Sewage_Pathogens.csv
  - Concentrations of bacteria in water at field sites (E. coli, Vibrio, Enterococcus) per 25 ml.
- Plastic_Waste_Sewage_Pathogens.csv
  - Weight of plastic collected from different sites; NP indicates no plastic collected.
- Sand_Background_Bacterial_Concentrations_Sewage_Pathogens.csv
  - Bacterial concentrations in sand at each site.
- Wipes_Dry_Weight_Sewage_Pathogens.csv
  - Dry weight of wet wipes collected at sites.
- Sand_Dry_Weight_Sewage_Pathogens.csv
  - Dry weight of sand collected at sites.
- Seaweed_Dry_Weight_Sewage_Pathogens.csv
  - Dry weight of seaweed collected at sites.
- Enterococcus_Concentrations_Sewage_Pathogens.csv
  - Concentrations of Enterococcus on plastic at each site.
- E_coli_Concentrations_Sewage_Pathogens.csv
  - Concentrations of E. coli on plastic at each site.
- Vibrio_Concentrations_Sewage_Pathogens.csv
  - Concentrations of Vibrio on plastic at each site.
- Minimum_Inhibitory_Concentrations_Sewage_Pathogens.csv
  - MIC data for bacteria isolated from plastic (E. coli, Enterococcus, Vibrio) against five antibiotics.

## Data collection context
- Location: sites indicated by black dots (exact coordinates not provided in text).
- Time: December 2021 for sewage-associated plastic waste collection.
- Sampling method:
  - Field transect: 100 m × 10 m along high-tide strandline; all sewage-associated plastic waste within transect collected.
  - Replicate composites: wipes (30 g in 100 mL), cotton bud sticks (four sticks in 20 mL), seaweed (3 g in 20 mL) per site.
  - Pre-enrichment: LB broth or Vibrio selective broth incubated at 37 °C for 18 h.
  - If material was limited (e.g., S2-4 wipes), adjustments were made (3 g wipes in 10 mL broth).
  - Post-enrichment: serial dilutions (10^-4 to 10^-7) plated on selective media (MLGA for E. coli, TCBS for Vibrio, SB for Enterococci); incubated as specified.
  - CFU presence/absence determined by colony counts.
- MIC protocol:
  - Isolated colonies from seaweed, wipes, and cotton buds were grown, then subjected to MIC testing against five antibiotics (amoxicillin, ampicillin, streptomycin, cephalexin, tetracycline).
  - Antibiotics tested in two-fold dilutions (256 μg/mL to 0.5 μg/mL) in LB broth in 96-well plates; cultures adjusted to OD600 0.1; incubated at 37 °C.

## Purpose and grants
- Primary purpose: understand whether plastics in sewage contexts harbor faecal bacteria, pathogens, and antimicrobial resistance.
- Compliance with funding: satisfies requirements of UKRI-NERC grants related to microbial hitchhikers on marine plastics (NE/S005196/1) and the SPACES project (NE/V005847/1).

## Data provenance and responsibility
- Section 6 (Who was responsible) is not filled in the document; responsibility for collection and interpretation is not specified.
- Completeness and quality notes:
  - Data checked for anomalies; ND denotes no data for missing values.
  - Documentation provides variable descriptions and units for each file, enabling cross-file interpretation.

## Data contents and column conventions
- Cross-file structure includes:
  - Site_name or Site_Number and Replicate identifiers.
  - Concentration measurements (CFU per various units: per 25 mL, per 5 mL, per 1 g, etc.) for E. coli, Vibrio, and Enterococcus.
  - Weights (wet/dry) for wipes, sand, seaweed, sanitary products, and cotton buds; total weights and moisture-change metrics where applicable.
  - MIC data organized by antibiotic with concentration units (μg/mL) and presence/absence of CFU for each material type.
- Notes on data interpretation:
  - ND indicates no data for a given measurement.
  - NP indicates no plastic collected at a site for plastic-weight related data.

## Governance and next steps for Data Stewards
- Key governance gaps to address:
  - Identify data owner/point of contact for responsibility (Section 6 missing).
  - Document data licensing and access permissions for reuse.
  - Capture precise site coordinates or geolocation metadata to enable discoverability.
  - Standardize column naming across files to facilitate integration (e.g., site identifiers, replicate conventions).
  - Ensure consistent units and documentation for all measurements to aid interoperability.
- Data stewardship actions:
  - Assign data steward and metadata schema to accompany the ten CSVs.
  - Prepare a data dictionary linking all files, with crosswalks for site identifiers and replication.
  - Archive data with provenance notes (collection date, methods, processing steps) and validation checks (ND entries, anomaly flags).