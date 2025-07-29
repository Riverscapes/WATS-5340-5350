---
title: Grading Exercise in GIS
weight: 3
---

There are many options for how to create a digital elevation model to represent your grading plan. For example, most design professionals use [AutoCAD's Civil 3D](https://www.autodesk.com/products/civil-3d/overview) software, as it has sophisticated [grading tools](https://knowledge.autodesk.com/support/civil-3d/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Civil3D-UserGuide/files/GUID-3E75D600-B442-4C78-8DCC-C649E1ED1F87-htm.html). In this class, everyone has experience in ArcGIS so we will stick with implementing a grading workflow in ArcGIS, despite it being inefficient, so you don't have to learn a new piece of software.

We assume you have familiarity with creating TINs and raster DEMs in ArcGIS using the 3D Analyst Extension. If not, you may find [this tutorial](http://gcd.riverscapes.xyz/Tutorials/Building_DEMs/building-dems.html) helpful.

<div class="responsive-embed">
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSPh1Fmqs0hfmQcZJx_4icaaOzRE4D_dsaicXIPGgx4In_p3UdKYW28NeQEsQ5wkg1mZApthNzcBRbe/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="749" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
</div>

## Grading Steps in ArcGIS

Much like the [Building a DEM  tutorial](http://gcd.riverscapes.xyz/Tutorials/Building_DEMs/building-dems.html), it is important to remember that what you are doing is building a DEM, but one that will span areas outside your limits of grading (those will be existing topography), and you will be specifying new topography within the limits of grading. Your final DEM will be a combination of those.

The generic steps in creating a DEM, are:
1. Create a TIN 
2. *Optionally* - Edit TIN with [Tin Editor](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/tin/interactive-tin-editing-tools.htm)
2. Convert TIN to DEM

[TINs](https://desktop.arcgis.com/en/arcmap/10.7/manage-data/tin/fundamentals-of-creating-tins.htm) can be built from a variety of data types, but minimally require one source of vector elevation data. Vector elevation data can come as:

- Mass points (i.e. a shapefile or feature class of type point with an elevation field)
- Contours (i.e. a shapefile or feature class of type polyline with an elevation field)
- 3D breaklines (i.e. a shapefile or feature class of type polyline with 3D geometry representing an elevation at every node)

Optionally, TINs can also include 2D breaklines, and/or polygons to act as hard clip or soft clip boundaries. 


### What we want
We want a new DEM, that is the old DEM outside our limits of grading, and is a modified DEM within our limits of grading reflecting our design.  We can use the following inputs to get it:


| TIN Input Features | Existing Topography <br>(outside Limits of Grading) | Design Topography <br>(inside Limits of Grading) |
|-------------------------------------------------------------|-----------------------------------------------------|----------------------------------------------------------------------|
| Contours<br>(shapefile of type polyline with elev field) | Recommended (e.g. 5 cm or 10 cm contour interval) | Recommended (likely @ 25 cm contour) these are your grading contours |
| Mass Points <br>(*shapefile of type point with elev field*) | Optional (points extracted from existing DEM) | Optional<br>(finish grade spot elevations) |
| Breaklines  | Optional | Optional <br>(breaklines at TOB, TOE, riffle crests, thalwegs, etc.) |

----------------------------------------

# Tutorials
There are two common methods for "getting a topo" of your dsign. The first is to just build that topo inside your limits of grading. The second is to build that new topo for the entire area of intrest. For the  homework, you only need to do option 1. Both are shown below.

----------------------------

## Option 1 - Just a DEM for Limits of Grading
The easier of the two options, is just to create your DEM for your area of interest and the only data in it is your finish grade design. This is what you want if you are going to do change detection for earthwork calculations.


### Step 1 - Get Existing Topography for Whole Area of Interest 

Your Area of Interest will be greater than just your design extents or limits of grading. If, for example, you want to run a hydraulic model of your finish design, you will want to span the whole valley bottom (floodable area) and enough distance upstream and downstream (e.g. 5-10 channel widths) to provide a reasonable boundary condition and context.

If you have raw topographic data (e.g. points and breaklines and/or boundary), you can skip ahead to 2. For the homework, [this is the data you want](https://usu.box.com/s/h4telshq62gf51bv46baxvri74uqcrij) and here's a video explaining the dataset and showing you how to work with it:
<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/7UM5KVb3yyY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>



### 2. Assemble your Elevation Data for your Grading Plan

As the table above indicated, you will minimally have some finish contours inside your Limits of Grading, and may optionally have some finish spot elevations, and maybe some breakline data.

### 2 A. Finish Contours
1. You will need to create a blank shapefile of type polyline (e.g. `25cm_FinishContours.shp`).
2. Open the attribute table, and add a field of type floating point, with a precision of 7 and scale of 2 called `elev`. This will be where you specify the finish elevation value.
3. Start an edit session in ArcGIS of your contour shapefile.
4. Draw finish contours  (with create features) everywhere you want to specify an elevation, and edit each contours `elev` attribute manually to specify the finish elevation. *TIP: it might be useful to have the existing 25 cm contours turned on and symbolized with a multi color ramp so you can easily identify the contour you are breaking away from and where you need to tie back into.*
5. Stop editing and save edits when done.

I walk you through this step here (warning, this is 20+ minutes becaue it is the whole main grading):
<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/-P8IZKDrYgc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### 2 B. Finish Spot Elevations (optional)
1. You will need to create a blank shapefile of type polyline (e.g. `FinishGrades.shp`.
2. Open the attribute table, and add a field of type floating point, with a precision of 7 and scale of 2 called `elev`. This will be where you specify the finish elevation value.
3. Start an edit session in ArcGIS of your point shapefile.
4. Add points (with create features) everywhere you want to specify an elevation, and edit each points `elev` attribute manually to specify the finish elevation. *Tip:  You might find it helpful to turn on labels for this feature so you can see elevations you are specifying.*
5. Stop editing and save when done.

Here's me adding 5 spot elevations to my design.
<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/9AsedtMyBWk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>


### 2 C. Define Limits of Grading
You will need to create a blank shapefile of type polygon, and draw a polygon boundary that represents your limits of grading. If you completely graded all the contours for your finish design, this is literally at the intersection of your finish (proposed) contours with your existing contours.  In reality this is the line that divides where on the outside existing features are left alone and within which heavy equipment (e.g. excavators, backhoes, scrapers, bulldozers) will be changing elevations with cut or fill. 

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/bFdhXUkodSA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>


## 3. Assemble the TIN

Get your 2a, 2b, 2c (contours, points and limits of grading together), and build that TIN.

<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/lIz4BphcqYQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>


## 4. Convert TIN to DEM
Convert your TIN to a DEM of the *exact* same resolution and orthogonal to the existing DEM ([see here if you care about the details of this](http://gcd.riverscapes.xyz/Tutorials/Building_DEMs/bestpractices.html)). This video shows you how to do this:

<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/tTKmPmRmUf0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

## 5. Do Earthwork Calculation in GCD
So, we want to know how much material we're moving around, how much cut and how much fill. We will use the [GCD Add-In](http://gcd.riverscapes.xyz) to do that (see [here for installation instructions](http://gcd.riverscapes.xyz/Download/install.html)).

<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/KJspSxmvgsU" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>


----------------

## Option 2 - an Integrated DEM with Design Burned into Surrounding Existing Topography


### Step 1 - Get Existing Topography for Whole Area of Interest 

Your Area of Interest will be greater than just your design extents or limits of grading. If, for example, you want to run a hydraulic model of your finish design, you will want to span the whole valley bottom (floodable area) and enough distance upstream and downstream (e.g. 5-10 channel widths) to provide a reasonable boundary condition and context.

If you have raw topographic data (e.g. points and breaklines and/or boundary), you can skip ahead to 2.

#### 1 A. Extract Elevations from Existing DEM
To get this, we need to first break out the topographic data from the existing DEM that will not be graded first. What we have is a raster DEM of existing topography (download data [here](http://capstone.restoration.usu.edu/Course_Topics/WATS_5340/Project/2018.html#datasets)). We can use a few commands, to extract vector topographic data (e.g. polyline contours, or point elevations) from the DEM. We want these vector datasets, because that's what is needed to build a TIN.  
- To get contours off of an existing Raster DEM, we simply use the [`contour`](https://desktop.arcgis.com/en/arcmap/10.3/tools/spatial-analyst-toolbox/contour.htm) command. Derive contours at a finer resolution than you used for design (i.e. 5cm or 10 cm instead of 25 cm). The finer resolution, will produce a better TIN. You might name this shape file something like `ExistingContours_5cm.shp`

<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/4LIswhInbZs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

- *Optionally* - if you want point data, you could generate a grid of points (or specify specific points in a new shapefile) and then use the [`extract by points`](https://desktop.arcgis.com/en/arcmap/10.3/tools/spatial-analyst-toolbox/extract-by-points.htm) command to extract elevations at those points from the DEM.

### 2. Erase Existing Elevations from within your Limits of Grading
Your final TIN will be built with existing elevations only outside your limits of grading. 

#### 2 A. Define Limits of Grading
You will need to create a blank shapefile of type polygon, and draw a polygon boundary that represents your limits of grading. If you completely graded all the contours for your finish design, this is literally at the intersection of your finish (proposed) contours with your existing contours.  In reality this is the line that divides where on the outside existing features are left alone and within which heavy equipment (e.g. excavators, backhoes, scrapers, bulldozers) will be changing elevations with cut or fill. 



#### 2 B. Erase Existing Elevations
<img class="float-right" src="https://desktop.arcgis.com/en/arcmap/10.7/tools/analysis-toolbox/GUID-40F0B845-07D7-4269-8E32-A5977821ADA2-web.gif">The [`erase`](https://desktop.arcgis.com/en/arcmap/10.3/tools/analysis-toolbox/erase.htm) command allows you to use your contours (as input), and your limits of grading (as erase feature), and produce a new contour shapefile (maybe call it something like `ExistingContours_5cm_OutsideLoG.shp`). This will be your input into your finish TIN for the existing topography.

<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/YF2AZ4CgmW8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### 3. Assemble your Elevation Data for your Grading Plan

As the table above indicated, you will minimally have some finish contours inside your Limits of Grading, and may optionally have some finish spot elevations, and maybe some breakline data.

### 3 A. Finish Contours
1. You will need to create a blank shapefile of type polyline (e.g. `25cm_FinishContours.shp`).
2. Open the attribute table, and add a field of type floating point, with a precision of 7 and scale of 2 called `elev`. This will be where you specify the finish elevation value.
3. Start an edit session in ArcGIS of your contour shapefile.
4. Draw finish contours  (with create features) everywhere you want to specify an elevation, and edit each contours `elev` attribute manually to specify the finish elevation. *TIP: it might be useful to have the existing 25 cm contours turned on and symbolized with a multi color ramp so you can easily identify the contour you are breaking away from and where you need to tie back into.*
5. Stop editing and save edits when done.

### 3 B. Finish Spot Elevations (optional)
1. You will need to create a blank shapefile of type polyline (e.g. `FinishGrades.shp`.
2. Open the attribute table, and add a field of type floating point, with a precision of 7 and scale of 2 called `elev`. This will be where you specify the finish elevation value.
3. Start an edit session in ArcGIS of your point shapefile.
4. Add points (with create features) everywhere you want to specify an elevation, and edit each points `elev` attribute manually to specify the finish elevation. *Tip:  You might find it helpful to turn on labels for this feature so you can see elevations you are specifying.*
5. Stop editing and save when done.

## 4. Assemble the TIN

Get your 3A, 3B, and 3 together and build a complete TIN:

<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/eFBlIeXWY_o" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

## 5. Convert TIN to DEM and Derive Hillshade

Make your complete map for design project conditions.
<div class="responsive-embed"><iframe width="560" height="315" src="https://www.youtube.com/embed/9FbhEnFSWAs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
