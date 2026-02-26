# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Keenan, P., Mackay, E.B., Thackeray, S.J., Maberly, S.C. (2021)

## Purpose and Scope
- Part of a long-term monitoring dataset for Derwent Water (Cumbria, England), collected fortnightly from 2014 to 2018.
- Variables included: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Sample depth: integrated from 0 to 5 meters.
- Sampling location: from a boat at the deepest part of the lake (buoy); if buoy access unavailable, samples collected from the shore.
- Data period: January 2014 through end of 2018; long-term monitoring ended early 2019 due to funding shortages.

## Data and Metadata Details
- Data status: raw data not yet quality controlled or calibrated; double entered and visually checked.
- Missing data: primarily due to weather conditions or staff shortages.
- Data format: comma-separated values (CSV) with columns:
  - Date (measurement date)
  - Variable, Description (names and units for TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value, Description (measurement values)
  - Sign (if values are below detection limit, indicated by a "<")
  - Flag, Description (1 = sample taken at buoy; 2 = sample taken from shore when buoy access not possible)

## Data Collection Protocol
- Measurements conducted from a boat at the buoy at the deepest lake location; when not feasible, shore sampling used.
- Integrated 0–5 m water column sampling.

## Quality and Limitations
- Data are preliminary/raw; no calibration or formal QC performed within this dataset.
- Data quality inferred through double entry and visual checks; presence of values below detection limits (LOD) indicated by signs.
- Flags denote sampling location, which affects comparability across samples.

## Access, Documentation, and Reuse
- Dataset is described and ready for download, with explicit field definitions and units.
- Example publications demonstrating dataset usage:
  - Winfield, I.J., Fletcher, J.M., & James, J.B. (2017). The 'reappearance' of vendace in Bassenthwate Lake. Fundamental and Applied Limnology, 189, 227-233. doi: 10.1127/fal/2016/0799.
  - Woolway, R.I., et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society, 97(8), S17-S18.
- Overview related reference: Maberly et al. (2017) From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District.
- Data usage notes: dataset has been employed in ecological and limnology research, illustrating its applicability for long-term lake monitoring analyses.

## Data Governance and Stewardship Considerations for Data Leaders
- Data readiness: raw with imminent QC/calibration requirements; plan for a formal QC workflow and metadata enhancement.
- Metadata and discoverability: comprehensive variable descriptions and sampling details provided; maintain clear provenance and readme for future users.
- Data quality management: implement calibration/validation steps, document detection limits, and maintain robust data quality flags.
- Data interoperability: standardize units and encodings to facilitate integration with other lake monitoring datasets or networks.
- Data continuity and funding risk: monitoring ended early 2019 due to funding; consider strategies for sustaining long-term data collection or archiving for later reactivation.
- Stakeholder use: dataset is suitable for policy-informed analyses and cross-network collaboration, given its clear sampling regime and documented limitations.
- Next steps for data leadership: establish ownership, formal QC plan, metadata schemas, and a data-access plan to ensure ongoing usability and integration with broader data ecosystems.