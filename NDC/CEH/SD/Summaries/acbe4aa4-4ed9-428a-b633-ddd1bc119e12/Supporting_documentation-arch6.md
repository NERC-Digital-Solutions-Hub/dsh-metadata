# Feather isotope ratios and sexing of oystercatchers breeding in Iceland

## Overview
- Study conducted across south, west, north-west and north-east Iceland during summers 2013–2017.
- Subjects: incubating oystercatchers (Haematopus ostralegus) captured on nests, marked with rings, and sampled for isotopes and sexing.
- Feathers grown on wintering grounds during pre-nuptial moult; isotopic data reflect diet/habitat during that wintering period.
- DNA-based sexing performed on blood samples for a subset of individuals.

## Data files and scope
- OystercatcherFeatherIstotopes.csv
  - Includes data for 552 oystercatchers caught and sampled during breeding in Iceland.
  - Data columns: Year (2013–2017), Individual ID, d15N (nitrogen isotope ratio), d13C (carbon isotope ratio), Status (Migrant, Unknown, or Resident), WinterLocation (winter observing location/country).
- OystercatcherSexing.csv
  - Includes data for 321 oystercatchers caught and sampled during breeding in Iceland.
  - Data columns: Individual ID, DNA-derived sex.

## Stable isotope analysis (OystercatcherFeatherIstotopes.csv)
- Sample preparation:
  - Feathers washed in 2:1 chloroform/methanol, air-dried.
  - Feathers cut into small fragments and weighed (0.45–0.55 mg).
  - Packaged in tin capsules for analysis.
- Measurement:
  - Analyzed with a combustion Costech elemental analyser linked to a Thermo Scientific Delta XP isotope ratio mass spectrometer (Conflo III).
  - Reported as δ13C (Hed: Vienna Pee Dee Belemnite, V-PDB) and δ15N (AIR N2) in ‰.
- Quality:
  - Replicate measurements of the internal laboratory standard (collagen) indicate measurement errors of 0.2‰ for δ13C and 0.1‰ for δ15N.

## Molecular sexing (OystercatcherSexing.csv)
- DNA extraction:
  - From blood using standard ammonium acetate technique; diluted to 10–50 ng/μL.
- Sex determination:
  - Based on the method of Fridolfsson & Ellegren (1999): A universal molecular approach for sexing non-ratite birds.
- Data columns:
  - Individual ID, DNA-derived sex (sex assigned from the analyses).