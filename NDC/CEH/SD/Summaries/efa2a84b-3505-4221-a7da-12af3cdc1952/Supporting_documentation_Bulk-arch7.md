# Bulk density, carbon and nitrogen content in soil profiles from permafrost in subarctic Canada

## Overview
- Study of soil cores collected in 2013 and 2014 to compare peatland plateaus, thawing features, burnt vs unburnt black spruce forests, and additional sites.
- Measured bulk density, carbon content, and nitrogen content in soil profiles.
- Provides spatially explicit data with site codes and core identifiers, suitable for GIS-based analysis and map visualisations.

## Sites and sampling design
- Site codes and descriptions:
  - FFU: FireFox Unburnt (unburnt black spruce forest)
  - FFB: FireFox Burnt (burnt in 1998)
  - BLF: BlackFox
  - WHF: WhiteFox
  - TPP: Teslin Peatland Plateau
  - TW: Teslin Wetland Mid
  - TWM: Teslin Wetland Margin
  - MCU: Mosquito Creek Unburnt
  - MCB: Mosquito Creek Burnt
  - WTP: White Truck Plateau
  - WTM: White Truck Moss
  - WTS: White Truck Sedge
  - WTW: White Truck Wetland
  - BCB: Boundary Creek Birch
  - BCS: Boundary Creek Spruce
- Replicates: generally five soil cores per site (5 replicates), though some sites had 3–4 cores.
- Core coding example: TPP1, TPP2, TPP3, TPP4, TPP5 (coding for cores aligns with flux data naming but locations differ).

## Sampling methods and depth coverage
- Depth target: cores aimed to 1 meter; actual depth varied due to obstacles (e.g., rock).
- Frozen-ground sites (e.g., FFU, FFB, BLF, TPP, MCU, MCB, WTP, BCB, BCS):
  - Upper core portion sampled with a 40 x 10 x 4 cm tin foil insert to thaw depth.
  - Deeper soil sampled with a powerhead corer (typical 10–15 cm sections).
  - Core segments recovered, wrapped, and transported in sealed PVC tube halves.
- Non-frozen sites:
  - Tin foil used for the upper 40 cm; deeper sampling with a Russian corer; samples wrapped in half-cut PVC tubes.
- Transport: samples kept frozen in Canada until shipment to the UK.

## Laboratory processing and measurements
- In the UK:
  - Cores cut to record volume; samples analyzed for bulk density, carbon, and nitrogen.
  - Upper portions cut at 1 cm resolution for lead dating purposes; deeper portions usually in ~10 cm sections based on horizon uniformity (organic vs mineral or blend).
  - Samples freeze-dried, weighed to calculate bulk density; a subsample ground for C and N analysis.
  - Carbon and nitrogen contents measured by combustion; expressed as percent dry mass.
  - Calibrations and standards used for each batch of C and N analyses.
- Bulk density units: grams of dry soil per cubic centimeter of wet soil.
- Data columns include a Remarks field noting issues (e.g., potential BD over/underestimation due to roots, post-thaw vegetation changes) and the presence of a tephra layer (White River Ash) in some cores.

## Data interpretation notes
- Vegetation and soil profile changes associated with thaw (Postthaw vs Pre-thaw peat) are commonly observed and recorded in Remarks.
- Tephra layer (White River Ash) documented in some cores.
- Important caveat: soil profile data and flux data (CO2, CH4) codes do not spatially match; coordinates provided in the soil data file may differ from those used for flux data. Example: soil profile information for TPP1 does not spatially correspond to flux data for TPP1.

## GIS and data integration considerations
- Suitable for creating map layers of bulk density, carbon content, and nitrogen content by depth and by site.
- Depth-resolved data enable vertical profile visualisations alongside site polygons/points.
- When integrating with flux data or other datasets, account for non-matching spatial locations between soil profiles and flux measurements.
- Data quality caveats:
  - Depth limits due to rock or thaw depth.
  - Variation in core count per site (5 vs 3–4 replicates).
  - Potential BD measurement biases from roots or partial core recovery.
  - Variability in sampling depth intervals (1 cm for upper sections; ~10 cm for deeper sections).