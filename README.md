# 📡 InSAR-Based Surface Deformation Monitoring Using Remote Sensing
### Case Study: 2025 Tibet Earthquake

---

## 🔍 Overview
This repository provides a **complete yet lightweight InSAR workflow** for monitoring
surface deformation using **Sentinel-1 SAR remote sensing data**.

The workflow is implemented in **Python using PyGMTSAR** and demonstrated through
a **2025 Tibet Earthquake case study**, while remaining reusable for:
- Earthquake deformation
- Volcanic deformation
- Geothermal surface deformation monitoring

---

## 🌍 Background
Interferometric Synthetic Aperture Radar (InSAR) measures **ground displacement
with millimeter-level accuracy** by exploiting phase differences between SAR acquisitions.

This method is widely applied in:
- Tectonic and seismic studies
- Volcanology
- Geothermal reservoir monitoring

This project demonstrates a **simple end-to-end InSAR pipeline**
suitable for **education, research, and portfolio demonstration**.

---

## 📍 Study Area
- **Region**: Tibetan Plateau
- **Event**: 2025 Tibet Earthquake
- **Sensor**: Sentinel-1A
- **Orbit**: Ascending
- **Polarization**: VV
- **Subswath**: IW2

---

## 🛰️ Data Sources
- Sentinel-1 SLC (ASF – Alaska Satellite Facility)
- Copernicus Global DEM (1 arc-second)
- Precise orbit files (auto-downloaded)

---

## 🧰 Requirements

### System
- Linux / VS Code / Google Colab (recommended)
- Python ≥ 3.9
- Internet connection (ASF data download)

### Python Packages
```
pygmtsar
xarray
dask
geopandas
numpy
pandas
matplotlib
pyvista
panel
```

---

## 📦 Installation

### 🔹 Option 1: Google Colab (Recommended)
Open the notebook directly in Google Colab.  
All dependencies will be installed automatically.

---

### 🔹 Option 2: Local Installation (Linux)

```bash
# Create virtual environment
python -m venv insar-env
source insar-env/bin/activate

# Upgrade pip
pip install --upgrade pip

# Install PyGMTSAR
pip install pygmtsar

# Install additional dependencies
pip install xarray dask geopandas numpy pandas matplotlib pyvista panel
```
⚠️ GMTSAR binaries are required and must be installed separately on local systems.

## ASF Credentials

You must have an ASF (Alaska Satellite Facility) account.

Inside the notebook, set:
```
asf_username = "YOUR_USERNAME"
asf_password = "YOUR_PASSWORD"
```
## Workflow Summary

1. Environment setup & dependency installation

2. Sentinel-1 SLC data download (ASF)

3. DEM acquisition
   
4. Scene stacking and alignment

5. Interferogram generation

6. Coherence estimation

7. Phase unwrapping (SNAPHU)

8. LOS displacement computation

9. 2D & 3D visualization

## Outputs

- Interferogram phase maps

- Coherence maps

- LOS displacement maps (mm)

- Interactive 3D deformation models

- Exported .vtk files

## Interpretation

LOS displacement values indicate ground motion toward or away from the satellite.
In the Tibet 2025 case study, deformation patterns reflect tectonic displacement
related to seismic activity.

## Applications

- Earthquake deformation analysis

- Volcanic inflation/deflation monitoring

- Geothermal reservoir deformation

- Teaching & academic demonstration

## Limitations

- Atmospheric correction not applied

- Single interferometric pair

- LOS-only deformation (no 3D decomposition)

## Author

M. Ilham Azhar
Geophysical Engineering
Sumatra Institute of Technology (ITERA)

## Disclaimer

This repository is intended for educational and research purposes only.
Results are not suitable for operational hazard assessment without further validation.

