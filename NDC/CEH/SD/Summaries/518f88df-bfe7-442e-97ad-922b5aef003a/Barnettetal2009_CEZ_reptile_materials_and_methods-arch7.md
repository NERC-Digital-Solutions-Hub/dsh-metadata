# Materials and methods for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERCEnvironmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7442e-97ad-922b5aef003a

## Overview
- Describes radionuclide activity concentrations in two reptile species from the Chernobyl Exclusion Zone (CEZ).
- Study period: 2000–2007; two CEZ sampling sites near the Red Forest.
- Data and methods supporting a dataset (CEZ_reptile_data.csv) and metadata (CEZ_reptile_metadata.rtf).

## Geospatial context and sites
- Two CEZ sites near Red Forest:
  - Red Forest 1: coordinates E 30.06188, N 51.38427; area ~0.15 km2 (triangular).
  - Red Forest 2: coordinates E 30.06405, N 51.38095; area ~0.01 km2 (square).
- Sites located about 2.6–2.7 km SW of the Chernobyl power plant.
- Reptile sampling occurred within defined site boundaries; soil sampling conducted at respective sites.

## Study species and sampling
- Species: Lacerta agilis (sand lizard) and Natrix natrix (grass snake).
- Captures: 20 L. agilis and 5 N. natrix over seven years.
- Capture methods: L. agilis captured in Shermann traps; N. natrix captured by hand.
- Specimens stored frozen; GI tracts removed; carcasses washed prior analysis.
- Soil cores: Red Forest 1 had 345 cores (June 2001); Red Forest 2 had 4 cores (May 2007).

## Radionuclide measurements in reptiles
- Whole-body content measured for:
  - 137Cs (cesium-137)
  - 90Sr (strontium-90) via its daughter 90Y
- Instrumentation:
  - Hyperpure germanium detector for 137Cs
  - Thin-film NaI detector for 90Sr
  - Spectra analyzed with Canberra Genie 2000 software
- Preparation and analysis:
  - Reptiles placed in cardboard boxes within a lead-shielded counting container
  - 137Cs activity derived from gamma spectra; 90Sr from 90Y data

## Radionuclide measurements in soils
- Soil samples: 0–10 cm depth
- Measurement methods mirror reptile analyses for 137Cs
- 40K counted with gamma detectors; counting error target <20%
- 90Sr in soils determined via sub-sample measurement of 90Y using a thin-film NaI detector
- Pu isotopes (238Pu, 239,240Pu) measured using radiochemical separation:
  - Digestion in 65% HNO3
  - 242Pu yield tracer added
  - Anion exchange (Bio Rad AG 1×8, 100–200 mesh)
  - Co-precipitation
  - Counting with a planar ion-implanted silicon detector
- Pu data rely on Lx-radiation from uranium daughter isotopes after α-decay

## Data products and formats
- Primary reptile data: CEZ_reptile_data.csv
- Metadata descriptor: CEZ_reptile_metadata.rtf
- Data types include species, site, year, sample type (reptile/soil), radionuclide concentrations (137Cs, 90Sr, 238Pu, 239,240Pu, 40K), and measurement details

## Data quality, limitations, and notes
- Soil core coverage varies by site (many cores at Red Forest 1 vs. few at Red Forest 2)
- Measurement uncertainty includes:
  - Target counting error thresholds (e.g., <20% for 40K)
  - Reported uncertainties for 137Cs and 90Sr from spectrometry
- Small sample sizes for reptiles, especially per species per year, may limit statistical power
- Complex, multi-method radiochemical analyses require careful QC and cross-method validation

## GIS considerations and how to use
- Georeferenced site coordinates enable spatial mapping of radionuclide burdens in reptiles and soils.
- Potential GIS applications:
  - Create per-site, per-species radionuclide distribution maps
  - Overlay with distance-to-plant, soil characteristics, or habitat features
  - Integrate with other CEZ datasets to assess exposure gradients and ecological risk
- Data integration notes:
  - Ensure consistent coordinate reference system when joining with other spatial layers
  - Align sample-level reptile data with site polygons and soil core locations
  - Consider temporal context (2000–2007) when analyzing trends

## References and data provenance
- Bondarkov et al. references (2002–2003) for radiochemical methods
- Related radiological studies on CEZ wildlife (2009; Barnett et al.)
- Data and metadata accessible via NERC Environmental Information Data Centre; see mentioned CSV and RTF files for details