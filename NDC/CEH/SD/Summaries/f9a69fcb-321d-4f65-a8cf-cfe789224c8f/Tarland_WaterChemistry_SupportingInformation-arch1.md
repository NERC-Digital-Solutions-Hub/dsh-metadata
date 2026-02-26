# Tarland Burn Water Chemistry and Discharge Dataset (2000-2010)

## Overview
- Long-running case study in the Tarland catchment (NE Scotland) as part of a Scottish Government–funded program (~15 years).
- Aims to investigate water quality, habitat and biodiversity, diffuse pollution, and flood mitigation under intensive land management.
- Context includes rural community with many private septic tanks.

## Data Description
- Dataset covers mean daily flow (m3/s) and water chemistry data from the Tarland Burn, 2000–2010.
- Measured water chemistry determinands:
  - Total dissolved phosphorus (TDP), soluble reactive phosphorus (SRP), total phosphorus (TP), particulate phosphorus (PP)
  - Nitrate-N (NO3-N), ammonium-N (NH4-N)
  - Suspended solids (SS)
  - Dissolved organic carbon (DOC), total dissolved nitrogen (TDN)
- Derived nitrogen and phosphorus forms:
  - Dissolved organic N (DON) = TDN − (NO3-N + NH4-N)
  - Dissolved organic P (DOP) = TDP − MRP
  - Particulate N (PN) = TN − TDN
  - Particulate P (PP) derived from digest values for unfiltered samples (via TN − TDN and TP − TDP relationships)
- Sampling site: Coull, near the catchment outlet (coordinates provided).

## Water Sample Collection
- Weekly grab samples from 2000–2003; more frequent sampling during rainfall events.
- Feb–Mar 2004: daily samples with autosampler (ISCO 3700).
- Apr 2004–May 2005: daily sampling with autosampler and increased frequency (every 4 hours during storms).
- Post June 2005: sampling became more infrequent and irregular.
- Autosampler details: not refrigerated; housed in a wooden shed; samples returned to the lab in cool boxes.
- Sampling intervals ranged from 5–14 days at the site, with daily to storm-event–driven intensification during certain periods.

## Sample Analysis
- Filtration: unfiltered vs. filtered portions (Whatman 0.45 μm cellulose acetate filters) to separate suspended solids (SS) gravimetrically.
- Colorimetric analysis (within 24 hours): NO3-N, NH4-N, MRP (molybdate reactive P).
- Digestion: automated persulphate/UV digestion for TDN, TDP, and DOC; unfiltered samples digested to obtain NO-N and MRP for PN and PP calculations.
- Analytical instruments: San++ analyser (Skalar) for colorimetry.
- Calculations:
  - DON = TDN − (NO3-N + NH4-N)
  - DOP = TDP − MRP
  - PN = TN − TDN
  - PP = digest-derived particulate P (based on unfiltered sample results)

## Discharge Data
- Stage height calibrated against discharge using velocity-area profiling across the channel at 60% depth.
- Velocities measured with a Valeport propeller.
- Stage logged at 1-minute intervals; mean daily flow computed by defining a day as 9:00 am to 8:45 am to align with Met Office rainfall data.

## Site and Location Details
- Tarland Burn is the uppermost tributary of the River Dee.
- Location sample: Coull, NE Scotland (WGS84 57.111, -2.810; OSGB 351050, 802540).

## Temporal Coverage and Data Gaps
- 2000–2010 coverage with variable sampling intensity:
  - 2000–2003: weekly sampling
  - 2004–2005: daily to storm-event–driven sampling
  - Post-2005: irregular sampling with gaps

## Potential Analyses and Uses
- Assess relationships between flow and nutrient species (dissolved vs. particulate fractions).
- Examine seasonal and storm-event responses in nutrient dynamics.
- Compare diffuse pollution impacts under different land-management practices and septic-tank contexts.
- Integrate with discharge data to explore hydrological controls on water quality.