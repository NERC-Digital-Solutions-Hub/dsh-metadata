# WP1 - Physico-chemical characterization of anaerobic digestate and biomass ash derived from UK bioenergy production (anaerobic digestion and thermal transformation)

## Overview
- Describes the AVAnD project (started January 2015; 3-year duration) and the physico-chemical characterization of two waste streams: anaerobic digestate and biomass ash.
- Digestates were collected from multiple UK industrial-scale anaerobic digestion plants across several batches (1st to 8th) at various times; ashes were collected from sites in Spain and the UK (six ash types in total).
- The WP1 dataset focuses on characterisation and formulation of waste blends; data for WP1 specifically include all batches, but WP1 data usage mainly corresponds to batches 1 and 2, with later batches used for other work packages.

## Data sources and scope
- Digestates: 5–10 kg per sample, sourced from end-of-process lines; batches span January 2015 to January 2018.
  - Batch timeline: 1st (Jan 2015), 2nd (Apr 2015), 3rd (Oct 2015), 4th (Mar 2016), 5th (Jun 2016), 6th (Sept 2016), 7th (Nov 2017), 8th (Jan 2018).
  - From batch 3 onward, only selected digestates (codes 4 & 5) were used beyond WP1.
  - Digestate source codes (DB1–DB4) indicate feedstock compositions (e.g., source-segregated food waste; mixtures including maize silage and other organics).
- Biomass ashes: 10–20 kg per ash sample; six ash types (fly and bottom fractions, bulk) from Spain and the UK; collected across batches including January 2015 and June 2016 (selected sources only for WP1-related work).
- All data in the dataset are those produced in-house; external laboratory results (when used) are noted separately (e.g., available N & P for Digestate batch 2).

## Sampling, handling, and storage
- Digestates:
  - Samples received as 5–10 kg; cooled and transported in appropriate containers with ice; stored in a cold room at <4°C until analysis.
  - For fresh digestates, no pre-processing (e.g., sieving) was performed; for dried analyses, samples were dried (60/105°C) to constant weight, milled, sieved to 1 mm, and stored at room temperature.
- Biomass ashes:
  - Each ash sample received as 10–20 kg; composite subsample taken, air-dried, ground/milled, sieved to pass 1 mm, and stored at room temperature.
  - For fully dried analyses, ashes were dried at 105°C to constant weight.

## Analytical methods and equipment
- A standard methods framework is used (described in TABLE 3, with modifications as needed) including:
  - pH: pH-meter (Mettler Toledo Seven Compact; Inlab Versatile Pro electrode).
  - Electrical Conductivity (EC): Conductivity meter (Jenway 4510).
  - Nitrogen forms: NO3−, NH4+, NO2− via Automated Flow Analyzer (with specific models listed).
  - Total Carbon (TC) and Total Nitrogen (TN): Elemental analyzer (Elementar Vario EL III).
  - Aqua Regia and Water-Soluble elemental analyses: ICP-OES (iCAP 6300; Thermo Fisher) with digestion (Microwave; MARSXpress) and extraction steps per BS EN and ISO standards.
  - Carbon/Nitrogen ratio (C/N): derived from TC and TN values.
- External laboratories:
  - Specific analyses performed externally include nitrogen and phosphorus forms (e.g., N-NO3, N-NH4, NO3-N, NH4-N) and other complementary analyses; procedures referenced (NRM laboratories and ISO/BS EN standards).
- Data interpretation and reporting:
  - Results are generally on a dry basis unless specified.
  - Replicates are analytical (originating from a bulk composite sample), with blanks indicating non-measured replicates or differing replicate counts.
  - The dataset documents the analytical methods used, the link between equipment and measured parameters, and the analytical formulas (e.g., C/N = TC/TN).

## Data structure and key variables
- Dataset notes:
  - The symbol BDL indicates readings below detection limits.
  - All replicates are analytical; the original sample is a bulk composite.
  - In-house data are presented; external laboratory data (when used) are flagged as such.
  - Blank spaces indicate missing measurements or differing replicate counts.
- Key measured parameters (examples from TABLE 3, with units and methods):
  - pH (unitless), EC (mS/cm), Dry Matter (DM, %), Loss on Ignition (LOI, %).
  - Nitrate (NO3−, g/kg), Ammonium (NH4+, g/kg), NO3-N and NH4-N (g/kg).
  - Water-soluble and Aqua Regia extractable elements: Ca, Mg, K, Na, Cu, Fe, Mn, Ni, Pb, Zn (various units: mg/kg, µg/kg).
  - Aqua Regia extractable elements: Ca, Mg, K, Na, P, S, Al, Cd, Co, Cr, Cu, Fe, Mn, Ni, Pb, Zn (units vary by element; e.g., mg/kg or µg/kg for some).
  - For each parameter, data are linked to origin (sample type), batch, and specific subtypes (e.g., biomass ash subtypes like fly/bottom; digestate batch numbers).

## Data use, interpretation, and limitations
- Purpose: to characterize and inform formulation of waste blends for WP1, enabling insight into physico-chemical properties relevant to biowaste treatment and agronomic applications.
- Data coverage:
  - Digestate data primarily cover batches 1–2 for WP1 purposes, with subsequent batches included for broader WP coverage.
  - All batches are included in the dataset for completeness of characterisation across the waste streams.
- Data quality notes:
  - Some data for digestate batch 2 (Available N & P) are external-lab results and left blank in the in-house dataset.
  - The dataset is designed to support end-user exploration (e.g., dashboards, pivot views) with self-serve access to chemical composition, moisture/dry basis, and elemental extractability.
- Practical considerations for users:
  - Pay attention to units (dry basis vs. as-received) and batch/sample metadata (source codes, feedstock composition, ash subtype).
  - When comparing WS (water-soluble) vs AR (aqua regia soluble) fractions, ensure consistent interpretation of extraction methods and digestion procedures.
  - Consider the standards cited (ISO/BS EN) for methodological context and reproducibility.

## References and standards
- ISO/DIS 14820-2; BS EN 15002:2006; BS EN 16168:2012; BS EN 13137:2001; BS EN 13038:2011; BS EN 13037:2011; BS EN 14346:2006; BS EN 15169:2007; ISO/DIS 13395; BS ISO 15958; DIN EN ISO 15681-2; BS EN 13652:2001; BS EN 13657:2002.
- These standards underpin sampling, preparation, extraction, and measurement of nutrients and elemental composition in waste, sludges, and soils.