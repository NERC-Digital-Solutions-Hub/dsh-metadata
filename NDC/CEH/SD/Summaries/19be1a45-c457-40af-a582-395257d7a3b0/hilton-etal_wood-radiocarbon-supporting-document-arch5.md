# Radiocarbon measurements on river wood deposits, Mackenzie River, Canada

## Overview
- A dataset of radiocarbon measurements from large wood (LW) deposits in the Mackenzie River delta, Northwest Territories, Canada, collected to constrain sources and ages of wood carried by the river system draining into the Arctic Ocean.
- Fieldwork conducted in August 2019 across multiple depositional environments to achieve broad spatial coverage (longitudes ~132W–135W, latitudes ~67N–69N).
- 42 sites visited; up to three LW samples collected per site; outermost growth-ring constraint due to weathering issues.

## Data collection and scope
- Sample collection: axe used to extract outer wood pieces (2–5 cm) from LW without bark to constrain earliest growth rings.
- Sample type coverage: large log pieces, small pieces, buried wood, and river cut banks descriptors captured.
- Depositional and site metadata recorded: region, site name, cover type, depositional landform, and depositional environment.

## Data fields and units (metadata)
For each sample (77 entries in the dataset):
- Sample identifier and measurement batch code
- Latitude and longitude (decimal degrees)
- Location descriptors: region and site name
- Wood physical data: diameter (cm) and length (m)
- Wood composition: carbon content of extracted cellulose (weight %)
- Isotopic composition: δ13C (‰, VPDB)
- Radiocarbon activity: Percent Modern (pMC) and Fraction Modern (F14C) with 1σ uncertainties
- Radiocarbon age: conventional age (years BP) with 1σ uncertainty
- Calibrated age ranges: upper and lower wood ages in AD (2σ), calculated with OxCal 4.4
  - Calibration curves: IntCal20 used when F14C < 1; Bomb21NH1 used when F14C > 1
- Sample descriptors: sample type, cover type, depositional landform, and depositional environment

## Quality control
- Quality control performed at NEIF Radiocarbon Facility involving blanks and analytical standards; analytical uncertainties reported at 1σ.
- δ13C corrections applied to normalize to VPDB -25‰ using measurements from a dual-inlet mass spectrometer.

## Data structure and accessibility
- Data file: CSV with 77 rows and 25 columns (A–Y).
- Purpose: enable robust dating of wood deposits and reconstruction of riverine wood transport/accumulation history.

## Experimental design and sampling regime
- Systematic sampling of LW carried by the Mackenzie River delta, designed to provide robust spatial coverage across the study area.
- Samples positioned to capture multiple depositional environments and wood sources along the river's course to the Arctic Ocean.

## Analytical methods
- Wood cellulose extraction: sequential chemical treatments (HCl, KOH, oxidizing steps with NaClO2 and HCl) to purify cellulose.
- Carbon analysis: total carbon recovered by combustion to CO2, graphite produced via Fe/Zn reduction for AMS measurement.
- AMS measurement: performed at SUERC; results reported as conventional radiocarbon years BP (AD 1950 reference) and F14C with ±1σ uncertainties.
- Isotopic correction: δ13C values corrected to δ13CVPDB = -25‰.

## Calibration and interpretation
- Radiocarbon results converted to calendar ages using OxCal v4.4.
- Calendar age ranges provided as 2σ lower and upper bounds (AD).
- Data support interpretation of wood deposition timing, transport pathways, and source characterization within the Mackenzie River system.
- Full discussion and context available in the publication:
  Sendrowski, A., et al., Wood-Based Carbon Storage in the Mackenzie River Delta: The World's Largest Mapped Riverine Wood Deposit, Geophysical Research Letters, 2023.

## Provenance and governance notes for Data Stewards
- Data provenance: measurements conducted at NEIF Radiocarbon Facility; AMS analysis at SUERC; subsequent calibration in OxCal informed by documented curves.
- Metadata richness supports discoverability and reuse (sampling strategy, site metadata, sample characteristics, analytical details, and calibration choices).
- Documentation aligns with standard radiocarbon data practices (1σ analytical uncertainties, explicit calibration curves for each sample, and explicit linkage to the publication for broader interpretation).
- Recommended governance actions:
  - Ensure repository inclusion with explicit metadata fields for sample identifiers, coordinates, site descriptors, material type, and calibration details.
  - Maintain traceability to lab facilities, measurement codes, and calibration curves used.
  - Preserve both uncalibrated radiocarbon results (BP, F14C) and calibrated age ranges (AD, 2σ) along with associated uncertainties.
  - Include publication reference and dataset versioning to support reproducibility and secondary analyses.