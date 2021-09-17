# [3D Wetlands App](https://lizcanosandoval.users.earthengine.app/view/hr-land-cover-gulf-of-mexico)

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fluislizcano%2F3D-wetlands-app&count_bg=%2379C83D&title_bg=%23555555&icon=github.svg&icon_color=%23E7E7E7&title=Visits&edge_flat=false)](https://github.com/luislizcano/3D-wetlands-app)
[![GPL license](https://img.shields.io/badge/License-GPL-blue.svg)](http://perso.crans.org/besson/LICENSE.html)
[![GEE](https://img.shields.io/badge/GEE%20App%20-3D--Wetlands-orange)](https://lizcanosandoval.users.earthengine.app/view/hr-land-cover-gulf-of-mexico)
[![DOI](https://zenodo.org/badge/362521290.svg)](https://zenodo.org/badge/latestdoi/362521290)


<p>Google Earth Engine (GEE) Application to visualize and compare land cover changes and Digital Elevation Models (DEM) over the wetland areas of the Northern Gulf of Mexico and Florida at very high-resolutions.</p>

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/gee-app.JPG" width="800">

## Contents:
#### [1. Introduction](#introduction)
#### [2. Features](#features)
#### [3. Demo](#demo)
#### [4. FAQ](#faq)
#### [5. Disclaimer](#disclaimer)
#### [6. Credits](#credits)


## <span id="introduction">1. Introduction</span>
The 3D Wetlands App provide access to two large collections, (1) Landcover and (2) DEM, ingested to Earth Engine. The landcover product offer access to 12,929 processed and classified imagery at 2 m per pixel from WorldView-2 and WorldView-3 satellites, with temporal coverage from 2009 to 2018 (this is not consistent over time).

Satellite imagery coverage:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/wv-coverage.JPG" width="800">

The landcover analysis includes the following classes:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/classes.JPG" width="300">

The DEM product was built with 178 airborne topographic Lidar surveys (bare-earth) over the wetland and coastal areas of the Northern Gulf of Mexico and Florida. This product has horizontal resolution of 2-m per pixel and vertical accuracy of 0.2 m. 

DEM Coverage:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/dem.png" width="800">

The 3D Wetlands App is open access through GEE. The users do not require a GEE account to use all the features available in the [app interface](https://lizcanosandoval.users.earthengine.app/view/hr-land-cover-gulf-of-mexico). If the user has a GEE account can have access to an [advanced version](https://code.earthengine.google.com/47c4f5bbc0182929f4273c24dd2315b6) which will allow to export data to the respective Google Drive account by clicking a button. To this point previous experience with GEE is **not required**. However, the access of the landcover and DEM collections for other specific uses through the code editor previous knowledge with GEE is required (See the [GEE Documentation](https://developers.google.com/earth-engine)).

## <span id="features">2. Features</span>
* Create, visualize and compare land cover mosaics of two user-defined periods in one or more selected Counties:
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/01.gif" width="300">

* Visualize the DEM associated to the selected Counties:
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/02.gif" width="700">

* See the number of images (land cover) available in selected Counties and number of images used to create a mosaic:
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/03.gif" width="300">

* Create mosaics including all or single landcover classes:
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/04.gif" width="700">

* Draw transects on the map and explore elevation and land cover profiles:
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/05.gif" width="700">

* Download the generated mosaics and DEM as .png, max resolution 1000x1000px (Basic Interface):
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/06.png" width="500">

* Export the generated mosaics and DEM as a GeoTiff image (Advanced Interface):
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/07.gif" width="800">

* Calculate the area (km2) of each class in the mosaic for the whole region or at elevation ranges and export as a .csv file (Advanced Interface):
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/08.gif" width="800">

* Access to the whole landcover and DEM collections through the code editor (Advanced Interface).
<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/09.JPG" width="600">

## <span id="demo">3. Demo</span>
### Basic Interface:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/wetlands-app-basic.gif" width="1000">

### Advanced Interface:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/demo/wetlands-app-advanced.gif" width="1000">

## <span id="faq">4. FAQ</span>
* **How are the landcover mosaics generated?**

The landcover mosaics are generated by calculating the maximum value of each pixel across the stack of all available images in the selected Counties. This prioritazes classes with higher pixel values such as Developed (pixel value 11) and minimize the presence of clouds (pixel value 1). If a single class is selected, then the final mosaic is just a stack of the respective pixel values.

* **Do I need a Google Earth Engine account to use the app?**

No, everyone can use the 3D Wetlands app through the GEE App platform. But, a GEE account is required for exporting data and other advanced features.

* **Can I have access to the landcover and DEM collections?**

Yes, full access to the collections is possible trough the GEE code editor (Advanced Interface).

* **Can I download the generated mosaics and DEM trough the app?**

Yes, the mosaics can be downloaded as .png (Basic Interface) or .tiff (Advanced Interface).

* **I don't see any map after pressing the "Generate" button**

1. Make sure you have selected at least one County.
2. Make sure you have selected a valid period for both left and right maps.
3. Check the number available images for the selected County and Tile Coverage Layer.

* **I don't see any map or area estimations to be downloaded**

1. Make sure you have pressed 'Run' in the Tasks tab.
2. Check if the process is still running on server.
3. Search for any new file in your Google Drive.

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/tasks.JPG" width="400">

* **Why I see an error when trying to plot a elevation profile?**

The transect have to start from valid Land Cover and DEM values.

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/transect.png" width="900">

* **Can I change the color bar legend of the DEM layer?**

The color bar is generated automatically from percentile 1% to percentile 99%. The colors and raneg only can be edited by using the Layers button (right upper corner) eabled in the Advanced Interface. *To edit the DEM layer of the left side of the map you need to drag the splitter all the way to the right of the Layers button.*

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/dem-range.JPG" width="500">

## <span id="disclaimer">5. Disclaimer</span>
The 3D Wetlands App provide access to processed satellite imagery and DEM data as a tool for public and academic use. The raw satellite data is property of DigitalGlobe. The 3D Wetlands App is a product of the ongoing research project *Enhanced 3-D Mapping for Habitat, Biodiversity, and Flood Hazard Assessments of Coastal and Wetland Areas of the Southern US* granted by NSF to Frank Muller-Karger and Timothy Dixon at the University of South Florida, in collaboration with James Gibeaut at the Harte Research Institute, TAMU-CC.

## <span id="credits">6. Credits</span>
The WorldView imagery was processed at the Institute for Marine Remote Sensing (IMARS) at the College of Marine Science, University of South Florida and the DEM was acquired by the Harte Research Institute for Gulf of Mexico Studies at Texas A&M University - Corpus Christi. Google Earth Engine is the platform where the data is stored and distributed. Special thanks to Noel Gorelick who helped to ingest the image collections in GEE.

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/USF-Logo2.png" width="300"> <img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/TAMUCC_block.png" width="200"> <img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/nsf-logo.jpg" width="300"> <img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/gee-logo.png" width="300">
