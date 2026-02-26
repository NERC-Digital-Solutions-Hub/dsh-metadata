# Spatial datasets of radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone

- The document describes extensive datasets on radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone (CEZ), combining soil sampling, radionuclide activity measurements, fuel particle investigations, and regional surveys. It covers primary CEZ sampling around the ChNPP (1995–1997), Pu-isotope analyses, depth profiling, hot particles, and supplementary regional data (Ivankiv region in 2014) and Polish particle data for comparison.

## Key components and coverage

- Soil sampling and site layout
  - About 1,200 sampling sites within a 36 km radius of ChNPP (July 1995–Sept 1997).
  - Grid-based site selection with ~1.2 km spacing; western trace sampling tightened to 100–500 m due to high gradients.
  - Most sampling done by helicopter; forest areas by motor vehicle.
  - At each site, absorbed dose rate at 1 m above ground measured; site homogeneity checked with DRG-01T dosimeters.
  - Coordinates determined by GPS (WGS-84); typical GPS accuracy ~100 m with a systematic deviation of ~300 m.
  - Envelope method used for composite soil samples: five 37 mm cores from corners and center over 2–30 cm depth; total mass ≥ 2 kg.

- Soil processing and radionuclide measurements
  - Samples dried, sieved (≤1 mm), homogenized; four sub-samples for gamma-emitting radionuclides (three 100 cm3 and one 1000 cm3 in Marinelli container).
  - Gamma measurement with HPGe detectors; typical counting ~1 hour (longer for lower activities).
  - Quality control: sub-sample replicates; if (Cmax − Cmin)/(Cmax + Cmin) > 0.15 for 137Cs, sub-samples are bulked/remixed and reanalyzed.
  - 90Sr determined by radiochemical method after dissolving sample; 90Sr:154Eu ratio used to assess leaching and to test depth adequacy.
  - 90Sr leachability and fraction of undissolved fuel particles (DFP) estimated via 2 M NH4Ac extraction with 85Sr tracer; calculations for D85Sr, D90Sr, and DFP provided; negative values treated as zero.

- Main agrochemical and soil-type context
  - Standard methods applied for humus (organic matter), pH (H2O and KCl), hydrolytic acidity, exchangeable Ca, K, P.
  - Mechanical soil composition recorded for USSR soil classifications; FAO/UNESCO codes also used for soil typing.
  - Some sites around village Bober included; limited agrochemical data there.

## Pu isotopes, depth profiling and hot particles

- Pu isotope measurements
  - 82 samples from main release traces analyzed for Pu isotopes using radiochemical separation, alpha counting with an alpha-spectrometer.
  - Chemical yield tracked with 236Pu or 242Pu tracers.
  - An additional 12 samples collected in autumn 2000 analyzed similarly; samples spanned distances up to 200 km outside CEZ in various directions.

- Pu depth profiling
  - Eight sites with cores sectioned into depth intervals (0–2, 2–4, 4–6, 6–8, 8–10, 10–15, 15–20, 20–25, 25–30 cm) for Pu isotopes, 137Cs, and 90Sr.
  - One site deeper (to 110 cm) with 10 cm slices for 238Pu, 239,240Pu, 137Cs, and 90Sr.

- Hot particles
  - Early-Chernobyl explosion produced numerous small (2–3 μm) uranium dioxide fuel particles and larger fragments (μm–100s μm) deposited within 2–5 km of reactor.
  - Data include particle type (fuel or condensed), size, and radionuclide activities (gamma for decay, alpha for fuel characterization); additional particles from inside the Shelter (sarcophagus) analyzed.
  - Particle burn-up values provided; analyses indicate lower burn-up in CEZ particles, reflecting younger fuel contributions.
  - Comparative data from Poland and other European sites (e.g., Bialystok, Gotland, Hungary) included to contextualize particle types (fuel-like vs condensed ruthenium-rich particles).

## Additional soil sampling campaigns and remaining fraction of fuel particles

- Soil sampling and preparation (CEZ baseline)
  - 115 soil samples collected (1995–1997) to reflect variation in physical and chemical characteristics of deposited particles.
  - Focus on narrow western trace (non-oxidized fuel particles) and oxidized traces in other directions; soddy podzolic sandy soils predominantly sampled.
  - 0–5 cm samples used for soil pH; 0–30 cm for Sr and related analyses; density of contamination from 90Sr ranged broadly (12 kBq m−2 to 60 MBq m−2).

- Estimation of remaining fraction of fuel particles
  - Fraction of exchangeable 90Sr determined to estimate undissolved fuel particles (DFP) using 85Sr yield and leaching data.
  - Calculation method uses exchangeable 90Sr and 85Sr data to compute D90Sr and D85Sr and derive DFP = 1 − (D90Sr / D85Sr).
  - If 90Sr:154Eu ratio is low, total 90Sr content is used to estimate undissolved fuel particles, due to potential leaching of 90Sr from sandy soils.

## Ivankiv region survey (2014)

- Large-scale grid-based survey
  - 3,389 sampling points on a 1 km grid across Ivankiv region and 3 km surrounding area; GPS (10 m or better) coordinates.
  - Dose rate measurements at 1 m and 0.1 m above ground using certified gamma-beta dosimeters; background subtraction performed (instrumental and cosmic).
  - 547 soil samples collected; gamma analyses for natural radionuclides (40K, 226Ra, 232Th) and anthropogenic radionuclides (137Cs, 90Sr).
  - Dose rate range: approximately 0.1–0.24 μSv h−1 at 1 m; natural background contributions estimated; wide East-West variations observed with Cs-137 and Sr-90 correlating with zonal contamination patterns.
  - Data indicate relatively low natural radionuclide activities compared to global averages; Cs-137 and Sr-90 provide focus for contamination pattern across Ivankiv.

## Data characteristics, formats and quality

- Data types and units
  - Activity concentrations in Bq kg−1 for gamma-emitting nuclides; 90Sr activity via radiochemical methods; 40K, 226Ra, 232Th for natural nuclides.
  - Dose rates in μSv h−1 (at 1 m and other heights as specified).
  - Depth-resolved data for Pu isotopes, Cs, Sr across multiple depth intervals.
  - Soil type codes (USSR/FAO-UNESCO) and agrochemical properties (humus content, pH, exchangeable cations, etc.).
  - Particle classifications (fuel vs condensed) with burn-up data where available.

- Data quality and QA
  - Use of replicates and ratio checks (Cmax − Cmin)/(Cmax + Cmin) to ensure sub-sample homogeneity before analyses.
  - ISO/IEC 17025-compliant QA/QC for Sr analyses in Ivankiv datasets; proficiency testing participation noted.
  - Background corrections and calibration details provided for gamma spectroscopy; yield tracers used for radiochemical analyses.
  - Some negative concentration values appear due to measurement uncertainty and are treated as zero in data users’ applications.

## Data products and potential uses

- Geospatial and environmental assessment
  - Creation of spatial maps of radionuclide contamination (137Cs, 90Sr, Pu isotopes, natural radionuclides) across CEZ and Ivankiv region.
  - Depth profiling enables understanding of fuel particle weathering, leaching dynamics, and vertical migration of radionuclides.
  - Estimation of remaining fuel particle fraction informs mobility and long-term risk assessments.

- Fuel particle characterisation and radiological risk
  - Pu-isotope inventories and hot particle data support source-term reconstruction and particle behaviour modelling.
  - Burn-up and particle age data help interpret time-dependent radiological risk and cleanup priorities.

- Data integration and cross-regional comparisons
  - CEZ particle datasets complemented by Polish and other European particle data to contextualize particle forms and activities.
  - Ivankiv 2014 data provide contemporary background levels and the influence of historical CEZ contamination on nearby regions.

- Practical outputs for data support roles
  - Well-documented measurement methodologies, QA workflows, and metadata enable reliable data curation, quality assurance, and end-user self-service exploration.
  - Datasets are suitable for dashboards, interactive maps, and analyses assessing contamination patterns, exposure scenarios, and environmental remediation planning.

## Notes and caveats

- Coordinate accuracy varies; GPS accuracy ~100 m with systematic ~300 m for certain CEZ data.
- Certain CEZ-site classifications (e.g., around Bober) include limited agrochemical data.
- In some samples, low 90Sr:154Eu ratios necessitated using total 90Sr for undissolved fuel particle estimates; negative values in data are treated as zero.
- Data span multiple campaigns (1995–1997 CEZ baseline, 2000 extension, 2014 Ivankiv survey, and cross-regional particle data), requiring careful harmonisation when combining datasets.

## References (selected)

- Spatial datasets of radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone. Kashparov et al., 2017.
- Pu isotope measurements and hot particle analyses; various methodological references within the dataset.
- Ivankiv region survey methodology and QA discussions; Kashparov et al., 2014.
- Supporting literature on soil analysis standards, gamma-spectrometry calibration, and radiochemical procedures cited throughout.