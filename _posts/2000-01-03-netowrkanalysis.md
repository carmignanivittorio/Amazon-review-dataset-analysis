---
title: "network analysis"
bg: orange
color: black
---

## Network Analysis
The main purpose of this analysis is to find out interesting relationship between products and customers. 
Particularly, we are interested in discovering connection between a user and a product as well as customers/products pair. 
In order to thorough analyse the dataset, we will build three different networks:
1. Bipartite Customers-Products network
1. Customers network
1. Products network
{: .letft}
### Bipartite Customers-Products network
The Customers-Products network represents the relationships between customers and products. 
* Nodes: Each node corresponds to a customer or a product.
* Edges: Each edge connects a customer to a product, it represents the review made by the customer about that product.

The network has **992122** nodes and **1701243** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistribution.png)
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistributionLog.png)
{: .center}
The degree analysis shows that there is a big gap between the minimum and maximum degree. However, it also shows that the majority of the nodes have a small degree, whereas, the higher degrees are spread among few nodes. This suggests that probably there are many customers which have reviewed a small number of products and vice versa, many products which have been reviewed by few customers. Simultaneously, it suggests that there few nodes which have an elevated degree. Since it is reasonably infeasible that a single customer has reviewed so many products, we believe that these nodes correspond to the top-sold items. 
### Top category analysis
Due to the huge size of the original network, we want to study a subgraph in order to understand if it reflects the same properties of the whole one. In particular, we will focus on the biggest one and we will analyse it.

The network has **264632** nodes and **462866** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistribution.png)
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistributionLog.png)
{: .center}
It can be seen that the subnetwork reflects the same behaviour of the original one.
{: .letft}
### Subgraph analysis
Due to the network's size, some analysis requires too much time to be executed by our hardware. Consequenlty, in order to be able to complete all the analysis we are interested in, we decided to create a bipartite subnetwork which will be used during all the following notebook's analysis.

The main problem was to find a reasonable trade-off between the number of nodes and computation time. A second one was that the network complexity grows exponentially with the number of nodes considered. Therefore, after several attempts, we decided to consider the products which have been reviewed 50 times. Thus, we built a bipartite network taking the product nodes within the associated customer nodes.

Below, the network is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Subnetwork.png)
{: .center}
The network has **6681** nodes and **6691** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/SubCustomerProductDegreeDistribution.png)
{: .center}
All these three networks satisfy the *Friendship paradox* with rate higher the 95 per cent.
{: .letft}
![customer degree network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerDegreeNetwork.png)
{: .center}

![customer closeness](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerClosenessNetwork.png)
{: .center}

![customer betweeness network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerBetweennessNetwork.png)
{: .center}

![customer eigenvector network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerEigenvectorNetwork.png)
{: .center}

![customer communities](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerNetworkCommunities.png)
{: .center}

![product degree network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductDegreeNetwork.png)
{: .center}

![product closeness](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductClosenessNetwork.png)
{: .center}

![product betweeness network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductBetweennessNetwork.png)
{: .center}

![product eigenvector network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductEigenvectorNetwork.png)
{: .center}

![product louvain communities](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductLouvainCommunities.png)
{: .center}

![product category communities](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductCategoryCommunities.png)
{: .center}

![product confusion matrix](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductConfusionMatrix.png)
{: .center}
