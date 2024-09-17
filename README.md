# PanopticText

Panoptic plugin that allows clustering images based on textual properties.
Two main clustering functions are provided:
- based on syntax, by using scikit-learn we create tfidf vectors and then apply a kmeans on this vectors
- based on semantic, by using bertopic we identify the main topics of the texts and create groups based on these topics.

These two functions are detailled below.

# Installation

`pip install git+https://github.com/Tyrannas/PanopticText.git`

# Functions

## Clusters
In addition to panoptic default KMeans clustering, this plugins adds two main functions:
- cluster_text_syntax: when using this function, you provide the text property that will be used to perform the clustering along with the number of clusters you want. 
- cluster_text_semantic: when using this function, you just provide the text property that will be used to perform the clustering. Two new properties will then be created, a multi_tags property that will be filled for each image with the important words found in the text, and another property which will be a string combining the 5 more importants words of the cluster. This will allow reacreating the clusters without computing everything again.
