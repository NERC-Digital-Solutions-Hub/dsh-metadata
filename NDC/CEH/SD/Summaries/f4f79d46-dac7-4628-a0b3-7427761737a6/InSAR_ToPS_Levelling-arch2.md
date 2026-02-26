# Survey Overview

- Purpose and scope
  - Conduct precise levelling surveys at two blanket peatland sites in the Flow Country to provide peat surface motion data for validating the ISBAS DInSAR technique over peatland.
  - Aim to capture variation in motion within 14 90x90 m pixels across different microtopographic features (hummocks, hollows, high/low ridges, bare peat, hags).
  - Data collection occurred approximately monthly from 30/07/2017 to 22/02/2019, with gaps due to thick snow (Dec 2017–Apr 2018) and occasional weather-related benchmark issues.

- Sites and context
  - RSPB Forsinard, Knockfin Heights (NC94958), Sutherland, Scotland
  - Plantlife Munsary (ND21677 46186), Caithness, Scotland
  - Part of the Flow Country, the largest expanse of blanket bog in Europe
  - Knockfin Heights: upland bog (>300 m a.s.l.), diverse erosive features, drained/undrained pools, sedge, sphagnum, heather, grasses; variation dependent on microtopography and drainage
  - Munsary: lowland bog (<100 m a.s.l.), high water tables, pool systems (Dubh Lochans), rare plants, surrounding margins with shrubland; historically grazed and burned, with recent peatland restoration; survey area near natural condition

- Survey design and benchmarks
  - Two benchmark types:
    - Permanent benchmarks: 6 mm galvanised rods (1 m total length) connected; installed to substrate level; baseline surface prepared with washers/bolts; protected from deer and vegetation; used as stable references; GPS tagging and long-range visibility aids
    - Floating benchmarks: anchored only to peat surface (0.5 m depth motion focus); flat-headed ground anchors to maximize surface area and levelling ease; positioned relative to permanent benchmarks
  - Benchmark locations
    - Approximately 1 km^2 area per site
    - Seven subsites per site selected based on prior InSAR data and aerial/photos; within each site, seven floating-benchmark locations distributed across peat microtopography (hummocks, lawns, hollows, bare peat, pools, peat hags)
    - Benchmark B5 lost at Knockfin Heights due to deer interference
  - Substrate and installation notes
    - Permanent benchmarks anchored into underlying substrate (bedrock at Knockfin Heights; glacial clay at Munsary); careful placement to avoid bending; most installed by hand where feasible
    - Floating benchmarks installed with ground anchors flush to peat; positioned to allow settling and vegetation recovery prior to first levelling

- Levelling methodology
  - Equipment: Leica LS15 precise level with 2 m Invar coded staff
  - Observation method: BBFF (backsight, backsight, foresight, foresight) with a single staff operator
  - Setup and measurement:
    - Leveling performed in line-levelling mode; distance balancing at 5 m; staff of 2 m; measurement limits (25 cm to 175 cm)
    - Distance autofocusing enabled; level station typically ~50 m from staff
    - Reading protocol: three measurements per reading; use mean
    - Quality thresholds: standard deviation (STDEV) < 0.5 mm for typical conditions; if higher, repeat; if repeated, relax to STDEV < 1 mm in poor weather
    - In high winds, STDEV threshold tightened to < 1 mm
    - Site loops generally achieve < 1 mm closure
    - Surveys repeated roughly every 5 weeks to align with 6-day InSAR cycles
    - Knockfin Heights temporarily inaccessible (Dec 2017–Apr 2018) due to snow
- Quality control and data integrity
  - Each survey loop repeated three times; loop closure checked
  - Measurements exceeding STDEV threshold repeated; otherwise, weather constraints may prevent repetition
  - Heights corrected post-survey for loop closure using Leica Infinity software
  - Fixed benchmarks assumed stable; vertical motion within fixed benchmarks consistent with RTK-GPS survey error

- Data and appendix structure
  - Data fields per observation:
    - Benchmark name; X and Y coordinates in OSGB (British National Grid)
    - Z (m.a.s.l.) height above sea level relative to Ordnance Datum Newlyn
    - Date of survey; Height relative to fixed benchmark (standardized to 100 m per subsite)
    - STDEV (m) from three measurements
    - NA entries indicate data not possible due to environmental conditions
  - Appendices include:
    - Table A1: Floating benchmark locations at Knockfin Heights with coordinates and microtopography descriptions
    - Table A2: Floating benchmark locations at Munsary with microtopographic codes and descriptions
    - Table A3: Loop closures for Knockfin Heights (coordinate and height closure data)
    - Table A4: Loop closures for Munsary (height closures across multiple dates)
  - Data notes
    - Data presented in OSGB grid coordinates and height above datum
    - Height values corrected for loop closure
    - Some entries marked NA due to environmental constraints or data loss

- References
  - Lindsay, R., et al. 2019. Eyes on the Bog - Long term monitoring network for UK peatlands, IUCN Peatland Programme
  - Lindsay, R., et al. 1988. The Flow Country: The peatlands of Caithness and Sutherland. JNCC