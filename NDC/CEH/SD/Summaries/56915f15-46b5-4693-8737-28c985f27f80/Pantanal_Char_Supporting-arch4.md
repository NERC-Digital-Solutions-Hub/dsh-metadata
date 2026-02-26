# SUPPORTING DOCUMENTATION FOR 'Radiocarbon-dated charcoal datasets obtained from lake sediments from the Pantanal, Brazil'

- Overview
  - Charcoal datasets generated from macroscopic charcoal fragments analyzed in radiocarbon-dated lake sediment cores from the Brazilian Pantanal.
  - Four sediment cores/sites are documented: Laguna Mandior e core M1, Laguna Mandior e core M5, Laguna Mimoso, and Laguna Caceres.
  - Data include site metadata, collection details, depth-resolved charcoal concentrations, and associated radiocarbon dates (uncalibrated, conventional radiocarbon years BP).

- Data assets and scope
  - Site metadata presented in Table 1, including coordinates, lake area, depth, elevation, and core characteristics.
  - Charcoal concentration data: particles >125 μm per cm³ at each 1-cm horizon, with depth values representing the midpoint of each 1-cm interval.
  - Radiocarbon dating information (Table 2): number of dates per core, dating providers, units, and data structure describing age-depth profiling.
  - Core-specific collection details: core diameters, sampling methods, and 1-cm horizon slicing strategy.

- Data structure and access
  - Concentration data are stored in separate CSV files for each horizon 1-cm interval within a core.
  - Radiocarbon dates are provided as headers within each core’s CSV file, with uncalibrated conventional ages (BP).
  - Data structure notes:
    - Laguna Mandiore core M1: 3 radiocarbon dates; Beta Analytic; conventional radiocarbon years BP; age-depth profiling with full lab reporting.
    - Laguna Mandiore core M5: 3 radiocarbon dates; Beta Analytic; conventional radiocarbon years BP; age-depth profiling with full lab reporting.
    - Laguna Mimoso: 2 radiocarbon dates; UGAMS and Beta Analytic; conventional radiocarbon years BP; age-depth profiling with full lab reporting.
    - Laguna Caceres: 3 radiocarbon dates; Beta Analytic; conventional radiocarbon years BP; age-depth profiling with full lab reporting.
  - Notable detail: some radiocarbon dates are provided with sample depths and d13C values (for example, in Laguna Caceres data).

- Site and sampling details (selected highlights)
  - Laguna Mandior e core M1 (collection date 2001)
    - Coordinates: 18°11′33"S, 57°34′05"W
    - Lake area: 150 km
    - Water depth: 4–6 m
    - Elevation: 90 masl
    - Max core depth: 68 cm
    - Sediment: Organic clay - unconsolidated
    - Collection method: 5 cm diameter Perspex tube, piston, sliced into 1-cm intervals
  - Laguna Mandior e core M5 (collection date 2001)
    - Coordinates: 18°5′30"S, 57°33′45"W
    - Lake area: 150 km
    - Water depth: 4–6 m
    - Elevation: 90 masl
    - Max core depth: 77 cm
    - Sediment: Organic clay - unconsolidated
    - Collection method: 5 cm diameter Perspex tube, piston, sliced into 1-cm intervals
  - Laguna Mimoso (collection date 2019)
    - Coordinates: 16°15'14.79"S, 55°45'7.10"W
    - Lake area: 1 km
    - Water depth: <1 m
    - Elevation: 135 masl
    - Max core depth: 112 cm
    - Sediment: Organic clay - consolidated
    - Collection method: 5 cm diameter PVC tube, sliced into 1-cm intervals
  - Laguna Caceres (collection date 2020)
    - Coordinates: 19°7'8.77"S, 56°53'3.33"W
    - Lake area: 0.1 m (area unit appears to be mis-stated in table)
    - Water depth: <1 m
    - Elevation: 88 masl
    - Max core depth: 84 cm
    - Sediment: Organic clay - consolidated
    - Collection method: 7 cm diameter PVC tube, sliced into 1-cm intervals

- Quality control and processing
  - Standard laboratory procedures for charcoal fragment preparation and counting.
  - Deflocculation protocols depend on sediment type:
    - Clay-rich sediments: 7% sodium hexametaphosphate (Na6P6O18), 200 ml
    - Organic-rich sediments: 10% potassium hydroxide (KOH), 200 ml
  - Heating: samples deflocculated at 80°C for 30 minutes.
  - Post-processing: residues washed, sieved at 125 μm and 250 μm; counting performed under a microscope in a Bogorov tray.
  - Volume measurement: sediment volumes determined by water displacement.
  - Data recorded at 1-cm resolution, with 125 μm and 250 μm fractions reported.

- Radiocarbon dating provenance and format
  - Dates come from commercial laboratories (Beta Analytic and UGAMS) and are reported as uncalibrated conventional radiocarbon years BP.
  - Each core’s CSV includes header sections with date details; depths correspond to resin depths for charcoal data alignment.
  - Example dates (uncalibrated, illustrative):
    - Caceres: samples at 41 cm (1940 ± 30 BP), 21 cm (1150 ± 30 BP), 13 cm (260 ± 30 BP) with associated d13C values.
    - Mandiore surface core: dates at 60 cm (3120 ± 30 BP), 44 cm (1690 ± 30 BP), 26 cm (1050 ± 30 BP).
    - Mimoso: dates at 46 cm (850 ± 80 BP) and 20 cm (310 ± 30 BP).
  - Full laboratory reporting is provided for each date within the data.

- Metadata, documentation, and governance
  - Table 1 provides core-site metadata (coordinates, lake area, depth, elevation, core depth, sediment type, collection method).
  - Table 2 details radiocarbon dating information (number of dates per core, dating providers, date units, data structure, and lab reporting).
  - Units and data structure explicitly defined: charcoal concentration per cm³ at each 1-cm horizon; radiocarbon dates as uncalibrated ages with depth-aligned horizons.

- Considerations for data leaders and future use
  - Data are organized by core with horizon-level resolution, enabling age-depth reconstruction and cross-core comparisons.
  - Radiocarbon ages are uncalibrated; users may need to calibrate dates prior to chronological interpretation.
  - Consistency of units and metadata across cores supports discoverability and integration into broader Pantanal paleoenvironment datasets.
  - Documentation includes explicit quality control procedures, enhancing data reliability and reproducibility.
  - Potential enhancements for data systems: standardizing calibration metadata, ensuring consistent depth units, and providing a unified access point or DOI for dataset versions.