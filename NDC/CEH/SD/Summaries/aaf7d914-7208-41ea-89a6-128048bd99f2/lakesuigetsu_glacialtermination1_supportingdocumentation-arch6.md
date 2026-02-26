# Diatom silica oxygen isotope and n-alkanoic acid hydrogen isotope composition of sediments from Lake Suigetsu, Japan (22,000 to 10,000 cal BP) SUPPORTING DOCUMENTATION

- This dataset provides stable isotope and lipid biomarker data from Lake Suigetsu SG12 core subsamples, spanning roughly 22,040 to 9,980 cal BP with ~100-year resolution (n = 120 subsamples).
- Measurements include:
  - δ18O of bulk diatom silica (diatom oxygen isotope) after extensive purification and contamination corrections.
  - δ2H of C16, C18, C28, and C30 n-alkanoic acids (biomarker hydrogen isotopes) after derivatisation to FAMEs and methylation corrections.
- Additional outputs include mass-normalised concentrations of total lipid extract (TLE) and the key n-alkanoic acids (C16, C18, C28, C30) to enable self-serve data exploration.

## Purpose and scope

- Data were collected to infer changes in the East Asian Winter Monsoon and East Asian Summer Monsoon during Glacial Termination I.
- Core material is from the SG12 section of Lake Suigetsu, with chronological control tied to SG06 chronology (IntCal20 timescale) via multiple indicators (radiocarbon dates, varve counts, tephra tie points).

## Core materials and age model

- Subsamples come from SG12 core cut from the centre of Lake Suigetsu (coordinates provided).
- Chronology relies on SG06 with >800 radiocarbon dates, varve counts, and tephra ties; ages are aligned to IntCal20.
- Subsampling: 1.2 cm-wide LL-channels across the depth range 1274.8–2119.4 cm, representing 9980 ± 30 cal BP to 22,040 ± 38 cal BP (continuous adjacent material).
- Event layers (floods, turbidites, tephra) were removed during sampling to avoid skewing the integrated signal.
- Depth-age corrections account for minor core expansion; ages provided in IntCal20 cal BP.

## Sample processing and quality control

- Each subsample split for two analyses:
  - δ18Odiatom
  - δ2Hbiomarker (C16, C18, C28, C30)
- Handling steps include cleaning to remove potential contamination, multiple density separations, and removal of carbonates and organic residues.
- Contamination assessment focused on Al2O3 content; samples with Al2O3 > 4.2% were excluded (n = 5) due to external aluminium contamination from detrital silicates.
- Ultimately, 113 datapoints remain for δ18Odiatom after corrections; 26 δ2H subsamples had raised baselines or other issues, reducing reliable datapoints across homologues.
- Data are accompanied by uncertainty estimates, mass-balance corrections, and methylation corrections applied during data processing.

## δ18Odiatom analysis methodology

- Diatom silica purified via heavy liquid density separations and oxidative/acid treatments; potential Al-bearing contamination identified and corrected.
- Oxygen in diatoms liberated by stepwise fluorination (BrF5), converted to CO2, and measured by mass spectrometry.
- Calibration and standardization:
  - Internal diatomite standard (BFC) used alongside samples.
  - δ18O values normalised to VSMOW after converting from VPDB via established scales.
  - External error: ±0.13 ‰ for BFC; ±0.33 ‰ for replicate diatom samples.
- Contamination correction:
  - Geochemical mass-balance approach used to correct δ18Odiatom for Al contamination, based on measured %Al2O3 and end-member compositions.
  - Monte Carlo propagation (10,000 replicates) yields 1σ uncertainties (mean ±0.36 ‰ for corrected δ18Odiatom).
- Final isotopic dataset includes corrected δ18Odiatom values and associated errors.

## δ2Hbiomarker analysis methodology

- Lipids extracted from the total lipid extract (TLE) using accelerated solvent extraction; fractions separated into neutral and acid fractions; acids derivatised to FAMEs for GC analysis.
- Concentrations for C16, C18, C28, and C30 n-alkanoic acids quantified by GC-FID and normalised to dry sediment mass.
- Compound-specific hydrogen isotopes measured by GC-IRMS, with methyl hydrogen corrections applied to convert FAME δ2H to n-alkanoic acid δ2H values.
- Calibration and standards:
  - In-house standard with C16–C30 n-alkanes calibrated to a reference Indiana n-alkane mixture.
  - Batch-wise QC: in-house standard measured repeatedly; H3+ correction factor ranges 4.24–4.57.
- Data quality considerations:
  - Some samples exhibited elevated baselines, compromising δ2H for certain homologues; 26 subsamples affected (primarily C16 and C18); 13 subsamples had unreliable δ2H for at least one homologue.
  - δ2H values used in analyses have uncorrected errors generally < ±10 ‰ (1σ), with cross-homologue checks (e.g., C28 vs C30) used to identify outliers.
- Final dataset composition:
  - 95 datapoints for C16, 86 for C18, 112 for C28, and 108 for C30 δ2H after quality control and corrections.

## Data structure and units

- Two CSV files:
  - lakesuigetsu_glacialtermination1_isotopes_results.csv
    - Contains sample number, lower/upper age (IntCal20 cal BP), corrected δ18Odiatom, corrected δ2H for C16, C18, C28, C30 (with associated errors), and information on age models and corrections.
  - lakesuigetsu_glacialtermination1_concentrations_results.csv
    - Contains sample number, lower/upper age (IntCal20 cal BP), and mass-normalised concentrations of total lipid extract (TLE) and n-alkanoic acids (C16, C18, C28, C30) normalised to dry sediment mass.
- Age information references SG06/Sg12 correlation models and event layers; data are aligned to IntCal20.

## Key references and data provenance

- Brewer et al. (2008) on contamination signals in biogenic silica oxygen isotope analysis.
- Bronk Ramsey et al. (2020) for Lake Suigetsu radiocarbon calibration reanalysis.
- Chapligin et al. (2011) inter-laboratory comparisons for diatom oxygen isotopes.
- Chivall et al. (2012) methylation effects in hydrogen isotope analysis of fatty acids.
- Leng & Sloane (2008) combined oxygen and silicon isotope analysis of biogenic silica.
- Mackay et al. (2011); McLean et al. (2018); Nakagawa et al. (2012); Schlolaut et al. (2018); Staff et al. (2011) providing Lake Suigetsu chronology context.
- Swann & Snelling (2023); Swann et al. (2018) methodological references and broader isotope records.