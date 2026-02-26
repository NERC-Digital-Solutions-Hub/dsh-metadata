# Survey Overview

- Purpose: Conduct precise levelling surveys at two blanket peatland sites in the Flow Country to provide peat surface motion data for validating the ISBAS DInSAR (Intermittent Small Baseline Subset Differential Interferometric Synthetic Aperture Radar) technique over peatland.
- Objective: Capture variation of peat surface motion within 14 90x90 m pixel areas across different microtopographic features (hummocks, hollows, high/low ridges, bare peat, hags); monthly measurements from 30 July 2017 to 22 February 2019.
- Gaps: Data gaps at Knockfin due to thick snow (Dec 2017–Apr 2018) and occasional single benchmark gaps from weather.

## Site Description

- InSAR ToPS study sites:
  - Knockfin Heights (RSPB Forsinard), Sutherland, Scotland (NC94958)
  - Munsary (Plantlife), Caithness, Scotland (ND21677 46186)
- Flow Country context: Large area of blanket bog; site characteristics include peat hags, drained/undrained pools, lawns, sphagnum, heather, and shrub cover.
- Site specifics:
  - Knockfin Heights: upland bog (>300 m a.s.l.) with erosive features, varied drainage, managed by multiple landowners including RSPB Forsinard estate.
  - Munsary: lowland peatland with numerous pool systems, high water tables, near-natural condition with historic grazing and peat extraction; recent restoration (drain blocking).

## Survey Design

- Benchmark types:
  - Permanent benchmarks: 6 mm galvanised rods (1 m) linked; surface marked with washers/bolts; mounted to stay above peat; regular setup to support stable measurement and GPS staff use.
  - Floating benchmarks: anchored to peat surface; 0.5 m depth measurement range; designed to track bulk motion of the top 0.5 m of peat; robust head design to ease leveling.
- Benchmark layout:
  - Approximately 1 km^2 study area per site.
  - At each site: seven subsites representing range of InSAR-derived subsidence rates and microtopography.
  - At each subsite: one permanent benchmark and seven floating benchmarks to compare against the permanent reference.
- Benchmark installation notes:
  - Permanent benchmarks installed to underlying substrate (bedrock or glacial clay) with careful hammering/embedding to minimize damage; visible markers placed to resist deer interference; some deer-related losses noted.
  - Floating benchmarks installed flush with peat surface; positions recorded to allow later levelling and recovery periods.

## Levelling Survey Design

- Equipment and method:
  - Leica LS15 precise level; 2 m Invar staff.
  - BBFF (backsight, backsight, foresight, foresight) setup with a single operator; measurements referenced to permanent benchmarks.
  - Line/leveling setup with careful spacing, aiming for about 50 m station separation; multiple checks to ensure data quality.
- Measurement protocol:
  - Each measurement repeated three times; standard deviation target < 0.5 mm; if not achievable due to weather, thresholds temporarily relaxed to < 1 mm.
  - Loop closures corrected post-survey using Leica Infinity software; high wind conditions adjust measurement thresholds.
  - Site loops typically achieve sub-millimetre closure; surveys repeated roughly every five weeks to align with six-day InSAR repeat cycles.
  - Snow disruption at Knockfin Heights caused a gap in Dec 2017–Apr 2018.

## Quality Control

- Repetition and closure:
  - Measurements repeated three times per survey; loop closure tracked (Tables A3–A4 in Appendix).
  - Measurements exceeding 0.5 mm standard deviation are repeated; weather-related exceptions may raise limits.
  - Heights corrected for loop closure; fixed benchmarks assumed stable; vertical motion within RTK-GPS error margins.

## Appendix and Data Presentation

- Data structure:
  - Data Type, Benchmark name, X/Y coordinates (OSGB), Z height (m.a.s.l.), Date, Height relative to fixed benchmark, STDEV (m).
  - Typical data fields include coordinates, date of survey, height offset, and measurement uncertainty.
- Floating benchmark location tables:
  - Tables A1 and A2 describe the location and microtopography for floating benchmarks at Knockfin Heights and Munsary, respectively.
- Loop closure and height data:
  - Tables A3 and A4 present loop closures and height changes across multiple survey dates for both sites.
  - Data include detailed OSGB coordinates, closure values, survey dates, and site-specific height changes.

## References

- Lindsay, R., Clough, J., Clutterbuck, B., Bain, C., Goodyer, E., 2019. Eyes on the Bog - Long term monitoring network for UK peatlands, IUCN Peatland Programme
- Lindsay, R., Charman, D.J., Everingham, F., O'Reilly, R.M., Palmer, M.A., Rowell, T.A., Stroud, D.A., 1988. The Flow Country: The peatlands of Caithness and Sutherland. JNCC

## Relevance to Monitoring Frameworks (Implications for Authors)

- Data quality and standardization:
  - Demonstrates rigorous field-level QA, standardized levelling procedures, and explicit measurement uncertainty, aligning with best practices for data quality in monitoring frameworks.
- Metadata and data accessibility:
  - Detailed site descriptions, benchmark types, installation methods, and measurement protocols; substantial metadata is generated to support data reuse and verification.
- Data gaps and continuity:
  - Acknowledges weather-related interruptions (snow, wind) and animal interference, highlighting the need for contingency planning and durable data governance to maintain long-term datasets.
- Data sharing and transparency:
  - Supplements with appendices (Tables A1–A4) describing data collection and locations; exemplifies the level of data sharing that may be necessary to validate remote-sensing techniques and support independent verification.
- Data integration and governance:
  - Integrates ground-based levelling with InSAR validation, illustrating how multiple data streams can be coordinated within a monitoring framework; underscores the importance of clear data ownership, provenance, and versioning.