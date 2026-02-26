# 1 Soils

- Purpose and scope
  - Describes a dataset of metal concentrations and exchangeability in four UK soils with contrasting contamination histories.
  - Focuses on Ni, Cu, Zn, Cd, and Pb across different extraction methods and isotopic dilution measurements to assess exchangeable metal pools.

- Study sites and sampling
  - Four soils sampled at 0–20 cm depth: Kegworth, Chat Moss, Clough Wood, and a sewage processing farm.
  - Contamination histories linked to road traffic, urban waste, calcareous mine spoil, and digested sewage sludge, respectively.
  - Soils air-dried, sieved to <2 mm; pH determined from soil–water suspensions; loss on ignition used as a proxy for soil organic matter.

- Chemical extraction methods
  - Four extractants used to obtain metal concentrations: 0.43 M HNO3, 0.43 M CH3COOH, 1 M CaCl2, and 0.05 M Na2H2EDTA.
  - Three replicates per soil per extractant; suspensions centrifuged and supernatants filtered to <0.22 µm; CaCl2 extracts acidified and stored at 4°C prior to analysis.

- Isotopic dilution assay design
  - Enriched isotopes used: 62Ni, 65Cu, 70Zn, 108Cd, 204Pb.
  - Bespoke mixed-isotope spikes prepared; spike volumes used to achieve ~20% enrichment in spikes.
  - Six replicate soil samples per metal were prepared; soil suspensions spiked with mixed-isotope solution and incubated; parallel preparations for each extractant type.

- Analytical methods (ICP-MS)
  - Multi-element concentrations and isotopic abundances measured by quadrupole ICP-MS (X-Series II) with collision cell technology and kinetic energy discrimination (CCT-KED) to minimize interferences.
  - Internal standards: Sc, Ge, Rh, Ir; external multi-element standards for calibration.
  - Isotope ratios measured: 62Ni/60Ni, 65Cu/63Cu, 70Zn/66Zn, 108Cd/111Cd, 204Pb/208Pb, and Pb isotopes 206/208 and 207/208 for interference checks.
  - Interferences corrected (e.g., 35Cl-35Cl with 70Zn); 204Hg correction via 202Hg; dilution performed as needed to keep detector in pulse-counting mode.
  - Mass-discrimination corrections applied using calibration standards and NIST SRM-981 for Pb; standards run every 20 samples.

- Calculation of exchangeable metal fractions
  - E Value (exchangeable concentration in 0.01 M Ca(NO3)2) and E Ext (in each extractant) derived from isotopic abundance data across spike, spiked-soil, and unspiked-soil solutions.
  - Calculations use spike and reference isotope abundances and soil mass to estimate exchangeable metal pools (formula provided but not reproduced here).

- Data outputs and structure
  - Reported metrics include:
    - M Total: total metal concentrations after digestion.
    - M Ext: metal concentrations in each extractant.
    - E Value: isotopically exchangeable metal fraction in soil.
    - E Ext: exchangeable fraction associated with each extractant.
    - Isotopic abundance measurements and corrections applied during ICP-MS analysis.

- Data quality and provenance notes (Data Leaders perspective)
  - Replication: three replicates per extractant per soil; six replicates for isotopic dilution components.
  - Metadata considerations: sampling locations, depths, contamination histories, extraction conditions, instrument settings, and correction procedures are critical for data discoverability and reuse.
  - Data standards and interoperability: explicit units (mg/kg for metals), clear method descriptions, and documentation of corrections (MD, interference corrections) support cross-study comparability.
  - Potential data gaps: NA values indicate non-applicable measurements; provenance of site-specific contamination histories is cited (Atkinson et al., 2011) for context.
  - Governance implications: dataset supports cross-site comparisons and meta-analyses of metal partitioning and bioavailability, enabling better alignment with data-sharing initiatives and community of practice around soil metal speciation and exchangeable pools.