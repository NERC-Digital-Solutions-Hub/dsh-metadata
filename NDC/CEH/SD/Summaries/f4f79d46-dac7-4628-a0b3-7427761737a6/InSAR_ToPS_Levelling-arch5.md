# Survey Overview

- Purpose: Capture peat surface motion data at two blanket peatland sites in the Flow Country to validate ISBAS DInSAR measurements, covering variation across microtopographic features (hummocks, hollows, ridges, bare peat, hags).
- Timeframe: Approximately monthly measurements from 30 July 2017 to 22 February 2019, with gaps (Dec 2017–Apr 2018 due to thick snow; occasional single benchmark data gaps due to weather).
- Data scope: Aimed to characterize motion within 14 90×90 m pixels, providing spatial context across microtopography and vegetation types.

## Site Descriptions

- Forsinard, Knockfin Heights (NC94958), Sutherland, Scotland
  - Upland blanket bog (>300 m.a.s.l.), multi-owner estate; features peat hags, drained/undrained pools, lochans; mixture of sedge, sphagnum, heather, grasses.
- Munsary (ND21677 46186), Caithness, Scotland
  - Lowland Flow Country site; numerous pool systems (Dubh Lochans); high water table; near-natural condition with some historic grazing/restoration; margins shrubby.

## Survey Design and Benchmarks

- Benchmarks: Two types
  - Permanent benchmarks: 6 mm galvanised rods (1 m) linked by bolts; mounted to underlying substrate; ground surface marked with washers/bolts to aid traditional measurements; ~50 cm above peat; deer interference considerations; GPS staff cradle provided; used as a stable substrate reference.
  - Floating benchmarks: Anchored to the upper peat surface; 0.5 m ground anchors; barbed rods; large contact area to reduce compression; used to measure bulk motion of the top 0.5 m.
- Benchmark Layout: Approximately 1 km^2 per site; seven subsites per site representing range of subsidence and microtopography; within each subsite seven floating benchmark locations corresponding to microtopographic features (e.g., hummocks, hollows, lawns, pools, peat hags). Note: benchmark B5 lost to deer damage early on.
- Installation details: Permanent benchmarks installed to level with underlying substrate (bedrock at Knockfin Heights, glacial clay at Munsary); manual driving where possible; 100–150 mm embedding in softer substrates to avoid bending; floating benchmarks positioned and left to settle before first levelling.

## Levelling and Measurement Procedure

- Equipment: Leica LS15 precise level; 2 m Invar staff.
- Method: BBFF (backsight, backsight, foresight, foresight); line levelling with a single operator; stations placed ~50 m from staff when possible; line set in line levelling mode with specified parameters (distance balancing 5 m, staff 2 m, staff limits 25–175 cm).
- Accuracy and cadence: Readings averaged from three measurements; targeting standard deviation (STDEV) < 0.5 mm (wind conditions may reduce threshold to < 1 mm); site loops aimed for closure < ~1 mm; loops repeated roughly every 5 weeks to align with InSAR 6-day repeat cycles.
- Quality considerations: Measurements repeated to ensure precision; if STDEV exceeded, measurements were repeated unless weather prevented; heights corrected post-survey for loop closure using Leica Infinity software; fixed benchmarks assumed stable within RTK-GPS error margins.

## Data Collection Details and Data Handling

- Data captured include:
  - Benchmark identifiers, OSGB X and Y coordinates (British National Grid)
  - Height above sea level (m.a.s.l.) relative to Ordnance Datum Newlyn
  - Date of survey
  - Height relative to a fixed benchmark (standardized per subsite)
  - STDEV (standard deviation from three measurements)
- Data status: NA entries indicate measurements not possible due to environmental conditions (wind, glare, etc.).
- Data structure: Appendix tables (A1–A4) detail floating benchmark locations, microtopography codes, loop closures, and per-site height closures across multiple survey dates.

## Data Structure and Metadata

- Data headers (Table A1–A4) cover:
  - Floating benchmark IDs, coordinates, and microtopography descriptions
  - Per-site loop closures with OSGB coordinates, heights, dates, and height changes
  - Detailed per-date height changes (Height_m) and their corresponding closures for both sites
- Metadata design supports traceability of measurements, including:
  - OSGB coordinates, height references, measurement dates, and per-measurement uncertainty (STDEV)
  - Documentation of conditions when data could not be collected

## Data Governance and References

- Data governance considerations:
  - Standardized coordinate system (OSGB) and consistent height referencing against fixed benchmarks
  - Clear metadata schema (locations, dates, heights, uncertainties) to enable reuse and longitudinal comparisons
  - Documentation of data collection procedures, instrumentation, and quality-control steps
  - Handling of data gaps due to environmental conditions and deer disturbance
- References:
  - Lindsay, R. et al. 2019. Eyes on the Bog - Long term monitoring network for UK peatlands, IUCN Peatland Programme
  - Lindsay, R. et al. 1988. The Flow Country: The peatlands of Caithness and Sutherland

## Data Stewardship Implications

- This dataset exemplifies robust data governance needs for environmental time-series:
  - Maintain and publish standardized metadata for multi-site levelling campaigns
  - Ensure versioned, archivable records of raw and processed measurements
  - Document data quality checks, loop closures, and any deviations from standard thresholds
  - Facilitate future discovery and reuse through consistent spatial references, data dictionaries, and access protocols