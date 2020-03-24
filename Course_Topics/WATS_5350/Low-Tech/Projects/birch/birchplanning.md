---
title: Planning Process & Data Resources
weight: 4
---
This page walks you through the steps and questions in the Planning Phase of the low-tech [Conservation Planning Process]({{ site.baseurl }}/Course_Topics/WATS_5350/Low-Tech/planning.html). I use the example of [Birch Creek, Idaho]({{ site.baseurl }}Course_Topics/WATS_5350/Low-Tech/Projects/birch/), but the process is generic to application to any riverscape.

# Your Assignment
On Canvas, you were set a [Low-Tech Planning Assignment](https://usu.instructure.com/courses/567581/assignments/2921686?module_item_id=3783031), which asks you to start preparing your low-tech project report for Birch Creek. Below I review that in this 5 minute video:
<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/buOS09oI_4U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

------
# Resources

## Project Site Description & Scope

The project site description & scope is really a synthesis of what I laid out for you in [LECTURE: Watch Birch Creek Project - Part 2](http://capstone.restoration.usu.edu/Course_Topics/WATS_5350/Low-Tech/Projects/birch/#part-2---birch-creek-project-objectives--conservation-planning-process).

**Birch Creek Base Mapping Resources**

| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
| Diamondback Wilde Ranch Property Boundary |  [<i class="fa fa-file-archive-o" aria-hidden="true"></i> DiamondbackW.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/DiamondBackW_Ranch.zip) - 0.07 MB | This is the property boundary for Jay's land. |
| High Resolution Ortho-Photo | 2 cm resolution Orthophoto from March 15, 2020 [Drone Deploy <i class="fa fa-location-arrow" aria-hidden="true"></i>](https://www.dronedeploy.com/app2/data/5e6eb01ca8b7a98011992e20;jwt_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJleHAiOjI1MzQwMjMwMDc5OSwiaWQiOiI1ZTZlYjAxY2E4YjdhOTgwMTE5OTJlMjAiLCJzY29wZSI6WyIzNzNjNzEyN2U2X0Y1MDlBQTI4NDVPUEVOUElQRUxJTkUiXSwidHlwZSI6IlJlYWRPbmx5UGxhbiJ9.tfH--qbaszSn9h8MWom0p8C1UY5eL04N8jtQe7083PpnG6oRjr4jVJH6ysBf6IkU-__yBDqq-S4F8443NxCb3Q) Flight: [<i class="fa fa-file-archive-o" aria-hidden="true"></i> Orthomosaic.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/DroneDeploy/BirchCreekWildeProperty_Orthomosaic_MonMar16035131.333880.zip) - 311 MB | This is from structure-from-motion photogrammetric analysis of a UAV flight. While precise and high resolution, it is not necessarily positionally very accurate (+/- 2 to 5 m), but has high relative accuracy and will more than suffice for basemapping efforts.|
| High Resolution Digital Surface Elevation Model | 2 cm resolution Orthophoto from March 15, 2020 [Drone Deploy <i class="fa fa-location-arrow" aria-hidden="true"></i>](https://www.dronedeploy.com/app2/data/5e6eb01ca8b7a98011992e20;jwt_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJleHAiOjI1MzQwMjMwMDc5OSwiaWQiOiI1ZTZlYjAxY2E4YjdhOTgwMTE5OTJlMjAiLCJzY29wZSI6WyIzNzNjNzEyN2U2X0Y1MDlBQTI4NDVPUEVOUElQRUxJTkUiXSwidHlwZSI6IlJlYWRPbmx5UGxhbiJ9.tfH--qbaszSn9h8MWom0p8C1UY5eL04N8jtQe7083PpnG6oRjr4jVJH6ysBf6IkU-__yBDqq-S4F8443NxCb3Q) Flight: [<i class="fa fa-file-archive-o" aria-hidden="true"></i> ElevationToolbox.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/DroneDeploy/BirchCreekWildeProperty_ElevationToolbox_MonMar16035203.044315.zip) - 43 MB | This is from structure-from-motion photogrammetric analysis of a UAV flight. This is a visual (RGB) representatoin of the DSM, and the values are a color ramp and hillshade representaton, NOT actual elevations. This is good for interpretive mapping, but not analysis.|
| High Resolution Vegetation Model | NDVI (normalied difference vegetation index) estimate of vegetation from March 15, 2020 [Drone Deploy <i class="fa fa-location-arrow" aria-hidden="true"></i>](https://www.dronedeploy.com/app2/data/5e6eb01ca8b7a98011992e20;jwt_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJleHAiOjI1MzQwMjMwMDc5OSwiaWQiOiI1ZTZlYjAxY2E4YjdhOTgwMTE5OTJlMjAiLCJzY29wZSI6WyIzNzNjNzEyN2U2X0Y1MDlBQTI4NDVPUEVOUElQRUxJTkUiXSwidHlwZSI6IlJlYWRPbmx5UGxhbiJ9.tfH--qbaszSn9h8MWom0p8C1UY5eL04N8jtQe7083PpnG6oRjr4jVJH6ysBf6IkU-__yBDqq-S4F8443NxCb3Q) Flight: [<i class="fa fa-file-archive-o" aria-hidden="true"></i> NDVIToolbox.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/DroneDeploy/BirchCreekWildeProperty_NDVIToolbox_MonMar16035352.045059.zip) - 350.8 MB | This is from structure-from-motion photogrammetric analysis of a UAV flight. This is a rough NDVI estimate of vegetation, which can discriminate spectral signals, but is not reliable for mapping vegetation types.|

### UAV Imagery

#### Pre Project
Here is a link to a  [Drone Deploy Flight <i class="fa fa-location-arrow" aria-hidden="true"></i>](https://www.dronedeploy.com/app2/data/5e6eb01ca8b7a98011992e20;jwt_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJleHAiOjI1MzQwMjMwMDc5OSwiaWQiOiI1ZTZlYjAxY2E4YjdhOTgwMTE5OTJlMjAiLCJzY29wZSI6WyIzNzNjNzEyN2U2X0Y1MDlBQTI4NDVPUEVOUElQRUxJTkUiXSwidHlwZSI6IlJlYWRPbmx5UGxhbiJ9.tfH--qbaszSn9h8MWom0p8C1UY5eL04N8jtQe7083PpnG6oRjr4jVJH6ysBf6IkU-__yBDqq-S4F8443NxCb3Q) from March 15, 2020, an an interactive map below:

<div class="responsive-embed">
<iframe width='500' height='500' src='https://www.dronedeploy.com/app2/data/5e6eb01ca8b7a98011992e20;jwt_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJleHAiOjI1MzQwMjMwMDc5OSwiaWQiOiI1ZTZlYjAxY2E4YjdhOTgwMTE5OTJlMjAiLCJzY29wZSI6WyIzNzNjNzEyN2U2X0Y1MDlBQTI4NDVPUEVOUElQRUxJTkUiXSwidHlwZSI6IlJlYWRPbmx5UGxhbiJ9.tfH--qbaszSn9h8MWom0p8C1UY5eL04N8jtQe7083PpnG6oRjr4jVJH6ysBf6IkU-__yBDqq-S4F8443NxCb3Q'></iframe>
</div>

### Photos

<div class="row small-up-2 medium-up-3">
  <div class="column">
    <div class="card">

      <div class="card-section" align="center">
      <a src="https://photos.app.goo.gl/WDAvPs8MUyBLen8A6"><img src="{{ site.baseurl }}/assets/images/projects/birch/BirchDronePreAlbum.png"></a>
        <p><a href="https://photos.app.goo.gl/WDAvPs8MUyBLen8A6"> <i class="fa fa-google-plus" aria-hidden="true"></i> Pre Project March 2020 UAV Flight</a> </p>
      </div>
    </div>
  </div>
  <div class="column">
    <div class="card">

      <div class="card-section" align="center">
      <a src="https://photos.app.goo.gl/aQaFZYwoUZcBM31z6 "><img src="{{ site.baseurl }}/assets/images/projects/birch/BirchFallPre.png"></a>
        <p><a href="https://photos.app.goo.gl/aQaFZYwoUZcBM31z6 "> <i class="fa fa-google-plus" aria-hidden="true"></i> Pre Project - October 2019 Field Trip.</a> </p>
      </div>
    </div>
  </div>


</div>

Flythrough Video (pre - project; narrated version available in [lecture](http://capstone.restoration.usu.edu/Course_Topics/WATS_5350/Low-Tech/Projects/birch/#part-2---birch-creek-project-objectives--conservation-planning-process)):

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/NpR0hWSkAwQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

--------
## CPP - Planning Resources

We follow an adaptation of the NRCS's Conservation Planning Process, for Phase 1 (i.e. planning) as illustrated below:
![CPP_LTPBR_P1-LT]({{ site.baseurl }}\assets\images\CPP_LTPBR_P1-LT.png)
*Figure 3 from Bennett et al. (2019).*

- <a href="http://dx.doi.org/10.13140/RG.2.2.15815.75680" ><i class="fa fa-file-pdf-o" aria-hidden="true"></i></a> Bennett, S., Wheaton, J., Bouwes, N., Shahverdian, S., Macfarlane, W.W. and Portugal, E. 2019. **[Chapter 3 - Planning for Low-Tech Process-Based Restoration](http://dx.doi.org/10.13140/RG.2.2.15815.75680)**.  In: [Low-Tech Process-Based Restoration of Riverscapes: Design Manual - Version 1.0]({{ site.baseurl }}/). Wheaton JM, Bennett S, Shahverdian S, and Maestas JD, (Editors). [Utah State University](http://restoration.usu.edu/) [Wheaton Ecogeomorphology & Topographic Analysis Lab](http://etal.joewheaton.org). Logan, UT.  57 pp. DOI: [10.13140/RG.2.2.15815.75680](http://dx.doi.org/10.13140/RG.2.2.15815.75680).

--------
### 1. Problems & Opportunities 
Perform an initial, broad-brush, description of problems and opportunities as suggested in page 5-7 of [Chapter 3 of the LTPBR Design Manual](http://lowtechpbr.restoration.usu.edu/manual/chap03/). You will get most of the context for this from the [Intro Birch Creek Lectures and Materials](http://capstone.restoration.usu.edu/Course_Topics/WATS_5350/Low-Tech/Projects/birch/). 
- Make sure to articulate the broad management goals as best you can.  
- Include a cursory assessment of *whether or not the project reach is structurally starved to consider the appropriateness of Low-Tech PBR.* Note, that in the resource analysis this is more explicilty considered by comparing existing conditions and expected or historic. 

--------
### 2. Project Objectives 
It is important to restate the broad managment goals in terms of specific project objectives. Revisit the problem (from 1 above) and purpose and confirm or clarify and then recast management goals as SMART (Skidimore 2011) objectives (see page 8-9 of [Chapter 3](https://www.researchgate.net/publication/332304801_Chapter_3_-_Planning_for_Low-Tech_Process-Based_Restoration?channel=doi&linkId=5cad2a7e458515cd2b0d2fe1&showFulltext=true) and in terms of measurable objectives and indicators that tie to riverscape health.



- Skidmore, P.B., Thorne, C.R., Cluer, B.L., Pess, G.R., Castro, J.M., Beechie, T.J. and Shea, C.C., 2011. [Science base and  tools  for  evaluating  stream  engineering,  management,  and  restoration  proposals](https://repository.library.noaa.gov/view/noaa/4020),  U.S.  Department  of  Commerce, Seatle, WA. 

**Indicator Template Resources**

An example template based on Table 3.1 on page 8 of [Chapter 3](https://www.researchgate.net/publication/332304801_Chapter_3_-_Planning_for_Low-Tech_Process-Based_Restoration?channel=doi&linkId=5cad2a7e458515cd2b0d2fe1&showFulltext=true) of the LTPBR Design Manual. is provided below.

| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
| Project Indicator Template |  [<i class="fa fa-file-excel-o" aria-hidden="true"></i> Condition Worksheet.xlsx](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/Condition+Worksheet.xlsx) | This is a template worksheet for populating active channel, active floodplain, vs. inaccessed floodplain mapping of your valley bottom as a means of cataloging condition and estimating recovery potential and constraining design. |

#### Overview of Project Indicator Template
This 7 minute video gives an over of the condition worksheet.

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/DJ0GgLbUpGw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

#### Populating Proportion of Active Valley Bottom Indicator
<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/BRIDPsWNYLU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

#### Populating Beaver Dam Structure Indicators

<div class="responsive-embed">
</div>

--------
### 3. Inventory of Resources
(see page 9-13 of Chapter 3 (Links to an external site.))

#### Valley Bottom Mapping 
(refine provided VBET valley bottom and classify into active channel, active floodplain and in-accessed floodplain components)

**Birch Creek VBET Resources**

| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
|Valley Bottom | Middle Bear River Valley Bottom [<i class="fa fa-file-archive-o" aria-hidden="true"></i> VBET.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/VBET.zip)- 479 MB! | This is an automated output of the [Valley Bottom Extraction Tool](http://rcat.riverscapes.xyz/Documentation/Version_1.0/VBET.html), that has not been validated or hande edited produced with the [Idaho BRAT project](http://brat.riverscapes.xyz/BRATData/USA/IDFG_Idaho/). It is dervied from a 10 m DEM and you should refine (i.e. copy and edit) it with the UAV flight data locally or field evidence. |
|Valley Bottom Clipped to Project Area | Unedited Still, but clipped to 1 mile project reach [<i class="fa fa-file-archive-o" aria-hidden="true"></i> WildeVBET.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/Birch_Wilde_2020.zip)- 7.6 KB | This is what you can copy and edit! |

##### Intial Valley Bottom
This video shows how to work with a [VBET](http://rcat.riverscapes.xyz/Documentation/Version_1.0/VBET.html) output using [RAVE](https://rave.riverscapes.xyz) to get a first-cut preliminary valley bottom (i.e. riverscapes) for your project area:

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/getTYkolo1U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

##### Manually Edit & Refine Valley Bottom
This next video shows you how to refine your valley bottom mapping using some of the UAV imagery as a line of evidence and the VBET output as a starting point:

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/MNLAU_6Z29Q" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

##### Differentiate Active and Inaccessed Valley Bottom
This next video shows you  why and how to map out your valley bottom in to areas of active channel and active floodplain and inaccessed floodplain. The goal of a stage zero restoration is to have active channels and floodplains cover your entire valley bottom. In the planning phase your job is to map conditions and recovery potential in the context of constraints and risk. This helps you do that.

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/PIjQftoUhRc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>


#### Identified Risks within & Adjacent to Riverscape 
Once you have a valley bottom mapped (even if over-estimted), you have a reasonable zone within which and adjacent to which you can assess potential risks associated with flooding and your proposed low-tech restoration.  You should map all known infrastructure and land use within and adjacent to riverscape, as well as immediately downstream; use the NRCS risk matrix to evaluate (see Appendix 3D, pages 36-37 of [Chapter 3 of LTPBR Design Manual](https://lowtechpbr.restoration.usu.edu)). 

**Birch Creek Landuse & Infrastructure Resources**

| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
|Beaver Restoration Assessment Tool | This is the entire BRAT Project [<i class="fa fa-file-archive-o" aria-hidden="true"></i> BRAT.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/BRAT.zip)- 1700 MB! | [BRAT](https://brat.riverscapes.xyz) includes a bunch of layers that give insights into land use and infrastructure resources |

Scroll down to the [BRAT]({{ site.baseurl }}/Course_Topics/WATS_5350/Low-Tech/Projects/birch/birchplanning.html#resource-analysis) download and video, to get the BRAT dataset. Once you have it, this video focuses in on how to use that information that BRAT harvest from freely available national datasets (like NHD, Census Tiger Data for Roads, Land Use Layers, Land Ownership, etc.) to map and make an informed assessment of risk to infrastructure resources and landuse within the riverscape. You job is to take a look at this free data, and decide if it captures what you know to be going on out on site, and if it captures concerns from the land owner (Jay) and/or stakeholders (e.g. USFS, road users and irrigators downstream).

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/OLEtfCK1ru4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

#### Risk vs. Opportunity Assessment 
Identify and map locations where opportunities are possible and where and if risks can be reasonably mitigated. In other words, what valley bottom space is available for low-tech PBR?


--------
### 4. Resource Analysis

#### Assessment of Current Conditions and Recovery Potential 

##### Geomorphic Condition 


This video below goes through some generic background on assessing geomorphic condition, primarily by using the Cluer & Thorne ([2013](https://pdfs.semanticscholar.org/97b5/7edce62571b00897b0ba5c182076772cf92a.pdf)) riverscape evolution model. 

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/UIgoCEuE0Oc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

Applying this to Birch Creek requires a visit in the field and broader training than we have provided you in fluvial geomorphology then this class. As such, I provide the GIS files below in the geomorphic resources that I have done for you and explain to you in the video below how I obtained them. 



| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
| Active Valley Bottom Assessment |  [<i class="fa fa-file-excel-o" aria-hidden="true"></i> Active Valley Bottom Worksheet.xlsx](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/Active+Valley+Bottom+Worksheet.xlsx) | This is a template worksheet for populating active channel, active floodplain, vs. inaccessed floodplain mapping of your valley bottom as a means of cataloging condition and estimating recovery potential and constraining design. |
|Geomorphic Condition Layers (done for you) | Desc [<i class="fa fa-map" aria-hidden="true"></i> Geomorphology.lpk](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/Geomorphology.lpk) - 54 KB | This is just a layer package for the geomorph files. |
|Geomorphology Shape Files | Desc [<i class="fa fa-file-archive-o" aria-hidden="true"></i> Birch_Wilde_2020_Geomorph.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/Birch_Wilde_2020_Geomorph.zip)- 53 KB | This is all the shape files in above layer package (but without symbology; use layer package for that) |




- <a href="https://pdfs.semanticscholar.org/97b5/7edce62571b00897b0ba5c182076772cf92a.pdf"><i class="fa fa-file-pdf-o" aria-hidden="true"></i></a>
 Cluer B, Thorne C. 2013. [A Stream Evolution Model Integrating Habitat and Ecosystem Benefits](https://pdfs.semanticscholar.org/97b5/7edce62571b00897b0ba5c182076772cf92a.pdf). River Research & Applications. DOI [10.1002/rra.2631](https://dx.doi.org/10.1002/rra.2631).

###### Geomorphic Condition of Birch Creek

In this 50 minute (sorry) video, I give you the answer to geomorphic condition (instead of asking you to do it).  I give you the answer because we have not spent enuough time (other than 25 minute background above on Cluer & Thorne (2013)) to help you do this assessment yourself. Moreover, it is difficult to do without walking this carefully in the field. However, I only give you the answer of current geomorphic conditons. **What I ask you to do is**:
- Fill out [<i class="fa fa-file-excel-o" aria-hidden="true"></i> Active Valley Bottom Worksheet.xlsx](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/Active+Valley+Bottom+Worksheet.xlsx) for the five reaches I delineate for you and get that % Active Valley Bottom indicator.
- Estimate for each of the five reaches what you think the recovery potential is (i.e. how much of the currently *inaccessed* valley bottom could be converte to *active channel* and/or *active floodplain* with restoration )

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/Qbo7mtLAH6o" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

###### Mapping Valley Setting & Confinment on Birch Creek
This is not necessary, but if you like the geomorphology stuff, this is just a little bit of context based on the Fryirs et al. (2015) and O'Brien et al. (2019) about how you can map confinement in Birch Creek:

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/gaGobjVPuIo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

- O'Brien, G.R., Wheaton, J.M., Fryirs, K., Macfarlane, W.W., Brierley, G., Whitehead, K., Gilbert, J. and Volk, C., 2019. Mapping valley bottom confinement at the network scale. Earth Surface Processes and Landforms, 44(9): 1828-1845. DOI: [10.1002/esp.4615](https://dx.doi.org/10.1002/esp.4615)
- Fryirs K, Wheaton JM, and Brierley G. 2015.  An approach for measuring confinement and assessing the influence of valley setting on river forms and processes. Earth Surface Processes & Landforms. DOI: [10.1002/esp.3893](https://dx.doi.org/10.1002/esp.3893)



-------

###### Flow Regimes ability to "Do the Work" of Restoration 
Assessment of Flow Regime to do "geomorphic work" necessary to follow desired recovery trajectory.

**Birch Creek Flow Resources**

| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
| Flow Regime Assessment |  [StreamStats](https://streamstats.usgs.gov/ss/) | Typical peak-flow statistics (e.g. Q2 and Q100) are easy to estimate using StreamSTats. You can download flow gague data and do your own regional curves, but this is a reasonable approximation in under 10 minutes. |
| Stream Power Assessment | BRAT Estimates (see below) | For a given segment of reach, you could also take any flow estimate, measurement, or flow statistic (e.g. from StreamStats) and multiply it by reach slope, gravity and density of water and do what BRAT attempts to do for you.|

In this video, I review how you can use [StreamStats](https://streamstats.usgs.gov/ss/) to address the flow regime's ability to "do the work" by simply getting you some discharge estimates. 

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/b2TL8fbKiBc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

- <i class="fa fa-file-pdf-o" aria-hidden="true"></i> [Birch Creek USGS StreamStats Report](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/StreamStats.pdf)
- <i class="fa fa-map" aria-hidden="true"></i> [Birch Creek USGS StreamStats Shapefile](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/StreamStatReport.zip)

BRAT also has estimates of flow and stream power (using same regressions as USGS):

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/d8Kz78Yp438" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

##### Riparian Condition to support Process of Wood Accumulation 

<a src="http://rcat.riverscapes.xyz"><img  class="float-left" src="{{ site.baseurl }}/assets/images/projects/RCAT_Logo-200.png"></a> 
Think about what you can do map  existing and potential woody resources (riparian and upland) for processes of wood recruitment, wood transport and wood accumulation). The [Ripairan Condition Assessment Tool](http://rcat.riverscapes.xyz) gets at some of these lines of evidence, others you will need to make an interpretation and your own assessment of. From page 19 of [Chapter 3 of the LTPBR Manual](https://www.researchgate.net/publication/332304801_Chapter_3_-_Planning_for_Low-Tech_Process-Based_Restoration?channel=doi&linkId=5cad2a7e458515cd2b0d2fe1&showFulltext=true), we look at riparian conditions to address the key question of “**is it likely that a self-sustaining source of woody structure can be restored**?” 

We can ask:
- What is existing riparian vegetation in the valley bottom relative to historic conditions? *with RCAT*
-  Can the riverscape and adjacent uplands support provide a source of woody debris and is natural wood recruitment possible? 
- How accessible is the floodplain for flooding and riparian vegetation recruitment (infrastructure / like levees; this is the *active channel plus active floodplain* you did [above]({{ site.baseurl }}/Course_Topics/WATS_5350/Low-Tech/Projects/birch/birchplanning.html#3-inventory-of-resources)?
- What land uses are taking place in the valley bottom and are they compatible with maintaining a self-sustaining source of structure? 
- How many woody debris jams are currently present? How many could be given the current wood supply? How many could be given the potential wood supply?

As with geomorphic condition, these questions can often be answered simply by walking a   site and assessing wood resources and  recruitment  potential.  You can count jams off the imagery and report them as quantities or linear densities (i.e. jams per mile) for more consistent intercomparison across sites. Below we show what can be gleaned from RCAT as a line of evidence:

<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/GTmVEuMhpX8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>


**Birch Creek Riparian Resources**

| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
|[Riparian Condition Assessment Tool](https://rcat.riverscapes.xyz) | Desc [<i class="fa fa-file-archive-o" aria-hidden="true"></i> Middle_Bear_RCAT.lpk](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/station/BRAT/Middle_Bear_RCAT.lpk)- 432 MB! | This is just a layer package . |



##### Riparian Condition Capacity to support Process of Beaver Dam Activity 


<a src="http://brat.riverscapes.xyz"><img class="float-left" src="{{ site.baseurl }}/assets/images/projects/BRAT_Logo-200.png"></a> 
Allowing beaver dispersing from upstream to move down in and maintain water in this reach could be adventagoues. Where beaver dam activity is an immediate, or long-term goal, the question to ask is whther or not beaver dam actiivty could be sustained and if so to what level? From BRAT, you can at least get:
- Nubmer of Dams in a reach that can be supported currently (e.g. count of capacity)
- Comparison to what might have been supported their historically (i.e. count of upper plausible extent of capacity)

With that information you can compare what sort of recovery potential is possible in terms of a capacity bump. Note that the recovery potential may be less than historic capacity if the area within 100 m of the channel is not likely to increase is favorable production of vegetation to support dam building activity.  Finally, you can:
- Count existing beaver dams
- Compare existing dams to current and potential capacity (uplift potential)
- Consider if there are any areas where beaver could cause unintended harm that may need to be mitigated and/or identified in adaptive management plan.


**Birch Creek Beaver Resources**


| Resource Type | Suggested Resource Link | Notes or Alternative Resource |
|------------------------|-------------------------|-------------------------------|
|[Beaver Restoration Assessment Tool](http://brat.riverscapes.xyz) MiddleBear_16010202 Full Project | This is the entire BRAT Project [<i class="fa fa-file-archive-o" aria-hidden="true"></i> BRAT.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/BRAT.zip)- 1700 MB! | You can make this assessment by asking the questions that BRAT does in the field or at the desktop with the [BRAT cIS](http://brat.riverscapes.xyz/Workshops/2018/johnday.html#brat-capacity-modelling) |
|[Beaver Restoration Assessment Tool](http://brat.riverscapes.xyz) MiddleBear_16010202 Just `BatchRun01`  | This is just the BRAT Project you need [<i class="fa fa-file-archive-o" aria-hidden="true"></i> BatchRun_01.zip](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/BatchRun_01.zip) - 1100 MB! | Above file includes a preliminary run you do not need |
|[Beaver Restoration Assessment Tool](http://brat.riverscapes.xyz) MiddleBear_16010202 Just `*.lpk` for `BatchRun01`  | This is just the layer package output of the BRAT you need [<i class="fa fa-map" aria-hidden="true"></i> BRAT_MiddleBear_16010202_Perrenial.lpk](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Courses/WATS5350/Lowtech/birch/BRAT_MiddleBear_16010202_Perennial.lpk)- 450 MB! | This is what's used in video below and smaller if you're having problems downloading |

This video shows how to download and use the primary outputs of BRAT:
<div class="responsive-embed">
<iframe width="560" height="315" src="https://www.youtube.com/embed/wKWCY47Z8G0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

