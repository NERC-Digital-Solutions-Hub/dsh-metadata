# This dataset contains:

## Data assets and site overview
- Field site: Bury Green Brook, Hertfordshire (51.848485, 0.079786); small, ephemeral gravel-bed river with riffle-pool morphology; ~100 m reach; channel width 3–6 m.
- Study aim: measure grain-scale river-bed structure and its variation through riffle-pool sequence.
- Field visits: five visits (Sept 2014; Jun 2015; Jul 2016; Apr 2017; Oct 2018).
- Data components included:
  - Field site overview document
  - Terrestrial Laser Scanner (TLS) data: field topography (.pts)
  - CT scans: raw and processed images (.tif), metadata, and .mat

## Field site control network
- Established in Sept 2014: 12 temporary benchmarks (2 ground permamarkers, 10 survey discs) on fixed features.
- Coordinate system: arbitrary origin (X=1000, Y=1000, Z=100 m); all surveys resectioned into this system before targets surveyed.
- Purpose: enable consistent registration across field visits.

## Terrestrial Laser Scan (TLS) data
- Coverage: ~75 m reach along the thalweg scanned over five visits; scans from 7 locations.
- Targets: 8 high-definition survey targets used for registration.
- Registration: individual scans registered to the arbitrary grid with target locations; RMSE ~0.002–0.005 m.
- Output: TLS data exported as text (.pts) with columns X, Y, Z, intensity.

## CT data (grain-scale bed imaging)
- Purpose: measure grain-scale structure at multiple locations (riffle crest, pool head/shallow/deep/tail).
- Basket deployment: 250 mm diameter metal mesh baskets buried Sept 2, 2015; rim ~1.5 × D below surface; left in place for 19 months; excavated Apr 7, 2017.
- CT scanning: μCT scanning at μ-VIS X-Ray Imaging Centre, Univ. of Southampton; voxel size 600 μm; multiple acquisition parameters specified for high-quality 3D reconstructions.
- Data formats and processing:
  - Pre-processed CT data: HUTCH_files folders containing sonograms and metadata to reconstruct projections.
  - Post-processed CT data: CT image stacks in .tiff format, two folders per basket (Matrix and ParticlesFull).
    - ParticlesFull: gravel grains
    - Matrix: fine-grained matrix
- Basket locations (examples): coordinates (X, Y, Z) and morphological location (Upstream/Downstream; Pool Head/Deep/Tail; Riffle Crest) for baskets such as 1BO, 2RR, 3OY, 4GO, 5OO, 6RG, 7PO, 8RB.

## References
- Hodge, R. A., Sear, D. A., & Leyland, J. (2013). Spatial variations in surface sediment structure in riffle-pool sequences.
- Voepel, H., Leyland, J., Hodge, R., Ahmed, S., & Sear, D. (2019). Development of a vector-based 3D grain entrainment model with XCT data.

## Image reconstruction workflow (CT data)
- Overview: reconstruction is a three-step process from raw scanner data to usable 3D volumes.
  1) Convert sinograms to radiographs.
  2) Determine Centre of Rotation (COR) for accurate reconstruction.
  3) Algebraic reconstruction to produce 3D volumes.
- Converting sinograms to radiographs:
  - Organize sinograms by sample color code; create DigiXCT folders (Radio, Recon, Sino).
  - Use the provided sinogram stacks to generate radiographs with the dedicated converter.
- Centre of Rotation (COR):
  - Use Nikon CT Pro 2D to identify COR, adjust reconstruction radius, and generate centred reconstructions.
  - Save centred reconstructions with filenames indicating sample color code and CC (e.g., rXxxYY_CC_Recon).
- Algebraic reconstruction (DigiXCT3 64-bit):
  - Prepare flat-file information from the reconstruction, enter camera and geometry parameters into the provided Excel workbook (My_calculator.xlsx).
  - Configure DigiXCT3 for input radiographs, output as image stacks (TIFF), and reconstruction method (e.g., NITRO).
  - Adjust preview, geometry, and reconstruction parameters to optimize grain/matrix representation.
  - Save reconstructions and associated vgl files for later use in registration and clipping steps.

## Registration and clipping (VGStudio Max and Fiji)
- Purpose: reorient study volumes so gravity is aligned with the Z-axis, then clip to a consistent sample region.
- Registration steps:
  - Import CT reconstruction stacks into VGStudio Max.
  - Re-orient so XY plane is orthogonal to gravity; register using markers on the downstream basket rim (via Simple 3-2-1 registration).
  - Validate alignment by cross-checking 2D slices and 3D view; adjust as needed and re-perform if rotation exceeds tolerance.
- Clipping workflow:
  - Use a selection cube/ROI to enclose the desired portion of the sample, ensuring all stones are captured while excluding the bottom region.
  - Create a Region of Interest (Region 1) and extract ROI; lock views to preserve alignment during clipping.
  - Export the clipped region as a raw volume (Raw volume (*.raw)) with a filename including sample run and color code (e.g., RRCC_Registered_Clipped_x<xxx>_y<yyy>_z<zzz>.raw) and generate a corresponding VGL file.
  - Export rotated TIFF version for archival and reproducibility (e.g., r1py_Registered_Clipped_Rotated.tif).
- Fiji rotation to align downstream marker:
  - Import the raw volume into Fiji (ImageJ) as 16-bit unsigned; orient using marker alignment, rotate with bilinear interpolation, and save as TIFF for storage in the Recon folder.
  - Ensure TIFF uses appropriate bit-depth (Long16 for matrix, Short16 for particles) for subsequent analyses.

## Data governance and reproducibility notes
- Dataset includes both raw and processed data across multiple modalities (TLS topography and CT imagery) with clear folder structures and naming conventions to support traceability.
- Detailed, step-by-step workflows for data reconstruction, registration, clipping, and orientation are documented to enable reproducibility and cross-team collaboration.
- Metadata and references accompany the data to support validation and reuse in further studies.