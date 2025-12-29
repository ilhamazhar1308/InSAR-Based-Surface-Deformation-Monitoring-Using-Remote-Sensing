📡 InSAR Surface Deformation Analysis Using Remote Sensing

This repository contains a simple yet practical InSAR (Interferometric Synthetic Aperture Radar) processing workflow for monitoring surface deformation using satellite remote sensing data.

The workflow is designed to be general-purpose and applicable to:

Earthquake-induced deformation

Volcanic deformation monitoring

Geothermal field deformation

Tectonic and land subsidence studies

📍 Case study applied in this notebook:
Tibet Plateau Earthquake, 2025

🧠 Overview

InSAR is a powerful geophysical remote sensing technique used to measure ground deformation with centimeter-to-millimeter accuracy.
This notebook demonstrates a basic processing chain, including:

Data preparation

Interferogram generation

Phase processing

Visualization of surface deformation

The workflow emphasizes clarity and reproducibility, making it suitable for:

Students

Early-stage research

Educational and demonstration purposes

🛠️ Tools & Libraries

PyGMTSAR – InSAR processing framework

NumPy, Pandas, Xarray – numerical & multidimensional data handling

Dask & Distributed – large dataset processing

GeoPandas – spatial data handling

Matplotlib & PyVista – 2D & 3D visualization

📂 Repository Structure
insar-surface-deformation-remote-sensing/
│
├── insar-surface-deformation-remote-sensing.ipynb
├── requirements.txt
└── README.md

⚙️ Installation
1️⃣ Clone Repository
git clone https://github.com/USERNAME/REPO_NAME.git
cd REPO_NAME

2️⃣ Install Python Dependencies

Make sure Python ≥ 3.9 is installed, then run:

pip install -r requirements.txt


⚠️ Note:
GMTSAR system dependencies are not included in requirements.txt because they require system-level installation.
When using Google Colab, PyGMTSAR handles this automatically.

3️⃣ Run the Notebook

Open the notebook using:

Jupyter Notebook

Jupyter Lab

Google Colab

📌 Case Study

Region: Tibet Plateau

Event: Earthquake, 2025

Method: InSAR-based surface deformation analysis

Although the example focuses on Tibet 2025, the workflow can be reused for other regions and geohazard applications.

🎯 Applications

Earthquake deformation mapping

Volcano inflation/deflation monitoring

Geothermal reservoir deformation

Tectonic studies

Land subsidence analysis

👤 Author

M. Ilham Azhar
Geophysical Engineering Student
Sumatra Institute of Technology (ITERA)


📄 License

This project is intended for educational and research purposes.

## Disclaimer
This project is intended for educational and research purposes.
Results should not be used for operational hazard assessment without further validation.
