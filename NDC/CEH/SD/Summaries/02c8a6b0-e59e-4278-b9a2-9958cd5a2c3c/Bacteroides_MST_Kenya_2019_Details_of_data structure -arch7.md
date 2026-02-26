# Details of data structure

- A six-file CSV dataset describing fecal sampling, isolation of Bacteroides hosts, and detection of FIB and MST markers, with geographic components suitable for GIS visualization.
- Files capture sampling locations, stepwise isolation results across two weeks, and water quality markers in drinking water and wastewater effluent.

## Overview for GIS-focused use

- Geographic data: multiple files include latitude, longitude, and altitude for sampling sites.
- Temporal data: dates of sample collection and weekly steps (Week 10-6-18 and Week 17-6-18).
- Biological/microbiological data: fecal sample origins, dilution factors, esculin reactions, CFU counts, Gram staining, and isolation status.
- Water quality data: levels of fecal indicator bacteria and various phage markers in water sources and wastewater effluents.
- Linkages enable map-based exploration of where samples were taken, how isolates were processed, and the distribution of FIB/MST markers.

## File-by-file data structure and GIS relevance

- LocationOfFaecalSampling.csv
  - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude.
  - GIS use: geolocate sampling sites for mapping anthropogenic or environmental exposure patterns.

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive Esculin (Anaerobic CFU); Negative Esculin (Anaerobic CFU); Positive Esculin (Aerobic CFU); Negative Esculin (Aerobic CFU).
  - GIS use: visualize sampling points and initial isolation outcomes spatially.

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin (Anaerobic CFU); Negative Esculin (Anaerobic CFU); Positive Esculin (Aerobic CFU); Negative Esculin (Aerobic CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.
  - GIS use: map isolate locations and link to subsequent analyses via isolate codes.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive Esculin (Anaerobic CFU); Negative Esculin (Anaerobic CFU); Positive Esculin (Aerobic CFU); Negative Esculin (Aerobic CFU).
  - GIS use: separate week’s initial results spatially for comparison with Week 10-6-18.

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin (Anaerobic CFU); Negative Esculin (Anaerobic CFU); Positive Esculin (Aerobic CFU); Negative Esculin (Aerobic CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.
  - GIS use: map end-point isolates and relate to Week 17-6-18 StepA results.

- DetectionOfFIB&MSTmarkers.csv
  - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/1 mL); Phages of Bacteroides fragilis GB124 (PFU/1 mL); Phages of potential human Bacteroides spp. codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3 (PFU/1 mL each); Phages of potential cattle Bacteroides spp. codes KN.1, KN.2, KN.3, KN.8, SIN.19 (PFU/1 mL each).
  - GIS use: map water quality markers, compare with sampling sites, and analyze spatial patterns of phage presence.

## Linkages and data integration

- Cross-file linkages:
  - IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; alignment by Location name from faecal sample collection.
  - IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; alignment by Location name from faecal sample collection.
- Codes for isolates:
  - Bacteroides spp. host codes combine location initials and isolate numbers (e.g., LU.2 = Luawk primary school pit latrine, isolate 2; SIN.19 = Sinogo water pan shoreline, isolate 19).
- Purpose:
  - Enables integrated GIS workflows to map sampling sites, track isolation progress, and overlay FIB/MST marker data on water sources for environmental health insights.

## Practical GIS considerations

- Data quality and consistency:
  - Data come from multiple files with different formats and resolutions; careful cleaning and reconciliation required before mapping.
- Data modeling:
  - Treat location names as keys for linking StepA and StepB records; unify coordinates from StepA with subsequent steps.
- Visualization ideas:
  - Point maps of sampling sites colored by isolation success or CFU counts.
  - Timelines or sequential maps comparing Week 10-6-18 vs Week 17-6-18 results.
  - Overlay water-source sites with FIB/MST marker levels to assess groundwater or surface water contamination patterns.
- caveats:
  - Ensure date formats, units (CFU, PFU), and esculin reaction statuses are consistently interpreted across files.
  - Resolve any mismatches in the Location name field between StepA and StepB continuations.

## Summary takeaway for GIS workflows

- The dataset provides geographically tagged sampling and isolation data across two weeks, plus water quality markers, enabling comprehensive map-based analyses of Bacteroides host isolation outcomes and fecal indicator/phage presence in environmental contexts. Proper integration hinges on linking StepA/StepB entries via location names and decoding isolate codes, to produce informative spatial visualizations for policy, clients, or public audiences.