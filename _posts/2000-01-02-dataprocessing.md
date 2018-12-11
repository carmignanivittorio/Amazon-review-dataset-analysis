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
<div>
<table style="width:100%">
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
{: .left}

<div>

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-xldj{border-color:inherit;text-align:left}
</style>
<table class="tg">
  <tr>
    <th class="tg-xldj"></th>
    <th class="tg-xldj"></th>
    <th class="tg-xldj"></th>
    <th class="tg-xldj"></th>
    <th class="tg-xldj"></th>
  </tr>
  <tr>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
  </tr>
  <tr>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
  </tr>
  <tr>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
    <td class="tg-xldj"></td>
  </tr>
</table>

</div>





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
