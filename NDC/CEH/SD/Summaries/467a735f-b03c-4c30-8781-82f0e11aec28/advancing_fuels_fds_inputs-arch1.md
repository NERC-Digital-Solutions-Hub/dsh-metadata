# Dataset for wildfire simulations in forest environments using Fire Dynamics Simulator (FDS)

- This dataset provides inputs for wildfire simulations in Fire Dynamics Simulator (FDS) within forest environments, using a 40 x 40 m Pinus ponderosa plot in Sycan Marsh, Oregon, USA.
- It includes five segmented LAS point clouds representing different fuel classes, corresponding Bulk Density Files (BDF), and three FDS input files for separate simulations to model fire behavior under varying conditions.

## Data components

- LAS files (5 total)
  - grass_crop.las: fuel class 'grass'
  - shrub_crop.las: fuel class 'shrub'
  - wood_crop.las: fuel class 'tree stem'
  - leaf_crop.las: fuel class 'tree branch+leaves'
  - leaf_crop_high.las: leaf class after virtual pruning treatment (branches under 3 m removed)

- Bulk Density Files (BDF)
  - Binary Fortran unformatted files encoding bulk density values mapped to the 10 cm voxel grid corresponding to each LAS point cloud.
  - Voxels are stored as a 2D array in the modified script to reduce file size.
  - Bulk density values represent vegetation biomass density (g/cm^3) for each voxel.

- FDS input files (3)
  - simulation_1.fds: wildfire simulation configuration for the baseline forest plot
  - simulation_2.fds: simulation after applying the virtual pruning treatment
  - simulation_3.fds: a very high-resolution wildfire simulation in the same forest plot

## Site and data collection

- Site: Sycan Marsh preserve, a large wetland area in the Klamath Basin, Oregon, USA (over 8000 hectares), with the studied plot embedded in surrounding forest.
- Point cloud acquisition: 2019-07-08 to 2019-07-12
  - Equipment: Riegl-VZ400i TLS
  - Sampling rate: 750 kHz; vertical sampling density 0.21 degrees
  - Height: mounted on a tripod at ≥1.5 m
  - Sensor: near-infrared, 1050 nm; max range up to 2000 m
  - Data rates: 50 kHz to 1 MHz

## Point cloud segmentation and processing

- Fuel classes segmented into grass, leaves, shrub, and wood; a virtual pruning treatment further segments the leaf class.
- Segmentation performed with custom deep learning algorithms; code available at https://github.com/3DFin.
- Bulk density files created using a modified Python script based on the FDS User Guide; original 3D voxel arrays converted to 2D to reduce size.
- Generic bulk density values corresponding to each fuel type applied to voxels.

## Virtual treatment and scenarios

- Virtual treatment: simulates reduction of vertical fuel continuity by pruning branches; leaf points within 3 meters of ground removed to model low-branch removal.

## How to run an FDS simulation with the data

- Install FDS (from NIST).
- Open a terminal and navigate to the directory containing the chosen simulation file (e.g., simulation_1.fds).
- Run: fds_local simulation_1.fds
- Post-run outputs include 3D visualizations and logs; view with Smokeview:
  - smokeview simulation_1
- Documentation and further details are available through the FDS-SMV manuals.

## References

- McGrattan, K., McDermott, R., Weinschenk, C., and Forney, G. (2013). Fire Dynamics Simulator Users Guide, Sixth Edition, NIST SP. Available online at NIST.