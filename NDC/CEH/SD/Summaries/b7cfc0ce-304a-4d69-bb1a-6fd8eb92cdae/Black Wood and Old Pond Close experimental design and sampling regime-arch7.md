# Black Wood, Hampshire

## Overview
- Document describes a hydrological interception study at two forestry sites in southern England: Black Wood plantation (2.4 km²) near Micheldever and Old Pond Close woodland (25 ha) near Yardley Chase.
- Focus on measuring interception, throughfall, stemflow, net precipitation, and runoff to understand spatial and temporal patterns.
- Emphasizes detailed sampling layouts, instrumentation, data collection, and chemical analyses, with implications for map-based data products and GIS integration.

## Spatial Context and Datasets
- Black Wood:
  - Location: near Micheldever, mid-way between Winchester and Basingstoke; bounded by A303, A33, M3.
  - Environment: beech (Fagus sylvatica), planted on limed agricultural land; 100–150 m above sea level; 800 mm/year rainfall; westerly winds; chalk bedrock with well-drained shallow soils.
  - Monitoring area: forest edge effects with edge-to-interior gradients; flat terrain used for plotting.
- Old Pond Close:
  - Location: eastern end of Yardley Chase, ~7 km NW of Olney, near Buckinghamshire/Northamptonshire border.
  - Environment: common ash (Fraxinus excelsior) canopy with understory; calcareous clay loam soils over Oxford Clay; elevation ~110 m a.s.l.; ~589 mm annual precipitation (1970–1986 baseline).
- Data implications for GIS: geolocated plots, transects, and measurement points (throughfall gauges, stemflow collectors, rainfall towers) suitable for spatial visualization and interpolation.

## Monitoring Framework and Sampling Design
- Black Wood:
  - Initiated May 1989 with neutron probes, tensiometers, automatic weather stations, and canopy rainfall measurement.
  - Experimental design: edge-interception gradients using a block sampling approach; plots arranged in rows parallel and perpendicular to the forest edge.
  - Plot layout: each plot ~100 m², bounding four trees; rows ~60 m apart.
  - Distances from edge for sampling: 20, 50, 100, 200, 350 m.
  - Deployment: per plot, 8 throughfall samplers and 4 stemflow collectors; trunks equipped with polypropylene collars; stemflow collected in 450 L bins.
  - Throughfall gauges: circular, radius ~7.6 cm; funnel rims ~50 cm above ground; small-mesh filters to reduce contamination.
  - Rainfall: above-canopy rainfall gauges on towers (two sites, beech and ash) with tubing to base collection bottles.
  - Sampling cadence: typically every 1–2 weeks; post-collection gauge relocation to reduce bias.
- Old Pond Close:
  - Sampling began March 1991 for just over one year.
  - Measurements:
    - Precipitation: two 14.8 cm funnel above canopy; samples combined for chemical analysis.
    - Throughfall: 10 roving gauges, 15.2 cm diameter, located along a 100 m transect; gauges relocated with time.
    - Net precipitation: 90 m² plastic sheet collector above understory, enclosing four stems; large-volume sampling with a tipping-bucket device.
    - Runoff: small stream runoff collected in clean 2 L bottles; careful bottle preparation and cleaning protocol.
  - Data handling: samples filtered (0.45 μm) before chemical analysis; replication combined for totals.

## Data Collection Methods and Analyses
- Precipitation and throughfall: volume measurements by weighing; throughfall and rainfall samples combined for chemical analysis.
- Net precipitation: volume-integrated sampling over a large area to capture canopy interception plus understory effects.
- Chemical analyses performed on combined samples:
  - pH (electrometric)
  - Major, minor, and trace elements (ICP emission spectroscopy)
  - Potassium (AAS)
  - Major anions and fluoride (ion chromatography)
  - Ammonium and silicon (colorimetry)
- Alkalinity: not measured directly; calculated using a simplified equation based on pH (Alkalinity = 6×10^(pH-6) − 10^(6−pH)), units in μEq/L, assuming atmospheric equilibrium.
- Runoff samples analyzed from stream drainage to complement interception measurements.

## GIS and Data Integration Considerations
- Spatially explicit layout:
  - Plot polygons (≈100 m²), tree-centered plots, and edge-distance attributes.
  - Point data for throughfall gauges, stemflow collectors, and rainfall towers with precise coordinates and elevations.
  - Transects and edge-oriented sampling enable creation of interception gradient maps.
- Temporal dimension:
  - Time-stamped precipitation, throughfall, net precipitation, and chemical analyses suitable for time-series visualization and trend analysis.
- Data harmonization:
  - Multiple data streams (physical measurements and chemistry) require consistent units, sampling intervals, and metadata for integration into GIS.
  - Challenges include heterogeneity of interception processes, relocation of gauges, and scale differences between plot-level and large-area net precipitation.
- Potential outputs:
  - Spatial maps of interception loss by distance from forest edge.
  - Visualization of throughfall and stemflow distribution across plots.
  - Geospatial models of rainfall partitioning and runoff linkage to plot location and canopy type.

## Key Points for Application
- The studies provide a rich, georeferenced dataset framework for mapping interception processes in forest canopies.
- Detailed plot layouts and measurement networks can be translated into GIS layers to analyze spatial patterns and resource allocation for hydrological modelling.
- Chemical analyses support linkages between hydrology and water quality across spatial sampling units.
- Considerations for GIS work include accurate geo-referencing of all sampling points, consistent time-series alignment, and careful handling of edge effects and understory influences.

## Endnotes and References (contextual)
- Several foundational methods and prior studies cited (e.g., interception studies at forest edges, roving gauges design, and large plastic-sheet rainfall gauges) provide methodological context for interpreting spatial patterns and for informing GIS-based visualization and modelling workflows.