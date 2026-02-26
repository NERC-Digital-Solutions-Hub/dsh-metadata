# West Halladale wildfire burn severity footprint in Flow Country peatlands

## Purpose and context
- Document a field campaign to characterize physical and chemical properties of peat within the West Halladale wildfire footprint.
- Focus on post-fire peat characteristics that inform carbon dynamics, humification, and peatland status across a burned area.

## Site description and sampling design
- Location: Flow Country peatlands in Caithness and Sutherland, northern Scottish mainland.
- Event: Dry, warm spring 2019 wildfire burned ~60 km² of wet heath and blanket bog (within ~4000 km² blanket bog area).
- Footprint sampling plan: 34 cores distributed across a burn severity map (low, medium, high) and drainage status (drained vs near-natural/undrained).
- Plot coding: Each plot labeled by severity (H, M, L) and drainage status (N for near-natural); numbers 1–15 within each combination.
- Field distribution: High severity largely in the northern, drained areas; near-natural southern end contained medium and low severity plots.

## Field sampling execution
- Field campaign: Five visits between late Feb and mid-Mar 2020.
- Core depth and selection: Targeted cores at 40–50 cm depth; not all plots suitable due to slopes, peat thickness, or access; final 34 cores collected (six plots per severity/drainage combination, plus extra in some drained high-severity areas).
- Core collection method: Used Russian corer, PVC half-pipes, Saran wrap, tape for depth; GPS for bottom-left plot coordinates; field notes captured on-site.

## Sample handling, storage and observations
- Data captured: Field notes (date, observer, burn severity, plot code, core depth, coordinates, elevation), vegetation context, photos.
- Data management: Transcribed to an Excel file, stored in ERI shared folder; cores returned to cold storage for later lab work.
- Covid-related delay: Ten cores analyzed in July 2020 due to lab access restrictions.

## Instruments and laboratory methods
- Field equipment: GPS, printed maps, Russian corer, PVC spacers, Saran wrap, measuring tape, camera.
- Laboratory equipment for analysis: Measuring tapes, knives, crucibles, analytical balances (three- and five-decimal accuracy), 100 mL cylinders for volume via water displacement, oven (105°C), muffle furnace (550°C), desiccator, Milli-Q water system.
- Sub-sampling: Each core section cut into 5 cm increments; samples weighed and processed in crucibles.

## Calibration and data recording
- Instrument calibration: Balances calibrated with standard weights per manufacturer instructions.
- Metadata and recorded values: Detailed per-core and per-sub-section data captured with explicit units and ranges to enable replication.

## Data structure and recorded values
- Field metadata (Peat_core_coordinate.csv): COREID, Depth (cm, 40–50 cm valid), Lat OSGB, Long OSGB, Grid Reference, Altitude, Exposure, Vegetation description.
- Laboratory measurements (Peat_core_data.csv): For each 5 cm sub-section: SEVERITY (LOW/MEDIUM/HIGH), TYPE (DRAINED/UNDRAINED), COREID, DEPTH (cm), VOL (volume in cm³), WET_PEAT, DRY_PEAT, BD (bulk density), MOIST%, vonPOST, LOI10, DRY_PEAT10, ASHg, OM%, ASH%, OC% (OC = OM/2), and von Post scale values.

## Analytical methods and calculations
- Bulk density, moisture, organic matter, ash content, and organic carbon calculated per 5 cm sub-section.
- Bulk density: md (dry mass) divided by volume (Vt, via water displacement).
- Moisture content: ((Mw − Md) / Mw) × 100.
- Organic matter content: LOI at 550°C vs 105°C dry weights; OM% = LOI / Md(105°C) × 100.
- Ash content: Ash weight as a percentage of dry weight at 105°C; OC% = OM% / 2 (assuming 50% organic carbon in organic matter).
- Von Post scale: Qualitative decomposition index (H1–H10) based on peat squeeze tests.
- Quality control: Excluded three sub-samples with weighing inconsistencies to prevent erroneous calculations.

## Data integrity, governance and openness
- Emphasis on traceability from field to lab: standardized coding (COREID), clear depth and coordinate metadata, and documented analytical workflows.
- Data cleaning: removal of sub-samples with clear weighing errors; thorough documentation of methods to enable reproducibility.
- Public sharing considerations noted in the broader monitoring framework context (data governance and openness are common challenges for monitoring projects).

## Key takeaways for monitoring and policy evaluation
- A stratified sampling approach links fire severity and drainage status to peat physical and chemical properties, enabling assessment of post-fire carbon dynamics and peatland recovery trajectories.
- Comprehensive metadata and standardized laboratory protocols facilitate data comparability across sites and time, supporting policy evaluation of post-fire restoration or conservation interventions.
- Operational challenges (access, Covid-19 delays, data governance barriers) illustrate real-world considerations for timely and open sharing of environmental data in monitoring programs.