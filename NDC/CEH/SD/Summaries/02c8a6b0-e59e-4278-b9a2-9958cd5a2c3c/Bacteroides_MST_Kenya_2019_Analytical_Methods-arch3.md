# Recovery and isolation of Kenyan Bacteroides spp. hosts from human and cattle faeces

## Overview
- Describes methods to recover and isolate Kenyan Bacteroides spp. hosts from human and cattle feces in rural Kenya.
- Documents detection of faecal indicator bacteria (FIB), somatic coliphages, and bacteriophages infecting Bacteroides spp. in environmental water samples and a wastewater plant.
- Uses location data, ethical approvals, and standardized laboratory procedures; data are organized in specific CSV files.

## Experimental design and sampling
- Study location: rural Siaya County, western Kenya.
- Sample sources:
  - Human: pooled fecal material from school pit latrines.
  - Cattle: pooled fecal material from cattle along shorelines of surface water sources.
- Locational data: collected with hand-held GPS; coordinates recorded in LocationOfFaecalSampling.csv.
- Sampling dates:
  - Faecal samples: 7–8 June 2018.
  - Isolation of Bacteroides hosts: 10–21 June 2018 (KEMRI Kisian laboratories, Kisumu).
  - Water and wastewater samples for FIB and phage detection: 18–21/06/2018; 05–08/11/2018; and 13/06/2019.
- Data files referenced for sample locations and host data include multiple CSVs (e.g., IsolationOfBacteroidesHostsWeek10-6-18StepA/B, IsolationBacteroidesHostsWeek17-6-18StepA/B, DetectionOfFIB&MSTmarkers).

## Sample collection and processing
- Human sampling: pit latrines in primary schools; consent obtained; ~25 g pooled sample collected per school.
- Cattle sampling: five stools per location, pooled into ~25 g per site; samples placed in 100 mL sterile pots with cold storage.
- Transport: samples to KEMRI laboratories in Kisian within ~4 hours; stored at 4°C for up to 24 hours until processing.

## Isolation of Bacteroides hosts
- Medium and conditions: Bacteroides bile esculine agar (BBEa) used for recovery; specific composition and pH per method description.
- Processing timeline:
  - Day 1: Prepare master faecal solutions; inoculate onto BBE agar; incubate anaerobically at 37°C for 24 h.
  - Day 2: Select dark colonies; subculture onto duplicate BBE agar plates; incubate at 37°C for 24 h under aerobic and anaerobic conditions.
  - Day 3: Identify Gram-negative obligate anaerobic rods; preliminary characterization by Gram stain and morphology.
  - Day 4: Inoculate selected isolates into BPRM broth; incubate; select growth; create cryopreserved vials with cryoprotectant; store at -20°C.
- Outcome: 10 new potential Bacteroides hosts isolated; five from cattle (SIN.19, KN.1, KN.2, KN.3, KN.8) and five from human sources (WAA.1, TIB.1, TIA.1, ONA.3, LU.2).
- Data files listing selected hosts: IsolationBacteroidesHostsWeek10-6-18StepB.csv; IsolationBacteroidesHostsWeek17-6-18StepA.csv; IsolationBacteroidesHostsweek17-6-18StepB.csv.

## Environmental microbiology methods

### Detection of faecal indicator bacteria (FIB)
- Standards: ISO 9308-1:2014 (Total coliforms and E. coli) and ISO 7899-2:2000 (intestinal enterococci).
- Method: membrane filtration; volumes screened per sample (0.1, 1, 10, 100 mL); filtration onto appropriate media.
- For wastewater: higher concentrations use dilutions of 10^-2 to 10^-5.
- Media and incubation: coliform chromogenic agar (CCE) for coliforms and E. coli; Slanetz and Bartley agar for intestinal enterococci; incubation up to 48 h for enterococci.
- Output: results expressed as CFU per 100 mL; TNTC adjustments applied by using smaller sample volumes as needed.

### Detection of somatic coliphages
- Host: E. coli WG-5.
- Procedure: prepare host culture to 0.33 OD at 600 nm; mix with semi-solid Scholten’s agar and sample; incubate to form plaques; enumerate PFU per 100 mL.
- Controls and timing: includes positive control; OD monitored and standardized during assay.

### Detection of bacteriophages infecting Bacteroides spp.
- Hosts: previously isolated human host GB-124 and Kenyan hosts (human: WAA.1, TIB.1, TIA.1, ONA.3, LU.2; cattle: SIN.19, KN.1, KN.2, KN.3, KN.8).
- Procedure: prepare BPRMB broth inoculum with hosts; incubate to reach target OD; prepare semi-solid Bacteroides phage recovery medium agar (ssBPRMA); mix with water samples to set plates; anaerobic incubation at 37°C for ~18 h.
- Output: plaques (PFU) counted to quantify phages infecting Bacteroides spp.; GB-124 phage used as a positive control.

## Data governance, metadata, and accessibility
- Data are organized and stored in clearly named CSV files (e.g., LocationOfFaecalSampling.csv, DetectionOfFIB&MSTmarkers.csv, various IsolationOfBacteroidesHostsWeek*.csv).
- Metadata include sample origin (human vs. cattle), sampling dates, locations, and host codes; locational data captured with GPS.
- Methods rely on ISO standards and well-documented media/dilution schemes to enable verification and replication.
- Ethical approvals and participant consent documented; samples transported and stored under defined conditions to preserve integrity.
- The document references that full descriptions of agar/media components are provided in a separate “Fieldwork and laboratory instrumentation” section.