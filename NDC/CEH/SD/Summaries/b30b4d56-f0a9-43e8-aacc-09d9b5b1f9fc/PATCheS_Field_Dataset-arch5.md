# This dataset contains:

## Field Site Overview
- Aim: measure grain-scale structure of a gravel-bed river and its variation through a riffle-pool sequence.
- Location: Bury Green Brook, Hertfordshire (approx. 51.848485, 0.079786); ephemeral, riffle-pool morphology; ~100 m study reach; channel 3–6 m wide.
- Field campaigns: five visits (Sept 2014; Jun 2015; Jul 2016; Apr 2017; Oct 2018).
- Related publication for site context: Hodge et al. 2013.

## Field Site Control Network
- 12 temporary benchmarks established in September 2014 (2 ground permamarkers, 10 survey discs).
- Arbitrary coordinate system with origin set to X=1000, Y=1000, Z=100 m; reaffirmed by resectioning during subsequent surveys.

## Terrestrial Laser Scan (TLS) Data
- Coverage: 75 m reach surveyed across five field visits.
- Setup: 8 High Definition Survey targets; 7 scan locations; scans registered to the arbitrary grid.
- Equipment and settings: Leica P20 scanner; 3.1 mm resolution at 10 m; RMSE of registration 0.002–0.005 m.
- Output: text (PTS) files with X, Y, Z, intensity; data exported per site visit.

## CT Data
- Purpose: grain-scale measurement of river-bed structure using buried baskets.
- Basket deployment: 250 mm diameter metal mesh baskets buried at riffle crest, pool head/shallow/deep/tail locations on 2 Sept 2015; left for ~19 months; retrieved 7 Apr 2017.
- CT scanning: μCT at μ-VIS X-Ray Imaging Centre, University of Southampton; voxel size 600 μm; 951 projections; reconstruction using Digi XCT; reference alignment with VGStudio Max.
- Data formats:
  - Pre-processed data: HUTCH_files folders with sonograms and metadata to reconstruct projections (multiple baskets per folder in some cases).
  - Post-processed data: CT image stacks in TIFF; two folders per basket: Matrix (fine-grained matrix) and ParticlesFull (grains only).
- Basket locations (X, Y, Z) and morphological locations provided (Table 1); coordinate system is the same as the total station and TLS data.
- References for methods: Hodge et al. 2013; Voepel et al. 2019.

## Image Reconstruction (CT)
- Overview: a three-step process to turn raw CT data into usable 3D volumes.
  1) Sinograms to radiographs: organize by basket color code, convert using DigiXCT tools, determine center of rotation (COR).
  2) COR determination and initial reconstruction: use Nikon CT Pro 2D workflow to center volumes, adjust radius, standardize file naming with color codes, batch processing via CT Agent and VG Studio Max for validation.
  3) Algebraic reconstruction: configure DigiXCT3 64-bit with flat-file parameters, Fiji for image dimensions, and an Excel workbook (My_calculator.xlsx) for hardware and geometry definitions; choose reconstruction method (NITRO preferred; alternative: FBP); generate 3D image stacks and associated file naming (r3yy, etc.).
- Output: TIFF image stacks or raw volumes; detailed naming conventions include run number (RR) and color code (CC); dedicated configuration files saved for reproducibility.
- Tools involved: DigiXCT (and DigiXCT3), Fiji (ImageJ), VGStudio Max, NT data handling with My_calculator.xlsx.

## Registration and Clipping
- Objective: reorient data so XY is orthogonal to gravity; register baskets using downstream marker; clip to standard height (third ring from top) for consistent analysis.
- Workflow:
  - Import DigiXCT reconstructions into VGStudio Max; set resolution and ROI/skip carefully.
  - Use Simple Registration to place three yellow markers on basket rim; validate with 3D/2D slices; adjust orientation if necessary.
  - Create a Region of Interest (ROI); extract ROI as Region 1; export aligned/clipped volume as a raw file and generate a corresponding VGL file for future reference.
  - Rotate downstream marker in Fiji to align with downstream X-axis; save rotated TIFF in Recon folder with _Rotated.tif suffix; ensure 16-bit data types (Long16 for matrix, Short16 for particles).
- Notes: maintain lock in Scene Tree to preserve alignment across views; careful handling of clipping to avoid eroding rim features; filenames should reflect processing steps and grid sizes (e.g., r1py_Registered_Clipped_x515_y509_z154.raw).

## Data Formats and Governance Considerations
- Data formats used:
  - Field data: TLS point clouds in .pts format; CT raw data and metadata in HUTCH_files; CT post-processing outputs in .tiff (two folders: Matrix and ParticlesFull).
  - CT volume exports: Raw volumes (.raw) and corresponding VGL metadata; rotated TIFFs for final registration checks.
- Coordinate systems and provenance:
  - A common, pre-established coordinate system ties TLS, CT, and field measurements; registrations rely on shared reference points (downstream markers, gravity orientation).
  - Documentation includes explicit basket locations (X, Y, Z) aligned to the same coordinate frame as total station and TLS data.
- Documentation and reproducibility:
  - Detailed, step-by-step workflows for sinogram conversion, COR finding, reconstruction parameterization, and registration/clipping to enable reproducibility.
  - References to related literature provided to contextualize methods.
- Potential considerations for data stewards:
  - Ensure metadata completeness for all datasets (site, dates, equipment, coordinate systems, basket IDs, processing steps).
  - Maintain clear data lineage (raw vs. processed vs. final orientation/clipped results) and consistent naming conventions across datasets.
  - Track any embargoes or access restrictions and ensure data discovery through portal/catalogue alignment.
  - Support interoperability across different processing software (DigiXCT, Fiji/ImageJ, VGStudio Max).

## References
- Hodge, R. A., Sear, D. A., & Leyland, J. (2013). Spatial variations in surface sediment structure in riffle-pool sequences: a preliminary test of the Differential Sediment Entrainment Hypothesis (DSEH). Earth Surface Processes and Landforms, 38(5), 449-465.
- Voepel, H., Leyland, J., Hodge, R., Ahmed, S., & Sear, D. (2019). Development of a vector-based 3D grain entrainment model with application to X-ray computed tomography (XCT) scanned riverbed sediment. Earth Surface Processes and Landforms, 44(15), 3057-3077.