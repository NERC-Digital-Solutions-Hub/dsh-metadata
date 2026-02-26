# Spatial radionuclide deposition data from the 60 km area around the Chernobyl nuclear power plant: results from a sampling survey in 1987

## Overview
- Dataset describing the radial network sampling of the 60-km zone around the Chernobyl Nuclear Power Plant (ChNPP) conducted in 1987.
- Measurements include dose rate in air at 1 metre and densities of soil contamination for radionuclides: 95Zr+95Nb, 106Ru, 134Cs, 137Cs, 144Ce, plus exchangeable 134Cs+137Cs.
- Reported densities are in Bq/m²; dose rates in mR/h. Uncertainties are provided at the 68% confidence level.
- Sampling achieved 489 of 540 planned points; sampling excluded swamps, rivers, and lakes.
- Data originate from one primary laboratory (UIAR) using a GEM-30185 ORTEC detector; four cores were analysed in other Soviet laboratories (data not available).

## Sampling design and data provenance
- Radial network established with sampling points every 10° (10° to 360°) at distances of 5, 6, 7, 8.3, 10, 12, 14.7, 17, 20, 25, 30, 37.5, 45, 52.5 and 60 km (540 total potential points; 489 sampled).
- Points georeferenced using maps and topography; sampling sites excluded if located in swamps, rivers, or lakes.
- Soil sampling performed with a 14 cm diameter corer to 5 cm depth; at each site five sub-samples collected within an envelope design (5–10 m apart).
- At collection, intact soil samples were kept in the corer to avoid cross-contamination; five cores per site were processed, one for primary analysis and four sent to other labs (data for these cores are not available).

## Measurements and analytes
- Dose rate: exposure in air at 1 m height, recorded per site.
- Gamma measurements: conducted on one 1 L Marinelli container per site to determine concentrations of gamma-emitting radionuclides: 95Zr+95Nb, 106Ru, 134Cs, 137Cs, 144Ce.
- Exchangeable Cs: 100 g soil aliquots leached with 1 M NH4OAc (pH 7) to determine the fraction of Cs-134+Cs-137 in exchangeable form.
- Activity concentrations converted to soil contamination densities: 1 Ci/km² = 37 kBq/m², accounting for sampled area (0.015 m² per site).
- Results include associated measurement uncertainties (68% confidence interval).

## Analytical methods and lab details
- Primary analysis: high-purity germanium gamma spectrometry (GEM-30185 ORTEC) with ADCAM-300 multichannel analyser (UIAR laboratory), results reported at 68% confidence.
- Additional cores from the same sampling site were analysed in different laboratories within the Soviet Union (data not available).
- Data capture includes instrument used and confidence level; timing: samples analysed within roughly 1.5 months of collection.

## Data quality, uncertainty, and limitations
- Uncertainty for site-average contamination density may be up to ~50% (per referenced methodology).
- Reported values are for the date of measurement; samples were analysed within 1.5 months of collection.
- Some core data are unavailable due to multi-lab processing; empty cells indicate missing data.
- Only a subset of the full planned points was sampled due to geographic exclusion and practical constraints.

## Data governance, documentation, and sharing considerations for Data Stewards
- Provenance: clearly document the 1987 sampling design (radial 60-km zone, 540 potential points, 489 sampled, 10° increments, distance classes).
- Metadata completeness: maintain definitions for each column (identifiers, geometry angles, distances, dates, dose rates, radionuclide densities, uncertainties, and instrument details) to enable discovery and reuse.
- Data standardization and interoperability:
  - Ensure consistent units (Bq/m² for densities, mR/h for dose rate) and the 1 Ci/km² = 37 kBq/m² conversion.
  - Maintain notes on empty cells and the meaning of missing data.
  - Preserve documentation of extraction methods for exchangeable Cs and gamma spectrometry procedures.
- Data quality management:
  - Track measurement uncertainties (68% confidence) and the potential ~50% site-average uncertainty.
  - Record lab provenance for each core and note unavailable datasets from other laboratories.
- Access, storage, and sharing:
  - Prepare the dataset for deposition into data portals and catalogue holdings with complete lineage (dataset origin, sampling design, lab analyses, and date of measurement).
  - Include instrument specifications (GEM-30185 ORTEC; ADCAM-300) and measurement timelines to support reproducibility.
- Usage guidance:
  - Provide clear definitions for density units (Bq/m²) and dose-rate units (mR/h), including the conversion factors used.
  - Highlight limitations due to partial data availability and the retrospective nature of the study (1987 sampling).

## References
- Kashparov, V., Levchuk, S., Zhurba, M., Protsak, V., Beresford, N.A., Chaplow, J.S. Spatial radionuclide deposition data from the 60 km area around the Chernobyl nuclear power plant: results from a sampling survey in 1987. Earth System Science Data, 2019 (in press).
- Khomutinin, Yu.; Fesenko, S.; Levchuk, S.; Zhebrovska, K.; Kashparov, V. Optimising sampling strategies for emergency response: 1. Soil. Journal of Environmental Radioactivity, 2019 (in press).