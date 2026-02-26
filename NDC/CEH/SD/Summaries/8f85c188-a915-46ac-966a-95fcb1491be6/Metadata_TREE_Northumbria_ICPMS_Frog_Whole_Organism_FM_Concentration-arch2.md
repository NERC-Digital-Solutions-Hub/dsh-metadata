TREE_Northumbria_ICPMS_Frog_Whole_Organism_FM_Concentration

## Overview
- Dataset capturing concentrations of multiple elements in frog whole-organism tissue (fresh mass) for environmental monitoring.
- Includes biological and sampling metadata (species names, site, date, sample descriptions, notes) alongside multi-element concentration data.
- Aimed at consistent reporting to support assessment of environmental health and policy performance over time.

## Data Schema and Key Variables
- Biological identifiers: Latin_Species_Name, Common_Species_Name
- Sampling metadata: Site, Date_Sample_Collected, CEH_Sample_Description, Notes (tissue/tissue-use context)
- Concentration measurements (in mg/kg fresh mass): I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Data conventions: Some concentrations use a less-than marker (e.g., <Be, <Ni, <U) to indicate upper-bound values; iodine (I) note indicates “Not calculated” in this dataset.

## Measurement Details and Units
- Unit for all concentrations: mg/kg fresh mass (FM)
- Notes indicate specific tissues used to calculate whole-organism concentrations
- Some fields marked as not calculated or as upper-bound values, affecting interpretation of those specific measurements

## Data Quality, Processing, and Standards
- Data are intended to be verified, quality assured, cleaned, and transformed prior to analysis
- Outputs are produced in clear formats (e.g., per-element concentrations) for standardised reporting
- Datasets are stored and uploaded to the appropriate data portals as part of the monitoring workflow

## Intended Use and Outputs
- Enable comparison of frog exposure/elemental burden across sites and time
- Support assessment of environmental health against standards or guidelines
- Provide a standardized basis for reporting to monitoring programmes and policy review

## Data Access, Storage, and Governance
- Datasets prepared for sharing with stakeholders; stored in approved portals
- Emphasis on enabling access to underlying data that underpin final outputs

## Challenges and Opportunities
- Challenge: increasing the value of the dataset by integrating with other relevant environmental data (avoiding single-use datasets)
- Opportunity: improve accessibility of underlying data used to create final concentration outputs to enhance scrutiny and reuse