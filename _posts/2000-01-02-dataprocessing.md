---
title: "Data Processing"
bg: blue
color: white
---

## Data Processing

To help users who want access to their data, Amazon offers their dataset as compressed tsv.gz files that can be download for free. The dataset we have chose can be downloaded from [this link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_multilingual_UK_v1_00.tsv.gz). Of course their are more dataset and they can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).
{: .left}

The compressed file that we used is 333 Mb. Uncompressed is 840 Mb. The .tsv file contains 1.7+ millions rows of data and 14 columns. After some processing we deleted some of the rows because they where either empty (NaN) or corrupted.
The 14 columns are :

1. marketplace
1. customer_id
1. review_id
1. product_parent
1. product_title
1. product_category
1. star_rating
1. helpful_votes
1. total_votes
1. vine
1. verified_purchase
1. review_headline
1. review_body
1. review_date


We decided to use 8 of the 14 columns for our project which are :

1. customer_id
1. product_id
1. product_title
1. product_category
1. star_rating
1. review_headline
1. review_body
1. review_date.

![test image](https://github.com/carmignanivittorio/SocialGraphProject/blob/master/img/product_category.png)
