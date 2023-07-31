
# Communicating Flood Risk through Interactive Data Visualization

### MIT Summer Research Program Case Study with MIT's Urban Risk Lab
### By Carolina Pérez Méndez
### Supervised under Mayank Ojha and Miho Mazereeuw


# **Table of Contents**

1. [Abstract](#abstract)
2. [Introduction](#introduction)
   
   2.1 [Objectives](#objectivesofthestudy)<br>
   
   2.2 [Purpose](#Purpose)<br>
   
   2.3 [Hypothesis](#hypothesis)<br>
   
   2.4 [Scope](#scope)<br>
   
   2.5 [Prerequisites](#prerequisites)<br>
   
4. [Methodology](#methodology)
   3.1 [Strategizing and Literature Review](#strategizing-and-literature-review)
   3.2 [Starting with Mapbox Studio Style](#starting-with-mapbox-studio-style)
   3.3 [Setting up the code](#setting-up-the-code)
   3.4 [Uploading my own model into Mapbox](#uploading-my-own-model-into-mapbox)
   3.5 [Setting up the water layer](#setting-up-the-water-layer)
   3.6 [Attaching the Metadata to the glTF](#attaching-the-metadata-to-the-gltf)
   3.7 [Style, lights, and popups](#style-lights-and-popups)
5. [Results](#results)
6. [Discussion](#discussion)
7. [Conclusion](#conclusion)
   6.1 [Research Poster](#research-poster)
8. [Appendix](#appendix)


# **Abstract**

Effective flood risk communication is crucial for promoting resilience and informed decision-making in flood-prone areas. However, current flood maps and risk communication techniques have inherent limitations that hinder their effectiveness. This research addresses these gaps by developing interactive data visualization strategies to enhance flood risk communication. It aims to improve understanding, engagement, and proactive measures for mitigating flood risks. The focus is on the development of three-dimensional mapping techniques to depict flood hazards in a more realistic and immersive manner. The research leverages Mapbox GL JS, a JavaScript library for developing web maps and applications with Mapbox's advanced mapping technology, to create an interactive three-dimensional flood map of the MIT campus as a living laboratory. This map will enable the sharing of flood risk information with different departments, facilitating adaptation and mitigation projects. The main challenge lies in importing and transforming 2D data into three-dimensional GIS data and employing suitable visualization techniques. The results are expected to enhance the accuracy, visual representation, and accessibility of flood risk data, empowering stakeholders to better understand and respond to flood risks. This research holds significance for architectural data visualization strategies, advancing the field and benefiting the broader community involved in flood risk management.

# **Introduction**

With the rise of interactive data visualization and advancements in technology, vulnerable communities are more equipped with powerful tools to understand and mitigate the risks posed by floods. Flood mapping has emerged as one of the most effective strategies for communicating flood risks, enabling individuals and organizations to grasp the nature, magnitude, and likelihood of hazards in their area. However, current flood maps often fall short of accurately representing the true extent of flood risk due to limitations and sources of uncertainty in data gathering and analysis processes.

In this research report, we delve into the realm of interactive data visualization to enhance flood risk communication. We helped develop a strategy that facilitates understanding, engagement, and informed decision-making among diverse stakeholders, ultimately promoting proactive measures for mitigating flood risks. To achieve this, we focus on the technical aspects and challenges involved in creating an interactive three-dimensional (3D) flood map, specifically within the context of the Massachusetts Institute of Technology (MIT) campus.

In an era marked by increasing climate uncertainties and the growing need for effective flood risk communication, the development of interactive 3D flood maps has emerged as a promising solution. These maps provide stakeholders with a visually immersive and intuitive representation of flood hazards, enabling them to better understand, analyze, and respond to potential risks. By exploring the technical aspects of creating an interactive 3D flood map, we aim to contribute to the field of flood risk communication and promote resilience in the face of flood events.

The MIT campus serves as an ideal case study for this research, offering a diverse range of structures that can be depicted in a 3D environment. By mapping the flood hazards present on the campus, we can enhance flood risk communication and empower stakeholders with valuable information to make informed decisions. Through this research, we aim to uncover the technical considerations and challenges involved in developing an interactive 3D flood map of the MIT campus, paving the way for more effective flood risk communication strategies. By three-dimensionally mapping flood hazards on the campus, we can share vital information with different departments and encourage the implementation of adaptation and mitigation projects.

By addressing the limitations and sources of uncertainty in current flood mapping processes, we can bridge the gap between scientific data and meaningful understanding. Through interactive data visualization, we strive to empower individuals, communities, and decision-makers to proactively respond to flood risks and build a more resilient future. The findings and insights gained from this research have the potential to inform and improve flood risk communication strategies not only on the MIT campus but also in other vulnerable areas around the world. The knowledge gained from this process will extend beyond the campus, benefiting residential areas, commercial zones, and cities collaborating with communities on urban adaptation and mitigation initiatives.

This report will include a step-by-step guide to how this map came into existence. It will also include the specific technical challenges that we encountered in its development, such as importing 3D data into Mapbox, a mapping platform, and transforming typical 2D data into 3D GIS data. And it will demonstrate how to employ suitable visualization techniques in flood maps, and how we designed our intuitive interface. Our comprehensive documentation encourages other designers and architects to continue experimenting with interactive three-dimensional mapping through web development tools and it shall facilitate the process for first-time users. The results of this research, including this report and findings on how to create map, are meant to help grow and improve data representation into the comprehensive "MIT Climate Resilience" dashboard being developed by the Urban Risk Lab within the framework of their Climate Grand Challenge, entitled "Preparing for a New World of Weather and Climate Extremes", which is an initiative aimed to deliver "high-impact climate solutions" and researching "game-changing advances." By executing this, we can reach a wide range of users and ensure wider accessibility and dissemination of flood risk information. Our research seeks to enhance the accuracy, visual representation, and accessibility of flood risk data, enabling stakeholders to make informed decisions and take action to improve resilience.

The findings from this research have the potential to advance the field of architectural data visualization and inform future practices in flood risk management. By lowering the knowledge barriers and improving the quality of representation and analysis, we can contribute to a more informed and resilient community. Through this research, we are pushing the boundaries of effective flood risk communication by bridging the gap between scientific data and meaningful understanding. By employing innovative approaches and techniques in interactive data visualization, we are empowering individuals, communities, and decision-makers in their quest to build a safer and more resilient future.

In conclusion, this research report explores the technical aspects and challenges involved in creating an interactive 3D flood map, focusing on the specific case of the MIT campus. By leveraging interactive data visualization techniques, we aim to enhance flood risk communication, promote understanding and engagement among stakeholders, and ultimately contribute to the development of proactive measures for mitigating flood risks. With the ever-increasing climate uncertainties, the development of effective flood risk communication strategies is paramount for building resilient communities and safeguarding lives and assets.

**2.1 Objectives of the study**

![Shape3](RackMultipart20230731-1-ifxyyx_html_55d1d6d0da9e15f6.gif) ![Shape2](RackMultipart20230731-1-ifxyyx_html_55d1d6d0da9e15f6.gif) ![Shape1](RackMultipart20230731-1-ifxyyx_html_55d1d6d0da9e15f6.gif)

3

2

1

 ![Shape4](RackMultipart20230731-1-ifxyyx_html_6795c5966541bb29.gif)

**2.2 Purpose**

The research that will be conducted during the summer holds significant importance as it not only expands on architectural data visualization strategies for communicating flood risk but also contributes to advancing the field. It can enhance both the quality of representation and analysis and lower the knowledge barriers that impede non-expert audiences' understanding of flood hazards in risk communication. ("3D Geovisualization Interfaces as Flood Risk Management Platforms: Capability, Potential, and Implications for Practice," 2020) The findings and insights gained from this research can potentially inform future practices in architectural data visualization, benefiting both the field itself and the broader community involved in flood risk management and decision-making.

**2.3 Hypothesis**

The hypothesis of this research is that creating interactive data visualizations tailored to the needs of various stakeholders will facilitate their active involvement in the decision-making process regarding flood risk mitigation. By providing user-friendly interfaces, intuitive controls, and customizable features, these interactive visualizations will enhance understanding, engagement, and informed decision-making among diverse audiences. The hypothesis suggests that such interactive data visualizations can effectively communicate complex flood risk information, foster stakeholder engagement, and ultimately promote proactive measures for mitigating flood risks at the community and individual levels.

**2.4 Scope**

This research is part of the MIT Summer Research Program, an immersive 9-week program for international and national students with an interest in executing cutting-edge research with renowned professors at one of the best institutions in the world. This summer I worked with the Urban Risk Lab during the duration of this program.

**2.5 Prerequisites**

In this section, we will identify and define all programs, platforms, websites, and tools used to develop the map.

**A. For Mapping**

A.1 Mapbox: is a platform focused on location data, catering to the need for personalized online maps on websites and applications. It presents a wide array of map styles, data sources, and developer tools, empowering designers and developers to craft engaging and ever-changing maps.

A.1.1 Studio: is a web-based design tool offered by Mapbox that allows users to create, customize, and design their own maps. It is a powerful map design studio that enables developers and designers to control every aspect of their maps, from choosing the color schemes and typography to defining the layout and interaction behaviors.

A.1.2 Style: refers to a JSON-based specification used to define the visual appearance and behavior of maps created with Mapbox. Its main components are Layers, Sources, Symbology, and Interactivity.

A.1.3 Examples: these are a set of maps or other details created by users using the platform. Mapbox provides them as a tool to help guide new users.

A.2 Qgis: It is a powerful platform that provides extensive functionalities for spatial data analysis, mapping, and visualization while emphasizing its commitment to openness and accessibility to all users without any licensing fees.

**B. For Coding**

B.1 Visual Studio Code (VS code): Visual Studio Code is a revolutionary code editor that has been redesigned and fine-tuned to cater specifically to the needs of developers working on contemporary web and cloud applications. This cutting-edge editor offers a seamless and efficient environment for writing, editing, and debugging code, empowering developers to tackle the complexities of modern software development with ease.

B.2 Mapbox GL JS: is a JavaScript library that allows you to create interactive and configurable vector maps on the Web. It renders map data from Mapbox Vector Tiles, using the Mapbox Style specification and hardware-accelerated graphics (WebGL).

B.2.1 Access token: is a unique identifier that grants access to Mapbox services and APIs. It acts as a security key, allowing developers to authenticate their requests and use Mapbox's location data platform in their applications. When you sign up for a Mapbox account, you can obtain an Access Token from the Mapbox website or dashboard. This Access Token must be included in the requests you make to Mapbox

B.3 Node Package Manager (npm): is the package manager for [Node.js](http://nodejs.org/). Designed to help JavaScript developers easily share packaged modules of code.

B.4 Github: is a cloud-based platform designed for software development and version control using Git. It offers developers a centralized space to store and efficiently manage their code.

B.3.1 Repository: is a central location where developers can store, manage, and collaborate on code and project files using Git. It generally contains all project files and it's revision history.

B.5 Threejs: is a JavaScript 3D Library that provides a set of tools and functionalities that make it easier for developers to work with WebGL, a low-level web-based graphics API, which allows for hardware-accelerated 3D rendering within modern browsers.

B.6 Live Server Plugin: is a VS code extension that allows us to start a development local server with live reload feature, catering to both static and dynamic pages.

B.7 Qgis2threejs Plugin: is a Qgis plugin that helps visualize vector data in 3d on a web view. It reads 3d shapefiles and allows the extrusion of 2d shapefiles. By leveraging this tool, we can export glTF objects and an HTML file of the map.

**C. Websites for acquiring resources:**

C.1 Bboxfinder: is a C# library typically used in mapping applications. Helps find max web mercator bbox for all coordinate systems supported by proj4.

C.2 Chatgpt: a language model supported by AI to generate responses to questions. It is a useful tool to learn tips and tricks for programming for first-time users.

C.3 Youtube: a popular video-sharing website useful for searching tutorials.

C.4 glTF editor: is an online editor that allows us to edit, visualize, scale, and save glTF files. Most importantly it allows us to control individually each node of the model. In addition to this it allows us to save a glTF file in other formats, for example STL.

C.5 Threejs editor: is a web-based visual editor designed to work with the Three.js library.

C.6 City of Cambridge GIS portal: a portal developed by the City of Cambridge that provides interactive mapping applications, static maps, and most importantly GIS data download.

**D. Three-dimensional software**

D.1 Blender: is a powerful and open-source 3D computer graphics software used for creating animated films, visual effects, art, 3D models, and interactive 3D applications.

D.2 Rhino (optional): a software program used for drafting and 3d modeling. It is mostly used because of its effective interface allowing users to draw from different views at once. It is mainly used for creating organic and complex shapes.

D.3 Sketchup (optional): a "3d modeling Computer-Aided Design (CAD) program" used for design applications.

**E. Layer file formats**

E.1 glTF: is a freely available standard used for transmitting and loading 3D scenes and models in applications. It aims to optimize the efficiency of transmitting 3D assets by reducing their size and minimizing the processing required to unpack and utilize them.

![](RackMultipart20230731-1-ifxyyx_html_b10d14f37ba7d8e.png)

Figure 1: Overview of glTF by Khronos

E.2 GeoJson: is a geospatial data interchange format that showcases geographic features and their attributes.

E.3 Shapefiles: is a digital vector data file format used for geographic information system software.

E.4 OBJ: is a 3d standard format. It has the ability to recognixe 3d objects' surface properties, including texture mapping and shading, making it efficient for developing realistic render of a model.

**IV. Methodology**

  1. Strategizing and Researching Past Projects

Getting started by identifying creative innovative ways to communicate flood risk. By brainstorming an effective way to carry this mission out, we agreed that the best experimental approach for this summer's case study was developing a three-dimensional map of the MIT campus, which allows us to study flood problems in depth. It allows for the experimentation of Mapbox mapping capabilities, the cloud mapping platform used to employ the task.

At the beginning, a project done by Smart City Cologne was used as an example for understanding risk assessment through 3d mapping.

Article: Planning the City of Tomorrow in 3D, written by Jim Baumann

[https://www.esri.com/about/newsroom/arcuser/planning-the-city-of-tomorrow-in-3d/](https://www.esri.com/about/newsroom/arcuser/planning-the-city-of-tomorrow-in-3d/)

![](RackMultipart20230731-1-ifxyyx_html_bdf7f181559f027c.jpg)

FALTA

  1. Starting with Mapbox Studio and Style

Choosing Mapbox as our main platform allows the map to be published and shared in the Urban Risk Lab's dashboard. But most importantly it gives us the flexibility and versatility to edit the map directly in Mapbox Studio by importing, filtering, and styling layers from shapefiles and geojson. Simultaneously, it allows us to use Mapbox GL js to edit the map and add additional data to the map through code.

First we start by opening Mapbox, creating an account with MIT institutional email and an access token, which Mapbox uses to associate your account with your requests to Mapbox API resources. Then we start by opening and editing a style in Mapbox Studio. For this particular map, I chose "Mapbox Light."

Style URL: mapbox://styles/mapbox/light-v11

This style is useful for highlighting colored-data layers. Once the style has uploaded, one has editing capabilities to edit the style as one desires. Most importantly, we can start by importing layers.

As provided by the Urban Risk Lab, the first two layers to be added were: "MIT Building.geojson", which demonstrates the silhouette of all MIT buildings on campus, and "2070\_100y\_Storm\_24h.geojson", which contains the flood hazard layer.

The next constitutes following this tutorial:

[https://docs.mapbox.com/help/tutorials/add-3d-buildings-studio/#option-2-style-an-individual-layer](https://docs.mapbox.com/help/tutorials/add-3d-buildings-studio/#option-2-style-an-individual-layer)

It gives direct instruction on how to create a 3d map and add 3d buildings in Mapbox Studio. In the Mapbox Studio style editor, turn on 3d buildings by clicking on the buildings component to open the component properties panel and click the 3d building toggle to "on". The file below gives instructions if your style does not contain a building layer.

After this, we can adjust the properties of our imported data by selecting the layer, choosing "select data" and changing the layer "type" into "fill extrusion". This will automatically create an extruded layer corresponding to the original layer data. After, we must style it accordingly by setting the height property, the base height property, and changing the color. We can style across data range but styling with a function is ideal.

The "2070\_100y\_Storm\_24h.geojson" was extruded and styled by setting "fill height extrusion" to "depth2d\*.3048". This "\*.3048" is a necessary conversion for changing from feet to meters, which is the unit Mapbox uses. The base height was set to "grounddepth2d\*.3048". The layer was color-coded based on Maximum Depth with shades of blue indicating crucial areas.

On the other side, ""MIT Building.geojson" was used as reference for placing the 3d buildings model. In order to highlight the buildings presented in this layer, the mapbox's building layer was turned off.

After editing, it is crucial to publish the style to preserve changes in future steps.

  1. Setting up the Code

For this step we first start by downloading Visual Studio Code, " a code editor redefined and optimized for building and debugging modern web and cloud applications". Start by creating a file and opening it in vs code. Create a basic "index.html".

Go back to Mapbox in the browser and install Mapbox GL JS to create a web map with Mapbox GL JS. There are two methods for installing it by using the Mapbox CDN or a module bundler, as recommended by Mapbox the node package manage (npm). After installing the npm package, include the GL JS CSS file by pasting this on the \<HEAD\>of the html file created previously.

\<link href='https://api.mapbox.com/mapbox-gl-js/v2.8.1/mapbox-gl.css' rel='stylesheet' /\>

And, by adding the map to your site by pasting this under \<BODY\> :

var mapboxgl = require('mapbox-gl/dist/mapbox-gl.js');

mapboxgl.accessToken = 'YOUR\_MAPBOX\_ACCESS\_TOKEN';

var map = new mapboxgl.Map({

container: 'YOUR\_CONTAINER\_ELEMENT\_ID',

style: 'mapbox://styles/mapbox/streets-v11'

});

Or add the Map class:

mapboxgl.accessToken = '\<your access token here\>';

const map = new mapboxgl.Map({

container: 'map', // container ID

style: 'mapbox://styles/mapbox/streets-v12', // style URL

center: [-74.5, 40], // starting position [lng, lat]

zoom: 9 // starting zoom

});

Now, we are set to use Mapbox GL JS by accessing it through VS Code.

First, we can start by inserting our Mapbox individual user access token to track our progress. Then, we can start setting a map style and an initial view. For changing the style, we can use the style URL from our published Mapbox style and copy-paste it after "style:" between the apostrophes. By downloading a VS code plugin called "Live Server", we can use it to open a window to view the index.html. Right-click and click on "Open with Live server" a window shall appear with the Mapbox style. Every time a change is made in Mapbox Studio style, it shall be published in order to view the updated version of the style in the HTML file. To set an initial view, we can use "bboxfinder" to find the latitude and longitude of a specific location and replace it where it says "center "on the map class code.

The next step is loading a basic web map using a Mapbox example. And luckily, there is a code already written for adding 3d models into Mapbox using Three.js, a popular JavaScript library used for creating and rendering 3D graphics in web browsers. It provides a simple and efficient way to work with WebGL, a web standard for rendering 3D graphics on the GPU (Graphics Processing Unit). Three.js abstracts the complexities of WebGL, making it easier to build and display 3D content on the web.

This URL provides more information of the documentation of the plugin: [Three.js – JavaScript 3D Library (threejs.org)](https://threejs.org/)

This URL provides the code and an introduction to [Add a 3D model | Mapbox GL JS | Mapbox](https://docs.mapbox.com/mapbox-gl-js/example/add-3d-model/)

And this is the code provided to import a Satellite as GLTF file in a Mapbox Style:

\<!DOCTYPE html\>

\<html\>

\<head\>

\<meta charset="utf-8"\>

\<title\>Add a 3D model\</title\>

\<meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no"\>

\<link href="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.css" rel="stylesheet"\>

\<script src="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.js"\>\</script\>

\<style\>

body { margin: 0; padding: 0; }

#map { position: absolute; top: 0; bottom: 0; width: 100%; }

\</style\>

\</head\>

\<body\>

\<script src="https://unpkg.com/three@0.126.0/build/three.min.js"\>\</script\>

\<script src="https://unpkg.com/three@0.126.0/examples/js/loaders/GLTFLoader.js"\>\</script\>

\<div id="map"\>\</div\>

\<script\>

mapboxgl.accessToken = 'pk.eyJ1IjoiY3BlcmV6bSIsImEiOiJjbGlsejM5ZWcwZ2t0M3NtcGJicWw0NmxwIn0.mh73FxbqH2Zl-5fRbuZB\_w';

const map = new mapboxgl.Map({

container: 'map',

// Choose from Mapbox's core styles, or make your own style with Mapbox Studio

style: 'mapbox://styles/mapbox/light-v11',

zoom: 18,

center: [148.9819, -35.3981],

pitch: 60,

antialias: true // create the gl context with MSAA antialiasing, so custom layers are antialiased

});

// parameters to ensure the model is georeferenced correctly on the map

const modelOrigin = [148.9819, -35.39847];

const modelAltitude = 0;

const modelRotate = [Math.PI / 2, 0, 0];

const modelAsMercatorCoordinate = mapboxgl.MercatorCoordinate.fromLngLat(

modelOrigin,

modelAltitude

);

// transformation parameters to position, rotate and scale the 3D model onto the map

const modelTransform = {

translateX: modelAsMercatorCoordinate.x,

translateY: modelAsMercatorCoordinate.y,

translateZ: modelAsMercatorCoordinate.z,

rotateX: modelRotate[0],

rotateY: modelRotate[1],

rotateZ: modelRotate[2],

/\* Since the 3D model is in real world meters, a scale transform needs to be

\* applied since the CustomLayerInterface expects units in MercatorCoordinates.

\*/

scale: modelAsMercatorCoordinate.meterInMercatorCoordinateUnits()

};

const THREE = window.THREE;

// configuration of the custom layer for a 3D model per the CustomLayerInterface

const customLayer = {

id: '3d-model',

type: 'custom',

renderingMode: '3d',

onAdd: function (map, gl) {

this.camera = new THREE.Camera();

this.scene = new THREE.Scene();

// create two three.js lights to illuminate the model

const directionalLight = new THREE.DirectionalLight(0xffffff);

directionalLight.position.set(0, -70, 100).normalize();

this.scene.add(directionalLight);

const directionalLight2 = new THREE.DirectionalLight(0xffffff);

directionalLight2.position.set(0, 70, 100).normalize();

this.scene.add(directionalLight2);

// use the three.js GLTF loader to add the 3D model to the three.js scene

const loader = new THREE.GLTFLoader();

loader.load(

'https://docs.mapbox.com/mapbox-gl-js/assets/34M\_17/34M\_17.gltf',

(gltf) =\> {

this.scene.add(gltf.scene);

}

);

this.map = map;

// use the Mapbox GL JS map canvas for three.js

this.renderer = new THREE.WebGLRenderer({

canvas: map.getCanvas(),

context: gl,

antialias: true

});

this.renderer.autoClear = false;

},

render: function (gl, matrix) {

const rotationX = new THREE.Matrix4().makeRotationAxis(

new THREE.Vector3(1, 0, 0),

modelTransform.rotateX

);

const rotationY = new THREE.Matrix4().makeRotationAxis(

new THREE.Vector3(0, 1, 0),

modelTransform.rotateY

);

const rotationZ = new THREE.Matrix4().makeRotationAxis(

new THREE.Vector3(0, 0, 1),

modelTransform.rotateZ

);

const m = new THREE.Matrix4().fromArray(matrix);

const l = new THREE.Matrix4()

.makeTranslation(

modelTransform.translateX,

modelTransform.translateY,

modelTransform.translateZ

)

.scale(

new THREE.Vector3(

modelTransform.scale,

-modelTransform.scale,

modelTransform.scale

)

)

.multiply(rotationX)

.multiply(rotationY)

.multiply(rotationZ);

this.camera.projectionMatrix = m.multiply(l);

this.renderer.resetState();

this.renderer.render(this.scene, this.camera);

this.map.triggerRepaint();

}

};

map.on('style.load', () =\> {

map.addLayer(customLayer, 'waterway-label');

});

\</script\>

\</body\>

\</html\>

Once it is saved in the index.html file of VS code it is visible when the live server is open. After going live, you will notice that it is wrongfully placed in another part of the world. You can use "bboxfinder once again to place the satellite accordingly, by changing the latitude and longitude in "const modelorigin: ()" under the "Parameters to ensure the model is georeferenced correctly on the map".

  1. Uploading my own model into Mapbox

We now know it is possible to load a 3d object into Mapbox. The challenge now is figuring out how to import one of our own models into Mapbox.

Starting by visiting the City Cambridge GIS portal and downloading their new, sophisticated 3d GIS Data. In which they have 3d buildings of Cambridge in different formats including: Skechup, ESRI Shapefile, STL, OBJ, and GLTF.

We saw before, on the code that our satellite model was a GLTF uploaded through a GLTF loader from Three,js.

A GLTF (GL Transmission Format) is an open standard file format designed for efficient transmission and loading of 3D scenes and models. It is specifically optimized for use in real-time graphics, such as web and mobile applications, virtual reality (VR), and augmented reality (AR) experiences.GLTF is developed by the Khronos Group, an industry consortium that focuses on the creation of open standards for graphics and media. The format was created to address the limitations of other 3D file formats, providing a more compact and efficient representation of 3D assets.

If we observe, the part of the code that adds the GLTF loader we can view that highlighted link is the source for the 3d object.

Code Block 1: Example Showing 3D Loader

const loader = new THREE.GLTFLoader();

loader.load(

'https://docs.mapbox.com/mapbox-gl-js/assets/34M\_17/34M\_17.gltf',

(gltf) =\> {

this.scene.add(gltf.scene);

}

);

this.map = map;

This means that by changing that URL we are able to to replace it with our own model. We do this by creating a Github account, creating a folder in desktop to store the files and creating repository in Github. The next is to import GLTF models into the folder. We can create a GLTF model by exporting through Sketchup or Blender.

Open the folder on VS Code to host the repository on your computer. Next, Ctr+Shift+P, and write \>git clone "enter" to clone your folder on repository. Choose "Clone from Github" and choose the file destination for repository.

After this un a new terminal, write "cd .\test3d\" and then press "enter". On the next line, code "git add .", on the following, "git commit -m 'add message'" (Note: on the left side of the menu the name of the GLTF file stopped being green.) After all this, add the file to the repository by "git push".

You can verify that this process was executed correctly by viewing the GLTF file directly on your repository through your Github account. If it appears this process was done correctly. If not, then trace back your steps to make sure you didn't miss anything.

This process ensured uploading the file to the repository now we have to trace it by creating the URL.

Its main composition is : 'https://raw.githubusercontent.com/username/repository\_name/branch/title\_of\_file'

An example of the URL is:

'https://raw.githubusercontent.com/example-user/3d-models /main/Building10'

Once the model is uploaded, open it in blender find the model origin and use "bboxfinder" to recenter the model.

![](RackMultipart20230731-1-ifxyyx_html_c72f221a44d21e2a.png)

![](RackMultipart20230731-1-ifxyyx_html_4ca0faadf66809ec.png)

  1. Attaching Metadata to the GLTF file
  2. 3d water layer
  3. Raycasting & Pop Ups
