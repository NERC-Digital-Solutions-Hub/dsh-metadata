# Spatial datasets of radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone

- A compilation of soil and particle contamination data from the Chernobyl Exclusion Zone (CEZ), Ukraine, generated between 1995 and 1997, with expanded data from autumn 2000 and additional hot-particle studies dating back to 1987–1992, plus Ivankov region data from 2014.
- Primary aim: map and understand radionuclide contamination, the behavior of fuel particles, and the distribution of key radionuclides (e.g., 90Sr, 137Cs, plutonium isotopes) in soils and particles, including depth profiles and regional comparisons.
- Data scope includes grid-based soil sampling around ChNPP (about 1200 sites within a 36 km radius; denser spacing (100–500 m) in western narrow trace of fallout), co-ordinate accuracy, sample preparation, and multiple analytical methodologies.
- Data assets are accompanied by extensive methodological detail, quality assurance documentation, and historical references, enabling reuse for modeling deposition, particle mobility, and radiological risk assessments.

## Data components and structure

- Soil sampling and preparation
  - Envelope composite samples: five cores (37 mm diameter) from 2–5 m2 areas, depth up to 30 cm; total mass ≥ 2 kg.
  - Depth rationale: most 90Sr resides in upper 10–20 cm a decade post-accident; 30 cm depth used to test adequacy.
  - Co-ordinates obtained with GPS (ScoutMaster, WGS-84); reported coordinate accuracy ~100 m with systematic ~300 m deviation.
- Soil activity measurements
  - Samples dried, sieved to <1 mm; four sub-samples per site for gamma-emitting nuclides (three 100 cm3, one 1000 cm3 in Marinelli geometry).
  - Gamma spectrometry (HPGe detectors ~30% efficiency) used for 137Cs, 154Eu, 241Am, 85Sr, etc.; quality checks to ensure sub-sample representativeness (max-min variation < 0.15).
  - 90Sr activity determined radiochemically via 90Y equilibrium, with procedures to improve accuracy by removing 137Cs prior to 90Sr/154Eu measurements.
  - Calibration using mixed spike standards; counting times adjusted to achieve <30% error at 95% CI.
- Pu isotope measurements
  - 82 samples from main release traces analyzed for Pu isotopes; radiochemical separation with 236Pu/242Pu tracers; alpha-spectrometry for activity.
  - Additional 12 samples (autumn 2000) analyzed similarly; broader geographic sampling up to 200 km from CEZ for comparative Pu isotopes.
- Pu isotope depth profiling
  - Eight sites with cores sectioned into layers (0–2 cm up to 25–30 cm; some site with 110 cm depth sliced into 10 cm intervals).
  - Measured 238Pu, 239,240Pu, 137Cs, 90Sr in depth slices.
- Hot particles
  - Early Chernobyl release yielded many uranium dioxide fuel particles (2–3 μm median radius) predominantly west of ChNPP; larger particles within 2–5 km.
  - Particles characterized as fuel or condensed ( ruthenium-rich matrices ); particle size, activity, and burn-up documented.
  - Methods include gamma, alpha spectroscopy, and radiochemical separation; particle-specific analyses (neutron activation, electron microanalysis, laser mass spectrometry).
  - Burn-up estimates indicate younger fuel in CEZ-derived particles, with lower burn-up than most reactor-core estimates.
- Particle inventories from other regions
  - Data include ~206 particles from NE Poland (1986–1989) with forms A–C (ruthenium-rich) for comparative context.
  - Augmented with published particle datasets from Sweden, Hungary, Bulgaria, and other locations for broader contextual understanding of hot particles.
- 115 soil samples (1995–1997) and 90Sr/137Cs-focused analyses
  - Broad environmental sampling along western, northern, southern traces of fall-out; soddy podzolic soils predominantly sampled; peat soils also sampled when available.
  - Density of contamination by 90Sr ranged widely (12 kBq/m2 to 60 MBq/m2 in some zones); soil types catalogued per USSR/FAO-UNESCO classifications.
- Ivankiv region survey (2014)
  - 3,389 grid-based sampling points (1 km) with 1 m and 0.1 m dose-rate measurements; GPS coordinates with high-resolution accuracy (≤10 m in the Ivankiv survey).
  - Soil sampling every third dose-rate point; 540–547 soil samples collected; 90Sr and gamma analyses conducted; natural radionuclide baselines (40K, 226Ra, 232Th) reported.
  - Dose-rate corrections included subtracting cosmic and instrument background; background values established via a frozen-water body and shielded measurements.
- Data accessibility and references
  - Core dataset linked to UIAR (Ukrainian Institute of Agricultural Radiology) and referenced extensively in the literature; included in the NERC Environmental Information Data Centre (data DOI and 2017 publication).

## Methods and analytical details

- Gamma spectrometry
  - HPGe detectors, 1 L Marinelli geometry, ~1 hour counting time (adjusted for low activity), calibration with multi-radionuclide standards.
- Radiochemical separation
  - 90Sr via nitric acid digestion, hydroxide/oxide precipitation, and beta counting after chemical separation; 137Cs separated prior to 90Sr/154Eu analyses to avoid cross-contamination.
- Pu isotope procedures
  - Standard radiochemical methods with resin-based extraction and alpha spectrometry; chemical yield controls using Pu tracers.
- Depth-resolved analyses
  - Layered coring with Pu, 137Cs, and 90Sr analyses to evaluate vertical migration and leaching behavior, especially in fuel-particle contexts.
- Hot particle characterization
  - Particle size, radioisotope activities measured by gamma, alpha, and beta techniques; annealing and temperature-duration estimates derived from 137Cs/90Sr data.
- Quality assurance
  - ISO/IEC 17025 adherence; participation in proficiency tests; documentation of QA procedures and cross-validation of sub-samples.

## Data quality, standards, and metadata

- Coordinate systems and accuracy
  - WGS-84, GPS-derived coordinates; CEZ sampling shows ~100 m accuracy with larger systematic deviations in some traces.
- Data quality and reporting
  - Negative values for some 90Sr measurements treated as zero; replicates used to ensure representativeness; measurement uncertainties reported and managed.
- Soil classification and metadata
  - USSR soil classification codes linked to FAO/UNESCO equivalents; soil types annotated per sampling site to aid interpretation and cross-site comparisons.
- References and provenance
  - Extensive citation network supporting the data (Kashparov et al., Ivanov et al., Kuriny et al., etc.); data aligned with published maps and environmental datasets; DOI-based data publication and long-term archiving.

## Access, use cases, and governance

- Data access and reuse
  - Data are published with references and links to the NERC Environmental Information Data Centre; can be used for deposition modeling, particle mobility studies, and comparative regional assessments.
- Ownership and contributors
  - Compiled by Kashparov, Levchuk, Zhurba, Protsak, Khomutinin, Beresford, and Chaplow, with involvement from UIAR and international collaborators.
- Potential uses for Data Leaders
  - Model validation for radionuclide deposition and fuel-particle transport in soils.
  - Cross-regional comparisons of hot-particle behavior and burn-up implications.
  - Informing remediation planning and risk assessment in post-accident landscapes.
  - Metadata-driven data governance: example of comprehensive methodology documentation, QA, and standardization across multi-component environmental datasets.

## Key challenges and considerations for data leaders

- Heterogeneity and scale
  - Spatial and vertical heterogeneity of contamination; variable sampling density across traces; differences in soil types and moisture can affect mobility and measurements.
- Access and data standards
  - Historical data use varied classification schemes (USSR vs. FAO-UNESCO); harmonization requires careful metadata handling.
- Data quality and uncertainty
  - Coordinate inaccuracies, measurement errors, calibration uncertainties, and potential underestimation in certain radiochemical analyses (e.g., 90Sr leaching in sandy soils).
- Provenance and compatibility
  - Integrating legacy datasets with newer high-resolution surveys (e.g., Ivankiv 2014) requires robust lineage tracking and consistent units, depths, and background corrections.

## References and further information

- Spatial datasets of radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone. Kashparov V., Levchuk S., Zhurba M., Protsak V., Khomutinin Yu., Beresford N.A. and Chaplow J.S. (2017). NERC Environmental Information Data Centre; includes extensive methodological and bibliographic references.
- Related methodological and location-specific studies cited within the dataset (e.g., Ivanov et al., Kuriny et al., Kashparov et al., Shestopalov et al., and international comparisons from Poland, Sweden, Hungary, and Bulgaria).