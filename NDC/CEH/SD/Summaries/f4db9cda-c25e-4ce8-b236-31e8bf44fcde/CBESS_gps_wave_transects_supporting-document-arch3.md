# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats.

## Overview
- A dataset detailing GPS locations and associated metadata for wave monitoring devices and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Centers on surface elevation relative to a Rod Surface Elevation Table (rSET) instrument and the depths of sediment deposited over feldspar marker horizons.
- Staff: Tom Spencer and Ben Evans.
- Uses globally standardised SET methodology to enable inter-comparability across networks.

## Sites and design
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Habitat contrasts: saltmarsh and mudflat sites chosen to represent different sediment types (clay soils in Essex; sandy soils in Morecambe Bay) and differing inundation, creek structure, and vegetation.
- Sampling framework: two observations within a one-year monitoring period.
- Site and horizon setup designed to support cross-site comparisons of sedimentation dynamics and surface elevation.

## Methods and instrumentation
- Instrumentation: Rod Surface Elevation Table (rSET) with receivers bolted to bespoke benchmark rods, and 50 cm x 50 cm marker horizons of potash feldspar installed for horizon depth measurements.
- Installation: SET benchmarks installed autumn 2012; multiple observers used to drive rods into substrate, then sealing with drainage pipes around the benchmark.
- Observation protocol: readings taken every 3–6 months at nine pins arranged in four quadrants around each benchmark; horizons cores collected contemporaneously with SET measurements.
- Data provenance: rSET method referenced to Cahoon et al. (2002) for high-precision wetland sediment elevation measurements. Global GNSS (Leica GS08) used to determine benchmark coordinates.
- Calibration and quality: Leica RTK corrections used in real time where applicable; accuracy of GPS locations better than 50 mm in all directions in OSGB1936 coordinates.

## Data and variables
- Primary variables: heights at Pins 1–9 and marker horizon depths for cores 1–3.
- Temporal scope: measurements conducted at standardized intervals over a one-year monitoring period.
- Data structure: observations recorded in Excel spreadsheets with a detailed dataset header and field descriptions; rows include date, time, location, site, habitat, quadrat/scan parameters, SET number, Pin readings, horizon depths, and notes.
- Metadata and notes: notes on readings capture potentially significant factors; NA values indicate non-performed measurements; coordinates and site descriptions accompany observations.
- Data accessibility: GPS locations for benchmarks and horizons are contained in the CBESS_gps_wave_transects dataset; field formats and data fields are documented within the dataset.

## Data governance, quality, and access
- Data formats: data stored in Excel spreadsheets; descriptive field metadata provided within the dataset.
- Quality control: standardized procedures described; transformation and cleaning steps implied to ensure comparability.
- Data sharing and governance: notes indicate public sharing of underlying data can be a barrier in some contexts; dataset documentation provides transparency on methods and provenance.
- Open data considerations: metadata, calibration procedures, and site-specific details are documented to support reuse and verification.

## References and related datasets
- Foundational reference: Cahoon, D. R. et al. (2002) on high-precision measurements of wetland sediment elevation using SET.
- Associated dataset: CBESS_gps_wave_transects contains GPS coordinates for benchmarks and horizons to support site replication and cross-study comparisons.

## Relevance for monitoring policy and decision-making
- Demonstrates a structured approach to coastal environmental health monitoring, combining physical habitat measurements (elevation, sediment depth) with precise geolocation data.
- Provides a replicable framework that can inform policy decisions on coastal resilience, habitat management, and long-term monitoring plans.
- Highlights data governance considerations (data availability, metadata quality, data sharing) that are critical for transparent, policy-relevant monitoring programs.
- Emphasizes the need to manage data silos, ensure timely data access, and maintain metadata to enable external scrutiny and evidence-based decision-making.