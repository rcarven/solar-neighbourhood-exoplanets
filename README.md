# 🌌 Exoplanetary Architectures & ELT-PCS Visibility in the Solar Neighbourhood (d < 10 pc)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Planets](https://img.shields.io/badge/Planets-130-blueviolet)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

An interactive, multi-source data analysis project exploring exoplanets orbiting stars within 10 parsecs of the Sun. This repository contains the full pipeline, from data curation to interactive web visualization—built, developed during a research internship at the **Centro de Astrobiología (CAB, CSIC-INTA)** as an undergraduate student from **Universidad Complutense de Madrid (UCM)**.

🔗 **[Explore the Interactive Dashboard Here](https://rcarven.github.io/solar-neighbourhood-exoplanets/)**

## 📋 About the Project

This work goes beyond a simple database by providing a comprehensive analysis of planetary architectures and their future direct-imaging detectability. We structured the project around three main pillars:

1. **Master Catalogue:** We synchronized and cross-matched data from Exoplanet.eu, the NASA Exoplanet Archive, and the Cifuentes et al. 2025 (Cif25) stellar catalogue. We recomputed distances using Gaia DR3 parallaxes and applied rigorous manual corrections from the literature.
2. **System Architectures:** Visual mapping of planetary orbits against conservative and optimistic Habitable Zones (HZ).
3. **ELT-PCS Observability:** We developed an interactive simulation to evaluate the direct-imaging detectability of these nearby exoplanets using the upcoming Planetary Camera and Spectrograph (PCS) for the Extremely Large Telescope (ELT), building upon the visibility framework of Markus Kasper.

## 🗂️ Repository Structure

* `/data`: Contains the curated master catalogue (`Exoplanets_SolarNeighbourhood_Catalogue.csv`). 
* `/notebooks`: The Python data analysis pipelines used to process the data and generate the visualizations.
* `/docs`: HTML files deployed via GitHub Pages to host the interactive web dashboard.

## 🚀 How to Reproduce the Analysis

1. **Clone the repository**
```bash
git clone [https://github.com/rcarven/solar-neighbourhood-exoplanets.git](https://github.com/rcarven/solar-neighbourhood-exoplanets.git)
cd solar-neighbourhood-exoplanets
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the notebooks in order**
* `01_data_pipeline.ipynb` — Merges raw data and outputs the master CSV.
* `02_table_generator.ipynb` — Renders the interactive DataTables view.
* `03_systems_architecture.ipynb` — Generates the HZ architecture plots.
* `04_ELT_Visibility_SolarNeighbourhood.ipynb` — Computes max angular separation/contrast and generates the ELT-PCS interactive scatter plot.

> **⚠️ Note:** Raw input catalogues (e.g., *eu_actualizado_cif2025.csv*, *distancias_gaia.csv*) are excluded from this repository due to size and licensing constraints. The notebooks are configured to read from the provided processed master catalogue in the `/data` folder where applicable.

## 📊 Quick Statistics

| Parameter | Value |
| :--- | :--- |
| **Total planets** | 130 (Confirmed, Candidates, Discarded tracked) |
| **Max distance** | 10 pc |
| **Detection methods** | RV, Transit, Astrometry, TTV |
| **Primary Data Sources** | Cif25, Exoplanet.eu, NASA Exoplanet Archive, Gaia DR3 |

## 📚 References & Acknowledgements

*This research has made use of the NASA Exoplanet Archive, which is operated by the California Institute of Technology, under contract with the National Aeronautics and Space Administration under the Exoplanet Exploration Program.*

If you utilize this repository or its data pipelines, please consider citing the following original sources:

**Primary Data Sources & Frameworks:**
* **NASA Exoplanet Archive:** Christiansen, J. L. et al. (2025). *The NASA Exoplanet Archive and Exoplanet Follow-up Observing Program*. PSJ.
* **Exoplanet.eu:** Schneider, J. et al. (2011). *Defining and cataloging exoplanets: the exoplanet.eu database*. A&A.
* **Stellar Parameters:** Cifuentes, C. et al. (2025). *CARMENES input catalogue of M dwarfs: IX*. A&A.
* **Distances & Parallaxes:** Gaia Collaboration et al. (2016, 2023). *The Gaia mission* & *Gaia Data Release 3*. A&A.

**Models & Code Implementations:**
* **Habitable Zones:** Compute limits based on the conservative and optimistic definitions by Kopparapu, R. K. et al. (2013, 2014).
* **Mass-Radius Relations:** Theoretical radii and planet classifications are calculated via the piecewise empirical relations implemented in Jared Males' [mxlib framework](https://jaredmales.github.io/mxlib-doc/), derived from Rogers, L. A. (2015), Marcy, G. W. et al. (2014), and Fortney, J. J. et al. (2007, 2010).
* **ELT-PCS Observability Calculations:** Angular separations and reflected-light contrasts are simulated using the Python orbital solutions framework developed by Pearce, L. A., Males, J. R., & Limbach, M. A. (2025).
* **Instrument Specifications:** The detectability threshold and contrast curves for the ELT Planetary Camera and Spectrograph are adapted from the roadmap by Kasper, M. et al. (2021).

**Software & Tools:**
* **TOPCAT:** Taylor, M. B. (2005).
* Data analysis and interactive visualizations were developed using `pandas`, `numpy`, `plotly`, and `astropy` (Astropy Collaboration).

## 📄 License

This project is open-source and available under the MIT License. 
The data is derived from public catalogues. If you utilize this curated dataset or pipeline, please cite the original sources appropriately. Special thanks to Dr. J.A. Caballero for his guidance during this research.

## 👤 Author

**Rafael Carmona Vendoiro** — Physics Undergraduate, Universidad Complutense de Madrid  
📧 rcarmo02@ucm.es · [GitHub](https://github.com/rcarven)
