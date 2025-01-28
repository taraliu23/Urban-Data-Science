# Cartography with QGIS

QGIS (formerly Quantum GIS) is an *open-source* Geographic Information System (GIS) software that allows users to view, analyze, and edit spatial data. It provides a platform for creating maps, performing geospatial analysis, and managing various types of geographic information. QGIS is widely used for mapping and spatial analysis tasks, and it is accessible to a diverse user community due to its open-source nature.

# Installing QGIS

1. Download QGIS
    
    Visit the official QGIS website: [https://qgis.org/](https://qgis.org/) and click on the  large green "**Download Now**" section. Choose the appropriate version for your operating system (Windows, macOS, or Linux). 
    
    <aside>
    💡
    
    It is advised to download the most stable version (LTR) instead of the latest version, but you can go either way.
    
    </aside>
    
2. Run the installer
    - For Windows, you will typically download an installer executable (.exe) file and select your appropriate system (32-bit or 64-bit). For macOS, it's a disk image (.dmg), and for Linux, the installation method might vary based on your distribution.
3. Launch QGIS
    
    Once the installation is complete, you can launch QGIS. The software may prompt you to set up some initial configurations.
    

<aside>
📖

https://guides.lib.vt.edu/c.php?g=1375762&p=10194090

</aside>

# **Making a Map**

## **Overview of the task**

- Create a choropleth map of California counties
- Utilize good cartography principles and save your map

## Download the data files

In this step, you will download the data files.

Click this link: 🔗 [california.geojson](https://gtvault-my.sharepoint.com/:u:/g/personal/tliu479_gatech_edu/ERf86VocBqtOuA08AP9lC28BNoxp4YUHVIBXBlalLu1URA?e=9FedRl) or visit [https://gtvault-my.sharepoint.com/:u:/g/personal/tliu479_gatech_edu/ERf86VocBqtOuA08AP9lC28BNoxp4YUHVIBXBlalLu1URA?e=9FedRl](https://gtvault-my.sharepoint.com/:u:/g/personal/tliu479_gatech_edu/ERf86VocBqtOuA08AP9lC28BNoxp4YUHVIBXBlalLu1URA?e=9FedRl) to download our example data.

## Open QGIS

1. Open QGIS (Windows: Start > QGIS Desktop / MacOS: Applications > QGIS.app ). This might take a few seconds to load and open or you can open the QGIS folder on your desktop. In this folder, find QGIS Desktop and double-click it to open this program.
    - If it is your first time opening QGIS, you will need to get through some messages/hints by clicking next.
2. Navigate QGIS by familiarizing yourself with the various parts of the QGIS browser, hover your mouse over icons to view names of various tools.

**Note:** Your browser may have different tools than the image below.

- *Layers pane*l - This is where layers (i.e. imagery, building layers) will be listed. The order of layers in the panel impacts the order of layers in the map - in other words, the layer at the top of the list will appear as the top layer in the map.
- *Toolbars* - Most of the tools you will regularly use in QGIS will appear as icons in the toolbars at the top, such as save, zoom, pan. The number of toolbars depends on various features you have activated or installed.
- *Map Canvas* - When layers are added to the Layers Panel, they will appear in the map canvas.
- *Menu Bar* - Provides access to QGIS functions using standard hierarchical menus.
- *Status Bar* - Coordinates, scale, and projection will appear in the Status Bar.

[https://lh7-us.googleusercontent.com/7Crwgo2ckHmOJFCdNuETbw9Eo2lYJEIbVSwtJmKkSHqWa28ZK_SU8MEIcWV-ng3kpZD5xNRrofnBVbhhnxw5OKgW6vSwAFNrgpZPAvV6bMmk3QMMxiRK1569uK29R9w9pmXPIqeNymxgL8BuxhhWb0k](https://lh7-us.googleusercontent.com/7Crwgo2ckHmOJFCdNuETbw9Eo2lYJEIbVSwtJmKkSHqWa28ZK_SU8MEIcWV-ng3kpZD5xNRrofnBVbhhnxw5OKgW6vSwAFNrgpZPAvV6bMmk3QMMxiRK1569uK29R9w9pmXPIqeNymxgL8BuxhhWb0k)

**Note:** This [**QGIS graphic user interface (GUI)**](https://docs.qgis.org/3.28/en/docs/user_manual/introduction/qgis_gui.html) document explains all the tools that are found on the interface you see when you first open QGIS.

## Creating a new Project and Saving

- Open the Meu bar, select **‘Project’ > ‘New’ .**
- On the Menu bar, select **‘Project’ > ‘Save As’**.
- Select the folder that you want to save your project in (ideally this will be the folder that you saved your shapefile datasets in.
- Select a name for your QGIS project, for example ‘virginia_railway_system’ and select “**Save**”.
- Your project will be saved as a ‘**.qgz**’ file.
- From here on out, you can click ‘*Save*’ and your project will be saved.

**Note:** you are advised to save your project after every 10 minutes of working to prevent losing your data in case your project crashes.

## Adding Data to QGIS

Since the canvas that first opens on QGIS is blank, you are advised to add a basemap (raster data) before adding any other data. This helps you to reference and check that the vector data that will be added are falling on the right coordinates on the map.

**1. Adding a Basemap (raster data)**

Before adding a basemap, you will need to install the plugin—this allows you to extend the functionality of QGIS—that will give you access to different free, online basemaps to add to your QGIS maps. This plugin is known as **QuickMapServices**.

**Note:** Managing and installing plugins requires an internet connection. If the Plugin Manager is not working, check your internet connection. Also, as QuickMapServices provides online basemaps, use of these layers requires a consistent internet connection.

To install this plugin, follow these steps:

- Click on the menu item Plugins **‣** Manage and Install Plugins

![https://libapps.s3.amazonaws.com/accounts/363383/images/plugins.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/plugins.PNG)

- In the Plugin Manager dialog box that opens, click on the search bar and type ‘**QuickMapServices**’, the plugin will appear in the list.
- Then click the ‘**Install Plugin**’ button.

![https://libapps.s3.amazonaws.com/accounts/363383/images/QMS.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/QMS.PNG)

- Once installed, QuickMapServices can be accessed on the Menu Bar. Select Web **‣** QuickMapServices
- For more basemaps, including aerial imagery, in the QuickMapServices sub-menu, open ‘**Settings**’. Click the ‘**More Services**’ tab. Select ‘**Get Contributed Pack**’.

![https://libapps.s3.amazonaws.com/accounts/363383/images/QMS2.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/QMS2.PNG)

![https://libapps.s3.amazonaws.com/accounts/363383/images/QMS3.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/QMS3.PNG)

- Return to the QuickMapServices sub-menu. There will now be a long list of options for basemaps, including Bing.

In this exercise, we will use OpenStreetMap as our basemap (raster) layer.

- Go to the ‘Menu Bar’, select **Web ‣ QuickMapServices ‣ OSM ‣ OSM Standard**
- A basemap of the world will open and OSM Standard will be added to your layer panel as a rasterdata layer.
    
    ![https://libapps.s3.amazonaws.com/accounts/363383/images/rasterpixel.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/rasterpixel.PNG)
    

![https://libapps.s3.amazonaws.com/accounts/363383/images/OSMRaster.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/OSMRaster.PNG)

**2. Adding vector data**

- Hover your mouse over the tools until you find the “**Add Vector Layer**” tool. Click on this icon to open the Add Vector Data dialog.
    
    ![https://libapps.s3.amazonaws.com/accounts/363383/images/addvector.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/addvector.PNG)
    

![https://libapps.s3.amazonaws.com/accounts/363383/images/addvectorlayer.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/addvectorlayer.PNG)

- Click the 3 dots under ‘**Source**’ and navigate to the location on your computer where you saved the geojson that you downloaded and click ‘**Open**’ (you can select all four layers at once).
    
    ![https://libapps.s3.amazonaws.com/accounts/363383/images/dots.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/dots.PNG)
    
- Then click “**Add**”
- When the data source and project have different CRS, you are prompted to choose the destination CRS.
    
    ![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image.png)
    
- The following data will be added:
    - california
    
    ![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%201.png)
    

**Note:** the color of datasets on the Map Canvas might differ from what you see on the image above.

- Zoom in and out of your map using the scroll button on your mouse, using two fingers on your touchpad, or right clicking and holding down.
- Drag the layers up or down so that they do not cover each other.
- You can turn layers on and off by checking/unchecking the box next to each name.

**Note:** Clicking the menus at the top of the screen will show various tools you can use to edit, visualize and analyze your data.

**Exploring the Attribute Table**

- Right click on each layer and select “**Open Attribute Table**”. A new window will open that shows the attribute table of the selected layer.
    
    ![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%202.png)
    
- Every point, line, or polygon file has an attribute table.
    
    ![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%203.png)
    
- Any data in the attribute table can be used for displaying and labeling on the map and making queries.
- You can also create new columns in the table and add data or calculations.
- Metadata can be key to understanding attribute tables that use codes and abbreviations.

<aside>
💡

**Note:** you cannot open an attribute table for a raster data layer because this format represents information as a grid of cells where each cell contains a value representing a certain attribute. Rasters don't have attribute tables in the same way that vector data does.

</aside>

## Symbolizing your Map

Data can be symbolized in a variety of ways, depending on the data format and available attributes.

**Changing a Single Symbol**

![https://libapps.s3.amazonaws.com/accounts/363383/images/symbolqgis.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/symbolqgis.PNG)

1. Right click on the point layer for “Virginia_Passenger_Rail_Stations” and scroll to the bottom to select ‘**Properties**’.
2. A new layer will open (Layer Properties), select “**Symbology**”
3. You can choose any symbol and color that you think best represents train stations (scroll if needed)
    - You can make more modifications to the symbol and get additional symbol styles by selecting “**Simple Marker**”.
    - Click the dropdown button under ‘Symbol layer type’ and select SVG Marker. This offers you a more versatile and flexible way to represent point features on your map with custom graphics.
    - Scroll down on the ‘SVG Groups’, select ‘transport’ and choose the marker that will best represent a train station from the ‘SVG Images’.

**Note:**

you can also use the search button

![https://libapps.s3.amazonaws.com/accounts/363383/images/search.PNG](https://libapps.s3.amazonaws.com/accounts/363383/images/search.PNG)

to search for a specific marker.

- Change the color, size, stroke, etc. for your points until you get a symbol that you think will best represent your layer.
- When you are satisfied with your symbol, click ‘Apply’ then ‘OK’.

**Symbolize Categories**

Let us change the color and categorize the counties data according to the their names:

1. Open the ‘Properties’ of the “california” layer.
2. Select the dropdown button under ‘Single Symbol’ and select “**Categorized**”.
3. Under ‘Value’ select “Population”, choose a color ramp, and click “**Classify**”. 
    
    ![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%204.png)
    

4. Click “**Apply**” and then “**OK**”. Your map will now have the counties represented by different colors.

![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%205.png)

4. For better visualisation effects, you can adjust the stroke style, and overall symbol opacity in the “Symbol Setting”

![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%206.png)

# Create a Layout of Your Map

In this section you are going to create your map that will be exported to become a basemap. A basemap is like the background picture on a map that helps you know where things are. It shows features like roads, rivers, and landmarks, so you can add your own information on top of it, like markers or points of interest.

1. On the Menu bar, clock ‘Project’ and select “**New Print Layout**”.
2. A small pane will appear where you will enter the title of your layout and a new layout Window will open.

![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%207.png)

1. On the left panel, click the “**Add Map**” icon and draw a box where you would like the map to be placed
    
    [https://lh7-us.googleusercontent.com/18wo2c1-VYiWSNnZGKlSO8NK9DJ50lArKtUoDHmQE8-cIp75s81nfOTNdFjsxUKlf7795m0t_BxtfSd75K-Jp8OsBIz5l1c2D0iU1TYzcc0GzO6VKam2qfhxkm1rX5zNuevmJzWtonl2V-hFm5HMVjA](https://lh7-us.googleusercontent.com/18wo2c1-VYiWSNnZGKlSO8NK9DJ50lArKtUoDHmQE8-cIp75s81nfOTNdFjsxUKlf7795m0t_BxtfSd75K-Jp8OsBIz5l1c2D0iU1TYzcc0GzO6VKam2qfhxkm1rX5zNuevmJzWtonl2V-hFm5HMVjA)
    
    - Drag the corner of the map to fill most of the page but leave room for a title, scale bar, legend, etc.

**Note:** if you need to adjust the scale of your map, do the following:

- Click the ‘Move item content’ icon and drag your map around, zooming in and out.
    
    [https://lh7-us.googleusercontent.com/bXOXwyXfzcphoiF505btcborLPP0kpZRxYPOh4OtF79aSu1EnSMLU5ypWeU6ZVqMp1nu_9jDmZqGxQ8k9lbfZ_DJUDHDHwXnjxkPK8rUChbJC6KC36FaWNuu52mWrZwFZEPQ4dF7QgSoMH0CBopFmCA](https://lh7-us.googleusercontent.com/bXOXwyXfzcphoiF505btcborLPP0kpZRxYPOh4OtF79aSu1EnSMLU5ypWeU6ZVqMp1nu_9jDmZqGxQ8k9lbfZ_DJUDHDHwXnjxkPK8rUChbJC6KC36FaWNuu52mWrZwFZEPQ4dF7QgSoMH0CBopFmCA)
    
- Another option is to change the scale number under ‘Main properties’ to a scale that works for your map
1. To add a legend to your map, click on the “**Add Legend**” icon, and drag in the box big enough to see all of the entries. To edit the wording in your legend, follow these steps:
    
    [https://lh7-us.googleusercontent.com/DjxupG0jIY_kd8zCZd9SrCjAsW3QRnRLShXt-Z8xwouIMau3-55LKt05jQjwKpZNqx7R5Q8QUwcaMDiZSYP-mQ4oIuyM4-CsAsOX8gzVH6Jk258DxfJor_uEj-oRURtPPtRhQTsILXwJaua97Eq4ez8](https://lh7-us.googleusercontent.com/DjxupG0jIY_kd8zCZd9SrCjAsW3QRnRLShXt-Z8xwouIMau3-55LKt05jQjwKpZNqx7R5Q8QUwcaMDiZSYP-mQ4oIuyM4-CsAsOX8gzVH6Jk258DxfJor_uEj-oRURtPPtRhQTsILXwJaua97Eq4ez8)
    
    - With your legend selected, uncheck “Auto update” to enable you to edit.
    - Double click on each layer and edit the layer names to what you want your viewers to see. Click the back button after each change to go back to the ‘Legend Item Properties’.
        
        [https://lh7-us.googleusercontent.com/8dQjx4nqwzngriJUCVgdpiLiLiKgl31tT7Xxy4IREokgHUJsD9MQ2lidYqGpPno87aYVtEpDVIBIDMkKt20dJ3tAhkDRLLuhta8lzcyMHG9R6XBCaejE1PNxApwlvP9L-HaFawVnwhxLtkJtIYYV_ic](https://lh7-us.googleusercontent.com/8dQjx4nqwzngriJUCVgdpiLiLiKgl31tT7Xxy4IREokgHUJsD9MQ2lidYqGpPno87aYVtEpDVIBIDMkKt20dJ3tAhkDRLLuhta8lzcyMHG9R6XBCaejE1PNxApwlvP9L-HaFawVnwhxLtkJtIYYV_ic)
        
    - To remove a layer that you do not need, for example ‘OSM Standard’, select the layer and click the remove icon.
        
        [https://lh7-us.googleusercontent.com/Rb9-BIT8kAyfCfVVaPExOU0e4SOyhRrFw5cm3_7aZt7swkF82nl2rFfnRq0Sk6hYfYKNqYgtwaULhAtyofgy4A49SOIjCa7FHr8lyOAsY6dZjh0A33Pgs_z7QWb6H-hvbHMvPCKrqL7ZvPROrRptp2o](https://lh7-us.googleusercontent.com/Rb9-BIT8kAyfCfVVaPExOU0e4SOyhRrFw5cm3_7aZt7swkF82nl2rFfnRq0Sk6hYfYKNqYgtwaULhAtyofgy4A49SOIjCa7FHr8lyOAsY6dZjh0A33Pgs_z7QWb6H-hvbHMvPCKrqL7ZvPROrRptp2o)
        
2. To add the North arrow, select the “**Add North Arrow**” icon and drag the box to where you want to put your North Arrow and adjust it accordingly.
    
    [https://lh7-us.googleusercontent.com/4Qhx8bpTgLYkMBtL2rh-ozGqPqXDS7pvDi2jDhVZV8Qb6WW2nwrRHCgmiwOowIBGFyP89TdYTNHxu1oxvyOoHSzOD2c8acuKX7fJ-P7iGD57BLSzNcGBSaAOXIo-4MO61zy7lcG-7LHloLpH_9vOIAM](https://lh7-us.googleusercontent.com/4Qhx8bpTgLYkMBtL2rh-ozGqPqXDS7pvDi2jDhVZV8Qb6WW2nwrRHCgmiwOowIBGFyP89TdYTNHxu1oxvyOoHSzOD2c8acuKX7fJ-P7iGD57BLSzNcGBSaAOXIo-4MO61zy7lcG-7LHloLpH_9vOIAM)
    

**Note:** you can change the North arrow types by selecting ‘arrow’ under the “SVG Groups” on the right panel

1. To add a scale bar, select the “**Add Scale Bar**” icon and drag the box to where you want to place your scale bar. You can adjust the scale properties using the ‘Scalebar’ properties on the right hand side.
    
    [https://lh7-us.googleusercontent.com/BJ0HY4LbwvD0-VNtTcli_LUih2_baZUNcvDUp9hGAIXvSswirCl9dEfYAaBEqbp1ph22dBFn31O8aJ_iKq222aMTYieRLOsEyGxFIiNlaysmXTYWMutbw2RX35c6njnWaFOvH0btd5zikTK8HhpJfss](https://lh7-us.googleusercontent.com/BJ0HY4LbwvD0-VNtTcli_LUih2_baZUNcvDUp9hGAIXvSswirCl9dEfYAaBEqbp1ph22dBFn31O8aJ_iKq222aMTYieRLOsEyGxFIiNlaysmXTYWMutbw2RX35c6njnWaFOvH0btd5zikTK8HhpJfss)
    
2. To add a text on your map, for example the map title, select the “**Add Label**” icon and drag the box to where you want to have your map title. To change your text properties, use the ‘Label’ under ‘Main Properties’ on the right hand side of your layout.
    
    [https://lh7-us.googleusercontent.com/3XU97kL0fbKTjeevo9ZsKu6hb5RrfDT_A31tw9eDSIl3tuF-KDehG0-M2VPNqL7Wb0u7xwbGCxOVDNo5Dn7W3QqrDNW1zg9Ef1IYsuIBpJvdRonSZyHFpv1CFcVRS8ru3UOdIFjhq9Wfq5zeRQYPXf0](https://lh7-us.googleusercontent.com/3XU97kL0fbKTjeevo9ZsKu6hb5RrfDT_A31tw9eDSIl3tuF-KDehG0-M2VPNqL7Wb0u7xwbGCxOVDNo5Dn7W3QqrDNW1zg9Ef1IYsuIBpJvdRonSZyHFpv1CFcVRS8ru3UOdIFjhq9Wfq5zeRQYPXf0)
    

Now you will get a map with essentials “TODALS”

<aside>
💡

## **TODALS: 6 basic elements of “a good” map**

**T = Title:** Gives reader a basic preview of what map is displaying or it’s purpose.

**O = Orientation:** Which way is north!? (so reader can figure out how to hold map)

**D = Date:** When was it created? (is this current, outdated, historic?)

**A = Author:** Who created/made/owns the map? (& is it a reliable source?)

**L = Legend/Key:** basic symbols/colors/etc are explained to the reader for clarity

**S = Scale:** shows the reader how much distance is covered on a map in relation to real world

</aside>

<aside>
📖

https://www.44north93west.com/todalss

</aside>

![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%208.png)

To make the map more visually appealing, here are some final touches:

- Make the fonts of title, author, and date consistent to “Arial” and “Arial Black”
- Remove the legend background in ‘Legend > Item Properites’
- Change the Arrow format in ‘North Arrow > Item Properites’ > SVG Browers > SVG Images’, Change its fill color to transparent, and stroke color to dark grey.

![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%209.png)

## Export Your Map

1. On the menu bar on the top left, click ‘Layout’ and select “**Export as Image**”.
2. Select where you want to save your map on your computer and change the ‘Export options’ if you want then click “**Save**”.
    - Your map might take a minute to save (this depends on how heavy the layers you have in your project are.
3. Once done, you can open your image and see how your map looks like.
4. To export the map as a PNG, click ‘Layout’ and select “**Export as an image**” and select where you want to save your map.
5. You can explicitly set image resolution in the ‘Image Export Options’ window

![image.png](Cartography%20with%20QGIS%20189140d41d12802f8b0ed0c456da2ba8/image%2010.png)

1. Change the ‘Export options’ if you want then click “**Save**”.
2. Once done, you can open your file and see how your map looks like. You can also save a PDF version of your cartography work 

<aside>
📖

https://guides.lib.vt.edu/c.php?g=1375762&p=10194090

</aside>