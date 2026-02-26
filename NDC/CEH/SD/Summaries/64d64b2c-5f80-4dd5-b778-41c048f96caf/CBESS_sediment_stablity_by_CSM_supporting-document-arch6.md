# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sediment stability by Cohesive Strength Meter (CSM) in salt marsh and mud flat habitats

## Overview
- Dataset measures surface sediment stability using a Cohesive Strength Meter (CSM) across CBESS sites.
- Habitats: salt marsh and adjacent mudflats.
- Regions/sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Sampling design: 22 quadrats with 3–5 replicate measurements per quadrat.
- Temporal coverage: Morecambe Bay samples collected in winter and summer 2013; Essex samples collected in winter, early spring, and summer 2013.
- Lead staff: David M. Paterson.

## Dataset scope, locations, and context
- Geographic coordinates provided for each observation site.
  - Essex: Abbotts Hall (51.7833°N, 0.8667°W), Fingringhoe Wick (51.8167°N, 0.9667°W), Tillingham Marshes (51.6833°N, 0.9333°W).
  - Morecambe Bay: Cartmel Sands (54.1667°N, 3.0000°W), Warton Sands (54.1333°N, 2.8000°W), West Plain (54.1500°N, 2.9667°W).
- Coastal sites include saltmarshes and nearby mudflats; regional differences in inundation, creek structure, and grazing pressure noted.

## Measurement method (CSM)
- Instrument: Cohesive Strength Meter (CSM), designed to quantify sediment erosion threshold.
- Procedure: vertical water jet pulsed at sediment; test chamber embedded in sediment; jet energy increases until sediment erosion changes light transmission within the chamber are recorded.
- Output: results expressed as stagnation pressure of the jet on the sediment surface (Nm^-2); calibration ties jet weight/flow to this pressure.
- Data handling: multiple routines for erosion run protocols depending on substratum (sand vs. mud; stable vs. unstable).

## Calibration and data processing
- Calibration addresses inter-machine variability due to hardware differences; uses volume-based calibration (not firing pressure) per Vardy et al. 2007.
- Typical workflow:
  - Weigh CSM jets using a precise scale; compute jet volume/flow (Q) from weight data.
  - Remove anomalous results (timing-related peaks/dips in older CSMs).
  - Derive a machine-specific calibration equation relating stagnation pressure to jet parameters.
  - During campaigns, determine the erosion threshold as a 10% drop in light transmission; convert using the calibration equation to stagnation pressure.
- Maintenance: calibrate every six months; perform additional calibration before important campaigns; replace clogged filters if performance degrades.
- References for methods: Tolhurst et al. 1999; Vardy et al. 2007; Paterson 1989.

## Data structure, formats, and fields
- Format: Comma-separated values (.csv).
- Core fields (examples):
  - Season (Winter, Summer)
  - Location (Morecambe or Essex)
  - Site (e.g., CS, WS, WP, AH, FW, TM)
  - Habitat (Mudflat, Saltmarsh)
  - Quadrat Number (1–22)
  - Replicate (1–5; some replicates missing)
  - Original readings (converted to stagnation pressure, Nm^-2)
  - Calibrated stagnation pressure (Nm^-2)
  - Mean and standard deviation across replicates
  - Data quality indicators (ND indicates no data)
- Additional metadata: monitoring period (Winter/Summer 2013), sample identifiers, and notes on data checks and QA.

## Data quality, QA, and maintenance
- QA procedures include data checks for mathematical integrity, random re-checks (5 per 100 readings), and reassessment of outliers.
- Known issues with older CSM units (timing errors) are mitigated by removing anomalies before calibration.
- Regular calibration advised (every six months) and before major campaigns; potential for sensor wear or component fouling (e.g., filters) to affect performance.

## Usage, access, and references
- Data are suitable for cross-site comparisons of sediment stability across habitats and regions, with a clear calibration pathway to convert raw jet data to comparable stagnation pressures.
- Key references describing methodology and calibration:
  - Tolhurst, Black, Shayler, Mather, Black, Baker, Paterson (1999)
  - Vardy, Saunders, Tolhurst, Davies, Paterson (2007)
  - Paterson (1989) on CSM design and use