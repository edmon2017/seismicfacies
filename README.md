# Seismic Facies Classification using a unsupervised machine learning approach

For this project, I'm going to use self organized maps to classify seismic facies.

The data that I'm going to use is from a public repositoy with seismic and well information form the F3 block, in the North Sea Offshore.

The repository is located in this link

https://terranubis.com/datainfo/F3-Demo-2020


## Problem description
Seismic data is an important tool for oil and gas exploration and production, one of the benefits of this tool is that allows to interpret the behavior of the rocks in subsurface.

However because this process is an indirect interpretation, it has a lot of uncertainties.

In this project, I try to estimate facies from seismic data, which basically are rock with similar properties.

The first step is load the data. In this project I'm going to use some seismic attributes that are going to be the predictors for the seismic facies.

![image](https://github.com/user-attachments/assets/b5028286-d075-44e1-9d45-eb89fd6d7ffb)

## Model creation
For this project, I'm going to use self organized maps and Kmeans.

A Self-Organizing Map (SOM) is an unsupervised neural network that projects high-dimensional data onto a typically two-dimensional grid while preserving the topological relationships between samples. Each cell in the grid has an associated weight vector; during training, input vectors “compete” to find the best-matching neuron and then adjust not only that neuron’s weights but also those of its neighbors. Over many iterations, similar inputs become mapped to nearby neurons, producing a spatially organized representation useful for clustering, visualization and dimensionality reduction.

Next we can analyze the result of the model and observe the Matrix with the distances between nodes

![image](https://github.com/user-attachments/assets/2b48b021-fa14-47ac-a77b-f24e702f08b4)

After, calculate the clusters, we can consider each of this as a seismic facies, the previous image is the result of the unsupervised facies classification. We can notice how the 3 values are clearly defined, with good lateral continuity and horizontal spearation, which is what we sohuld expect from a geological point of view.

![image](https://github.com/user-attachments/assets/c7d70e0d-07d8-4a6b-a183-8a2ceb096566)


## Conclusions
Unsupervised machine learning was succesfully applied to the geoscience problem.
Using a combination of self orgainzed maps and Kmeans, it was possible to classify seismic facies, and we can notice there was a good correlation between this classification and the lithology.
Future work could consider include different seismic attributes in the model or used some king of supervised aproach using the information from wells
