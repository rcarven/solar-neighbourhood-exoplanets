# 🌌 Exoplanet Catalogue in the Solar Neighbourhood (d < 10 pc)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Planets](https://img.shields.io/badge/Planets-129-blueviolet)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

A curated, multi-source catalogue of **129 confirmed exoplanets** orbiting stars
within 10 parsecs of the Sun. Built as part of an undergraduate research project
at the Universidad Complutense de Madrid.

> 🔗 **[Explore the interactive table →](https://rcarven.github.io/solar-neighbourhood-exoplanets)**

---

## 📋 About the Catalogue

The catalogue integrates and cross-matches data from three primary sources:

| Source | Role |
|--------|------|
| [Exoplanet.eu](http://exoplanet.eu) | Base catalogue |
| [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/) | Additional planets & parameters |
| [Cifuentes et al. 2025 (Cif25)](https://ui.adsabs.harvard.edu/abs/2025A%26A...693A.228C/abstract) | Stellar parameters (Teff, mass, radius, SpType) |

Stellar distances were recomputed from Gaia DR3 / Hipparcos parallaxes via SIMBAD.
Manual corrections for 3 removed planets and 1,334 edited parameters were applied
from the literature.

**Key parameters** (126 columns per planet): orbital period, semi-major axis,
eccentricity, mass, radius, detection method, stellar properties, and full
reference traceability per parameter.

---

## 🗂️ Repository Structure
```
solar-neighbourhood-exoplanets/
├── data/
│   └── Exoplanets_SolarNeighbourhood_Catalogue.csv   # Master catalogue
├── notebooks/
│   ├── data_pipeline.ipynb      # Data pipeline (merging, corrections, export)
│   └── table_generator.ipynb   # Interactive HTML table generator
├── docs/
│   └── index.html                 # Interactive table (hosted via GitHub Pages)
└── requirements.txt
```

---

## 🚀 How to Use

**1. Clone the repository**
```bash
git clone https://github.com/rcarven/solar-neighbourhood-exoplanets.git
cd solar-neighbourhood-exoplanets
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the notebooks in order**
- `data_pipeline.ipynb` — requires the raw input files (see note below)
- `table_generator.ipynb` — reads the master CSV and outputs the HTML table

> ⚠️ **Note:** The raw input files (`eu_actualizado_cif2025.csv`, `eu_cif2025corr.fit`,
> `distancias_gaia.csv`, etc.) are not included in this repository due to their size
> and licensing. The processed master catalogue (`data/`) is provided directly.

---

## 📊 Catalogue Statistics

| Parameter | Value |
|-----------|-------|
| Total planets | 129 |
| Host stars | ~100 |
| Max distance | < 10 pc |
| Detection methods | RV, Transit, Transit+RV, Astrometry, TTV |
| Stellar data source | Cif25 (78 systems) + Exoplanet.eu |

---

## 📄 License & Citation

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.

The data itself is derived from public catalogues. If you use this catalogue in
your work, please also cite the original sources (Exoplanet.eu, NASA Exoplanet
Archive, Cifuentes et al. 2025).

---

## 👤 Author

**Rafael Carmona** — Physics student, Universidad Complutense de Madrid
📧 rcarmo02@ucm.es · [GitHub](https://github.com/rcarven)
