---
layout: page
title: MedalMosaic
description: A Data Exploration Tool Unveiling 120 Years of Olympic Data
img: assets/img/viz_project.png
github: https://github.com/kapil40/Olympics-Dashboard
report: /assets/pdf/272.pdf
importance: 1
category: Data Science
---

Using Olympics data of over 120 years, ranging from the 1896 Athens Games to the 2016 Rio Games, I have designed 5 dynamic graphs on a dashboard. 

The interactivity elements present on the dashboad enable the user to change the parameters like **Year**, **Countries**, **Height**, **Weight**, **Gender**, etc. By doing so, the user can get interesting insights into athlete performance in a particular sport or year, or how different countries perform in different sporting events. 

<!-- 
To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    --- -->

<div class="row">
    <div class="col-sm">
        {% include figure.html path="assets/img/map.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm">
        {% include figure.html path="assets/img/barchart.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm">
        {% include figure.html path="assets/img/pca.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
     On the left, a <strong>choropleth</strong> showing participation from various countries. Middle, a <strong>bar chart</strong> showing sport wise participation. Right, <strong>PCA scatterplot</strong> showing relative performance of top 25 countries of that year.
</div>
<div class="row">
    <div class="col-sm">
        {% include figure.html path="assets/img/dash.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <strong>The complete dashboard!</strong>
</div>

<!-- You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images. -->

Interactivity elements in the dashboard are included in the PCA scatterplot and the Parallel Co-ordinates plot: 


<div class="row justify-content-sm-center">
    <div class="col-sm">
        {% include figure.html path="assets/img/inter1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm">
        {% include figure.html path="assets/img/inter2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<!-- <div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div> -->

<!-- {% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
``` -->
<div class="video">
<br><br>
<p>Video to the demonstration of my dashboard!</p>
</div>
<div class="video">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/puMQc-RNkVA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>


{% endraw %}
