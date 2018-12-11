---
title: "Data Processing"
bg: blue
color: white
---

## Data Processing

To help users who want access to their data, Amazon offers their dataset as compressed tsv.gz files that can be download for free. the dataset we have chose can be downloaded from [this link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_multilingual_UK_v1_00.tsv.gz). Of course their are more dataset and they can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).
{: .left}

The compressed file that we used is 333 Mb. Uncompressed is 840 Mb. The .tsv file contains 1.707.496 millions rows of data and 14 columns. After some processing we deleted some of the rows because they where either empty (NaN) or corrupted.
The 14 columns are :

<table>
<tr>
<td>marketplace</td>
<td>customer_id</td>
<td>review_id</td>
<td>product_parent</td>
<td>product_title</td>
<td>product_category</td>
<td>star_rating</td>
<td>helpful_votes</td>
<td>total_votes</td>
<td>vine</td>
<td>verified_purchase</td>
<td>review_headline</td>
<td>review_body</td>
<td>review_date</td>
<tr>
</table>

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


![product_category_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/product_category.jpg)

![star-rating_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/star_rating.png)

![Correlation between Categories and Star-Rating](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Correlation%20between%20Categories%20and%20Star-Rating.png)
{: .center}
