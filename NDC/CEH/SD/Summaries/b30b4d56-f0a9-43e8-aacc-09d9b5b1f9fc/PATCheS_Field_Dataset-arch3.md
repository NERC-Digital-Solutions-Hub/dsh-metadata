# This dataset contains: Overview of field site and datasets

- Purpose and site
  - Field work aimed to measure grain-scale structure of a gravel-bed river and its variation through a riffle-pool sequence.
  - Study site: Bury Green Brook, Hertfordshire (small, ephemeral river with riffle-pool morphology), ~100 m reach, channel width 3–6 m.
  - Field visits occurred five times: Sept 2014; Jun 2015; Jul 2016; Apr 2017; Oct 2018.
  - Background reference: Hodge et al. (2013).

- Field site control network
  - An arbitrary coordinate system was established with 12 temporary benchmarks (2 ground permamarkers, 10 survey discs) tied to trees/posts.
  - Surveying performed with a reflectorless Leica total station; system resectioned into the common coordinate frame for subsequent surveys.

- Terrestrial Laser Scan (TLS) data
  - Scans collected along ~75 m of the channel at each visit.
  - 8 High Definition Survey targets used; data registered to the arbitrary grid with RMSE 0.002–0.005 m.
  - Scans exported as text (PTS) with columns: X, Y, Z, intensity.

- CT data (computed tomography)
  - Objective: measure grain-scale bed structure at multiple locations.
  - Method: bury 250 mm diameter metal mesh baskets at riffle crest, pool head/shallow/deep/tail locations; baskets left for 19 months, excavated Apr 2017.
  - CT imaging performed with a Nikon μCT scanner (μ-VIS X-Ray Imaging Centre, University of Southampton) with voxel size 600 μm; ~951 projections; artifacts corrections noted.
  - Data formats:
    - Pre-processed: provided in HUTCH_files with sonograms and reconstruction metadata.
    - Post-processed: CT image stacks in .tiff; two folders per basket: Matrix (fine-grained matrix) and ParticlesFull (grains only).
  - Basket burial locations (example entries listed with coordinates in the same total-station coordinate system).

- References
  - Hodge, R. A. et al. (2013) on spatial variations in surface sediment structure.
  - Voepel, H. et al. (2019) on a vector-based 3D grain entrainment model with XCT data.

- Image reconstruction workflow (CT data)
  - Step 1: Sinograms to radiographs
    - Organize sinograms by color-coded sample folders; create DigiXCT workflow folders (Radio, Recon, Sino).
    - Use sinogram-to-radiograph converter per sample code.
  - Step 2: Centre of rotation (COR)
    - Use Nikon CT Pro 2D to identify CORs; adjust reconstruction radius; save centred images with filenames including sample color code and “ Recon”.
  - Step 3: Algebraic reconstruction (DigiXCT)
    - Prepare flat-file with COR, detector/pixel sizes, source-object/detector distances.
    - Configure hardware, input, and output settings (image stacks in TIFF, 32-bit float data, dimensions, and voxel sizes).
    - Select reconstruction method (NITRO used here); optional volume processing and preview adjustments.
    - Save final reconstruction as a stack within the Recon folder; export a corresponding vgl file when prompted.
  - Step 4: Registration and clipping (VGStudio Max)
    - Reorient the sample so gravity aligns with the Z-axis; register using downstream basket marker; clip the volume at the third ring from the top rim to standardize the region of interest.
    - Create Regions of Interest (ROI), extract and export aligned/clipped volumes as Raw (.raw) and VGL files; filenames include run number, color code, and clipping details.
  - Step 5: Fiji (ImageJ) processing and orientation
    - Rotate downstream marker to align with X-axis; ensure 16-bit unsigned format; save the rotated image as TIFF with a filename indicating registered, clipped, and rotated status.
  - Step 6: Export and data management
    - Maintain careful naming conventions to reflect run, color code, processing steps, and grid sizes.
    - Rotated TIFFs accompany raw CT data for downstream analysis (e.g., Matlab).

- Registration, clipping, and downstream processing notes
  - Registration checks performed by visual inspection across 2D and 3D views; adjust as needed, preserving rim integrity.
  - Clipping strategy focuses on enclosing stones while preserving the basket rim visibility; the resulting ROI is exported for reproducibility.
  - Fiji steps emphasize orientation accuracy where the downstream tab aligns with the X-axis, with careful conversion to 16-bit TIFFs for subsequent analyses.

- Output and reproducibility
  - Data are provided in multiple formats (PTS TLS data, pre/post CT data in folders, TIFF/RAW volumes, VGL files) to enable re-use and auditability.
  - The workflow comprises a transparent, multi-software pipeline (Leica Cyclone, Nikon CT Pro 2D, DigiXCT, VGStudio Max, Fiji/ImageJ) with explicit step-by-step instructions to reproduce reconstructions and ROIs.
  - Data management includes explicit folder structures, sample codes, and consistent naming conventions to track processing stages and dataset lineage.