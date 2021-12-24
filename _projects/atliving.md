---
layout: distill
title: ATLivingSafe
description: An interactive safe housing recommendation site.
img: assets/img/atl_cover.png
importance: 1
category: work
authors:
  - name: Qian Huang
  - name: Manqiu Liu
  - name: Yucheng Liang
  - name: Chukang Zhong
  - name: Jia Shi
date: 2021-12-08
toc:
  - name: Overview
  - name: Innovations
  - name: Methods
  - name: Data
  - name: Analytics
  - name: Visualizations
---

## Overview 
We created a safety-oriented apartment listing site that considers each property listing as a web of routes centered at the apartment and expanding into the wider neighborhood.  

This site uses React.js for the frontend, Node.js for the backend, and MongoDB for the database.

See our project [here](https://github.com/gtfiveguys/atl-living-safe-00)  :sunglasses:
See the demo video [here](https://youtu.be/iW4vNfS1OnQ)  :computer:

## Innovations
1. We designed a safety-oriented apartment recom- mendation site for students and incorporated the safe-
ness of apartment’s surrounding areas and the safeness of their daily routes.  

2. We encoded geographical data into grids and built predictive model to evaluate the safeness of each grid, which incorporated the adjacent effects of crime inci- dents and public facilities as well as reduced computa- tional cost.  

3. We visualized the safeness of areas and routes as well as the total safety score, which explicitly showed the overall safeness of chosen student apartments.  

5. We enabled our users customize their daily visit spots and calculate safety score accordingly.


## Methods
We assessed users' everyday travels from the apartment to areas like universities, stores, and other places while evaluating the safety of a certain unit. Then We constructed a predictive model based on apartment data from online scraping and crime statistics from the previous ten years to calculate a safety score for each grid on the map, then mapped apartments and routes to each grid to arrive at our safety score.  


## Data
1. Apartment Data.   

2. Crime Data. We analyzed the crime data from 2009 to 2021 from the Atlanta Police Department and predicted future crime rate based on time series analysis. We also did exploration data analysis on the crime data.  

3. Geographic Data. We collected our geographical data from OpenStreetMap, which contains information of geomorphic characteristics, public transportation, public facilities.  

## Analytics

1. **Location Safety Score Evaluation** We split the area of Atlanta into 260*280 grids based on longitude and latitude. In order to incorporate adjacent crime incidents for each grid, we applied kernel method on the matrix.
2. **Route Safety Score Evaluation** We computed the safety score of a route and evaluated the safety status by utilizing the waypoints data. To compute the safety score of a route, we add the safety score of all the waypoints on the route.
3. **Dashboard** If the user is logged into our system with a Google account, the apartments they have saved will be stored in our server database and will be displayed when the users open the dashboard under their accounts.


## Visualizations

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/atlivingsafe.png" title="atlivingsafe image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    ATLivingSafe Site
</div>

