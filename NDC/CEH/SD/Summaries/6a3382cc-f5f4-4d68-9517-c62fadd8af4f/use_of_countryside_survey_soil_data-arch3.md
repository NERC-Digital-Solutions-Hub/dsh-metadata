# Countryside Survey Soils 2007: Method development, power analyses and protocols

## Overview
- Describes sampling design, locations, procedures, measurements, and statistical approaches used in Countryside Survey (CS) soils from 1978 to 2019, including the rolling survey initiated in 2019.
- Aims to support monitoring of soil properties to assess change and inform policy decisions.
- Emphasizes considerations for data quality, comparability over time, and appropriate statistical handling given the CS structure.

## Sampling design
- Years of sampling: 1978, 1998, 2007, and rolling survey starting in 2019.
- Sampling intensity: 256 squares in earlier years; 591 CS squares in 2007; rolling survey aims for ~100 squares per year for five years before repeating.
- Power analyses conducted to determine the number of samples needed to detect significant change (referenced to Emmett et al. 2008).
- A pilot survey occurred in 2018, informing the rolling design.

## Sample location
- Soils are sampled from CS X-plots within each CS square; there are 5 X-plots per square.
- X-plots are not replicates and can represent different land uses or soil types within a square.
- Some plots are relocated over time due to destruction, access restrictions, or relocation uncertainty; each location has a unique repeat identifier (e.g., 2RPT1).
- Re-sampling locations in practice involves sampling near the original area, about 2–3 meters from the exact plot.

## Sampling
- Depth: top 15 cm of the soil profile (8 cm for invertebrate samples); 1978 used a soil pit; later surveys used a hammered core method.
- Practical challenges: stones or shallow soils may prevent full 15-cm cores.
- In 1998, 2007, and the rolling survey (2018/2019–2023), multiple cores per X-plot were collected; not all cores had the same measurements.

## Measurements
- 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
- 1998 onward (including 2007 and rolling survey): multiple cores per X-plot; different cores measured with varying analyses; no chemical analyses by soil horizon; samples homogenised prior to pH and LOI.
- Bulk density: measured in 2007 and in 2018/19–2023 (not using ISO bulk density method due to practical constraints).
- Documentation: detailed method descriptions and implications are provided in Emmett et al. 2008.

## Statistical analysis
- Analyses should account for CS sampling structure and land class effects to avoid bias.
  - If land classes are ignored, estimates reflect population stock and change; if weighted by land classes, results become national estimates.
- Bootstrapping is not always employed; recommended use of mixed models with square as a random factor to account for multiple X-plots within each CS square.
- Design considerations:
  - In CS-type designs where spatial structure is not the primary interest, a dispersed set of observations can increase overall precision and regional representativeness.
- Guidance: CS users should consult UKCEH before analysis and interpretation; reference CS publications available on the CS website.

## Data governance and accessibility (implications for monitoring frameworks)
- Emphasizes data quality assurance, standardisation of measurements, and transparent data management.
- Highlights potential barriers to data sharing, including metadata gaps and data originator access.
- Underlines the importance of open data practices and clear documentation to enable reuse and cross-year comparability.

## Key takeaways for monitoring framework design
- Longitudinal soil monitoring benefits from rolling designs with clearly defined repeat identifiers and documented relocation rules.
- Ensure robust metadata and consistent measurement protocols to enable valid temporal comparisons.
- Use mixed models to properly account for hierarchical sampling structure (X-plots within squares).
- Consider data governance upfront: metadata completeness, data sharing permissions, and alignment with national data standards.
- Plan for data interpretation caveats due to land class structure and non-uniform sampling across years.
- Provide guidance and references to end-users (e.g., consult UKCEH) to ensure appropriate analyses and interpretation.