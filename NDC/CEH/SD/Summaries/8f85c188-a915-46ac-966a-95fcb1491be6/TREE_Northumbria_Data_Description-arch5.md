# Element and radionuclide concentrations in wildlife (including representative species of the ICRP's Reference Animals and Plants) and associated soils from forests in north-east England, 2015-2016

## Overview
- Dataset describing stable element concentrations, radionuclide activity (K-40 and Cs-137), and concentration ratios (CRs) across a range of wildlife, soils, and vegetation.
- Targets representative terrestrial RAPs (ICRP 2008) to support environmental protection frameworks.
- Samples collected March 2015–October 2016 from two forests in north-east England: Holystone Woods and Kielder Forest (with some samples from Spadeadam Forest).
- Data intended to facilitate data sharing, standardisation, and use in environmental radiological assessments.

## Sampling sites and design
- Main sampling areas:
  - Holystone Woods (NGR 3940 6030)
  - Kielder Forest (NGR 3760 6010), including Redesdale and Spadeadam sub-areas
- GPS-referenced sampling locations (accuracy ~5 m); study area boundaries described in accompanying CSV.
- Species and media sampled include soil, water, grasses, trees, herbaceous plants, shrubs, fungi, earthworms, bees, wood mice, bank voles, roe deer, common frogs, frogspawn, European toads.

## Sample types and analyses
- Sample categories:
  - Soil, Water
  - Vegetation (wild grasses, pines, herbaceous plants, shrubs)
  - Fungi (fruiting bodies)
  - Invertebrates and vertebrates (earthworms, bees, wood mice, bank voles, roe deer)
  - Amphibians (common frogs, frogspawn, European toads)
- Analytes and methods:
  - Stable elements: concentrations in fresh mass (FM), dry mass (DM), and ash mass (AM) where applicable; analysed by ICP-MS or ICP-OES after acid or alkaline digestions.
  - Radionuclides: activity concentrations of K-40 and Cs-137 with two-sigma counting error and minimum detectable activity (MDA); gamma analysis performed on select samples using germanium detectors.
  - Concentration ratios (CRwo-soil, CRwo-water, and tissue-specific CRs) calculated to relate whole-organism or tissue concentrations to soil or water concentrations.
- Tissue and sample processing:
  - Soils: dried and ground; digested with HNO3/HF/HClO4; TMAH extraction used for some fractions.
  - Vegetation: microwave-assisted acid digestion and TMAH extraction; standard reference materials used for QA.
  - Animal tissues: microwave digestion with HNO3/H2O2; TMAH extraction for select tissues; whole-organism estimates derived from tissue-specific concentrations.
  - Water: filtered and acidified for ICP-MS analysis.

## Data structure and files
- Total of 42 workbooks distributed as:
  - Sample information workbooks (n=4): sample IDs, site, location, mass, tissue descriptions, preparation notes, and notes on analyses.
  - Stable element concentration (FM) workbooks (n=15): element concentrations in FM across vegetation and tissues of roe deer, common frogs/spawn, wood mice; water concentrations; FM-based whole-organism data for several species.
  - Stable element concentration (DM) workbooks (n=9): DM concentrations for soil, vegetation, and tissues; ash-based concentrations for some animals; DM-based whole-organism data.
  - Radionuclide data workbooks (n=6): radionuclide activity concentrations (K-40, Cs-137) with MDA and counting errors; data in FM/DM as applicable; Cs-137 concentration ratios.
  - Stable element concentration ratios (FM) workbooks (n=8): CRs for bees, roe deer, earthworms, common frogs, European toads, bank voles, wood mice, and RAP plants/trees.
- Metadata and documentation elements:
  - NGR coordinates, sampling dates, sexes where available, sample masses (FM/DM/AM), tissue types, and notes on analysis and QA.
  - References to related methodology and prior transfer parameter work (ICRP RAPs, ERICA, etc.).

## Measurement details and quality assurance
- Instrumentation and calibrations:
  - ICP-MS (iCAP-Q) with multiple cell modes (He, STD, H2) for interferences; internal standards included Ge, Rh, Ir.
  - ICP-OES (DV 7300) for core elements in water and other matrices.
  - Gamma spectroscopy with hyper-pure Ge detectors; efficiency calibration against mixed nuclide standards; activity concentrations decay-corrected to sampling day.
- QA and reference materials:
  - Use of NIST SRMs and CRM materials (NIST 2711a, 1573a tomato leaves, 1577c bovine liver) to verify digestion and analysis accuracy.
  - Regular participation in proficiency testing schemes; blanks and duplicates included in QA routine.
- Data reporting:
  - Concentrations reported as mg/kg (FM/DM/AM) for solids, mg/L for water; radionuclide activity reported as Bq/kg (FM/DM) with MDA where applicable.
  - LODs and detection limits provided; some reported as “<” when below detection.

## Whole-organism concentrations and CR calculations
- Approaches to estimate whole-organism concentrations:
  - Roe deer: concentrations estimated from bone, muscle, liver, and thyroid masses; total body composition based on dissection data and literature.
  - Wood mice: concentrations estimated from bone, muscle, liver, and thyroid (iodine) tissues.
  - Common frogs: concentrations estimated from muscle, bone, liver, and gonads; gonads included due to minimal contribution findings in prior work.
  - European toads: similar tissue-based estimation; thyroid-related iodine considerations noted.
  - Bank voles and other species: whole-organism estimates derived from available tissues or ashed carcasses where analysed.
- Concentration ratios (CR):
  - CRwo-soil: concentration in whole-organism divided by soil concentration (FM or DM) depending on dataset.
  - CRwo-water or plant-based CRs: calculated where appropriate.
  - For some species, CRs are presented on FM, with tissue- or age-specific considerations noted.
- Handling of undetectables:
  - If tissue concentrations below LOD contribute ≥10% to total body content, whole-organism value reported as a “less than” value.
  - If contribution <10%, whole-organism estimate treated as reasonable approximation.

## Data accessibility, governance, and reuse
- Data are organised into modular workbooks enabling reuse, re-analysis, and integration with other datasets (e.g., TRACEABLE links to ICRP RAP parameters and TREE project outputs).
- Documentation notes include site geometry, sampling protocols, digestion methods, QA procedures, and calculation approaches to support reproducibility.
- Potential for updates or re-analyses exists, but data are provided with sufficient metadata to enable discoverability and proper interpretation in line with data governance standards.
- Primary purpose of dataset: support parameterisation of environmental protection tools (e.g., ICRP RAP-based models) and broaden understanding of radionuclide and stable-element transfer in forest ecosystems.

## Particular caveats and limitations
- Partial dissolution issues with TMAH digestion for some plant tissues and coarse samples (e.g., pine heartwood cores) may underestimate iodine content in certain matrices.
- Some samples were not analysed; data quality notes indicate occasional “No analysis conducted” markers.
- Variability in tissue completeness and digestion completeness across species and tissues may affect comparability of some tissue-based estimates.
- CR values for some organisms rely on tissue-based approximations when complete whole-organism data are not available.

## References and acknowledgements
- Key methodological and interpretive references cited (ICRP RAP framework, transfer parameter studies, related forest ecosystem studies).
- Acknowledgements to sampling sites, field/lab staff, and funding sources (NERC, Environment Agency, Radioactive Waste Management Ltd.; TREE project).