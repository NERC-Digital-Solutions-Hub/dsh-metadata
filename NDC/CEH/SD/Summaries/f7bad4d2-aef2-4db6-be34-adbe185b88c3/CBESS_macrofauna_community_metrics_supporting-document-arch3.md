# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal community metrics - total abundance (TA), total biomass (TB), species richness (SR), evenness (J) and community bioturbation potential (BPc) in mudflat and saltmarsh habitats.

## Overview
- Provides coastal biodiversity and ecosystem service metrics for macrofaunal communities in mudflat and saltmarsh habitats.
- Calculated metrics: total abundance (TA), total biomass (TB), species richness (SR), evenness based on abundance (Jab) and biomass (Jbi), and community bioturbation potential (BPc).

## Data scope and sampling design
- Data derived from 6 sites across 2 locations: Essex and Morecambe Bay.
- Each location includes two habitat types: mudflat and saltmarsh.
- Sampling occurred in winter and summer 2013; no planned repeat sampling.
- 3 replicates across 22 quadrats at 4 spatial scales.

## Locations and habitat descriptions
- Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Saltmarsh sites represent contrasting soil types: clay soils in Essex and sandy soils in Morecambe Bay.
- Essex saltmarsh and Morecambe saltmarsh also differed in inundation frequency, creek structure, and dominant vegetation. Mudflat sites differed in sediment type (Essex: cohesive clays, mud and silt; Morecambe: coarse, mobile sediments).

## Monitoring framework and procedures
- Part of the CBESS field campaign (winter and summer 2013).
- Core sampling and processing conducted per habitat and season.

## Variables and parameters observed
- Abundance-based metrics: Total abundance (TA), Species richness (SR), Evenness based on abundance (jab).
- Biomass-based metrics: Total biomass (TB), Evenness based on biomass (jbi).
- Community bioturbation potential (BPc).

## Field and laboratory methods
- Sampling: 3 cylindrical cores per quadrat (depth 10 cm, diameter 10 cm).
- Fixation: cores fixed in 4% buffered formalin in seawater.
- Processing: cores sieved (0.5 mm); residues preserved in 70% IMS.
- Taxonomic resolution: to species level or major group debris when damaged.
- Abundance data: individuals counted and stored; debris noted as YES/NO.
- Biomass data: individuals weighed to 0.0001 g; if too light, recorded as 0.0001 g.
- Unit conversion: abundance and biomass scaled to per m^2 by multiplying by 127.323955; rounding rules applied accordingly.

## Calculations and data quality
- TA = sum of abundance per m^2; TB = sum of biomass per m^2.
- SR = total number of species per m^2.
- H' max = ln(SR); H' (abundance) and H' (biomass) computed via Shannon-Wiener Index.
- Jab = H' / H'max (abundance-based evenness); Jbi = H' / H'max (biomass-based evenness).
- BPc = sum over species of BPp per m^2; BPp = BPi × Ai, where:
  - Ai = abundance of species i per m^2
  - BPi = sqrt(Bi) × Mi × Ri
  - Bi = biomass of species i per m^2
  - Mi = mobility of species i
  - Ri = reworking activity of species i
- Data checking: raw data input by two people with double-checking; biomass validated against abundance data; metric calculations cross-checked.

## Data formats and field descriptions
- File format: .csv.
- Key fields include:
  - Row Number (sorting), Season (Winter W or Summer S), Location (Morecambe M or Essex E), Site (CS, WS, WP, AH, FW, TM), Habitat (Mudflat MF or Saltmarsh SM), Quadrat Number (1–22), Scale (A-D), Replicate (1–3).
  - Metrics: Total abundance, Total biomass, Species richness, H' max, H' (abundance), Jab, H' (biomass), Jbi, BPc.
- Metric definitions and formulas are provided for reproducibility, including:
  - H' (abundance) = -Σ Pi ln(Pi); Pi = abundance_i / sum(abundance)
  - Jab = H' / H'max; H'max = ln(SR)
  - H' (biomass) and Jbi analogous with biomass values
  - BPc components and conversions described above.

## Data provenance and authors
- Staff responsible for the dataset: Christina Wood and Martin Solan.