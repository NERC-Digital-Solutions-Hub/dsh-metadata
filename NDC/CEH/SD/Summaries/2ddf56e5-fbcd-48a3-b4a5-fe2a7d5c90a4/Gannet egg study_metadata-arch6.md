# Predatory Bird Monitoring Scheme Egg Data

## Data Overview
- A metadata/schema for an egg contaminant dataset collected under the Predatory Bird Monitoring Scheme (PBMS).
- Used to support long-term temporal trend analysis of contaminant levels in eggs.
- PBMS reports and trend analyses are available for download at the PBMS results site (http://pbms.ceh.ac.uk/results.htm).

## Data Content and Measurements
- Temporal scope: Year (4-digit) corresponding to egg collection year.
- Spatial scope: Eggs collected from multiple sites worldwide, with site identifiers and descriptive location names.
  - Site 0: Ailsa Craig
  - Site 1: Bass Rock
  - Site 2: St Kilda
  - Site 3: Grassholm
  - Site 4: Scar Rocks
  - Site 5: Hermness
  - Site 6: Little Skellig (Ireland) with coordinates
  - Site 7: Great Saltee (Ireland) with coordinates
- Measurements (in homogenised egg contents and related matrices):
  - SHELL_INDEX: Indicator of eggshell thickness (units: mg/mm; references Ratcliffe 1970)
  - HEOD: Concentration of a specific organochlorine compound in egg contents (units: µg/g wet weight)
  - DDE: Concentration of DDE in egg contents (µg/g wet weight)
  - Hg: Total mercury in egg contents (units: µg/g dry weight)
  - PCB: Total concentration of certain PCBs above the retention time of a specific standard (µg/g wet weight)
  - PCB congeners (individual): Includes numerous congeners (PCB008, PCB018, PCB029, PCB028, PCB031, PCB052, PCB077, PCB101, PCB105, PCB114, PCB118, PCB123, PCB126, PCB128, PCB138, PCB149, PCB153, PCB156, PCB157, PCB167, PCB169, PCB170, PCB180, PCB189, PCB209, and others such as PCB141, PCB163, PCB171, PCB183, PCB187, PCB194, PCB199, PCB201, PCB205, PCB206) with units µg/g wet weight.
- Data flags and availability:
  - ND = None Detected
  - NA = Not Analysed
  - Many individual PCB congeners and some measurements may be ND or NA depending on the sample and analysis.
- Additional notes:
  - The dataset is designed for long-term trend analysis; outputs and reports are available from the PBMS site.

## Data Provenance and Purpose
- Generated as part of the Predatory Bird Monitoring Scheme.
- Aimed at enabling long-term temporal trend analysis of contaminant exposure in predatory bird eggs.
- Outputs published as reports on the PBMS website to support policy, research, and data-informed decision-making.

## Data Access and Usage
- Suitable for building dashboards, pivot tables, and self-service analyses to explore trends across sites, years, and contaminants.
- Can be combined with other PBMS outputs or external datasets to enhance interpretation.
- Users should be aware of data gaps (ND/NA markers) and potential variability due to patchy data and site-specific sampling.

## Data Quality, Gaps, and Challenges
- Data patchiness and varying availability across sites and years.
- Some measurements are not analysed (NA) or not detected (ND) in certain samples.
- Communication of complex chemical data (many congeners) requires careful interpretation when summarising to non-technical audiences.

## Key References and Further Information
- PBMS long-term temporal trend analyses and downloadable reports are available via the PBMS results site: http://pbms.ceh.ac.uk/results.htm
- Shell thickness interpretation follows Ratcliffe, D. A. (1970) on eggshell changes in birds.