# Survey Overview

## Overview
- Purpose: Provide peat surface motion data to validate the ISBAS DInSAR technique over peatland.
- Study objective: Show variation of peat surface motion within microtopographic features across two blanket peatland sites.
- Data collection period: Approximately monthly measurements from 30/07/2017 to 22/02/2019.
- Gaps: December 2017–April 2018 at Knockfin Heights due to thick snow; occasional single benchmark data gaps due to weather.
- Sites: RSPB Forsinard, Knockfin Heights (Sutherland, Scotland) and Plantlife Munsary (Caithness, Scotland) in the Flow Country.

## Study Sites
- Knockfin Heights: Upland blanket bog (>300 m.a.s.l.); varied erosive features (peat hags, pools, lochans); mixed vegetation; ownership by multiple landowners (RSPB Forsinard estate among them).
- Munsary: Lowland Flow Country; high water tables; pool systems (Dubh Lochans); near-natural condition with historic grazing, peat extraction, and burning, with recent restoration (drain blocking).
- Site layout: Two main sites with mapped benchmark locations and subsites representing peat microtopography and subspecies of vegetation (hummocks, hollows, lawns, bare peat, etc.).

## Survey Design and Benchmarks
- Benchmark types:
  - Permanent benchmarks: Connected to underlying substrate (bedrock or clay). Constructed from 6 mm galvanised rods, joined with bolts; ground surface marked for reference; protruding rod trimmed; used for linking to substrate for relative motion measurements.
  - Floating benchmarks: Anchored to the peat surface only; measure bulk motion of the top 0.5 m of peat; 0.5 m ground anchor with barbed rod to integrate with surface.
- Benchmark layout: Approximately 1 km^2 per site; seven subsites per site with permanent benchmarks; within each site seven floating benchmark locations to cover microtopography.
- Site specifics:
  - Knockfin Heights: Benchmarking tied to eroded upper surface of underlying metamorphic bedrock; vegetation and peat features documented.
  - Munsary: Benchmarks anchored to glacial clay; peat surface markers placed to accommodate vegetation growth and peat movement.
- Placement and marking: Permanent benchmarks installed to level underlying substrate; floating benchmarks placed and left for settling before first levelling; GPS tagging and high-visibility markers used.

## Levelling Procedure and Data Quality
- Instrumentation: Leica LS15 precise level with a 2 m Invar staff.
- Measurement protocol: BBFF (backsight, backsight, foresight, foresight); single-operator levelling with line levelling mode; multiple readings per measurement with averaging.
- Spacing and targeting: Station positioned about 50 m from staff when possible to minimize error; readings conducted with stringent setup to reduce wind-related movement.
- Measurement thresholds and checks:
  - Standard deviation threshold: STDEV < 0.5 mm; if higher, re-measure; in windy conditions, threshold relaxed to < 1 mm.
  - Site loops: Generally achieve closure of <1 mm.
  - Repetition: Each survey loop repeated three times; loop closure corrections applied post-survey using Leica Infinity.
- Time cadence: Surveys conducted roughly every 5 weeks to align with 6-day InSAR repeat cycles.
- Quality control: Re-measurements if SD exceeded limits; fixed benchmarks treated as stable within error margins established by RTK-GPS checks.

## Data Structure and Metadata
- Data types and columns (Appendix A):
  - Benchmark name; X (OSGB); Y (OSGB); Z (m.a.s.l) height above Ordnance Datum Newlyn; Date of survey; Height relative to fixed benchmark (standardized to 100 m per subsite); STDEV (m) from three measurements.
  - Data values include NA (not measurable due to environmental conditions such as wind or glare).
- Data organization:
  - Floating benchmark locations described in Table A1 (Knockfin Heights) and Table A2 (Munsary) with coordinates and microtopography descriptions.
  - Loop closures and measurement details recorded in Tables A3 and A4, including OSGB coordinates, closure heights, and height changes over time.
- Coordinate system and reference:
  - OSGB (British National Grid) coordinates for all benchmarks.
  - Heights referenced to fixed benchmarks and corrected for loop closure; vertical motion reported as height changes relative to these references.
- Data content goal: Enable end users to analyze peat surface motion and compare with InSAR-derived subsidence measurements.

## Data Quality, Gaps, and Provenance
- Data quality emphasis: High-precision levelling with small stdev tolerances; multiple checks and loop closures to ensure vertical accuracy.
- Data gaps: Snow-related gap at Knockfin Heights; other minor weather-related data gaps acknowledged in the dataset documentation.
- Provenance and references: Detailed methodology and site descriptions with provenance to support reproducibility and cross-study comparisons.

## Data Products and Reuse
- Primary data product: Time series of peat surface height changes at identified floating benchmarks relative to permanent benchmarks, suitable for validating InSAR-based subsidence motion (ISBAS DInSAR).
- Metadata richness: Comprehensive site descriptions, benchmark construction details, microtopography mapping, and complete appendix tables with coordinates and measurement statistics to support secondary analyses.
- Potential uses beyond validation: Cross-site comparisons of peat motion across microtopography (hummocks, hollows, lawns, bare peat), assessment of peatland stability, and integration with remote sensing time series.

## References
- Lindsay, R., Clough, J., Clutterbuck, B., Bain, C., Goodyer, E., 2019. Eyes on the Bog - Long term monitoring network for UK peatlands, IUCN Peatland Programme
- Lindsay, R., Charman, D.J., Everingham, F., O'Reilly, R.M., Palmer, M.A., Rowell, T.A., Stroud, D.A. 1988. The Flow Country: The peatlands of Caithness and Sutherland. Peterborough Joint Nature Conservation Committee