---
title: Bond Scoping Exercise
weight: 2
---
<div  align="center">


	<a class="button hollow" href="{{ site.baseurl }}/Course_Topics/WATS_5350/ConsFinance/"><i class="fa fa-arrow-circle-o-left" aria-hidden="true"></i>  Back to Resilience Bonds <br> Parent Module</a>
 </div>

## Background

<img src="{{ site.baseurl }}/assets/images/howmuch.png" class="float-right"> If a bond is essentially a loan (or financing) that can support implementation a "project", we need to know _what is the scope of the proposed work_ (e.g. _where is it, how big is it, how many acres, how many miles_) and fundamentally **how much is it going to cost?** 

Later, we will also need to know  _who is going to pay for it_(i.e. beneficiaries), _what is their ability to pay for_, and _how much the work is worth to those paying for it_. In this exercise, we're just trying to land at a defensible estimate of _what is the restoration we want to propose_ and _how much is going to cost_. You wouldn't ask a bank for a loan for a house (i.e. a mortgage) without knowing how much the property is selling for (i.e. purchase price). The bank will do its due diligence to a) independently confirm with an appraisal that the house is worth more than you are asking for in the loan, and b) make sure that you are able to pay that back (e.g. employment, assets, income, credit score etc.). We're not dealing with those pieces yet for this exercise. We are just looking on Zillow and seeing how much the type of home we want to buy in this town is going to cost us and whether that buys us a 1 bedroom studio apartment, a 3 bedroom townhome, or a 5 bedroom house. 

## The Assignment

As discussed in class, you are working in teams to prepare a preliminary answer to the basic question of how much do we need for a proposed resilience bond in the HUC 8 (use [this map](https://www.arcgis.com/home/webmap/viewer.html?url=https%3A%2F%2Fhydro.nationalmap.gov%2Farcgis%2Frest%2Fservices%2Fwbd%2FMapServer&source=sd) to figure out your HUC 8) you and your team chose. Specifically, how much:

- Total **acres** of Proposed *Upland Treatments* (e.g. PJ removal, forest thinning, fuels treatments)
- Total **miles** of riverscape proposed for *Low-Tech PBR* treatments
- **Estimated Total Cost** of Proposed Actions (you can provide ranges and medians)

To support your analysis, please use the following assumptions on implementation costs to calculate ranges and medians in your table/spreadsheet:

- For Upland Treatments use: Min cost of $300/acre; Median cost of $1000/acre; Upper cost of $2500 /acre
- For Riverscape LTPBR Treatments use:  Min cost of $50,000/mile; Upper cost of $100,000/mile; and also a Reference Traditional Restoration cost of $350,000/mile

To identify your upland treatments:

- Maybe filter down to just PJ and or Douglas Fir on land that looks treatable (e.g. USFS / BLM ownership) or large private tracts (ignore lots of small parcels)


To identify your LTPBR treatments: 
- Just filter down and use the length in the `Conservation and Restoration Opportunties` management layer and - filter to just the`Low-Hanging-Fruit` result. - Optionally, maybe also filter down to just public BLM and USFS lands. 

-----
## Some Supporting GIS to Help You

There are lots of ways to approximate the above, but here is one recommended workflow based on using data from the warehouse, QGIS and QRAVE.

In class, we just used [WebRAVE](http://rave.riverscapes.xyz/Download/install_webrave.html) to look at projects. Below, I show you how to do this in QGIS with [QRAVE](http://rave.riverscapes.xyz/Download/install_qrave.html) (if you want to install QGIS from scratch for first time, [see here](http://rave.riverscapes.xyz/Download/install_qrave.html#qgis---need-to-get-gis) and you can do it < 5 minutes), but you can do same thing in ArcGIS 10.X with [ArcRAVE](http://rave.riverscapes.xyz/Download/install_arcrave.html).

### Getting Data from Warehouse
<div class="row small-up-2 medium-up-2">
  <div class="column">
    <div class="card">
      <div class="card-section">
        <h4>Warehouse Info </h4>
In class, we gave you all access to the <a href="https://data.riverscapes.xyz/#/BEAR">Bear River Resilience Bond Program</a> in the Riverscapes Consortium <a href="https://riverscapes.xyz/Data_Warehouses/">Warehouse</a>.
<br><br>
If you still need to register for access, see <a href="https://riverscapes.xyz/Data_Warehouses/signup.html">these instructions</a> and then email Joe.
</div></div></div>
 <div class="column">
    <div class="card">


      <div class="card-section">
        <h4>Video Tutorial </h4>
<div class="responsive-embed"> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/Xlg--J14JAE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>

</div>
<i class="fa fa-clock-o" aria-hidden="true"></i>  5 minutes <i class="fa fa-youtube-play" aria-hidden="true"></i>  
</div></div></div></div>

### Riverscape Context for Upland Treatments (acres)
<div class="row small-up-2 medium-up-2">
  <div class="column">
    <div class="card">
      <div class="card-section">
        <h4>Riverscape Context and LANDFIRE</h4>
It could take you a very long time to manually digitize polygons looking just at the aerial imagery. I show you how you can do that in QGIS in first 5 minutes. A more repatable and powerful GIS workflow is to filter down based on some GIS layers. In this 55 minute video, we use the <a href="https://tools.riverscapes.xyz/rscontext/">Riverscapes Context</a> project for a HUC 8 to do the following steps:
<ol>
<li>Use <a href="https://landfire.gov">LANDFIRE</a> existing vegetation (<a href="https://landfire.gov/evt.php">EVT</a>)to identify dominant vegetaton types and choose some to target for treatment areas.</li>
<li>Create a raster that highlights just those chosen vegetaton classes.</li>
<li>Convert that raster to polygons, and calculate acreage.</li>
<li>Clip those polygons based on some other information (i.e. only treat on federal BLM and USFS land.</li>
<li>Use summary statistics to get total acreage.</li>
<li>Fill out spreadsheet with acreage and cost estimates.</li>
</ol>
</div></div></div>
 <div class="column">
    <div class="card">


      <div class="card-section">
        <h4>Video Tutorial </h4>
<div class="responsive-embed"> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/9JX5u53NuDI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>

</div>
<i class="fa fa-clock-o" aria-hidden="true"></i>  55 minutes <i class="fa fa-youtube-play" aria-hidden="true"></i>  
</div></div></div></div>


### BRAT for LTPBR Riverscape Treatments (miles)
<div class="row small-up-2 medium-up-2">
  <div class="column">
    <div class="card">
      <div class="card-section">
        <h4>BRAT-Based Workflow</h4>
We will learn more about the Beaver Restoration Assessment Tool (<a href="https://tools.riverscapes.xyz/brat/">BRAT</a>) in our LTPBR Planning Module. For now, we are just going to take its analysis of "Low-Hanging Fruit Conservation and Restoration Opporunities" to approximate where and how much <a href="http://lowtechpbr.restoration.usu.edu/">low-tech PBR restoration</a> to do in your HUC 8. In this 17 minute video, we do the following steps:
<ol>
<li>Open up BRAT in QRAVE in QGIS</li>
<li>Load the Conservation and Restoration layer from the Managment outputs</li>
<li>Summarize the total mileage of  "Low-Hanging Fruit Conservation and Restoration Opporunities" </li>
<li>Use some simple "Select by Expression" queries to filter down to only the reaches on BLM and USFS land. </li>
<li>Use summary statistics to get total mileage.</li>
<li>Fill out spreadsheet with acreage and cost estimates.</li>
</ol>
</div></div></div>
 <div class="column">
    <div class="card">


      <div class="card-section">
        <h4>Video Tutorial </h4>
<div class="responsive-embed"> 
<iframe width="560" height="315" src="https://www.youtube.com/embed/l8uDiNT2DoY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>

</div>
<i class="fa fa-clock-o" aria-hidden="true"></i>  17 minutes <i class="fa fa-youtube-play" aria-hidden="true"></i>  
</div></div></div></div>


---
## What you are being asked to turn in on Canvas

Please upload:

1. A shared URL to your Google Sheet with numbers (don't forget to turn on sharing)
2. A PDF of your Map (show HUC 8, some context and the polygons for upland treatment, and the portion of the river network you used for areas to treat)