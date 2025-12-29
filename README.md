# 📡 InSAR-Based Surface Deformation Monitoring Using Remote Sensing
### Case Study: 2025 Tibet Earthquake

---

## Overview
This repository presents a **complete yet lightweight InSAR workflow** for monitoring
surface deformation using **Sentinel-1 SAR remote sensing data**.

The workflow is implemented in **Python using PyGMTSAR** and demonstrated through
a **2025 Tibet Earthquake case study**, while remaining flexible for application to:
- Earthquake deformation analysis
- Volcanic deformation monitoring
- Geothermal surface deformation studies

---

## Background
Interferometric Synthetic Aperture Radar (InSAR) is a remote sensing technique that measures
**ground surface displacement with millimeter-level accuracy** by exploiting phase
differences between multiple SAR acquisitions.

InSAR is widely applied in:
- Tectonic and seismic studies
- Volcanology
- Geothermal reservoir monitoring

This project demonstrates a **simple end-to-end InSAR processing pipeline**
suitable for **education, early-stage research, and technical portfolios**.

---

## Study Area
- **Region**: Tibetan Plateau  
- **Event**: 2025 Tibet Earthquake  
- **Sensor**: Sentinel-1A  
- **Orbit Direction**: Ascending  
- **Polarization**: VV  
- **Subswath**: IW2  

---

## Data Sources
- Sentinel-1 SLC data (Alaska Satellite Facility – ASF)
- Copernicus Global DEM (1 arc-second)
- Precise orbit files (automatically downloaded)

---

## Requirements

### System
- Linux / Google Colab (recommended)
- Python ≥ 3.9
- Stable internet connection (ASF data access)

### Python Packages
All required Python libraries are listed in:

requirements.txt

---

##  Installation

### 🔹 Option 1: Google Colab (Recommended)
Open the notebook directly in **Google Colab**.  
All dependencies and GMTSAR binaries are handled automatically.

---

### 🔹 Option 2: Local Installation (Linux)

```
# Create virtual environment
python -m venv insar-env
source insar-env/bin/activate

# Upgrade pip
pip install --upgrade pip

# Install dependencies
pip install -r requirements.txt
```
⚠️ Important
GMTSAR binary dependencies are not installed via pip
and must be installed separately for local execution.

🔐 ASF Credentials
You must have an ASF (Alaska Satellite Facility) account to download Sentinel-1 data.

Set your credentials inside the notebook:
```
asf_username = "YOUR_USERNAME"
asf_password = "YOUR_PASSWORD"
```
## Workflow Summary
1. Environment setup and dependency installation

2. Sentinel-1 SLC data download (ASF)

3. DEM acquisition

4. Scene stacking and alignment

5. Interferogram generation

6. Coherence estimation

7. Phase unwrapping (SNAPHU)

8. LOS displacement computation

9. 2D and 3D visualization

## Outputs
- Interferogram phase maps

- Coherence maps

- LOS displacement maps (mm)

- Interactive 3D deformation visualizations

- Exported .vtk files

## Interpretation
Line-of-Sight (LOS) displacement values represent ground motion toward or away from
the satellite.

In the 2025 Tibet earthquake case study, observed deformation patterns reflect
tectonic surface displacement associated with seismic activity.

## Applications
- Earthquake deformation analysis

- Volcanic inflation and deflation monitoring

- Geothermal reservoir deformation studies

- Teaching and academic demonstrations

## Limitations
- Atmospheric effects are not corrected

- Only a single interferometric pair is analyzed

- Deformation is measured in LOS direction only

## Author
M. Ilham Azhar

Geophysical Engineering

Sumatra Institute of Technology (ITERA)

## Disclaimer
This repository is intended for educational and research purposes only.
Results should not be used for operational hazard assessment
without further validation.
