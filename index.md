# Introduction
Our world is powered by technology, at the heart of which are computer chips. Chip manufacturers are constantly pushing to optimize the chip manufacturing process to produce chips more efficiently. The key steps of this process are highlighted below. <br>
![design flow](assets/designflow.png)
*VLSI Chip Design Flow* <br>
The chip’s functionality and logic are designed, which is then turned into a circuit representation. The components of this circuit are digitally placed onto the area of the chip, and then wires are digitally routed between them with computer programs, all before the chip is physically produced and tested. One of the issues that prevents chips from being produced is congestion, which is basically when there are too many wires in a certain area on a chip. However, to assess whether or not there is congestion in a chip, one has to go through both placement and routing, which are both timely and computationally expensive. To speed up this process, research has been done to predict congestion before routing and sometimes before placement. The approach we take aims to predict congestion post-placement pre-routing by turning a chip design into a graph and passing its structure and features through a graph neural network. Through our experiments, we hope to gain better insights about the strengths and shortcomings of graph neural network architectures, as well as insights about the data that can contribute to better congestion predictions.

# Problem Statement
We seek to predict local congestion within semiconductor chips prior to routing, aiming to minimize the need for costly reiterations in the design process. Our focus is on identifying key factors influencing congestion to facilitate optimal chip placement and routing. Routing congestion occurs when the demand of wires in a given area exceeds the capacity. <br>
![congestion](assets/congestion.png){:height="300px" width="300px" align="center"} <br>
*Congestion Depicted in a Netlist*

# Methods
Our approach involves exploratory data analysis (EDA) to understand the dataset, pre-processing data for model implementation, and training/testing our GAT model alongside a baseline XGBoost model. We engineer features such as coordinates, width, and pin count to enhance congestion prediction. <br>
![gnn](assets/gnn.png)
*Graph Neural Network*

# Results
Experiments show that our GAT model, particularly with engineered features, outperforms the XGBoost model in learning congestion patterns. While XGBoost excels in assigning demand values accurately, the GAT model provides insights into congestion patterns, paving the way for more efficient chip design. <br>
![heatmaps](assets/heatmaps.png){:height="400px" width="400px" align="center"} <br>
*Our Results*

# Conclusion
Our study explores the use of deep learning techniques for early congestion prediction in VLSI chip design. By leveraging GAT models with engineered features, we aim to improve chip design efficiency and contribute valuable insights to the field.

## Index Terms
* Very Large-Scale Integration
* Routing Congestion
* Deep Learning
* Graph Attention Network
* Post-Placement
* Pre-Routing

Our project repository can be accessed at: <br>
[GitHub Repo](https://github.com/lisasunhwang/Capstone-B07-3)
