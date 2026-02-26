# CFD Data for Biofilm Streamer in Laminar Flow and Bedform Permeability Study

## Overview
- Two CFD data descriptions are included:
  - Biofilm-streamer laminar flow simulations (1240 files total across Reynolds numbers 400–700).
  - Bedform permeability study with flow over dunes, using a Brinkman-layer model (datasets ending _porbed and _dune).
- Purpose: support map-based visualization and spatial analysis of hydrodynamics, biofilm oscillations, and bed-permeability effects.

## Simulations 1: Biofilm-streamer laminar flow (Re 400–700)
- Data scope
  - 1240 files total; 310 files for each Reynolds number (Re = 400, 500, 600, 700).
  - Time series from 0.12 s in 0.12 s increments; total simulation time 30 s.
  - Investigates how changing Reynolds number influences ambient flow characteristics and biofilm oscillation frequency.
- Model domain and geometry
  - Channel: length 25 cm, depth 4 cm.
  - Biofilm tail: length 2.5 cm; attached to a rigid cylindrical base (1 cm diameter).
  - Base center located 2 cm from inlet and 2 cm from both the bottom and top walls.
- Physics and solver
  - Fluid-structure interaction (FSI) with two nonoverlapping domains: fluid Ω_f and solid Ω_s (biofilm).
  - Fluid domain solved with Navier–Stokes; solid domain with linear elasticity for the biofilm.
  - Coupled solver; flow partially develops for the first 2 seconds before engaging the structural solver.
  - Point P coordinates tracked at every time step for the full duration.
- Parameters
  - Inlet mean velocity Umean 0.4–0.7 m/s (to achieve Re 400–700 with given D and ν).
  - Fluid density ρ_f = 1000 kg/m^3; biofilm density ρ_b = 1000 kg/m^3.
  - Young’s modulus Es = 5000; Poisson’s ratio υ_s = 0.4; dynamic viscosity μ = 0.01 Pa·s.
- Data variables in files
  - X, Y, Z coordinates (m)
  - Cn concentration (g/L)
  - U, V, W velocity components (m/s)
- Data access and references
  - Full details in Sinha et al. (2017), Water Resources Research (open access link provided).
- GIS relevance
  - Provides spatially resolved velocity and concentration fields in a 3D channel.
  - Suitable for generating 2D/3D maps, cross-sections, and time-evolving visualizations of flow around a biofilm structure.

## Simulations 2: Bedform permeability with Brinkman-layer flow (_porbed and _dune)
- Data scope
  - CFD model combining boundary-layer and Brinkman (porous) flow to assess bed permeability effects over bedforms (dunes).
- Model domain and geometry
  - Channel: length 4.8 m, width 0.35 m, height 0.60 m.
  - Permeable bed: uniform spheres (D = 0.038 m) arranged in six layers; h_bed ≈ 0.228 m; porosity ≈ 50%.
  - Permeable bed spans the entire bed; dunes with k = 0.41 m, amplitude 0.056 m, and leeside angle 27° spanning the width.
- Flow conditions
  - Free-stream velocity Uo = 0.16 m/s; Reynolds number Re ≈ 3.0 × 10^4; Froude number Fr ≈ 0.12.
  - Outlet uses fixed-pressure boundary; mass can enter/leave; walls are no-slip; free surface approximated as a rigid lid.
- Data variables in files
  - X, Y, Z coordinates (m)
  - PRPS (material variable; water/solid)
  - VEL1-X, VEL1-Y, VEL1-Z (velocity components)
  - U1, V1, W1 (downstream, lateral, vertical velocities)
  - P1 (pressure); KE (turbulent kinetic energy); Ε (dissipation rate); EP (turbulent dissipation); EPKE (product of KE and dissipation)
  - XN, ZN (normalized coordinates); NKE (normalized KE); UN, WN (velocities normalized by inlet)
- Data access and references
  - Full details in Sinha et al. (2017), Water Resources Research (open access).
- GIS relevance
  - Delivers rich spatial fields of velocity, pressure, and turbulence over a permeable bed and dune geometry.
  - Enables mapping of surface/subsurface flow patterns, bed-permeability effects, and cross-sectional analyses relevant to river/channel modelling.

## Data packaging, formats, and challenges
- Data characteristics
  - High-volume CFD outputs organized by scenario and file suffixes (_dune, _porbed).
  - Multivariate 3D grids with time-resolved data.
- GIS workflows
  - Import coordinates and fields to produce velocity magnitude maps, pressure maps, and turbulence maps.
  - Create time-series visualizations and derived products (e.g., cross-sections, flow over-bed profiles).
  - Integrate with bedform geometry for combined surface/subsurface flow analyses.
- Challenges for GIS integration
  - Data spread across multiple files with varying conventions; need consistent metadata and standards.
  - Large dataset size requiring scalable data handling.
  - Translating 3D CFD outputs to GIS-friendly 2D/3D visualizations may require slicing or projection.

## References
- Sinha, S., Hardy, R.J., Blois, G., Best, J.L., and Sambrook Smith, G.H. (2017). The influence of bed permeability on the structure of turbulent flow over bedforms: a numerical investigation. Water Resources Research.