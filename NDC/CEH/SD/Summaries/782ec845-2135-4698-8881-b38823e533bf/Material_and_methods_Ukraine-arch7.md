# Spatial datasets of radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone

## Overview
- A comprehensive set of spatially-referenced radionuclide data from the Ukrainian Chernobyl Exclusion Zone (CEZ), designed for map-based visualization and GIS analyses.
- Integrates soil sampling, radionuclide activity measurements, depth profiles, hot-particle data, and regional surveys to enable spatial interpretation of contamination patterns.

## Data coverage and sampling design
- Sampling conducted at about 1200 sites within a 36 km radius around ChNPP between July 1995 and September 1997.
- Sampling grid with approximate inter-site distance of 1.2 km; higher density (100–500 m) in the western narrow trace with high contamination gradients.
- Most sampling done by helicopter; forest sampling used motor vehicles.
- Site coordinates determined with a GPS receiver (ScoutMaster) using WGS-84; reported GPS accuracy about 100 m with a systematic deviation around 300 m.
- Envelope method used for composite soil samples (five sub-samples from cores, 2–5 m apart, to 30 cm depth; total mass ≥ 2 kg).
- Depth of sampling set at 30 cm due to high association of 90Sr with upper 10–20 cm a decade after the accident.
- Additional sampling along multiple traces to assess variability in physical/chemical characteristics of deposited fuel particles.

## Soil sampling and preparation (general protocol)
- Soil samples dried, sieved to 1 mm, homogenized, and subdivided for radionuclide analyses.
- Sub-sampling for gamma-emitting radionuclides (Ci, Bq/kg) via four sub-samples (three 100 cm3, one 1000 cm3 in Marinelli geometry).
- Gamma-spectrometry with HPGe detectors (≈30% efficiency, ≈1.90 keV FWHM at 1333 keV) and GammaVision32 software; activity calibration using spike standards.
- Sub-sample consistency checks: if (Cmax − Cmin)/(Cmax + Cmin) > 0.15 for 137Cs, sub-samples are bulked and re-analysed; once within 0.15, a representative 100 cm3 sub-sample is used for 90Sr analysis.
- 90Sr determined radiochemically (Pavlotskaya 1997) after dissolution and separation; 90Sr:90Y equilibrium used for measurement with a low-background beta-counter.
- Quality assurance aligned to ISO/IEC 17025 standards; selected analyses validated by proficiency testing.

## Main radionuclides measured (gamma spectrometry)
- Gamma-emitting radionuclides measured: 137Cs, 154Eu, 241Am, 85Sr, and others as part of quality checks.
- 90Sr activity derived radiochemically; 90Sr:154Eu ratio used to discriminate fuel-particle binding and migration.

## Agrochemical characteristics
- Determination of humus (organic matter), pH (H2O and KCl), hydrolytic acidity, exchangeable Ca, K, and P using standard methods (GOST 26213-91, 26423-85, 26483-85, 26212-91, 26207-91, 26204-91).
- Mechanical soil composition recorded but not reported directly; soils classified according to USSR and FAO/UNESCO schemes.
- Table 2 (not reproduced here) maps soil types to conventional codes; some sites near village Bober had limited agrochemical data (only pH).

## Pu isotope measurements
- From 82 samples along the main traces of the Chernobyl release, Pu isotopes determined from homogenized 100 cm3 subsamples.
- Radiochemical separation using a standard Pu method; chemical yield tracked with 236Pu or 242Pu tracers; alpha spectrometry performed on the produced plates.
- An additional 12 samples collected in autumn 2000 analyzed with identical Pu-methodology, extending sampling to up to 200 km from the CEZ.

## Pu isotope measurements at different depths
- For eight sites, cores were sectioned into layers (0–2, 2–4, 4–6, 6–8, 8–10, 10–15, 15–20, 20–25, 25–30 cm) and analysed for Pu isotopes, 137Cs, and 90Sr.
- One additional site in 2001 extended to 110 cm depth with 10 cm slices, analyzing 238Pu, 239,240Pu, 137Cs, and 90Sr.

## Hot particles
- Early explosion released numerous UO2 fuel particles (median radius 2–3 μm) deposited up to ~100 km west of ChNPP; larger fragments deposited within 2–5 km.
- Regular sampling network established in CEZ in 1987–1989; >1,200 large hot particles (>10 μm) identified and isolated from soils within inner 30 km; ~500 additional particles collected 1989–1996.
- Particle types: mostly fuel particles (up to 97% in inner CEZ), with a minority of condensed ruthenium particles; fuel particles show activity corresponding to reactor fuel at accident time (excluding volatile radionuclides).
- Particle analysis involved gamma spectrometry, alpha spectrometry, and radiochemical separations; burn-up estimates used to infer the age/irradiation state of deposited fuel.
- Comparisons with Polish particles and other European datasets (for broad context) included.

## Estimation of remaining fraction of fuel particles
- Fraction of exchangeable 90Sr used to estimate undissolved fuel-particle fraction (DFP) via a method combining exchangeable and residue activities (85Sr and 90Sr yields, respectively).
- Equations and details describe calculation of leached fractions and the undissolved fuel-particle fraction, with special handling when 90Sr:154Eu ratio is low or when high leaching has occurred in sandy, low-humus soils.
- Data note: some negative values may occur due to measurement uncertainty and are treated as zero in usage.

## Ivankov region survey (2014)
- 3389 sampling points identified on a 1 km grid across Ivankov region and 3 km surrounding area; GPS coordinates with ≤10 m accuracy.
- Dose-rate measurements at 1 m and 0.1 m heights at 1 km intervals using certified dosimeters; background subtraction performed (cosmic and instrument background).
- 547 soil samples collected; 90Sr analysis via 0–30 cm samples; gamma analysis; natural radionuclides (40K, 226Ra, 232Th) also quantified.
- Reported ranges: 40K ≈ 140 Bq/kg; 226Ra ≈ 12 Bq/kg; 232Th ≈ 10 Bq/kg; 137Cs and 90Sr show elevated levels in eastern Ivankov; 1 m dose rates ranged 0.1–0.24 μSv/h.
- Data quality and QA reflect ISO-based protocols; results provide contemporary context for long-term radiological distribution in the region.

## Data quality, standards, and metadata
- QA/QA: ISO 18589-5:2009 for soil analysis; ISO/IEC 17025-compliant laboratories; proficiency testing references (IAEA, etc.).
- Use of recognized references and standards (GOST, UNSCEAR, FAO/UNESCO soil classification) to support metadata and comparisons.
- Uncertainties and data caveats noted, including potential underestimation in fuel-particle-rich western traces and handling of negative values.

## How these data support GIS and map-based products
- Provides multi-layer spatial data: radionuclide activities (137Cs, 90Sr, Pu isotopes, 154Eu, 241Am, etc.), dose rates, soil types, and depth-resolved information (0–30 cm and deeper cores).
- Enables creation of 2D and 3D GIS layers: surface contamination density, vertical distribution, hot-particle presence, and burn-up-related radionuclide compositions.
- Supports interpolation and spatial analysis across the CEZ (including Ivankiv region) for risk assessment, exposure modeling, and historical comparisons.
- Datasets are linked to published metadata and references, with data products available through the NERC Environmental Information Data Centre and related studies (e.g., Kashparov et al., 2017).

## Notable datasets and references
- Spatial datasets of radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone (Kashparov et al., 2017), NERC EIDC.
- Ivankov (Ivankiv) region study (2014) with dose-rate and radionuclide measurements, including 40K, 226Ra, 232Th, 137Cs, and 90Sr.
- Pu isotope, hot-particle, and depth-profile publications referenced throughout the methodologies.