# Nitrous oxide fluxes from an intensively managed grazed grassland in Scotland

- Objective
  - Measure fluxes of nitrous oxide (N2O) from an intensively managed grazed grassland before and after a tillage event on May 1, 2012, to understand how tillage and management affect N2O emissions.

- Study site and management context
  - Easter Bush, Scotland (approx. 55° 51' 55.30"N, 3° 12' 22.17"W).
  - Two 5.4 ha fields with intensive livestock production; continuous sheep grazing and high nitrogen fertilization (≈200 kg N ha−1 y−1).
  - Soil: clay loam, imperfectly drained, with a pH ~5.1; drainage system present but not functioning well, leading to surfacewater events.
  - Fields: North (un-tilled) continuously grazed; South (tilled) ploughed to 30 cm on May 1, 2012 after glyphosate kill, harrowed, rolled, and reseeded with ryegrass; nitrogen fertilization applied to both fields at times (North had two 70 kg-N ha−1 applications in May and August; South had a single 70 kg-N ha−1 application in August).

- Experimental design and timing
  - Baseline measurements prior to tillage; tillage event occurred on May 1, 2012; post-tillage measurements continued to capture immediate and subsequent flux responses.
  - Key management events captured in a timeline (Feb–Sept 2012) including tillage, herbicide application, reseeding, grazing, and fertilizer applications.

- Measurement methods
  - Eddy covariance (EC)
    - Setup: EC system installed March 27 on field boundary; 2.4 m height; 10 Hz measurements.
    - Gas analysis: 3-axis ultrasonic anemometer for wind; quantum cascade laser (QCL) for N2O, H2O, and CO2; data at 30-minute intervals processed with EddyPro.
    - Processing and corrections: double coordinate rotation (vertical and crosswind); spike removal; block averaging; time lag removal by covariance maximization; corrections for high/low-frequency losses (Moncrieff et al. 1997); density fluctuation corrections (Burba et al. 2012); quality control (Foken et al. 2005) with category 2 flagging to remove poor-quality flux measurements.
    - Field separation: initial classification of flux data by wind direction to attribute to tilled vs un-tilled field; data outside acceptable wind directions were discarded due to obstructions.

  - Chamber measurements
    - Static chambers
      - Structure: PVC cylinders, 38 cm inner diameter, 22 cm height; inserted 5 cm into soil; 40-minute closures; three 100 mL gas samples at 0, 20, 40 minutes.
      - Analysis: gas samples analyzed by GC with an electron capture detector.
      - Deployment: ten chambers per field, positioned within the EC flux footprint (10–200 m from the mast); chambers occasionally moved to avoid microclimate biases and to allow farm vehicle access.
      - Flux calculation: F = (dC/dt) × (ρ × V) / A.
    - Dynamic chamber (QCL-based)
      - Setup: chamber (39 cm ID, 22 cm high) placed on soil with a 15 cm insertion; closed system with tubing to QCL; ~30 m radius from cabin; flow ~6–7 L min−1; ~22 s lag.
      - Data: N2O fluxes calculated from 1 Hz data over 3 minutes; both linear and non-linear asymptotic regression methods applied; best-fit method selected per measurement.
      - Sensitivity: detection limit ~0.04 nmol m−2 s−1 (superior to static chamber method).

- Data outputs and metadata
  - Primary data file: Easter_Bush_EddyC_Tillage_2012 containing time-stamped fluxes and ancillary variables (tau, H, LE, CO2_flux, H2O_flux, N2O_flux, wind metrics, u*, TKE, L, (z-d)/L, Bowen ratio, etc.).
  - Associated field metadata include location, field management events, environmental conditions (air temperature, soil temperature, rainfall, PAR), and instrumentation details.

- Data quality, governance, and challenges
  - Data quality controlled through established protocols (frequency response corrections, density adjustments, and standard QC framework).
  - Potential barriers for monitoring programs highlighted by the study design include obstructions affecting EC data (wind-direction-based data segregation) and the need to align multiple measurement methods (EC and chambers) for robust inference.
  - The approach demonstrates integration of continuous (EC) and discrete (chamber) measurements to capture spatial–temporal variability in N2O fluxes and the effects of agricultural management practices.

- Relevance to monitoring framework considerations
  - Illustrates the importance of combining multiple measurement modalities to monitor environmental health indicators (N2O fluxes) in agricultural landscapes.
  - Highlights data governance aspects: standardised processing workflows, clear QA/QC steps, transparent methodology for challenging data (e.g., wind-obstructed periods), and documentation of metadata and data outputs.
  - Demonstrates the need for metadata completeness and data accessibility to support verification, replication, and governance in environmental monitoring frameworks.