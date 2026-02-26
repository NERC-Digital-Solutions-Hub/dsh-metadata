# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

## Overview
- Dataset documenting GPS locations for instruments and marker horizons used in wave monitoring and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Aims to enable inter-comparability and discovery by ensuring standardized data collection around CBESS monitoring points.
- Staff responsible: Tom Spencer and Ben Evans.

## Dataset contents and scope
- Basic description: Surface elevation relative to a rod SET instrument on local benchmarks, and depths of sediment deposited above feldspar marker horizons adjacent to SET benchmarks.
- Monitoring design: Installations and measurements initiated in autumn 2012, with observations taken twice over a 1-year monitoring period.
- Variables observed: Heights at pins (Pin 1–9) and horizon depths at marker horizons (Core 1–3).
- Instrumentation and standardization: Rod Surface Elevation Table (RSET) used to enable inter-comparability across the global network; detailed design described in Cahoon et al. (2002) and at USGS RSET resource.
- Data management: GPS coordinates and related metadata are recorded and stored in Excel spreadsheets; related field descriptions and data formats are documented.

## Locations and site descriptions
- Essex sites (saltmarsh and mudflat contrasting soils):
  - Abbotts Hall (AH): 51.783 N, 0.8667 E
  - Fingringhoe Wick (FW): 51.8167 N, 0.9667 E
  - Tillingham Marshes (TM): 51.6833 N, 0.9333 E
- Morecambe Bay sites:
  - Cartmel Sands (CS): 54.1667 N, 3.0000 W
- Habitat and soil contrasts:
  - Saltmarsh habitats with two soil types: clay soils in Essex and sandy soils in Morecambe Bay.
  - Mudflat sites in Essex: cohesive clays, mud and silt; Morecambe mudflats: predominantly coarse, mobile sediments.
- Broader site differences: Essex and Morecambe Bay saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation.

## Measurements, procedures, and data collection
- Monitoring timing: Measurements occur every 3–6 months around SETs and horizons within a 12-month period.
- SET installations: Benchmark rods installed by driving into substrate (6–12 m depth) with receivers bolted to rods and cemented into竖 plastic pipes around the benchmark.
- Pin readings: Nine pin measurements per SET quadrant (four quadrants around each benchmark).
- Marker horizons: 50 cm × 50 cm feldspar horizons installed just beyond instrument reach; depth of sediment above horizons measured via cores.
- Core handling and depth interpretation: If horizon depth is not horizontal, depths averaged from three sides; if less than 1 mm of sediment present, recorded as 0 mm; 'NA' used when horizon not detectable.
- Observational notes: Field notes recorded for potentially significant factors affecting results within spreadsheets.
- Coordinates and accuracy: SET benchmarks and Horizon GPS coordinates collected with Leica GS08 GNSS; accuracy better than 50 mm in all directions; coordinate system OSGB1936 (2).

## Data structure, formats, and documentation
- Data formats: Data recorded in Excel spreadsheets; field descriptions and dataset structure documented (e.g., headers, row numbering, and field definitions).
- Dataset fields include: Description, location (Morecambe/Essex), site, habitat, quadrat, scale, record number, date, time, SET number, Pin readings (1–9), marker horizon depths (core 1–3), notes/comments, and related metadata.
- Related dataset: GPS locations of benchmarks and marker horizons are contained in the associated dataset "CBESS_gps_wave_transects".
- References and provenance: Methodology linked to Cahoon et al. (2002) for high-precision elevation measurements using RSET; real-time Leica RTK corrections used for calibration.

## Data quality, completeness, and governance
- Quality indicators: Confidence intervals for individual pin readings cited (±4.3 mm per Cahoon et al. 2002); precise GNSS accuracy claimed (better than 50 mm).
- Data completeness considerations: Some fields marked as NA (not applicable or not performed); data checking procedures noted as NA in some entries, indicating potential gaps in formal QA documentation.
- Metadata and standards: Emphasis on standardized RSET methodology to enable cross-network comparability; clear documentation of file formats and field meanings to support interoperability.
- Update and stewardship: Dataset designed to be updated with ongoing measurements and related CBESS data (e.g., CBESS_gps_wave_transects) to support dataset discoverability and reuse.

## Access, usage, and governance considerations for Data Stewards
- Access points: Core GPS locations and related metadata are stored in the CBESS_gps_wave_transects dataset; primary dataset includes detailed instrumental and horizon measurements.
- Reuse considerations: Clear methodological references (Cahoon et al. 2002) and instrument standards (RSET) to support reproducibility and cross-study comparisons.
- Metadata to maintain: Site descriptions, habitat classification, coordinates with OSGB1936 reference, accuracy, measurement cadence, and note fields documenting influential factors.
- Data provenance: Documentation links to original measurement procedures and calibration steps (Leica RTK corrections); references provided for traceability.

## Contact and responsibility
- Primary contacts: Tom Spencer and Ben Evans (dataset staff responsible for data collection and management).