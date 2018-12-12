---
title: "Data Processing"
bg: blue
color: black
---

## Data Processing

To help users who want access to their data, Amazon offers their dataset as compressed tsv.gz files that can be download for free. The dataset we have chosen can be downloaded from [this link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_multilingual_UK_v1_00.tsv.gz). Of course their are more dataset and they can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).
{: .left}

The compressed file that we used is 333 Mb. Uncompressed is 840 Mb. The .tsv file contains 1.707.496 millions rows of data and 14 columns. After some processing we deleted some of the rows because they where either empty (NaN) or corrupted.
There are 15 columns in the .tsv file which are :

<br>
![table](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/table.png)

<br>
<br>
We decided to use 8 out of the 15 columns for our project which are :

1. customer_id
1. product_id
1. product_title
1. product_category
1. star_rating
1. review_headline
1. review_body
1. review_date.

The original dataset contains 32 categories. Since 12 of them have less than 1000 reviews (all together they represents the 0.19% of the entire dataset), we decided to exclude them. In the following graphs we show some of the basic statistics we were able to conduct with the data we obtained.

<br>
Below, the graph represents the numbers of reviews based on the star rating. As we can see the distribution is not uniform.
Most of the reviews tend to get a positive rating and more than one million reviews have been rated with 5 stars.
{: .left}

![star-rating_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/star_rating.png)
{: .center}
<br>

We present here the number of reviews divided by category. As you can see the dataset is not uniform. The largest one, "Video - DVD", has more than 460000 reviews while "Shoes" "only" 1718.
{: .left}

![product_category_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/product_category.jpg)
{: .center}
<br>

Finally, an heat-map is showed to display the correlation between Star-Rating and Categories. As we can expect, the "Video-DVD" category has the most and more positive rating reviews.
{: .left}
<br>
![Correlation between Categories and Star-Rating](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Correlation%20between%20Categories%20and%20Star-Rating.png)
{: .center}
