# Materials and Methods for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone

- What the data are and cover
  - Radionuclide concentrations (whole-body) of vertebrates in the Chernobyl Exclusion Zone (CZ): 137Cs, 90Sr, and Pu isotopes.
  - Taxa included: passerine birds, bats, and ground-dwelling small mammals; additional unreported bat data from sites around the CZ; soils data from related studies.
  - Dataset context: Biota_radionuclide_data.csv, drawing on Beresford et al. (2016) with supplementary data from Beresford et al. (2008) and related work; cross-referenced with live-monitoring results described in Bondarkov et al. (2011).

- Site and habitat description
  - Main study site: approximately 8 km west of the Chernobyl nuclear power plant.
  - Habitat: woodland dominated by Pinus sylvestris and Quercus robur, with Sorbus aucuparia and Tilia platyphyllos; sparse understorey of Pteridium aquilinum.
  - Soils (Beresford 2008): soddy pseudopodzolic sandy/boggy soils; a 200 m × 200 m area (40,000 m2) around sampling sites with soil samples analyzed for 137Cs, 238,239,240Pu, and 90Sr (mean ± SD values provided).

- Sampling and specimen handling
  - Species sampled: a range of passerines and bats from mist nets; ground-dwelling small mammals collected at multiple sites (2004–2008 focus).
  - Collection and processing: mist netting for birds and bats; specimens euthanised and stored frozen; pre-analysis preparation included removal of gastrointestinal tract (GIT) for birds and bats, removal of pelt and GIT for small mammals; samples weighed and washed before analysis.
  - Individual sample workflow aimed at enabling whole-body radionuclide concentration measurements.

- Laboratory methods and measurement details
  - 137Cs measurement:
    - Instrumentation: hyper-pure germanium detector for 137Cs; a thin-film NaI detector for 90Sr (as a separate measurement path).
    - Counting setup: boxes and lead shielding; 137Cs spectra analyzed with Canberra Genie-2000 software; counting times ranged from 150 to 1200 seconds depending on activity.
    - Calibration/validation: method calibrated against phantoms containing 137Cs and 90Sr; validated against traditional radiochemical methods.
    - Uncertainty: typical counting errors < 7% for 137Cs.
  - 90Sr measurement:
    - Approach: determined from its daughter nuclide 90Y; counting error typically < 3%.
  - Pu isotopes measurement:
    - Sample preparation: dissolution in 65% HNO3 with 242Pu as a yield tracer; anion exchange (Bio Rad AG 1 x 8) and co-precipitation.
    - Detection: counted with a planar ion-implanted silicon detector.
    - Uncertainty: counting errors typically < 20% for Pu isotopes.

- Data provenance, linking, and context
  - Primary sources: Beresford et al. (2016) on transfer of 137Cs, Pu isotopes, and 90Sr to birds, bats, and small mammals; Beresford et al. (2008) on soil activity concentrations and exposure estimation using the ERICA tool; Bondarkov et al. (2011) and related studies on live-monitoring methods.
  - Data products: Biota_radionuclide_data.csv (and related metadata in Biota_radionuclide_metadata.rtf).
  - Additional context: the dataset includes results for species not reported in Beresford et al. (2008) and includes Pu isotopes data; soil context and exposure descriptions are provided to support interpretation.

- Data quality, usage notes, and caveats
  - Measurement quality: validated methodology, cross-calibrated against phantoms and alternative analytical approaches; explicit counting uncertainties provided.
  - Data limitations: variability in data coverage across species and sites; some data are supplementary/unreported in earlier papers; spatial patterns in soils showed no clear pattern in the Beresford (2008) site study.
  - Data use potential: enabling cross-taxa exposure assessments, comparisons across radionuclides, integration with soil data for ecological risk assessments, and development of data products (dashboards, summaries, or self-serve analyses) for stakeholders interested in radiation ecology in CZ.

- How this supports data work and reuse
  - Clear provenance and links to primary literature and validation methods facilitate data integration with other CZ radionuclide datasets.
  - Detailed sampling and analytical workflows support reproducibility, quality assurance, and potential method comparisons or methodological improvements.
  - The dataset structure and accompanying metadata are suitable for building data products that help end users explore radionuclide burdens across species and sites.

- References (key sources)
  - Beresford, N.A. et al. 2008. Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone – ERICA Tool application.
  - Beresford, N.A. et al. 2016. Transfer of 137Cs, Pu isotopes and 90Sr to birds, bats, and small mammals in the CZ.
  - Bondarkov, M.D. et al. 2011. Method for simultaneous 90Sr and 137Cs in vivo measurements.
  - Gaschak, S. et al. 2010. Sr-90 and Cs-137 in bats in the CZ.