---
title: "Data Processing"
bg: blue
color: white
---

## Data Processing

To help users who want access to their data, Amazon offers their dataset as compressed tsv.gz files that can be download for free. The dataset we have chose can be downloaded from [this link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_multilingual_UK_v1_00.tsv.gz). Of course their are more dataset and they can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).
{: .left}

The compressed file that we used is 333 Mb. Uncompressed is 840 Mb. The .tsv file contains 1.7+ millions rows of data and 14 columns. After some processing we deleted some of the rows because they where either empty (NaN) or corrupted. The 14 columns are : marketplace, customer_id, review_id, product_parent, product_title, product_category, star_rating, helpful_votes, total_votes, vine, verified_purchase, review_headline, review_body. We decided to use 8 of the 14 columns for our project which are : customer_id, product_id, product_title, product_category, star_rating, review_headline, review_body, review_date.
