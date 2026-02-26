# Materials and methods for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERCEnvironmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7442e-97ad-922b5aef003a

- Overview and purpose
  - Presents materials and methods underpinning radionuclide data for vertebrates in the Chernobyl Exclusion Zone (CEZ), with data intended for deposition in the NERC Environmental Information Data Centre (EIDC).
  - Supports data discovery, reuse, and governance by detailing sampling, processing, measurement, and metadata considerations for radionuclide concentrations in reptiles.

- Datasets described
  - CEZ_reptile_data.csv: seven-year dataset (2000–2007) containing data for two reptile species at two CEZ sites near the Red Forest (Red Forest 1 and Red Forest 2).
  - Species and sampling: Lacerta agilis (sand lizard) and Natrix natrix (grass snake); 20 L. agilis and 5 N. natrix ultimately obtained; lizards trapped in Sherman traps, snakes captured by hand.
  - Temporal and spatial scope: Red Forest 1 (approx. 2.6 km SW of Chernobyl NPP) and Red Forest 2 (approx. 2.7 km SW); sampling across triangular and square areas of ~0.15 km² and ~0.01 km² respectively.
  - Sample storage and processing: reptile tissues stored frozen; GI tract removed; carcasses washed; soils oven-dried and homogenised prior to analyses.
  - Look-up and outcomes: whole-body activity concentrations for 137Cs and 90Sr; 238Pu and 239,240Pu concentrations; soil data from 0–10 cm depths.

- Data collection and processing
  - Specimen handling: whole-body analyses following removal of GI tract and washing of carcasses.
  - Soil sampling: cores collected at Red Forest sites (345 cores at Red Forest 1 in June 2001; four cores at Red Forest 2 in May 2007).
  - Data preparation: samples prepared for radiometric analysis; documentation and storage of specimens and soils for traceability.

- Measurement methods and analysis
  - 137Cs: whole-body activity concentration measured with a hyperpure germanium detector; spectra analysed with Canberra Genie 2000; 40K activity monitored to achieve counting error targets (<20% for 40K).
  - 90Sr: activity concentration determined via measurement of its daughter 90Y using a thin-film NaI detector.
  - 238Pu and 239,240Pu: activity concentrations determined through radiochemical separation after dissolution in 65% HNO3; yield tracer 242Pu added; anion exchange separation; co-precipitation; counted with an appropriate detector.
  - Additional notes: measurement approaches and corrections referenced to Bondarkov et al. (2002–2003) for method validation and specific procedural steps (including self-absorption corrections derived from Kα/X-radiation considerations).
  - Soil radionuclides: 137Cs and 40K quantified via hyper-pure germanium detectors with Genie 2000; Sr-90 via 90Y assay; Pu isotopes via Lx-radiation method and related alpha/radiochemical procedures.

- Metadata, documentation, and provenance
  - Data generated and contextualized by multiple authors (Gaschak, Beresford, Barnett, Wells, Maksimenko, Chaplow) with foundational methods validated by Bondarkov et al.
  - Related metadata and methodological details referenced in CEZ_reptile_metadata.rtf and the associated literature; full methods and citations are included to support reproducibility and data reuse.
  - Data references and supporting documentation are intended to be stored in or linked from the NERC EIDC.

- Data governance, sharing, and availability
  - Sharing considerations: dataset authors note that “sharing limitations” should be respected; mechanisms for updates to datasets should be in place.
  - Data ingestion: CEZ_reptile_data.csv (and related methodological materials) are prepared for cataloguing and storage within the NERC EIDC; data producers may need to engage to supply or update data as needed.
  - Data updates: systems should support ongoing updates or corrections to the dataset as new analyses or corrections arise.
  - Accessibility: data are intended to be discoverable by researchers through the NERC EIDC, with metadata enabling discovery by wildlife radiological researchers and other data stewards.

- Practical considerations for Data Stewards
  - Ensure robust metadata: include sampling dates, exact site coordinates, trap types, species, sample processing steps, and measurement specifics (detectors, software, detection limits, QC checks).
  - Capture QA/QC and validation: reference validation sources (e.g., Bondarkov et al.) and document any deviations or calibration data; specify counting errors targets and how they were achieved.
  - Document data formats and units: use consistent units for activity concentrations (e.g., Bq/kg or Bq per animal), specify detection limits, and annotate any data curation steps.
  - Manage interoperability: align with CEZ_reptile_metadata.rtf and related metadata standards to facilitate interoperability with other CEZ datasets and radiological monitoring data.
  - Address data availability and limitations: record any data sharing restrictions, embargoes, or limitations due to sample provenance, and outline procedures for updates and versioning.
  - Data stewardship and roles: recognize cross-institutional collaboration (Ukrainian coauthors and international contributors) and establish clear data ownership, access, and contact points within the NERC EIDC framework.

- Challenges and considerations highlighted
  - Incomplete picture of user needs and priorities for all potential users of these data.
  - Timeliness for data submission and data creator engagement to meet standards and metadata completeness.
  - Interoperability across different systems, formats, and legacy databases requiring bespoke integration approaches.
  - Handling large datasets (soil cores and multi-isotope measurements) and integrating with other CEZ data.
  - Ensuring updated, well-documented datasets with appropriate governance and discovery mechanisms.