# Summary

- LOCATE was a multidisciplinary NERC project (National Oceanography Centre, British Geological Survey, UK Centre for Ecology and Hydrology, Plymouth Marine Laboratory) with university and Environment Agency involvement, aimed at understanding carbon flow from land into the ocean across Great Britain. Part 2 contains ICP-MS results from river samples; Part 1 covers river water parameters and has a companion estuary dataset. Part 2 data can be linked with Part 1 and estuary datasets via provided references and additional materials (locate_river_info.txt documents rivers sampled).

- Data scope and sampling design:
  - Monthly sampling in 2017 from 41 rivers across England, Scotland and Wales; additional samples in November 2016 (trial). Dorset Stour (DSTO) had an adjusted schedule (not sampled in most months; started Apr 2017).
  - Sampling sites coordinated to align with HMS sites for data integration. Most sites sampled within a 2–3 day window each month; a few weather-related exceptions noted.

- Experimental procedures and field practices:
  - In-field processing for most samples; POC samples filtered later in the lab.
  - Samples kept dark and cold (cool box or freezer) throughout handling.
  - Field measurements: salinity, electrical conductivity (SEC), and temperature were recorded in the field where possible; if salinity probes were unavailable, sealed bottles were analyzed later, with temperature still recorded.
  - Sampling depth typically 0–30 cm at mid-channel; sampling vessels rinsed to avoid contamination; gloves worn during collection.
  - Sample packaging and transport: bottles for ICP-MS (60 mL) and isotope samples (20 mL glass vials) were prepared and acidified on return to the institute to 1% HNO3; blanks prepared from MQ water acidified similarly.
  - Transport to BGS Keyworth laboratory for acidification and analysis.

- ICP-MS analyses and QA/QC:
  - Instrument: Agilent 8900 ICP-QQQ; method Ag_2.3.21 for major and trace elements; units in mg/L or μg/L.
  - Sample type: 0.45 μm filtered water acidified to 1% HNO3; post-receipt, samples further treated with 0.5% v/v HCl.
  - Quality control: UKAS ISO/IEC 17025:2017 accredited laboratory (UKAS number 1816).
  - QC procedures: three calibration blocks per run, QC stock reagents (LoQC 1, LoQC 2, HiQC 3, HiQC 2) with a comprehensive suite of elements; blanks and dilutions used to establish detection limits.
  - Detection limits: each element has two DL values presented in the data (Batch DL and Method DL); if a measurement is below DL, it is typically reported as < DL.
  - Data handling: results stored in a 61-column CSV file with detailed element concentrations (Ca, Mg, Na, K, P, S, Si, SiO2, Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, V, Cr, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, La, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Yb, Tm, Lu, Hf, Ta, W, Tl, Pb, Bi, Th, U) plus metadata fields.

- Data format and documentation:
  - Data are provided as a CSV with 61 columns, including fields such as LIMS code, River, Month, and concentrations for each element. Detection limits are described in separate lines within the element columns (Batch DL and Method DL).
  - Supporting metadata include sampling river details in locate_river_info.txt, which describes the rivers and sampling context.
  - Part 1 details (river water parameters) are published under a separate DOI and lodged with EIDC; companion estuary datasets are available via BODC. Part 2 data are associated with the LOCATE project and the BGS laboratory data stewardship processes.

- Access, provenance, and governance considerations:
  - Primary data producers and custodians include the BGS Keyworth laboratory and the LOCATE project partners; QA and accreditation are documented (UKAS ISO/IEC 17025:2017).
  - For data stewards, important provenance elements include: the sampling timeline (2016 trial; 2017 main campaign), site coordination (Andy Tye, BGS), field protocols, pre-analysis handling (acidification and storage), instrument and method specification (Agilent 8900, Ag_2.3.21), QC procedures, and DL reporting.
  - Related datasets and references are available through EIDC and BODC, enabling cross-dataset discovery and reuse with proper attribution.

- Practical implications for Data Stewards:
  - Ensure consistent metadata capture across Part 2 and Part 1 datasets to enable integrated discovery and reuse.
  - Maintain clear documentation of sampling windows, site changes (e.g., HMS site alignment), and any deviations (e.g., DSTO sampling timeline).
  - Preserve data lineage from field collection through laboratory analysis to the final CSV, including instrument settings, DLs, and QC results.
  - Manage unit standards (mg/L and μg/L) and handling of non-detects (< DL) within catalogs and downstream analyses.
  - Facilitate access via established portals (EIDC, BODC) and refer to locate_river_info.txt for site-specific context and sampling details.