# Recover and isolation of Kenyan Bacteroides spp. hosts

- Purpose and study context
  - Describes isolation of human and cattle Kenyan Bacteroides spp. hosts using methods from Payan et al. (2005) and Gómez-Doñate et al. (2011), adapted for rural Siaya County due to lack of municipal wastewater facilities.
  - Data collection includes locational data with GPS coordinates (World Geodetic System) for sampling sites; location data stored in LocationOfFaecalSampling.csv.
  - Sampling conducted in June 2018; Kenyan Medical Research Institute laboratories in Kisian (Kisumu) used for recovery and isolation; detection of fecal indicator bacteria, bacteriophages, and phages infecting Bacteroides spp. hosts at multiple dates; datasets referenced in several CSV files.

- Sampling sites and timeline
  - Study area: rural Siaya County, western Kenya; samples from school pit latrines (human) and cattle faeces from shoreline of surface water sources.
  - Human fecal sampling: pooled samples collected from five pit latrines per school on 7–8 June 2018.
  - Cattle fecal sampling: pooled samples (five stools per location; ~25 g total) collected from shorelines of 10 water sources on 7–8 June 2018.
  - Isolation of Kenyan Bacteroides hosts: 10–21 June 2018.
  - Water and wastewater sampling for FIB and phages: 18–21 June 2018; 5–8 November 2018; 13 June 2019.
  - Datasets and location references: LocationOfFaecalSampling.csv; DetectionOfFIB&MSTmarkers.csv; multiple isolation step files.

- Data collection and transport
  - Fecal samples collected using sterile techniques; pooling to 25 g per sample; transported to KEMRI Kisian within 4 hours and stored at ~4°C for up to 24 hours.

- Host isolation methods
  - Isolation performed on Bacteroides bile esculine agar (BBEa) with a multi-day workflow:
    - Day 1: Prepare master faecal solutions; serial dilutions; inoculate onto BBE agar; anaerobic incubation.
    - Day 2: Select dark colonies; purify on BBE; incubate under aerobic/anaerobic conditions.
    - Day 3: Gram stain; select Gram-negative obligate anaerobes; subculture on BBE and BPRM plates; incubate anaerobically.
    - Day 4: Inoculate into BPRM broth; identify cultures with growth; prepare cryopreserved stocks with bovine serum.
  - Outcome: 10 new potential Bacteroides spp. hosts selected.
    - Cattle-origin hosts: SIN.19, KN.1, KN.2, KN.3, KN.8.
    - Human-origin hosts: WAA.1, TIB.1, TIA.1, ONA.3, LU.2.
  - Data files listing hosts: IsolationBacteroidesHostsWeek10-6-18StepB.csv; IsolationBacteroidesHostsWeek17-6-18StepA.csv; IsolationBacteroidesHostsWeek17-6-18StepB.csv.

- Detection of faecal indicators and phages
  - Faecal indicator bacteria (FIB) and somatic coliphages from water sources and KIWASCO wastewater plant:
    - Methods follow ISO 9308-1 (Total coliforms and E. coli) and ISO 7899-2 (intestinal enterococci); results expressed as CFU/100 mL.
    - Filtration and plating on chromogenic/Slanetz & Bartley media with standard incubation.
  - Somatic coliphages:
    - Host: E. coli WG-5; OD monitoring to ~0.33 at 600 nm; assay on semi-solid Scholten’s agar; results as PFU/100 mL.
  - Bacteroides phages (infecting Bacteroides spp. hosts):
    - Hosts: GB-124 reference strain plus Kenyan hosts (WAA.1, TIB.1, TIA.1, ONA.3, LU.2 and SIN.19, KN.1/2/3/8).
    - Procedure uses BPRMB/BPRMB-derived assays; incubation and OD monitoring; results as PFU.
  - Positive controls: naturally occurring phages from faecally contaminated surface waters.

- Data files and datasets
  - LocationOfFaecalSampling.csv (sampling site coordinates)
  - IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - IsolationOfBacteroidesHostsWeek10-6-18StepB.csv
  - IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - IsolationBacteroidesHostsweek17-6-18StepB.csv
  - DetectionOfFIB&MSTmarkers.csv

- Ethics and approvals
  - Ethical approval obtained from University of Southampton (ref 31554; 12/02/2018) and Kenya Medical Research Institute (KEMRI SERU CGHR/091/3493; 17/10/2017).
  - Participant information sheet and consent forms used for sampling from school headteachers.

- GIS relevance and data considerations
  - Rich geospatial dataset: precise sampling coordinates, site metadata, and multiple sampling campaigns enable spatial analyses of host distribution, environmental reservoirs, and microbial indicators.
  - Data integration needs careful harmonization across multiple CSV files; consistent use of the World Geodetic System coordinates facilitates overlay with environmental layers and water source maps.
  - Temporal aspect: sampling dates span human, cattle, and water-related sampling across several years, enabling spatiotemporal analyses.

- Practical notes for GIS use
  - Location and host codes (e.g., SIN.19, KN.1, WAA.1, etc.) link microbiological results to specific sites and sources.
  - Dataset organization supports layering: fecal sampling locations, water sources, and microbial detection results can be mapped and analyzed together.
  - Data quality controls described (anaerobic/isolation steps, controls for phage assays) inform confidence in spatially-rendered results.