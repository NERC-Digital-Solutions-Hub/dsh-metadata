# Predatory Bird Monitoring Scheme Data: Egg Contents and Contaminants

## Overview
- A dataset aligned with the Predatory Bird Monitoring Scheme that records egg-level data across multiple breeding sites, including collection year, site location, shell thickness indicator, and chemical contaminant concentrations.
- Generated to support long-term temporal trend analyses; related reports are available on the PBMS website.

## Data fields, structure, and units
- Ref, Description: Unique alpha-numeric egg identification code.
- Year (4digit): Year the egg was collected.
- Site, Description: Location of the colony where the egg was collected. Includes site names and coordinates (e.g., Ailsa Craig, Bass Rock, St Kilda, Grassholm, Scar Rocks, Hermness, Little Skellig, Great Saltee).
- Site, Classes/Units/CAS Number: Site code and corresponding metadata, including geographic coordinates for several sites.
- SHELL_INDEX: Indicator of eggshell thickness as described by Ratcliffe (1970). Units: mg/mm². Designated as NA (Not Analysed) when not available.
  - Description notes the historical reference for eggshell changes due to pesticides.
- HEOD: Concentration of a specific organochlorine compound in homogenised egg contents. Units: µg/g wet weight. CAS number provided for the compound; ND indicates None Detected or NA if not analysed.
- DDE: Concentration of the dichloroethenylidene biphenyl compound in homogenised egg contents. Units: µg/g wet weight. CAS number provided; ND/NA as applicable.
- PCB: Total concentration of all detected congeners with retention times greater than the Dichlobenil standard. Units: µg/g wet weight. ND indicates None Detected; NA indicates Not Analysed.
- PCBxxxx (congeners): Individual PCB congeners (e.g., PCB008, PCB018, PCB029, PCB028, PCB031, PCB052, PCB077, PCB101, PCB105, PCB114, PCB118, PCB123, PCB126, PCB128, PCB138, PCB149, PCB153, PCB156, PCB157, PCB167, PCB169, PCB170, PCB180, PCB189, PCB209, etc.). Each has:
  - Description: Concentration of the specific congener in homogenised egg contents.
  - Units: µg/g wet weight (with ND/NA statuses similar to total PCB).
  - CAS Number: Provided where applicable.
- Additional Information: General notes. In this dataset, the field is present but unused beyond indicating its purpose (PBMS context).

## Site details
- Site 0: Ailsa Craig (NX019997)
- Site 1: Bass Rock (NT602873)
- Site 2: St Kilda (NF089994)
- Site 3: Grassholm (SM598092)
- Site 4: Scar Rocks (NX258332)
- Site 5: Hermness (HP607176)
- Site 6: Little Skellig, County Kerry, Ireland (coordinates 51°46'0"N, 10°32'0"W)
- Site 7: Great Saltee, Wexford, Ireland (coordinates 52°7'0"N, 6°36'0"W)

## Data quality and status indicators
- ND (None Detected): No detectable concentration for the specified analyte.
- NA (Not Analysed): The analyte was not analysed in this dataset.
- CAS Numbers provided for many chemicals to support traceability and cross-referencing.

## Data provenance and access
- Generated as part of the PBMS, which conducts long-term temporal trend analyses.
- PBMS results and reports can be downloaded from the PBMS website: http://pbms.ceh.ac.uk/results.htm

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle considerations:
  - Clear field naming and metadata (descriptions, units, CAS numbers) to support discoverability and interoperability.
  - Spatial metadata with site codes and geographic coordinates enabling cross-site comparisons.
  - Inclusion of data quality signals (ND/NA) and shell thickness context (SHELL_INDEX) for interpretation and prioritization.
  - Provenance linkage to a long-running monitoring program, supporting governance, reproducibility, and trend analyses.
- Highlights data system needs for Data Leaders:
  - Maintain consistent metadata standards and documented data provenance across data products.
  - Ensure discoverability and access to long-term datasets and reports.
  - Identify data gaps (e.g., analyses not performed, certain congeners not detected) to inform future data collection and sequencing.
  - Support cross-site collaboration by providing uniform site identifiers and location details.