# InSAR-Based-Surface-Deformation-Monitoring-Using-Remote-Sensing

A basic remote sensing and InSAR processing workflow for monitoring surface deformation, applicable to earthquake, volcanic, and geothermal studies.

# InSAR-Based Surface Deformation Monitoring Using Remote Sensing
### Case Study: 2025 Tibet Earthquake

## Overview
This repository presents a basic yet complete workflow for monitoring surface deformation using
Interferometric Synthetic Aperture Radar (InSAR) and remote sensing data.
The implementation is developed in Python using **PyGMTSAR** and applied to a **case study of the 2025 Tibet earthquake**.

The workflow is designed to be **flexible and reusable**, allowing application to:
- Earthquake deformation analysis
- Volcanic deformation monitoring
- Geothermal surface deformation studies

---

## Background
InSAR is a remote sensing technique that utilizes phase differences between two or more SAR images
to measure ground surface displacement with millimeter-level accuracy.
It is widely used in geophysics for detecting deformation caused by:
- Tectonic earthquakes
- Volcanic inflation and deflation
- Geothermal reservoir dynamics

This notebook demonstrates a **simple end-to-end InSAR processing pipeline** suitable for educational
purposes and early-stage research.

---

## Study Area
- **Region**: Tibetan Plateau
- **Event**: 2025 Tibet Earthquake
- **Sensor**: Sentinel-1A SAR
- **Orbit Direction**: Ascending
- **Polarization**: VV
- **Subswath**: IW2

---

## Data Sources
- **Sentinel-1 SLC** data from ASF (Alaska Satellite Facility)
- **Copernicus Global DEM (1 arc-second)**
- Orbit files automatically downloaded using PyGMTSAR

---

## Software and Libraries
- Python 3.x
- PyGMTSAR
- GMTSAR
- Xarray, Dask
- GeoPandas
- Matplotlib
- PyVista & Panel (3D visualization)
- Google Colab environment

---

## Workflow Overview
The InSAR processing steps implemented in this notebook are:

1. **Environment Setup**
   - Install PyGMTSAR and GMTSAR dependencies
   - Configure Google Colab and widget manager
   - Initialize virtual framebuffer for 3D visualization

2. **Data Acquisition**
   - Download Sentinel-1 SLC scenes from ASF
   - Download precise orbit files
   - Download Copernicus Global DEM

3. **Scene Preparation**
   - Scan SLC data
   - Select subswath and polarization
   - Stack initialization

4. **Geometric Processing**
   - Scene reframing using AOI
   - DEM loading
   - Image alignment
   - Geocoding

5. **Interferogram Generation**
   - Phase difference calculation
   - Topographic phase correction
   - Multilooking and filtering
   - Goldstein phase filtering

6. **Coherence Estimation**
   - Correlation calculation
   - Coherence masking

7. **Phase Unwrapping**
   - SNAPHU unwrapping
   - Low-coherence masking

8. **Surface Deformation Analysis**
   - Line-of-Sight (LOS) displacement computation
   - Conversion to geographic coordinates
   - Visualization of displacement patterns

9. **Visualization**
   - 2D maps of interferogram and LOS displacement
   - Interactive 3D visualization using PyVista

---

## Outputs
The notebook produces the following outputs:
- Interferogram phase maps
- Coherence maps
- LOS displacement maps (mm)
- 3D interactive deformation visualizations
- Exported VTK files for further analysis

---

## Interpretation
Positive and negative LOS displacement values represent ground motion toward or away from the satellite.
In the Tibet earthquake case study, deformation patterns indicate tectonic surface displacement
associated with seismic activity.

---

## Applications
This workflow can be applied to:
- Earthquake deformation monitoring
- Volcanic inflation/deflation studies
- Geothermal reservoir deformation analysis
- Educational demonstrations of InSAR processing

---

## Limitations
- Atmospheric effects are not explicitly corrected
- Only a single interferometric pair is analyzed
- Deformation is measured in LOS direction only

---

## Author
**M. Ilham Azhar**  
Geophysical Engineering – Sumatra Institute of Technology (ITERA)

---

## Disclaimer
This project is intended for educational and research purposes.
Results should not be used for operational hazard assessment without further validation.
