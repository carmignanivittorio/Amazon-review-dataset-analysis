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
The Customers-Products network represents the relationships between customers and products. Specifically, the network is created as follows: 
* Nodes: Each node corresponds to a customer or a product.
* Edges: Each edge connects a customer to a product, it represents the review made by the customer about that product.

The network has **992122** nodes and **1701243** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistribution.png)
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistributionLog.png)
{: .center}
The degree analysis shows that there is a big gap between the minimum and maximum degree. However, it also shows that the majority of the nodes have a small degree, whereas, the higher degrees are spread among few nodes. This suggests that probably there are many customers which have reviewed a small number of products and vice versa, many products which have been reviewed by few customers. Simultaneously, it suggests that there few nodes which have an elevated degree. Since it is reasonably infeasible that a single customer has reviewed so many products, we believe that these nodes correspond to the top-sold items. 
### Top category analysis
Due to the huge size of the original network, we want to study a subgraph in order to understand if it reflects the same properties of the whole one. In particular, we will focus on the subnetwork composed by the biggest category and we will analyse it.

The network has **264632** nodes and **462866** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistribution.png)
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerProductDegreeDistributionLog.png)
{: .center}
It can be seen that the subnetwork reflects the same behaviour of the original one.
{: .letft}
### Subgraph analysis
Due to the network's size, some analysis requires too much time to be executed by our hardware. Consequenlty, in order to be able to complete all the analysis we are interested in, we decided to create a bipartite subnetwork which will be used during all the following notebook's analysis.

The main problem was to find a reasonable trade-off between the number of nodes and computation time. A second one was that the network complexity grows exponentially with the number of nodes considered. Therefore, after several attempts, we decided to consider the products which have been reviewed 50 times. Thus, we built a bipartite network taking the 50-reviewed product nodes within the associated customer nodes.

Below, the network is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Subnetwork.png)
{: .center}
The network has **6681** nodes and **6691** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/SubCustomerProductDegreeDistribution.png)
{: .center}
Even this network follows the property of the original one. 

Another noteworhty point is that all these three networks satisfy the *Friendship paradox* with rate higher the 95 per cent. This suggests that they seem to be a scale-free network.
{: .letft}
## Customers network
This network represents the relationships among customers. We study this network in order to find out interesting properties across customers. Specifically, the network is created as follows:
* Nodes: Each node corresponds to a customer.
* Edges: Each edge connects two customers which have reviewed at least one product in common. In order to properly assign weights among edges, each edge has weight equal to the number of common products divided by the sum of the rates difference.

Since the network's size exponentially increases with the number of products considered, it was infeasible to create the projection of the whole orignal network. Consequently, we built the projection of the subnetwork.
Below, the network is shown:
{: .letft}
![customer degree network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerDegreeNetwork.png)
{: .center}
The network has **6547** nodes and **163697** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerDegreeDistribution.png)
{: .center}
Looking at the size and the degree distribution, we can observe that there is a large number of edges. This is due to the fact that the original bipartite subnetwork is composed of products with 50 reviews. As a matter of fact, the majority of the nodes has degree equal to 49 while the remaining degrees are spread among few customers. This enforces the conclusion of the previous network. Indeed, many customers have degree equal to 49 because they have reviewed only one product.
{: .letft}
### Connectivity analysis
In this section, we are interested in finding the centrality properties of the network. To do an accurate study, we will perform four different centrality analysis: degree centrality, closeness centrality, betweenness centrality and eigenvector centrality. By doing this, we want to understand if there are customers more connected than others, as well as if there are some interesting relationship between the most connected and the isolated ones.
#### Degree centrality
Looking at this measure, it can be observed that there are many customers whith the same degree (49). This is due to the fact that we are considering the subnetwork composed by the product with 50 reviewed. Basically, this analysis corresponds to the degree ones that we have done in the previous section.
#### Closeness centrality
{: .letft}
![customer closeness](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerClosenessNetwork.png)
{: .center}
The graph suggests that there two main groups. The former is composed by nodes with a smaller closeness centrality. The latter is characterized by a higher value of closeness centrality. We suppose that the first group represents the customer with few reviews, whereas, the second one gathers the customers with more than one review.
#### Betweenness connectivity
{: .letft}
![customer betweeness network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerBetweennessNetwork.png)
{: .center}
Looking at the graph, it can be observed that the majority of the nodes have a tiny betweenness centrality. Only a few nodes have a remarkable value. This suggests that there are many "isolated" customers which are connected with other few ones.
#### Eigenvector centrality
{: .letft}
![customer eigenvector network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerEigenvectorNetwork.png)
{: .center}
The eigenvector centrality enforces what we have seen in the previous one. In fact, nodes with a higher betweenness have an even higher eigenvector centrality. This is due to nature of the eigenvector centrality.
{: .letft}
#### Assortativity
The assortativity coefficient is very close to zero. This suggests that the network is non-assortative. This reveals that nodes do not strictly tend to connect with nodes that have a similar degree.
#### Community
In this section, we will perform an analysis in order to find out communities among the customers. The main purpose is to identify if customers are correlated, therefore, we will study if the network reveals interesting properties. In case of positive result, this analysis could be used to perform a product recommendation to the customers.
{: .letft}
![customer communities](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/CustomerNetworkCommunities.png)
{: .center}
450 communities have been found by the algorithm. Additionally, the modularity is very close to 1. This suggests that the found partition is reliable and the network shows a "community" structure. The biggest community has 250 nodes and all the top 10 communities have more than 100 nodes. Meanwhile, the smaller ones are composed of isolated nodes. This suggests that customers with a higher number of reviews create communities with other customers which have reviewed the same products. On the other hand, customers which have reviewed only one product remains isolated.
{: .letft}
## Products network
This network represents the relationships among products. We study this network in order to find out interesting properties across products. Specifically, the network is created as follows:
* Nodes: Each node corresponds to a product. Nodes are characterized by two properties:
    * Category: It is the category of the product
    * Title: It is the name of the product
* Edges: Each edge connects two products which have been reviewed by at least one customer in common. In order to properly assign weights among edges, each edge has weight equal to the number of common customers.

The network has **58443** nodes and **5699232** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductDegreeDistribution.png)
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductDegreeDistributionLog.png)
{: .center}
Looking at the results, it can be seen that the network has a huge number of edges. This means that products are well connected. Additionally, the degree distribution suggests that there is a remarkable number of products with a small degree but at the same time, other ones have a large number of connections. Probably, this is due to the fact that many products have been reviewed by a small number of customers, therefore, they are poorly connected with the other ones. On the other hand, products with many reviews are well connected, because they share more customers. We expected this kind of result, in fact, it sounds reasonable that the majority of products have few reviews and few products have been bought by a lot of users.
{: .letft}
### Best products analysis
Here, we are interested in identifying which are the best products in terms of review number, as well as which are the best categories. By doing this, we want to understand if there is a clear distinction between them or thre are more products/categories with a similar number of reviews. 
Below, the top 5 categories are shown:
{: .letft}
![product degree network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/TopCategory.png)
{: .center}
Below, the top 50 products are shown:
{: .letft}
![product degree network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/TopProduct.png)
<br>
The result of this analysis reflects what we already found in the category analysis. The top categories are related to entertainment content. This means the top category, Video DVD, has significantly more reviews than the second one, Music. The same is recursively respected among the other ones. Looking at the product's result, it confirms what category analysis suggested. In fact, almost all of the top 50 products correspond to DVD. An interesting point is that only two very famous mobile apps like Candy Crush Saga and Facebook, appear in the top 50. On the whole, we understood that customers are really in love with movies and DVD.
{: .letft}
### Subnetwork analysis
Due to the large size of the network, we were not able to proceed the analysis using the projection based on the whole network. It requires an infeasible amount of time. Consequently, we decided to build the projection related to the [subnetwork](#Subnetwork). Throught this subnetwork's projection, we will study the centrality, assorativity and community property of the network.

Below, the network is shown:
{: .letft}
![product degree network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductDegreeNetwork.png)
{: .center}
The network has **134** nodes and **171** edges. Below, the degree distribution is shown:
{: .letft}
![subnetwork](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/SubProductDegreeDistribution.png)
{: .center}
The degree distribution follows the usual shape. Looking at the graph, it shows that there are some hub nodes in the middle which probably represent the products with more reviews.
### Connectivity analysis
In this section, we are interested in finding the centrality properties of the network. To do an accurate study, we will perform four different centrality analysis: degree centrality, closeness centrality, betweenness centrality and eigenvector centralities. By doing this, we want to understand if there are products more connected than others, as well as if there are some interesting relationship between the most connected and the isolated ones.
#### Degree centrality
This measure reflects what we have already seen before. In summary, it can be seen that there are more products which are poorly connected because they have been reviewed by customers which have reviewed only that product. Meanwhile, the products with higher degree correspond to the ones which have been reviewed by more active customers. With active we mean that they have reviewed more than one product.
#### Closeness centrality
{: .letft}
![product closeness](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductClosenessNetwork.png)
{: .center}
This measure seems very similar to the customer network's one. The graph suggests that there two main groups. The former is composed by nodes with a smaller closeness centrality. The latter is characterized by a higher value of closeness centrality. As in the customer network, we suppose that the first group represents the products with reviews made by inactive customers, whereas, the second one gathers the products reviewed by the active ones.
#### Betweenness centrality
{: .letft}
![product betweeness network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductBetweennessNetwork.png)
{: .center}
The graph confirms what we saw in the degree and closeness centralities. Indeed, the nodes with higher centralities have a higher betweenness. This is due to the fact that since they are more connected, they are more likely to work as a bridge between the shortest path of the other two nodes.
#### Eigenvector centrality
{: .letft}
![product eigenvector network](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductEigenvectorNetwork.png)
{: .center}
The eigenvector centrality enforces what we have seen in the previous one. It can be seen that the bigger nodes become even bigger, whereas, the smaller ones become even smaller. This is due to the eigenvector centrality's property.
#### Assortativity
The assortativity coefficient is close to zero. This suggests that the network can be considered non-assortative. This reveals that nodes do not strictly tend to connect with nodes that have a similar degree.
### Community
In this section, we will perform an analysis in order to find out communities among the products. The main goal is to find out if products are correlated, hence, we will analyse if the network reveals relevant properties. An interesting point is that in case of a positive result, it will be possible to perform a product recommendation of the products. Additionally, we will compare the communities found by the Louvain algorithm with ones formed by the real categories.
#### Louvain communities
Below, the network is shown based on the Louvain communities:
{: .letft}
![product louvain communities](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductLouvainCommunities.png)
{: .center}
#### Category communities
Below, the network is shown based on the categories:
{: .letft}
![product category communities](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductCategoryCommunities.png)
{: .center}
#### Confusion matrix
Below, the confusion matrix is shown:
{: .letft}
![product confusion matrix](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/ProductConfusionMatrix.png)
{: .center}
Firstly, the modularity is roughly 0.6. This means that there is a good community structure in the network but lower than the customer's one. This result was not really expected. Since products are gathered in categories, we supposed that they would have had a clearer community structure than customers. Furthermore, it can be seen that the communities found by the algorithm partially correspond to the actual categories. The main difference is that the Louvain algorithm tends to group nodes in a clearer way, whereas, looking at the real categories, nodes are more mixed. On the whole, this analysis shows that there is a community structure in the network. Additionally, albeit there are some nodes which tend to connect with nodes of other categories, it confirms that nodes of the same category tend to be more connected with other nodes of the same category. Morevoer, we believe that considering a bigger subnetwork, the results would be even more accurate.
{: .letft}