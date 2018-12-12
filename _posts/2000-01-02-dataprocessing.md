---
title: "Data Processing"
bg: blue
color: black
---

## Data Processing

To help users who want access to their data, Amazon offers their dataset as compressed tsv.gz files that can be download for free. the dataset we have chose can be downloaded from [this link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_multilingual_UK_v1_00.tsv.gz). Of course their are more dataset and they can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).
{: .left}

The compressed file that we used is 333 Mb. Uncompressed is 840 Mb. The .tsv file contains 1.707.496 millions rows of data and 14 columns. After some processing we deleted some of the rows because they where either empty (NaN) or corrupted.
The 14 columns are :
<div align = "center">
<table style="width:80%">
<tr>
<td>marketplace</td>
<td>customer_id</td>
<td>review_id</td>
<td>review_date</td>
</tr>
<tr>
<td>product_parent</td>
<td>product_title</td>
<td>product_category</td>
<td>vine</td>
</tr>
<tr>
<td>star_rating</td>
<td>helpful_votes</td>
<td>total_votes</td>

</tr>
<tr>
<td>verified_purchase</td>
<td>review_headline</td>
<td>review_body</td>

</tr>
</table>
</div>
{: .center}
<br>

We decided to use 8 of the 14 columns for our project which are :

1. customer_id
1. product_id
1. product_title
1. product_category
1. star_rating
1. review_headline
1. review_body
1. review_date.

Because there are many categories in our data-set we decided to exclude some as the number of the reviews wouldn't contribute to our project analysis. In the below graphs we show some of the basic statistics we where able to conduct with the data we obtained.

<br>

The graph below shows the distribution of the reviews based on the category of the product
{: .center}

![product_category_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/product_category.jpg)
{: .center}
<br>

This graph shows the Star-Rating of the reviews as seen by the customers
{: .center}

![star-rating_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/star_rating.png)
{: .center}
<br>

And finally in the graph below we represent a heatmap that takes the Star-Rating and the Categories and finds correlations between those 2.
{: .center}
<br>
![Correlation between Categories and Star-Rating](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Correlation%20between%20Categories%20and%20Star-Rating.png)
{: .center}
