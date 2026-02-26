# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal community metrics - total abundance (TA), total biomass (TB), species richness (SR), evenness (J) and community bioturbation potential (BPc) in mudflat and saltmarsh habitats.

- Overview
  - Dataset capturing macrofaunal community metrics: TA, TB, SR, J (abundance-based and biomass-based), and BPc in mudflat and saltmarsh habitats.
  - Derived from CBESS field campaign in 2013 across multiple sites and habitats, to support environmental monitoring and policy-relevant assessments.

- Study design and scope
  - Sites and locations: 6 sites across 2 locations (Essex and Morecambe Bay).
  - Habitats: mudflat and saltmarsh at each location.
  - Sampling period: winter and summer 2013.
  - Replication and scales: 3 replicates across 22 quadrats at 4 spatial scales (A–D).
  - Staff: Christina Wood and Martin Solan.

- Locations and habitat context
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Habitat contrasts:
    - Saltmarsh: three sites with clay soils (Essex) and three with sandy soils (Morecambe Bay).
    - Mudflat: Essex (cohesive clays, mud and silt) vs Morecambe Bay (coarser, mobile sediments).
  - Broader environmental context: Essex and Morecambe Bay saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation.

- Variables and metrics
  - Observed metrics: Total abundance (TA), Total biomass (TB), Species richness (SR), Evenness based on abundance (J_abundance), Evenness based on biomass (J_biomass), Community bioturbation potential (BPc).
  - Definitions aligned to per square metre (m^2) basis.

- Field and laboratory methods
  - Sample collection: 3 cylindrical cores per quadrat (10 cm depth, 10 cm diameter).
  - Preservation: fixed in 4% buffered formalin in seawater; residues preserved in 70% Industrial Methylated Spirit (IMS).
  - Processing: sieved (0.5 mm); sorted to species or major debris; remaining material stored for reference.
  - Abundance: counted individuals per species; decimals not used; damaged parts grouped as major debris with presence noted.
  - Biomass: individuals weighed to 0.0001 g after blotting; for very small specimens, a 0.0001 g placeholder used.
  - Scaling: results converted to per m^2 using a factor of 127.323955.

- Data processing and metrics calculation
  - TA: sum of abundance per m^2.
  - TB: sum of biomass per m^2.
  - SR: total number of species per m^2.
  - J_abundance: Pielou’s evenness based on abundance (H'/H'max); H' is Shannon-Wiener from abundance, H'max = ln(SR).
  - J_biomass: Pielou’s evenness based on biomass (H'/H'max) using biomass values.
  - BPc: BPc = sum of BPp per m^2; BPp = BPi × Ai where BPi = √Bi × Mi × Ri; Ai = abundance per m^2; Bi = biomass per m^2; Mi = mobility; Ri = reworking.

- Data quality, checks, and validation
  - Data entry: two-person input with cross-check.
  - Biomass consistency: cross-checked against abundance data (CBESS_macrofauna_abundance.csv) to ensure value alignment.
  - Calculations: metrics recalculated and double-checked.

- Data formats and access
  - File format: CSV.
  - Metadata: includes dataset field descriptions (sorting row numbers, seasons, locations, sites, habitats, scales, replicates, and metric definitions).

- Additional notes
  - Location and habitat descriptors provided to support comparative analyses.
  - NA indicators used where data are missing or not applicable.