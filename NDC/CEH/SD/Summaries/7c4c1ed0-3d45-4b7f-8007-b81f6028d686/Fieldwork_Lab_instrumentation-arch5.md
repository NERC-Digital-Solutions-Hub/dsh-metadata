# Soil pools and properties

## Overview
- A comprehensive soil dataset capturing physical, chemical, biological, and isotopic properties from field-collected soils at the Glacier Bay field laboratory station.
- Measurements include moisture, organic matter, pH, bulk density, grain size, inorganic N species, nitrification/denitrification potentials, and stable isotope ratios (C and N) in soil and plant material.
- Data generated across multiple labs (field lab, University of Birmingham, Paris) with standardized methods and quality controls.

## Data collection and processing workflow
- Samples kept shaded and cool; processed within four days of collection at the field station.
- Field-moist soils sieved to 2 mm; 2 mm fraction used for gravimetric moisture, loss on ignition, and pH.
- Separate hand-core sample used to estimate bulk density after drying.
- Soil grain size determined via laser diffraction (Mastersizer) on prepared subsamples.
- Organic matter removal from dried subsamples using 0.1 M NaClO, heating, centrifugation; repeated until organic matter removal is complete.
- Grain size distribution obtained with dispersion solution and a 1-minute ultrasonic burst; Mie scattering used for sizing.
- Total soil water content calculated by multiplying gravimetric moisture by total soil weight from a referenced source.
- Soil extracts prepared with 10 g dry-weight soil and 80 mL 2 M KCl; samples agitated, filtered to 0.2 μm, frozen, and shipped for analysis.
- N species quantified: NH4+, NO2-, and NO3- via colorimetric methods (buffers, cadmium reduction, Griess reactions) with UV/Vis detection. LOD 0.05 μg/mL; accuracy ≥90%; CV <1%.

## Measurements and assays
- Nutrient pools:
  - Ammonium (NH4+), nitrite (NO2-), nitrate (NO3-) from KCl extracts; colorimetric assays performed; documented accuracy and detection limits.
- Microbial activity potentials:
  - Nitrification potential: nitrite oxidation monitored during a 30-hour incubation with NaNO2; end-point analyzed colorimetrically.
  - Net mineralization and net nitrification: 24-day unamended soil incubations to track NH4+ and NO3- accumulation.
  - Denitrification potentials: total denitrification (NO3- to N2) and partial denitrification (NO3- to N2O) assessed using acetylene inhibition; anaerobic jars (10 g soil, 10 mL water) incubated at 20°C with substrates; headspace N2O measured by GC with ECD; samples taken at 1 and 4 hours; CV < 2%.
- Isotopic analyses:
  - Natural abundance δ13C and δ15N in soil and plant tissue; total C and N measured with elemental analyzer and isotope-ratio MS.
  - All isotopic analyses performed at external facility; CVs: δ13C ≈ 0.2‰; δ15N ≈ 0.3‰.
  - Enrichment factor (εf-s) calculated as difference between foliar and soil δ13C and δ15N to assess fractionation and openness of the N cycle.

## Data governance, provenance, and quality
- Methods are described with instrument models, conditions, and calculation steps to enable reproducibility and auditability.
- Documented detection limits, accuracy, and precision (e.g., LODs, CVs) to inform data quality assessments.
- Sample provenance includes site, collection timing, processing steps, and cross-lab handoffs (field lab to Birmingham to Paris).
- Data management practices recommended: maintain detailed metadata for sample IDs, collection dates, locations, methods used, instrument calibration, and data processing workflows.
- Data sharing and dissemination:
  - Data should be uploaded to relevant portals and catalogues for discoverability, with clear metadata linking to methods and analytical provenance.

## Considerations for data stewardship
- Ensure interoperability across datasets by harmonizing units, terminology, and method citations (e.g., N species names, incubation conditions, isotopic conventions).
- Retain full traceability: chain-of-custody from field collection through laboratory analyses to final datasets.
- Accommodate multi-institution data integration (field lab, Birmingham, Paris) with centralized, machine-readable metadata schemas.
- Plan for updates or re-analyses (e.g., reprocessing samples, re-calibration) and document any versioning of datasets.