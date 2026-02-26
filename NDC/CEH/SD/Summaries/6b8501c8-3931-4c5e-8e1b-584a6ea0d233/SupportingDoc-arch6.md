# Growing season methane and nitrous oxide static chamber fluxes from Sodankylä region, Northern Finland - Supporting Documentation

- Objective: quantify methane (CH4) and nitrous oxide (N2O) fluxes during the growing season (2012) using static chambers in forest and wetland habitats near Sodankylä Arctic Research Centre; two campaigns (Summer and Autumn) with 60 chambers across three forest subplots (no enclosure, 12-year, ~50-year enclosures) and a wetland area capturing vegetation and water-table variability.

- Site description:
  - Location: Arctic Research Centre of Sodankylä, 67°22'N, 26°39'E, ~179 m a.s.l., central Lapland, Northern Finland; sub-arctic/boreal vegetation zone.
  - Ecosystems: UVET Scots pine forest on sandy podzol and a eutrophic flark fen wetland.
  - Forest structure: mean vegetation height ~12 m; stand age ~60–100 years; density ~2100 ha-1; lichen cover linked to reindeer presence.
  - Wetland: treeless flarks with sedges, mosses, Sphagnum; birch fen components and Betula spp. shrubs.

- Experimental design and sampling regime:
  - Campaigns: Summer (Jul 12–Aug 2) and Autumn (Sep 22–Oct 14) 2012.
  - Sampling: 60 static chambers (21 forest, 39 wetland).
  - Forest: chambers distributed across three subplots (no enclosure, 12-year enclosure, ~50-year enclosure).
  - Wetland: chambers positioned to span vegetation types and water table depths.
  - Frequency: flux measurements approximately every 2 days.
  - Replication: forest subplots include multiple chambers; wetland includes numerous chambers to capture spatial variability.
  - Total measurements: Summer had ~10 measurements per chamber; Autumn had 7 forest and 8 wetland measurements (per chamber context).

- Collection methods:
  - Static chambers: 40 cm diameter opaque polypropylene, with 10 cm deep shallow bases installed one day prior; lids sealed during a ~45-minute flux measurement.
  - Sampling: air samples collected 4 times per chamber over ~45 minutes; 100 mL samples flushed into 20 mL glass vials; analyzed within about one month.
  - Ancillary measurements: soil temperature at 10 cm depth (four replicate points per sampling); forest soil moisture (VMC) near each chamber base; wetland water-table depth via 21 dip wells near/around chamber bases; soil respiration measured adjacent to forest chambers and to 14 wetland chambers; vegetation recorded visually.
  - Root-zone data: Plant Root Simulator (PRS) probes deployed near each chamber for summer (11–12 Jul deployment; 1 Aug recovery) and autumn (22–23 Sep deployment; 13–15 Oct recovery); deployment length-corrected in analysis.

- Fieldwork and laboratory instrumentation:
  - Gas analysis: HP5890 series GC with electron capture detector (N2O) and flame ionisation detector (CH4) for concentrations (detection limits: CH4 < 70 μg L-1; N2O < 7 μg L-1).
  - In situ measurements: soil temperature (Omega HH370); soil moisture (Theta probe HH2); soil respiration (PP-Systems SCR-1 IRGA).
  - PRS probes: cation/anion data via Western Ag Innovations Inc. probes.

- Calibration steps and quality control:
  - Gas chromatograph calibration: 4-point calibration with standards approximately every 20 samples.
  - CH4 and N2O standards provided with specified concentrations (table of standards included in the study).
  - Analytical processing and QA: fluxes calculated with GCFlux version 2, which tests multiple models and selects best-fit approach for each chamber set; CH4 fluxes from best-fit model (linear or asymptotic); N2O fluxes derived from linear model due to proximity to detection limits.
  - Reported flux units: instantaneous fluxes in nmol m-2 s-1.

- Data structure, values, and units:
  - Date_Time: dd/mm/yyyy hh:mm (local time).
  - Chamber_number: unique chamber identifier.
  - CH4 Flux: nmol m-2 s-1.
  - N2O Flux: nmol m-2 s-1.
  - Soil Temperature: °C.
  - WaterTableDepth: cm.
  - SoilMoisture: % (volumetric moisture content).
  - Soil Respiration: g m-2 h-1.
  - Location metadata: chamber coordinates provided (forest and wetland site coordinates per chamber).

- Data notes and interpretation:
  - Flux estimates come with model-dependent uncertainty; N2O fluxes are particularly limited by detection limits and are based on linear-model calculations.
  - Data enable assessment of spatial variability across forest enclosures and wetland vegetation/water-table gradients, as well as seasonal (summer vs autumn) differences.
  - Includes accompanying environmental context (soil moisture, temperature, respiration, PRS-derived nutrient availability proxies) to support interpretation and data product creation (dashboards, summaries, or self-serve exploration).

- References:
  - Clough et al. 2015 (Chamber Design guidelines).
  - Levy et al. 2011 (Uncertainty quantification in static chamber fluxes).