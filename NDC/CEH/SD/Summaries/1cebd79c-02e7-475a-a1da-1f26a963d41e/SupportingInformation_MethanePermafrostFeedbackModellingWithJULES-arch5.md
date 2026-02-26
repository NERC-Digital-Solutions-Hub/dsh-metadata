# Background, Experiment Design and Analytical Methods

- Purpose and scope
  - Describes the dataset used in Comyn-Platt et al. (2018) and provides a summary of data, methods, and structure for full details in the data citation article.
  - Enables assessment of climate-carbon cycle interactions, including permafrost thaw and wetland methane feedbacks, within the JULES land surface model and the IMOGEN climate–carbon cycle emulator.
  - Outputs are designed to support calculation of anthropogenic fossil fuel emission budgets under different warming targets and model configurations.

- Models and data lineage
  - JULES (Joint UK Land Environment Simulator) – land surface model (version 4.8) with a multi-layer soil-carbon component.
  - IMOGEN – an intermediate complexity emulator that uses pattern scaling to represent climate/meteorology from 34 CMIP5 GCMs.
  - Data built on established literature and models (JULES, IMOGEN) and linked to prior studies on methane, permafrost, and wetland processes.

- Experiment design (12 simulations total)
  - Temperature pathways (3): 
    - 2deg: stabilisation at 2°C by 2100
    - 1p5deg: stabilisation at 1.5°C by 2100
    - 1p5degOS: 1.5°C by 2100 with overshoot to 1.75°C
  - Model configurations (4): 
    - BLco: baseline without methane feedback
    - CH4_lowQ10: low temperature sensitivity methane feedback
    - CH4_poorFEN: methane feedback with fen-like wetlands
    - CH4_richFEN: methane feedback with rich fen wetlands
  - Purpose: explore carbon stocks, feedbacks (wetlands, permafrost), and warming impacts to derive fossil fuel emission budgets.

- Data products and contents
  - Global and gridbox-level outputs for 1850–2099, including:
    - Vegetation and soil carbon stocks (cv, cs_gb, cs_old_gc)
    - Methane flux from wetlands (fch4_wetl_cs)
    - Land cover fractions (frac)
    - Soil temperature and moisture (t_soil, smcl)
    - Wetland fraction (fwetl)
    - Wood-products carbon (wood_products)
    - Atmospheric CO2 and methane concentrations (co2_ppmv, ch4_ppbv)
    - Global warming indicators (dtemp_g, dtemp_o, dtemp_l)
    - Ocean CO2 uptake (Ocean_uptake)
  - Units and dimensions are provided (e.g., kg m^-2 for carbon; K for temperature; time, latitude, longitude for grid data; global for certain variables).

- Data structure and accessibility
  - NetCDF files with self-describing headers; accessible via standard tools (R, Python, nco, etc.).
  - File contents cover variables, dimensions, and metadata needed for visualization and analysis.

- File naming and organization
  - Directory structure: exp/scenario/exp_CEN_center_MOD_scenario.CarbonStocks.1850-2099.nc
  - Exp values: BLco, CH4_lowQ10, CH4_poorFEN, CH4_richFEN
  - Scenarios: 2deg, 1p5deg, 1p5degOS
  - Filenames align with CMIP5 portal conventions for centre and model names; centers and models listed in Appendix Table.

- Documentation, provenance, and related work
  - Connected to Comyn-Platt et al. (2018) and prior methanogenesis and permafrost studies (Gedney 2004; Burke et al. 2018) and JULES/IMOGEN development papers.
  - Appendix provides a list of the climate modelling centres and GCM names used to drive JULES via IMOGEN.

- Governance, use and reuse considerations for Data Stewards
  - Clear provenance: links to foundational papers and dataset lineage; ensure citation and versioning align with the Comyn-Platt (2018) work.
  - Metadata and interoperability: NetCDF with standard dimensions and units; verify consistency across simulations and configurations.
  - Reproducibility: factorial design supports cross-comparisons across pathways and methane-feedback configurations; suitable for validating fossil fuel emissions budgets under different warming targets.
  - Data management: large multi-model outputs; maintain structure, naming conventions, and centre/model mappings to CMIP5 portal; ensure long-term accessibility and documentation.

- Appendix and references
  - Appendix lists the modelling centres and GCMs used (e.g., BCC, BNU, CCCma, CMCC, CNRM-CERFACS, CSIRO, INM, IPSL, MIROC, MOHC, MPI-M, MRI, NASA-GISS, NCAR, NCC, NOAA-GFDL, NSF-DOE-NCAR).
  - Key references include Comyn-Platt et al. (2018), JULES (Clark et al. 2011), IMOGEN (Huntingford et al. 2010), and CMIP5 design (Taylor et al. 2012).