---
title: "text analysis"
bg: '#63BD2F'
color: white
---

## Text Analysis
Let's see what we have discoverd about Amazon's reviewers and reviews.

### Lexical Diversity
We ere interested in seeing the lexical richness of the categories' reviews. Below you can see our plot of the lexical diversity.
{: .left}

![lexical diversity](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/lexical%20diversity.png)
{: .center}

"Video" and "Books" are really close to one.  This is because we usually describe a book with a wider range of adjectives comparing to a router. In contrast, the "Shoes" category seems poorest together with "Baby" and "Watches".
Regarding the difference between headline and body, we can see that there is a big gap. This means that reviewers usually use the same words to do the review's body, while they are more "creative" in the title.
{: .left}

### Tags
{: .center}

Here we have studied the distribution of the tags: "Adjectives, Nouns, Verbs" in both body and headline. We would like to see if there are any differences between the categories. We expected to find more "adjectives" and "nouns" since we are analyzing reviews. Below we reported the graph for the body.
{: .left}

![body tags](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/body%20tags.png)
{: .center}

The differences between categories are more evident in the headline's graph but still, they are really minor.
Comparing the two graphs, it can be seen that in the headlines is rarer to find verbs. As we forecasted, "Noun" and "adjectives" represents the most famous tags.
{: .left}

### Collocations
{: .center}

We had 2 goals in this section.
1) Retrieve the collocations, bigram, and trigrams, for both texts with/without stopwords. And show the top4/top3 for bigrams/trigrams.
2) Actually, use these collocations to change the structures' text. Precisely, we would keep the collocations as they are in the next analysis. In this way the analysis of the TF_IDF (which will be performed later) could be more interesting. In particular, in the word clouds, the 2/3 words (which form a collocation) will appear together and not in a random position (inside the picture).
{: .left}

![body tags](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/bigrams.PNG)
{: .center}

### TF-IDF vs Common words
{: .center}

 In this section we are going to analyze the differences between the use of the frequency and TF-IDF to retrieve the importance a word in a text.

This is wordlcloud taking into account all the reviews (body+headline) using the most common word. As we could expect, most words are related to books and videos, which are the categories with highest number of reviews. Then, we can see a lot "good" adjectives. This is due to the fact of having a lot of good reviews (5 stars).

![amazon most common words](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/amazon_cloudword_most_common_word.png)
{: .center}

Let's start drawing now...

![baby](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/baby.png)
{: .center}

![books](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/books.png)
{: .center}

![camera](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/camera.png)
{: .center}

![digital_ebooks](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/digital_ebook.png)
{: .center}

![digital_music](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/digital_mucic.png)
{: .center}

![digital_video](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/digital_video.png)
{: .center}

![electronics](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/electronics.png)
{: .center}

![home](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/home.png)
{: .center}

![mobile apps](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/mobile_apps.png)
{: .center}

![music](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/music.png)
{: .center}

![musical instruments](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/musical_instruments.png)
{: .center}

![pc](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/pc.png)
{: .center}

![shoes](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/shoes.png)
{: .center}

![sports](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/sports.png)
{: .center}

![toys](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/toys.png)
{: .center}

![video](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/video.png)
{: .center}

![video dvd](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/video_dvd.png)
{: .center}

![video games](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/video_games.png)
{: .center}

![watches](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/watches.png)
{: .center}

![wireless](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/wireless.png)
{: .center}

As we expect, the TF-IDF works far better. In fact, it can catch all the brands, people relate to the respective category. This is really clear within the category Camera where: in TF-IDF you can find Nikon, Manfrotto, Fujifilm, Lowepro etc. While in the most common words are not recognizable. In contrast, in the most common words wordClouds appear a lot of adjectives which are common with all the categories such as great, good, love etc.
We did the same also for star rating, but it did not work well. Therefore we tried to do another duel.
{: .left}

### TF-IDF body vs TF-IDF headlines
{: .center}

In this section we are going see where can we find the most important words: headline vs body. It is reasonable to think that the headline will give better results.

Let's start drawing now...
{: .left}

![1_5](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/1.5_stars.png)
{: .center}

![2_5](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/2.5_stars.png)
{: .center}

![3_5](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/3.5_stars.png)
{: .center}

![4_5](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/4.5_stars.png)
{: .center}

![5_5](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/5.5_stars.png)
{: .center}

It is pretty clear that the headline contains more "important" words. For example:
* "Rubbish", **"Total_waste_money"** for one star (we would underline the collocation).
* "Baaaaaad", bleh" for two stars.
* For three stars the results are not really clear, this should be the neutral evaluation.
* "Wonderful", "comforting" for four stars.
* "Unmissable","awesomeness","unbeatable" for five stars.

### Similarity between categories
{: .center}

In this section, we want to see which is the similarity between the different categories. In particular, see if there are interesting hidden common characteristic among the categories, in terms of words. We have used the cosine similarity to calculate the distance between the TF-IDF vectors (which represent the various categories).
{: .left}

![similarity matrix](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/similarity_matrix.png)
{: .center}

The matrix does not show really interesting results. Most of the strong relations are between the digital and the classic version of the same category.
{: .left}

## Sentimental Analysis
{: .center}

![line charts](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/sentiment%20charts.png)
{: .center}

![newheatmap](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/new_heatmap.png)
{: .center}

![categories sentiment distribution](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/categories%20sentiment%20distribution%20new.png)
{: .center}

![joy plot](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/joy%20plot.png)
{: .center}

![sentiment headlines](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/sentiment%20headlines.png)
{: .center}
