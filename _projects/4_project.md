---
layout: page
title: Analysis of Breast Cancer data - 2
description: Analysing breast cancer data using Multi dimensional Scaling and Parallel Co-ordinates Plot
img: assets/img/lab2b.png
github: https://github.com/swaradgat19/BreastCancerDataVisualization-2
importance: 3
category: Data Science
---


I have a [dataset](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset) with 31 attributes. I've performed **Multi Dimensional Scaling (MDS)**. I’ve visualised the results using **D3.js** and used **Flask** for the backend. The axes represent the 2 components. The colors represent the clusters. I have performed **K-Means** on the N-Dimensional space and visualised the clusters here. 

<!-- This represents the MDS Variables’ plot. Each point on the scatterplot represents a numerical attribute. I have used $$1-corr$$ as the distance matrix instead of the eucledian distance. I have added an interaction element on each scatterplot circle. On clicking 5 different attributes on the scatterplot, a PCP is generated besides it. -->


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MDS.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MDS_var.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
The results of the MultiDimensional Scaling are visualized here. Dimentionality reduction is performed and 31 attributes are represented on a 2D scatterplot. The <strong>first image</strong> shows MDS performed on all <strong>data points</strong>. The <strong>second figure</strong> shows a <strong>custom MDS</strong> performed on all the 31 features. The closer two features are, the more correlated they are. 
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MDS_PCP.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
A dynamic MDS graph is shown here. On selecting 5 features from the plot, a <strong>Parallel Co-ordinates Plot</strong> is rendered on the right. The PCP gives insighful information about <strong>feature correlation</strong>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/PCP.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<!-- <div class="caption">
    This image can also have a caption. It's like magic.
</div> -->


<div class="video">
<br><br>
<p><strong>Video to the demonstration of my application!</strong></p>
</div>
<iframe width="560" height="315" src="https://www.youtube.com/embed/ePbQvitwIGg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>