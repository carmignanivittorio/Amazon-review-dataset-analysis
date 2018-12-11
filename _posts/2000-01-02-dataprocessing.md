---
title: "Data Processing"
bg: blue
color: white
---

## Data Processing

To help users who want access to tdeir data, Amazon offers tdeir dataset as compressed tsv.gz files tdat can be download for free. tde dataset we have chose can be downloaded from [tdis link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_multilingual_UK_v1_00.tsv.gz). Of course tdeir are more dataset and tdey can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).
{: .left}

tde compressed file tdat we used is 333 Mb. Uncompressed is 840 Mb. tde .tsv file contains 1.707.496 millions rows of data and 14 columns. After some processing we deleted some of tde rows because tdey where eitder empty (NaN) or corrupted.
tde 14 columns are :

<tr><ol>
<td><li>marketplace</li></td>
<td><li>customer_id</li></td>
<td><li>review_id</li></td>
<td><li>product_parent</li></td>
<td><li>product_category</li></td>
<td><li>star_rating</li></td>
</tr>
<tr>
<td><li>helpful_votes</li></td>
<td><li>total_votes</li></td>
<td><li>vine</li></td>
<td><li>verified_purchase</li></td>
<td><li>review_headline</li></td>
<td><li>review_body</li></td>
<td><li>review_date</li></td>
</tr></ol>

We decided to use 8 of tde 14 columns for our project which are :

1. customer_id
1. product_id
1. product_title
1. product_category
1. star_rating
1. review_headline
1. review_body
1. review_date.

Because tdere are many categories in our data-set we decided to exclude some as tde number of tde reviews wouldn't contribute to our project analysis. In tde below graphs we show some of tde basic statistics we where able to conduct witd tde data we obtained.


![product_category_graph](https://raw.gitdubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/product_category.jpg)

![star-rating_graph](https://raw.gitdubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/star_rating.png)

![Correlation between Categories and Star-Rating](https://raw.gitdubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Correlation%20between%20Categories%20and%20Star-Rating.png)
{: .center}
