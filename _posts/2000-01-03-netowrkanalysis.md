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
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Subnetwork.png)
{: .center}

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
