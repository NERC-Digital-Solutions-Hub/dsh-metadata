# SUPPORTING DOCUMENTATION: Actuarial and phenotypic senescence in a wild field cricket ( Gryllus campestris ) population over ten years

## Overview
- Long-term field study at WildCrickets site in Asturias, North Spain, documenting actuarial and phenotypic senescence in Gryllus campestris over a multi-year period.
- Combines spatially-referenced field observations with continuous video monitoring, environmental data, and individual-level biological sampling to understand life histories and behaviours.

## Spatial context and study geometry
- Study area: meadow of ~20,000 m2, with the cricket population occupying ~800 m2 on the flat portion near the former riverbed.
- Key spatial features: proximity to railway line and roads; meadow bordered by meadows, orchards, and patches of eucalyptus, chestnut, and oak.
- GIS-relevant components:
  - Burrow locations (unique identifiers for the population’s microhabitats).
  - Camera network footprint covering burrows and surrounding area.
  - Weather station in the meadow center plus multiple temperature sensors distributed around and within simulated burrows.
  - Meadow boundaries and topography (slope/shading influence on cricket distribution).

## Data collection regime
- Population monitoring cadence: weekly burrow searches from February through July; adults emerge in spring, with eggs laid from early May; last adults die by end of June/early July.
- Population scale and habitat use:
  - Crickets are flightless; prefer sunny meadow areas, avoid shaded zones near trees or uphill.
  - Migration between fields appears limited by shade and roads.
- Sampling regime (individual-level data):
  - Each emerging adult trapped, weighed (±0.01 g), photographed, and marked with a unique PVC tag on the pronotum.
  - Samples collected: cuticular hydrocarbons, haemolymph, and a leg tip segment for pheromone/DNA profiling.
  
## Data collection infrastructure
- Video and camera network:
  - Infrared cameras installed in large numbers (64 initially, increasing to 133, and up to 140 by 2017) to monitor burrow entrances.
  - Cameras run 24/7 from first adult eclosion until no cricket activity remains for two days.
  - Video capture managed with motion-activated DVR systems; cameras rotated to maximize data on individual movements across burrows.
- Weather and environmental data:
  - Central weather station (Davis Vantage Pro2) logging variables at 10-minute intervals.
  - Seven additional temperature sensors located on the meadow surface and inside buried simulated burrows.
- Field instrumentation:
  - Each burrow flagged with a unique identifier; non-videoed burrows monitored via direct observation every 1–2 days to maintain complete emergence records.

## Data management, processing, and workflow
- Calibration and data integrity:
  - All instruments factory calibrated; consistent with standard practice.
- Data extraction and processing:
  - Per-day data extraction from video in two steps:
    - Step 1: rapid sweep to classify burrows as in-use vs empty across multiple cameras.
    - Step 2: detailed review of selected cameras to log events (e.g., emergence, encounters, singing, mating, oviposition, predator interactions) into a spreadsheet.
  - Data integration:
    - Event data imported into a MS Access database for further processing and analyses.
- Quality control:
  - Automated QC queries in MS Access to detect inconsistencies (e.g., a cricket recorded as using two burrows simultaneously).
  - Data not used until consistency checks are complete.

## Temporal scope and data products
- Timeframe:
  - Twelve consecutive years of monitoring described; camera deployment and data collection expanded over time (e.g., 64 → 140 cameras by 2017).
- Data types and potential GIS outputs:
  - Spatiotemporal events tied to individual crickets (emergence dates, movements between burrows, mating events).
  - Spatial layers for GIS: burrow locations with event histories, camera locations and coverage, weather-sensor sites, meadow boundary, and habitat features influencing distribution.
  - Derived metrics for GIS analyses: burrow occupancy over time, activity heatmaps around burrows, shelter/shade influence, and movement networks between burrows.

## Data characteristics and limitations for GIS specialists
- Multimodal data formats:
  - Video data (DVR) with metadata; spreadsheet event logs; MS Access database; Excel workflows; sensor time-series data.
- Spatial precision:
  - Exact coordinate data for burrows and camera sites is implied but not specified; GIS workflows would benefit from precise geolocation of all burrows, cameras, and sensors.
- Temporal resolution:
  - High-resolution temporal data (hourly/daily video events; 10-minute weather readings) enabling fine-grained spatiotemporal analyses.
- Data completion and quality:
  - Routine QC reduces errors, but missing data could occur for non-videoed burrows or periods with limited video coverage.

## Practical GIS-oriented takeaways
- Transformable data products:
  - Burrow-centric GIS layers with time-stamped events and occupancy status.
  - Camera network layer showing coverage and usage by burrow, enabling spatial optimization analyses.
  - Weather and microclimate sensor layers to model environmental influences on activity and senescence.
- Workflow considerations:
  - Maintain metadata standards across data formats to enable seamless integration into GIS platforms.
  - Preserve linking keys (burrow IDs, camera IDs, individual cricket IDs) to enable longitudinal spatial analyses of phenotypic and actuarial traits.