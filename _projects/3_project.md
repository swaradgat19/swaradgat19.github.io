---
layout: page
title: Analysis of Breast Cancer Data - 1
description: Analyzing breast cancer data using Principal Component Analysis and Scatterplot Matrix
img: assets/img/lab2a.png
# redirect: https://unsplash.com
github: https://github.com/swaradgat19/BreastCancerDataVisualization
# video: https://drive.google.com/file/d/1iQg7aaVO96ZIz4WbyTl3UZDxWT0A84Le/view?usp=drive_link
importance: 3
category: Data Visualization and Analytics
---

The [dataset](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset) contains numerical data regarding breast cancer. It contains 31 attributes, which describe the various properties of the tumour. The label of this dataset is **‘diagnosis’**, which has two labels. The tumour is either **malignant** or **benign**. Malignant indicates that it is cancerous and benign meaning that it is non-cancerous. There are 31 attributes which describe the tumour, including ‘radius_mean’, ‘texture_mean’, ‘area_mean’, etc.

I have performed **Principal Component Analysis** on this dataset and visualised the results using the following visualization techniques: 

1. Scree Plot
2. Biplot
3. Scatterplot
<br>
<br>
<div class="row">
<ul>
    <div class="desc1">
        <li><p>
        The scree plot shows the principal component on the X-axis and the corresponding "explained variance ratio (%) on the Y-axis. An <strong>interactivity element</strong> has been added on the scree plot. If a red dot is clicked <strong>(intrinsic dimensionality index(di) )</strong>, a table is generated showcasing the explained variance ratios of all principal components till the selected value. We also see the <strong>top 4 attributes</strong> of each principal component. 
        </p></li>
    </div>
    <div class="col-sm- mt-4 mt-md-0">
        {% include figure.html path="assets/img/scree.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <br>
    <br>
    <div class="desc2">
    <li><p>
        This is the biplot. The top 10 attributes are represented as lines on the PCA scatterplot. The dots on the scatterplot represent data points. The closer two axes are to each other, the more correlated they are. We get a good understanding of the correlation of attributes from the Biplot. 
    </p></li>
    </div>
    <div class="col-sm- mt-4 mt-md-0">
        {% include figure.html path="assets/img/biplot.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <br>
    <br>
    <div class="desc3">
        <li><p>
            On selecting the <strong>intrinsic dimensionality index(di)</strong> in each , we get the top 4 attributes for that principal component. The four attributes are taken and a dynamic scatterplot is plotted. The four attributes are on the diagonal. The two labels are “Malignant” and “Benign”. It is color coded accordingly.

        </p></li>
    </div>
    <div class="col-sm- mt-4 mt-md-0">
        {% include figure.html path="assets/img/scatterplot.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
        <!-- <div class="caption3">
        <p>Scatterplot Matrix</p>
    </div> -->
    </ul>
</div>