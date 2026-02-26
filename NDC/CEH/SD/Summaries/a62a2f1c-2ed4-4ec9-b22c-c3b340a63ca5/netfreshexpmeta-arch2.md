# Overview A dataset of stable isotope concentrations (δ13C or δ15N) and community abundance data for stream macroinvertebrate taxa measured during a mesocosm drought experiment at the Llyn Brianne Experimental Observatory, Wales, UK

## Aim
- Document how stream macroinvertebrate communities and their trophic diets respond to habitat and food availability changes during a hydrological drought.
- Provide data in a consistent format to enable scrutiny of environmental health and policy performance over time.

## Study setting and design
- Four mesocosm blocks at the Llyn Brianne Stream Observatory (Carpenter, Davies, Hanwell, Sidaway) fed by four upland streams; blocks differ in pH (two circumneutral, two acidic).
- Each block contains three cobble-channel mesocosms (20 m × 0.2 m × 0.2 m) with about 2 m s-1 average channel flow and 1 L s-1 baseflow.
- Drought treatments: 100% baseflow (control), 50%, and 10% baseflow, applied in a random block design under a Before-After-Control-Impact (BACI) framework.
- Sampling schedule: Before the drought (T0, 20 July 2023), During the drought (T1, ~30 days later, 24 August 2023), After recovery (T3, ~40 days after recovery, 9 October 2023). Each sampling period included a “Before,” “During,” and “After” phase for different analyses.
- Replication: Nine Hess-sampler replicate samples per channel at each time point, across three segments per block (total 216 samples across the study).

## Data collected and analysis
- Macroinvertebrate community data: organisms identified to family level; abundance recorded for each taxon; Chironomidae morphotaxa distinguished by head capsule morphology.
- Stable isotope data: δ13C and δ15N measured for macroinvertebrate taxa after a 24-hour gut depuration; taxa then freeze-dried and weighed for isotope analysis.
- Analytical framework: standard isotope chemistry and mass-balance interpretation to assess dietary shifts and trophic dynamics in response to drought.

## Methods in detail
- Mesocosms and treatments: four blocks with three channels each; water from four streams with varying pH; flow reductions implemented via intake valves and stage-discharge curves; treatments maintained through the exposure period.
- Macroinvertebrate sampling: Hess samplers collected 9 replicates per time point per block; samples split for ethanol-preserved taxonomy and live depuration for gut contents prior to isotope analyses.
- Taxonomy and processing: organisms identified to family level using standard keys; Chironomidae morphotaxa categorized as filterers or predators.
- Stable isotope workflow: depurated organisms frozen, freeze-dried, homogenized, and weighed for isotope analysis using EA-IRMS; standards USGS40 and USGS41a used for δ13C and δ15N; long-term precision reported for quality control.
- Data handling: data organized with replicates as rows; metadata include mesocosm block, treatment, time, segment, and taxon; two associated data sheets described (see Data Structure).

## Data structure and accessibility
- Two CSV data files:
  - netfreshexpsi.csv: Stable isotope data
  - netfreshexpcomm.csv: Macroinvertebrate community data
- Key columns:
  - Site: mesocosm block codes Ll3 (Hanwell), Ll6 (Carpenter), Ll7 (Davies), Ll8 (Sidaway)
  - Treatment: flow level during drought (100% baseflow, 50%, 10%)
  - Time: sampling period (Before, During; and For isotopes, Before and During)
  - Segment: channel segment (1–9; 1 at the top, 9 at the bottom; each segment 1 m)
  - Taxon: macroinvertebrate taxon or stable isotope target
  - For community data: abundance data by taxon
  - For isotope data: d13C and d15N values
- Structure notes:
  - Community file contains Site, Treatment, Time, Segment, and abundance by taxa (including Chironomidae morphotaxa)
  - Isotope file contains Site, Treatment, Time, and Taxon with d13C and d15N values
- Purpose: designed for integrative analyses of community composition and dietary sources across drought treatments and timepoints; intended for storage and sharing via established portals and data ecosystems (e.g., EIDC, UKCEH workflows)

## Quality assurance and standards
- Isotope standards: USGS40 (for δ13C and cross-checks) and USGS41a (for δ15N); USGS40 used as reference for carbon and nitrogen concentrations.
- Quality control: long-term precision values provided for fresh topsoil control material; analyses duplicated or tested to exceed 2 standard deviations or 3 for outliers as appropriate.
- Data processing: Isodat 2.0 used for isotope data handling.

## References
- Dobson et al. (2012); Durance et al. (2016); Edington & Hildrew (1995); Elliot & Humpesch (2012); Macadam et al. (2022); Seymour et al. (2018); Windsor (personal communication); Wallace et al. (2003).

## Relevance for environmental monitoring
- Provides a standardized, traceable dataset linking habitat alteration (drought) to changes in aquatic invertebrate communities and their trophic ecology.
- Combines community metrics with stable isotope data to enable nuanced assessments of ecosystem health, resource use, and food-web responses over time.
- Grounded in BACI design and robust QA, supporting time-series analyses and policy-relevant environmental health monitoring while enabling data interoperability and reuse.