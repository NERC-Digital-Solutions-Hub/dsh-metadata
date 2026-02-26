# IMOGEN: Climate pattern scaling set for an ensemble of 22 GCMs - adding uncertainty to the IMOGEN impacts system (In Prep)

- Purpose: The dataset provides the parameters and monthly land-surface pattern changes used by the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system. It supports testing new land surface parameterisations before full GCM implementation and projecting future emission scenarios not yet simulated by GCMs.
- Modelling approach: Utilises pattern-scaling to emulate GCMs, linking local monthly meteorology changes to global warming in a linear fashion. An Energy Balance Model (EBM) translates evolving radiative forcing into land warming, accounting for oceanic delays.

Introduction and scope
- IMOGEN is coupled with the JULES land surface model and relies on pattern-scaling patterns derived from multiple GCMs.
- A detailed dataset description is forthcoming in Zelazowski et al. (In Prep): “Climate pattern scaling set for an ensemble of 22 GCMs – adding uncertainty to the IMOGEN impacts system.”

Data Description
- Energy Balance Model (EBM) parameters (per GCM): 
  - λ_l: climate sensitivity over land (W m^-2 K^-1)
  - λ_o: climate sensitivity over ocean (W m^-2 K^-1)
  - κ: ocean effective thermal diffusivity (W m^-1 K^-1)
  - ν: constant ratio of mean land to ocean SST warming (unitless)
  - f: ocean fraction (one minus land fraction, including Antarctica)
- Calibration: Parameters calibrated against 22 GCMs from CMIP3 (Meehl et al., 2007).
- Pattern data: Local and monthly patterns (patterns per degree of global warming) are available for download; ASCII format.
- Data notes: Patterns are mapped to a common grid (2.5° x 3.75° HadCM3 grid; 1631 land points).

Data Structure
- Directory structure: For each GCM, a directory named pattRelPR_d2_[GCM name] (22 directories in total).
- Files: Within each directory, monthly ASCII files labeled jan, feb, ..., dec.
- File format: Each file contains a header line and 1631 lines of data corresponding to land points.
- Data columns (per land point):
  1. Longitude
  2. Latitude
  3. Temperature change per degree global warming (Kelvin × Kelvin^-1)
  4. Relative humidity change per degree global warming
  5. Wind change per degree global warming
  6. Unused (0.0)
  7. Longwave change per degree global warming
  8. Shortwave change per degree global warming
  9. Unused (0.0)
  10. Precipitation change per degree global warming
  11. Unused (0.0)
  12. Pressure change per degree global warming
  13. Unused (0.0)
- Grid details: All GCMs re-mapped to a common 2.5° x 3.75° grid; 1631 land points.

Quality Control and Future Development
- Status: Part of a beta program to extend IMOGEN EBM and pattern parameterisation beyond CMIP3.
- Validation: Calibrated against CMIP3, with plans to emulate CMIP5 data (full traceability and UK ISO standards anticipated).

Usage and provenance
- Coupling: IMOGEN is routinely coupled to JULES; examples of coupling available in related publications (Huntingford et al., 2010; Best et al., 2011; Clark et al., 2011).
- References and context: 
  - IMOGEN overview and pattern-scaling rationale (Huntingford et al., 2010; Huntingford & Cox, 2000).
  - CMIP3 multi-model dataset context (Meehl et al., 2007).
  - JULES model descriptions (Best et al., 2011; Clark et al., 2011).

Acknowledgements
- Data providers: Modeling groups, PCMDI, WGCM, WCRP CMIP3 project.
- Support: U.S. Department of Energy, Office of Science.

Notes for Data Leaders
- Data availability: Patterns and parameters are organized per GCM with clear naming and monthly files, enhancing discoverability and reuse.
- Metadata and standards: Current description includes explicit parameter definitions, file structure, and units; future updates aim for enhanced traceability and conformity with UK ISO standards.
- Community and collaboration: Dataset sits within a framework that supports broader data sharing and cross-model comparisons, with ongoing work to extend to CMIP5 and beyond.