<p align="center">
    <a href="https://www.asc-csa.gc.ca/eng/satellites/swot/">
        <img alt="Image du SWOT | Image of SWOT" src="https://www.asc-csa.gc.ca/images/satellites/swot/swot-v2-ban.jpg" height="300">
    </a>
    <br> Crédit d'image | Image credit: <a href="https://www.asc-csa.gc.ca/eng/satellites/swot/">ASC/CSA</a>
</p>

<p align="center">
    <a href="#stars">
        <img alt="Étoiles sur GitHub | GitHub Repo stars" src="https://img.shields.io/github/stars/asc-csa/SWOT-post-processing-tutorial">
    </a>
    <a href="#watchers">
        <img alt="Spectateurs sur Github | GitHub watchers" src="https://img.shields.io/github/watchers/asc-csa/SWOT-post-processing-tutorial">
    </a>
    <a href="https://github.com/asc-csa/SWOT-Data-Filter/commits/main">
        <img alt="Dernier commit sur GitHub | GitHub last commit" src="https://img.shields.io/github/last-commit/asc-csa/SWOT-post-processing-tutorial">
    </a>
    <a href="https://github.com/asc-csa/SWOT-Data-Filter/graphs/contributors">
        <img alt="Contributeurs sur GitHub | GitHub contributors" src="https://img.shields.io/github/contributors/asc-csa/SWOT-post-processing-tutorial">
    </a>
    <a href="https://twitter.com/intent/follow?screen_name=csa_asc">
        <img alt="Suivre sur Twitter | Twitter Follow" src="https://img.shields.io/twitter/follow/csa_asc?style=social">
    </a>
</p>

---

<h3 align="center">
  <a href="#titre-du-projet">Français</a> |
  <a href="#project-title">English (follows)</a>
</h3>

---

<a id="titre-du-projet"></a>
# Filtre des données SWOT - Tutoriel

> **Description brève :**  
> La mission SWOT (Surface Water and Ocean Topography) fournit des données d'une grande précision sur l'une de nos ressources communes les plus précieuses : l'eau.

## À propos

**Filtre des données SWOT - Tutoriel** est un tutoriel qui fournit un script Python pour rendre les données de la mission SWOT plus accessibles. Il couvre :

- Filtrage et conversion des données netCDF vers des fichiers TIFF
- Traitement des données brutes NASA pour améliorer l'accessibilité
- Conservation des données de bonne qualité pour les analyses
- Optimisation des fichiers pour un usage plus convivial

La mission SWOT de la NASA et du Centre national d'études spatiales est réalisée en collaboration avec l'Agence spatiale canadienne (ASC) et l'Agence spatiale du Royaume-Uni. Elle permet de sonder 90 % des eaux de surface de la Terre, d'observer les menus détails de la surface des océans et de déterminer comment lacs, rivières, fleuves, réservoirs et océans changent avec le temps.  

*Ce tutoriel est fourni à des fins pédagogiques et expérimentales.*

## Prérequis

- Python 3.8 ou plus récent
- Jupyter Notebook ou Jupyter Lab (pour Google Colab)
- Bibliothèques Python : xarray, rioxarray
- GDAL (gdal-bin)
- Compte Earth Data NASA (pour télécharger les données SWOT)
- Google Colab ou environnement Python local

## Démarrage rapide

1. 📦 **Cloner le dépôt**
   ```bash
   git clone https://github.com/asc-csa/SWOT-Data-Filter.git
   cd SWOT-Data-Filter
   ```
2. 🐍 **Créer un environnement**
   ```bash
   # Avec virtualenv
   python -m venv env
   source env/bin/activate

   # Ou avec conda
   conda create -n swot_env python=3.8
   conda activate swot_env
   ```
3. 📥 **Installer les dépendances**
   ```bash
   pip install xarray rioxarray
   apt install gdal-bin  # Sur Linux/Ubuntu
   ```
4. 🚀 **Lancer le tutoriel**
   ```bash
   # Option 1: Google Colab (recommandé)
   # Télécharger SWOT_filtre.ipynb et l'ouvrir dans Colab

   # Option 2: Local
   jupyter notebook SWOT_filtre.ipynb
   ```

> **Remarque :** Google Colab est recommandé car GDAL y est pré-installé. Vous aurez besoin d'un compte Earth Data NASA pour télécharger les données SWOT.

Les données de la mission SWOT nécessaires pour ce tutoriel sont disponibles sur le site Earth Data de la NASA (https://search.earthdata.nasa.gov/search?q=SWOT_). Il est nécessaire de se créer un compte Earth Data afin de pouvoir télécharger les images.  
Nous avons utilisé les produits « SWOT Level 2 Water Mask Raster Image Data Product, Version C » de la mission SWOT pour ce tutoriel :

- SWOT_L2_HR_Raster_100m_UTM22J_N_x_x_x_013_533_051F_20240415T150120_20240415T150141_PIC0_01
- SWOT_L2_HR_Raster_100m_UTM22J_N_x_x_x_014_533_051F_20240506T114623_20240506T114644_PIC0_01

## Astuces & Conseils

- **Google Colab :** Recommandé car GDAL est pré-installé et évite les problèmes de configuration
- **Compte Earth Data :** Nécessaire pour télécharger les données SWOT depuis NASA
- **Format TIFF :** Plus léger et compatible avec de nombreux logiciels SIG
- **Qualité des données :** Le filtrage ne conserve que les pixels de bonne qualité pour des analyses fiables

## Licence

Ce projet est sous une licence MIT modifiée – voir le fichier [LICENSE](https://github.com/asc-csa/SWOT-Data-Filter/blob/main/LICENSE.txt) pour plus de détails.

---

<h3 align="center">
  <a href="#project-title">English </a> |
  <a href="#titre-du-projet">Français (précède)</a>
</h3>

---

<a id="project-title"></a>
# SWOT Data Filter - Tutorial

> **Brief description:**  
> The SWOT mission is providing us with new and detailed information on one of the most important resources we share – water.

## About

**SWOT Data Filter - Tutorial** is a tutorial that provides a Python script to help make the SWOT mission data more accessible. It covers:

- Filtering and converting netCDF data to TIFF files
- Processing raw NASA data to improve accessibility
- Retaining only good quality data for analysis
- Optimizing files for more user-friendly usage

Led by NASA and France's space agency (CNES), SWOT surveys 90% of Earth's surface water; observes the fine details of the ocean's surface topography; and measures how lakes, rivers, reservoirs and oceans are changing over time.

*This tutorial is provided for educational and experimental purposes.*

## Prerequisites

- Python 3.8 or newer
- Jupyter Notebook or Jupyter Lab (for Google Colab)
- Python libraries: xarray, rioxarray
- GDAL (gdal-bin)
- NASA Earth Data account (to download SWOT data)
- Google Colab or local Python environment

## Quick Start

1. 📦 **Clone the repo**
   ```bash
   git clone https://github.com/asc-csa/SWOT-Data-Filter.git
   cd SWOT-Data-Filter
   ```
2. 🐍 **Create environment**
   ```bash
   # Using virtualenv
   python -m venv env
   source env/bin/activate

   # Or using conda
   conda create -n swot_env python=3.8
   conda activate swot_env
   ```
3. 📥 **Install dependencies**
   ```bash
   pip install xarray rioxarray
   apt install gdal-bin  # On Linux/Ubuntu
   ```
4. 🚀 **Run the tutorial**
   ```bash
   # Option 1: Google Colab (recommended)
   # Download SWOT_filtre.ipynb and open in Colab

   # Option 2: Local
   jupyter notebook SWOT_filtre.ipynb
   ```

> **Note:** Google Colab is recommended as GDAL is pre-installed. You will need a NASA Earth Data account to download SWOT data.

The SWOT mission data needed for this tutorial is available on NASA's Earth Data site (https://search.earthdata.nasa.gov/search?q=SWOT_). Please note that you need to create an Earth Data account in order to download the images.  
We used the « SWOT Level 2 Water Mask Raster Image Data Product, Version C » from the SWOT mission for this tutorial:

- SWOT_L2_HR_Raster_100m_UTM22J_N_x_x_x_013_533_051F_20240415T150120_20240415T150141_PIC0_01
- SWOT_L2_HR_Raster_100m_UTM22J_N_x_x_x_014_533_051F_20240506T114623_20240506T114644_PIC0_01

## Tips & Tricks

- **Google Colab:** Recommended as GDAL is pre-installed and avoids configuration issues
- **Earth Data Account:** Required to download SWOT data from NASA
- **TIFF Format:** Lighter and compatible with many GIS software packages
- **Data Quality:** Filtering retains only good quality pixels for reliable analysis

## License

This project is licensed under a modified MIT license - see the [LICENSE](https://github.com/asc-csa/SWOT-Data-Filter/blob/main/LICENSE.txt) file for details.
