# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) individual bioturbation potential in mudflat and saltmarsh habitats.

## Summary
- purpose: document an environmental monitoring dataset measuring individual bioturbation potential (BPi) across mudflat and saltmarsh habitats within the CBESS program.
- outputs: per-species BPi values aggregated to site, habitat, quadrat, and scale; enables assessment of sediment bioturbation activity and potential ecosystem function.
- data provenance: derived from 6 sites across 2 locations (Essex and Morecambe Bay), each with 2 habitat types (mudflat and saltmarsh), sampled in winter and summer 2013.
- spatial/temporal coverage: 22 quadrats sampled across 4 spatial scales; winter and summer surveys conducted as part of the CBESS field campaign; no planned repeats beyond the 2013 campaign.
- data quality and governance: collected by trained staff (Christina Wood & Martin Solan); two-person data entry with cross-checks against biomass and abundance; calculations double-checked; data stored as CSV and intended for upload to appropriate data portals.

## Dataset scope and locations
- dataset name: CBESS – individual bioturbation potential (BPi) in mudflat and saltmarsh habitats.
- study sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands); a total of 6 sites.
- habitat types: mudflat (cohesive clays, mud and silt in Essex; coarse, mobile sediments in Morecambe), and saltmarsh (two contrasting soil types: clay in Essex; sandy in Morecambe).
- site descriptions also note differences in inundation frequency, creek structure, and dominant vegetation between regions.

## Sampling, timing, and design
- sampling frame: general CBESS field campaign conducted in winter and summer 2013.
- replication and scale: 3 replicates per quadrat; 22 quadrats total across 4 spatial scales (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100 m–upper limit).
- habitats and quadrats: per habitat per site, quadrats were sampled to capture spatial heterogeneity.

## Measurements and data processes
- primary variable: individual bioturbation potential (BPi) per species.
- field/lab procedures:
  - collect 3 cylindrical sediment cores (10 cm depth, 10 cm diameter) per quadrat; fix in 4% buffered formalin in seawater.
  - sieve cores (0.5 mm); identify organisms to species level; count individuals.
  - biomass: blot individuals on tissue to remove excess preservative; weigh to 0.0001 g; apply a minimum weight of 0.0001 g if needed.
  - convert abundance and biomass to units of per square meter using a calibration factor.
- data derivation:
  - BPi = (sqrt Bi) × Mi × Ri for each species, where Bi = biomass, Mi = mobility, Ri = reworking.
  - BPc = sum of BPp (BPp = BPi × Ai) for all species per square meter, where Ai = species abundance per m².
- species observed: numerous macrofauna and meiofauna taxa typical of mudflat and saltmarsh ecosystems (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Mytilus edulis juveniles, and many others listed in the dataset field descriptions).

## Data quality, documentation, and formats
- data validation: raw data entered by two people; cross-checked with biomass-abundance consistency (CBESS_macrofauna_abundance.csv); calculations of BPi and BPc double-checked.
- data format: primarily CSV files.
- metadata: includes detailed field descriptions (season, site, habitat, quadrat, scale, measurement type) and per-species BPi entries to enable re-use and re-analysis.

## Roles, access, and reuse
- personnel: Christina Wood and Martin Solan responsible for dataset collection and processing.
- data accessibility: dataset prepared for upload to data portals; under CBESS governance to enable broader access and reuse.
- reuse considerations: standardized methods and explicit calculations (BPi and BPc) support cross-study comparisons and integration with other environmental monitoring datasets; potential for coupling with other environmental data to enhance ecosystem service assessments.

## Notable considerations for analysts
- dataset represents a snapshot from 2013; planned to be non-repeated within this campaign, which may limit temporal trend analyses but provides robust spatially distributed bioturbation indicators.
- habitat contrast (Essex vs. Morecambe Bay) offers opportunities to examine how sediment type, inundation, and vegetation influence bioturbation potential.
- comprehensive per-species data enables detailed cross-species contributions to overall bioturbation, supporting nuanced ecological interpretations and potential integration with environmental health metrics.