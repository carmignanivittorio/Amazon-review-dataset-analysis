---
title: "Data Processing"
bg: blue
color: black
---

## Data Processing

To help users who want access to their data, Amazon offers their dataset as compressed tsv.gz files that can be download for free. the dataset we have chose can be downloaded from [this link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_multilingual_UK_v1_00.tsv.gz). Of course their are more dataset and they can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).
{: .left}

The compressed file that we used is 333 Mb. Uncompressed is 840 Mb. The .tsv file contains 1.707.496 millions rows of data and 14 columns. After some processing we deleted some of the rows because they where either empty (NaN) or corrupted.
There are 15 columns in the .tsv file which are :

<br>
![table](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/table.png)

<br>
<br>
We decided to use 8 of the 15 columns for our project which are :

1. customer_id
1. product_id
1. product_title
1. product_category
1. star_rating
1. review_headline
1. review_body
1. review_date.

Because there are many categories in our data-set we decided to exclude some as the number of the reviews wouldn't contribute to our project analysis. In the below graphs we show some of the basic statistics we were able to conduct with the data we obtained.

<br>

The graph below shows the distribution of the reviews based on the category of the product. As you can see the most reviewed category is the "Video - DVD" with more than 400000 reviews and the category with the least reviews is the "Shoes"
{: .center}

![product_category_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/product_category.jpg)
{: .center}
<br>

This graph shows the Star-Rating of the reviews as seen by the customers. Most of the reviews tend to get a positive rating and more than one million reviews have been rated with 5 stars. That means that the reviews were useful for those who read them.
{: .center}

![star-rating_graph](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/star_rating.png)
{: .center}
<br>

And finally, in the graph below we represent a heat-map that takes the Star-Rating and the Categories and finds correlations between those 2. As we can conclude, the "Video-DVD" category has the most and more positive rating reviews.
{: .center}
<br>
![Correlation between Categories and Star-Rating](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/Correlation%20between%20Categories%20and%20Star-Rating.png)
{: .center}
