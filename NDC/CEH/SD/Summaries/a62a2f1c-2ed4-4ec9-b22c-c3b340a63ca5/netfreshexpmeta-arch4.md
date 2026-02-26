# Overview A dataset of stable isotope concentrations (  13 C or  15 N) and community abundance data for stream macroinvertebrate taxa measured during a mesocosm drought experiment at the Llyn Brianne Experimental Observatory, Wales, UK.

## Data Purpose and Scope
- Dataset combines stable isotope concentrations (δ13C and δ15N) with macroinvertebrate community abundance.
- Collected to understand how communities and diets respond to habitat and food availability changes during a hydrological drought.

## Experimental Design
- Location: Llyn Brianne Stream Observatory, Wales, UK.
- Experimental setup: Four mesocosm blocks (Carpenter, Davies, Hanwell, Sidaway) with three channels per block fed by four upland streams.
- Treatments (BACI framework): 100% baseflow (control), 50% baseflow, 10% baseflow.
- Timeline: Sampling before drought (T0, 20 July 2023), during drought (T1, ~30 days), after drought (T3, ~40 days post-recovery).
- Replication: Random block design; nine replicate samples per channel per time point (three segments × three channels per block).

## Sampling and Processing
- Macroinvertebrates collected with Hess samplers (165 cm2, 500 μm mesh).
- Sampling at each time point: nine replicates per channel (six preserved in ethanol for taxonomy and isotopes; three kept in channel outflows for gut depuration before isotope analysis).
- Lifecycle: 216 samples collected across the study.
- Taxonomic treatment: Identified to family level; Chironomidae split into two morphotaxa (filterers and predators).

## Stable Isotope Analysis
- Sample preparation: depuration of gut contents, then freeze-drying and homogenization.
- Measurement: δ13C and δ15N via elemental analyzer (EA 1112) interfaced with an IRMS.
- Standards: USGS40 and USGS41a for δ13C and δ15N; USGS40 also used for total C and total N references.
- Quality control: long-term precision reported for standard materials; data processing with Isodat 2.0.

## Data Structure and Files
- Two primary CSV files with replicates as rows:
  - netfreshexpcomm.csv: Macroinvertebrate community data.
    - Key columns: Site (mesocosm block), Treatment (flow level), Time (Before, During, After), Segment (1–9), Taxon (family-level taxa).
  - netfreshexpsi.csv: Stable isotope data.
    - Key columns: Site, Treatment, Time, Taxon (taxon from which isotopes were measured).
- Column explanations provided in the dataset documentation (e.g., stream codes Ll3, Ll6, Ll7, Ll8 mapped to Hanwell, Carpenter, Davies, Sidaway).

## Location, Environment, and Context
- Streams feeding mesocosms varied in pH (Ll6/Ll7 near neutral 6.8–7.2; Ll3/Ll8 acidic 5.3–5.8).
- Mesocosm channels: three cobble substrate channels per block, each ~20 m long, with ~1 L/s baseflow.
- Discharge manipulation based on stage-discharge curves; flow monitored and adjusted to maintain treatments.

## Data Quality, Provenance, and Standards
- Taxonomic references and keys cited for identification.
- Stable isotope methodology and reference materials clearly documented.
- Data stored under a structured format with explicit metadata for discoverability and reuse.
- Provenance tied to the NETFRESH project (NE/X010597/1).

## Potential Applications for Data Leaders
- Evaluate data strategy for environmental monitoring: integration of community abundance with trophic chemistry.
- Assess data discoverability and metadata completeness across dual data modalities (taxonomy/abundance and isotopes).
- Support data quality planning, standardization, and documentation practices across multi-method datasets.
- Enable cross-site or cross-study synthesis on drought impacts, using clear data structures and reproducible processing pipelines.