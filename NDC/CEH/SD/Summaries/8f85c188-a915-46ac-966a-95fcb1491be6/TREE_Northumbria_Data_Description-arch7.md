# Element and radionuclide concentrations in wildlife (including representative species of the ICRP's Reference Animals and Plants) and associated soils from forests in north-east England, 2015-2016

## Overview and aim
- Reports stable element concentrations, radionuclide activity (K-40 and Cs-137), and concentration ratios (CRs) for a range of samples.
- Targets representative terrestrial species of ICRP RAPs to support environmental protection framework.
- Data cover soils, water, vegetation, fungi, invertebrates, small mammals, amphibians, and roe deer collected 2015–2016.

## Study area and sampling design (GIS-relevant location data)
- Two main forests in north-east England:
  - Holystone Woods (NGR 3940 6030)
  - Kielder Forest (NGR 3760 6010)
- Additional sampling areas within Kielder vicinity: Redesdale forest (southwest of main Kielder area) and Spadeadam Forest (northeast Cumbria).
- Main sampling areas: Holystone ~0.06 km2; Redesdale ~0.16 km2; boundaries referenced in TREE_Northumbria_Soil_Sample_Information.csv.
- Sampling locations recorded with GPS (accuracy ~5 m); NGR coordinates provided for sites and samples.

## Sampling subjects and data types
- Biological matrices and samples:
  - Soil, water, wild grasses, pine trees, herbaceous plants and shrubs, fungal fruiting bodies, earthworms, bees, wood mice, bank voles, roe deer, common frogs, frogspawn, European toads.
- Data types collected and compiled:
  - Stable element concentrations (FM and DM) in vegetation and animal tissues.
  - Radionuclide activity concentrations (K-40, Cs-137) in various media and whole-organism contexts.
  - Whole-organism concentration estimates for select species (e.g., roe deer, wood mice, bank voles, amphibians, bees, earthworms).
  - Concentration ratios (CR) comparing whole-organism or tissue concentrations to soil or water.

## Laboratory methods and quality assurance (data quality aids GIS integration)
- Stable elements:
  - Analysis by ICP-MS with multiple collision-cell modes; internal standards and external calibrations; QA via SRMs and proficiency schemes.
  - Digestion methods: acid (HNO3, HF, HClO4) for soils/vegetation; alkaline (TMAH) extractions for iodine and other elements.
- Radionuclides:
  - Gamma analysis using hyper-pure germanium detectors; activity concentrations decayed to sampling day.
- Sample preparation:
  - Comprehensive processing for each taxon (e.g., whole-body measurements, tissue dissection, drying, grinding, and freezing).
  - Osteological/soft-tissue separation for tissue-specific concentrations; whole-organism estimates derived from tissue masses and measured concentrations.
- Data reporting thresholds:
  - Results include MDA/LOD reporting; < MDA values indicated as < value; special handling when tissue contributions exceed 10% of total content.

## Data structure and content (GIS-ready considerations)
- Data repository comprises 42 workbooks:
  - Sample information (species, site, NGR, sample codes, FM/DM/AM masses, dimensions, notes, preparation/analysis)
  - Stable element concentrations (FM and DM) by vegetation and animal tissues; water concentrations; whole-organism concentrations for several species
  - Stable element concentration ratios (CR) for whole-organism vs soil or water; species-specific CRs for plants, fungi, bees, earthworms, amphibians, and mammals
  - Radionuclide data (K-40 and Cs-137) by media; CRs based on FM/DM
  - Concentration ratios by tissue and whole-organism basis for multiple taxa
- Coverage includes representative RAPs across flora and fauna relevant to environmental radiological assessments.

## Calculations and interpretation (relevant to map-based products)
- Whole-organism concentrations:
  - For roe deer, wood mice, and amphibians, combine tissue concentrations and masses to estimate total body content.
  - For some species, specific tissues are emphasized (e.g., bone, muscle, liver, thyroid) to derive whole-organism values.
- Concentration ratios (CR):
  - CRwo-soil and CRwo-water calculated to quantify transfer from environment to organisms.
  - Ratios are presented on fresh mass, dry mass, or ash mass bases as appropriate.
- Data limitations and handling:
  - Some elements or tissues have nondetectable results; LOD-based reporting and 10% contribution rule applied for reporting whole-organism results as exact or as < values.
  - Iodine concentrations may be underestimated in some plant matrices depending on digestion method.

## Usage and applications for GIS and map-based data products
- Enables spatial visualization of:
  - Elemental and radionuclide distributions across Holystone, Kielder, Redesdale, and Spadeadam areas.
  - Cross-taxa transfer patterns via CRs and whole-organism concentration estimates.
- Supports integration with ICRP RAPs and ERICA-type transfer parameter datasets.
- Facilitates environmental risk assessments, contamination mapping, and comparative analyses among taxa and habitats.
- Data structure supports geospatial analyses, metadata tracking, and multi-layer visualization (soil, water, vegetation, soils-to-biota transfer).

## References, acknowledgements, and funding
- Core methods and transfer parameter context drawn from ICRP RAPs and related radiological protection literature.
- Acknowledges Forestry Commission sampling access, field and lab collaborators, and funding by NERC, Environment Agency, and Radioactive Waste Management Ltd. under the RATE TREE project.