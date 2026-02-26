# SUPPORTING DOCUMENTATION: Trade-off between reproduction and body maintenance in a wild field cricket ( Gryllus campestris ) population

## Overview
- Long-term field study monitoring a Gryllus campestris population in a meadow near Asturias, Spain.
- Focus on reproduction versus body maintenance trade-offs using a rich, spatially explicit data collection regime.
- Data collected include individual identification, behavioral events, physiological samples, environmental context, and camera/video records.

## Study site and spatial setup
- Meadow area: about 20,000 m2; primary cricket habitat centered on a roughly 800 m2 flat area on the meadow.
- Landscape context: bordered by railway, roads, and surrounding meadows; shading/slope influence cricket distribution.
- Microhabitats: crickets avoid shaded areas and prefer sunlit meadow patches; burrows are focal points for monitoring and behavior.
- Spatial instrumentation: network of burrow-specific monitoring points with multiple infrared cameras; weather station at meadow center plus temperature sensors in and around burrows (simulated burrows).
- Camera deployment: started with 64 cameras in 2006; expansion to 140 cameras by 2017; cameras moved between burrows to maximize information.

## Sampling regime and data collection
- Timeframe: monitored for twelve consecutive years; adult emergence synchronized annually (about 14 days, ±3.66 days, with 95% within two weeks).
- Biological sampling: after adult emergence, each cricket is weighed, photographed, and tagged with a unique PVC pronotum tag for individual identification; small samples taken for pheromone/DNA profiling (cuticular hydrocarbons, haemolymph, leg tissue).
- Life cycle monitoring: crickets overwinter as late instar nymphs; adults emerge in spring; eggs laid from May; complete lifecycle with last adults dying by early July.
- Burrow-focused observations: direct observations supplement video data to cover non-videoed burrows; daily checks to confirm occupancy and emergence timing.

## Field instrumentation and data collection infrastructure
- Video system: 64–140 infrared cameras recording around burrow entrances continuously from early eelosion to end of activity season; motion-activated DVR system with centralized storage.
- Weather instrumentation: Davis Vantage Pro2 weather station; ten-minute interval logging; additional soil/within-burrow temperature sensors.
- Data capture workflow: two-stage video analysis (coarse pass to identify active burrows, followed by detailed review of selected cameras); data imported into MS Access database for processing.
- Calibration: instruments are factory calibrated.

## Data management, quality control, and methodology
- Video/data quality control: consistency checks in MS Access to prevent conflicting burrow occupancy records and other errors.
- Data integration approach: combination of video data, direct observations, biological samples, and environmental measurements into a centralized data framework.
- Data handling steps:
  - Emergence date: determine adult emergence timing; cited as highly synchronized with a defined emergence window.
  - Calling activity: binary hourly measure (singing yes/no) based on 10-minute samples per hour; used to derive daily singing metrics.
  - Searching activity: burrow visit duration transformed into a binary short/long variable to reflect intensive searching behavior.
  - Dominance in fights: win/loss scoring across fights, assigned to both participants with age-adjusted scoring.
  - Mating promptness: latency converted to binary (≤50 minutes vs >50 minutes) to reflect rapid mating potential given spermatophore production timing.

## Key variables and analytical focus
- Emergence date: timing of adult emergence as a critical reproductive milestone.
- Behavioral indicators:
  - Singing activity (temporal pattern, frequency).
  - Searching activity (movement between burrows as a proxy for mate-search effort).
  - Dominance outcomes (territory/burrow occupancy and mating opportunities).
  - Mating promptness (latency to mating after encounter).
- Biological samples: pheromone profiles and DNA profiles to understand individual variation in reproductive strategies.
- Environmental context: meadow microhabitat preferences, shading effects, and weather conditions relevant to activity patterns.

## GIS and spatial data implications
- Spatial layers implied:
  - Burrow locations with unique identifiers and occupancy status over time.
  - Camera coverage map showing which burrows are monitored in which years.
  - Movement and interaction patterns across the burrow network (implied by occupancy and mating events).
  - Weather and microclimate layers (perimeter sensors and in-burrow environments).
- Potential GIS products:
  - Occupancy heatmaps and temporal-spatial patterns of burrow use.
  - Maps of emergent activity corridors and preferred microhabitats.
  - Spatial analyses linking environmental variables to singing, mating, and dominance behaviors.

## Scope and accessibility
- Longitudinal data spanning 12 years with high temporal resolution (daily to hourly) and extensive behavioral, physiological, and environmental measurements.
- Data management relies on a mix of DVR video archives, Excel spreadsheets, and MS Access databases, implying a need for careful data integration for map-based products and end-user visualizations.

## Relevance to GIS Specialists
- Demonstrates a richly spatially structured field study with explicit burrow-level geolocations and a networked camera array ideal for map-based data products.
- Provides a strong example of integrating multi-source data (behavioral, physiological, environmental) into spatial analyses to explore how habitat structure and microclimate shape reproductive strategies.
- Highlights data workflows, quality control, and long-term data management considerations critical for producing shareable GIS datasets and visualizations for researchers and stakeholders.