<p align="center">
    <a href="______________">
    </a>
</p>


[En Français](#Filtre des données SWOT - Tutoriel)  
[In English](#SWOT Data Filter - Tutorial)    

# Filtre des données SWOT - Tutoriel

## Contexte

La mission SWOT (en anglais seulement)(pour Surface Water and Ocean Topography) fournit des données d'une grande précision sur l'une de nos ressources communes les plus précieuses : l'eau.
La mission SWOT de la NASA et du Centre national d'études spatiales est réalisée en collaboration avec l'Agence spatiale canadienne (ASC) et de l'Agence spatiale du Royaume-Uni. Elle permet de sonder 90 % des eaux de surface de la Terre, d'observer les menus détails de la surface des océans et de déterminer la mesure dans laquelle lacs, rivières, fleuves, réservoirs et océans changent avec le temps.
Le but de ce tutoriel est de fournir un script python qui permet de rendre les données de la mission SWOT plus accessibles.  Ce projet permet de filtrer et convertir les données brutes de la NASA de format netCDF vers des fichiers TIFF, lesquels sont plus légers et conviviaux.  Le filtrage des données permet de conserver uniquement les données de bonne qualité pour les analyses.

## Avant de commencer :

Assurez-vous d'installer les bibliothèques nécessaires à faire fonctionner le tutoriel.

```
!pip install xarray
!pip install rioxarray
!apt install gdal-bin
```

## Démarrage rapide : 

Si vous souhaitez interagir directement avec le notebook:

1. Télécharger le fichier du tutoriel [SWOT_filtre.ipynb].
2. Vous pouvez utiliser ce script dans Google Colab (à partir de votre compte gmail).

Données : 

Les données de la mission SWOT nécessaires pour ce tutoriel sont disponibles sur le site Earth Data de la NASA (https://search.earthdata.nasa.gov/search?q=SWOT_). Nous avons utilisé le produit suivant de la mission SWOT pour ce tutoriel: 'SWOT Level 2 Water Mask Raster Image Data Product, Version C'. Il est à noter qu'il nécessaire de se créer un compte Earth Data afin de pouvoir télécharger les images.



# SWOT Data Filter - Tutorial

## About
The SWOT mission is providing us with new and detailed information on one of the most important resources we share – water.

Led by NASA and France's space agency (CNES), SWOT surveys 90% of Earth's surface water; observes the fine details of the ocean's surface topography; and measures how lakes, rivers, reservoirs and oceans are changing over time.

The purpose of this tutorial is to provide a python script that helps make the SWOT mission data more accessible.  This project allows you to filter and convert raw NASA data in netCDF format to TIFF files, which are lighter and more user-friendly. Data filtering ensures that only good quality data is retained for analysis.
 

## Before starting

Make sure to install the requirements for the tutorial.

```
!pip install xarray
!pip install rioxarray
!apt install gdal-bin
```

## Quick start

If you wish to interact with the notebook directly:

1. Download the tutorial file [SWOT_filtre.ipynb].
2. You can use this script in Google Colab (using your Gmail account).

The SWOT mission data needed for this tutorial is available on NASA's Earth Data site (https://search.earthdata.nasa.gov/search?q=SWOT_). We used the following product from the SWOT mission for this tutorial: 'SWOT Level 2 Water Mask Raster Image Data Product, Version C'. Please note that you need to create an Earth Data account in order to download the images.
