---
title: "text analysis"
bg: '#63BD2F'
color: black
---

## Text Analysis
Let's see what we have discoverd about Amazon's reviewers and reviews.

<br>
### Lexical Diversity
We ere interested in seeing the lexical richness of the categories' reviews. Below you can see our plot of the lexical diversity.
{: .left}

![lexical diversity](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/lexical%20diversity.png)
{: .center}

"Video" and "Books" are really close to one.  This is because we usually describe a book with a wider range of adjectives comparing to a router. In contrast, the "Shoes" category seems poorest together with "Baby" and "Watches".
Regarding the difference between headline and body, we can see that there is a big gap. This means that reviewers usually use the same words to do the review's body, while they are more "creative" in the title.
{: .left}

<br>
### Tags
{: .center}

Here we have studied the distribution of the tags: "Adjectives, Nouns, Verbs" in both body and headline. We would like to see if there are any differences between the categories. We expected to find more "adjectives" and "nouns" since we are analyzing reviews. Below we reported the graph for the body.
{: .left}

![body tags](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/body%20tags.png)
{: .center}

The differences between categories are more evident in the headline's graph but still, they are really minor.
Comparing the two graphs, it can be seen that in the headlines is rarer to find verbs. As we forecasted, "Noun" and "adjectives" represents the most famous tags.
{: .left}

<br>
### Collocations
{: .center}

We had 2 goals in this section.
1) Retrieve the collocations, bigram, and trigrams, for both texts with/without stopwords. And show the top4/top3 for bigrams/trigrams.
2) Actually, use these collocations to change the structures' text. Precisely, we would keep the collocations as they are in the next analysis. In this way the analysis of the TF_IDF (which will be performed later) could be more interesting. In particular, in the word clouds, the 2/3 words (which form a collocation) will appear together and not in a random position (inside the picture).
{: .left}

![body tags](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/bigrams.PNG)
{: .center}

<br>
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

<br>
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

<br>
### Similarity between categories
{: .center}

In this section, we want to see which is the similarity between the different categories. In particular, see if there are interesting hidden common characteristic among the categories, in terms of words. We have used the cosine similarity to calculate the distance between the TF-IDF vectors (which represent the various categories).
{: .left}

![similarity matrix](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/similarity_matrix.png)
{: .center}

The matrix does not show really interesting results. Most of the strong relations are between the digital and the classic version of the same category.
{: .left}

<br>
## Sentimental Analysis
{: .center}

Here, We will explore the sentiment of the reviews. In order to accomplish this task we are going to use the word list provided by SentiWords ([***Page link***](https://hlt-nlp.fbk.eu/technologies/sentiwords); [***References***](http://hltdistributor.fbk.eu/license.php?licenseId=f99f59c080464addad699f91bd8c190e)). This list contains **150'000** words (which include collocations). Moreover, We changed the interval of values from [-1,1] to [0,100].

<br>

### Categories vs Star rating
We want to see if the headline better catches the sentiment of the review comparing with the body, as resulted in tf-idf body vs headline (star rating). We have plotted 2 graphs, which show the same data, to have a more clear overview of the outcomes.
{: .left}

![line charts](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/sentiment%20charts.png)
{: .center}

<br>

![newheatmap](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/new_heatmap.png)
{: .center}

* From both graphs, it is verified the fact that the sentiment grows together with the star rating for all the categories.
* As we imagined, the headline better catches the sentiment. In fact, the headlines' interval has a range of values approximately doubled respect to the body's one; [48,65] vs [50,59].
* Another fact worth noticing in the graph is that, the general reviews sentiment is more than 50. Since 50 represents the neutral value, it means that the reviews are almost always "happy" (if "happy" is considered above 50) but they do not exceed. This behaviour could be explained by the fact that people try to be impartial in the process of reviewing. The interesting thing is represented by fact that people are equitable "only" with low rating. In contrast, they are more willing  of writing "happy" words if the products satisfied their need (more stars). This is strange in the sense that, generally, it is easier to "judge".
* The Baby's reviews with 5 stars seems to be the happiest. This is reasonable, in the sense that the category Baby is the "cuteness" among these categories.
* In contrast, all the technological equipment (Video, Camera, Video Games, ...) contains sadder reviews in general.
{: .left}

<br>

### Best Categories
{: .center}

Let's understand which are the happiest/saddest categories. Then, let's see the categories' sentiment distribution.
{: .left}
<br>
![categories sentiment distribution](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/categories%20sentiment%20distribution%20new.png)
{: .center}

<br>
***Plot explanation*** : in this plot, there is a lot of information which will be explained. Firstly, the plot shows the sentiment distribution for each category. Each box has a different shape based on how the review's sentiment is distributed. Secondly, the black line which can be found in each box represents the average. As you can see, the categories are plotted in order respect to this value. All the boxes have approximately the same shape, width, and height. It does not mean that they have the same number of reviews but, the distribution is normalized based on the own values. To see the difference in the number of values, the grey things over the boxes were plotted. Specifically, each point is a review and its position is based on its sentimental value. In fact, you can see that Music and DVD have a lot of reviews comparing to Shoes. Moreover, it can be seen that in the tails appear fewer points (because they represent exceptions in terms of sentiment).

**Outcomes**:
* From this plot we can say that there are not many differences between the distributions.
* Video and Baby are the "happiest" category with an average sentiment value about 63.
* In contrast, Music and Watches are the "saddest" with an average sentiment value about 55, which is still a "happy" value.
* It is reasonable to think that this data is biased by the large presence of "5-star reviews". Since this plot does not show the distribution "in details", an additional "more classic" graph will be created.
{: .left}
<br>
![joy plot](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/joy%20plot.png)
{: .center}
<br>
 This graph is more detailed. In particular it can be observed that, most of the distributions presents 2 peaks, approximately in 50 and in 65. As we said before, this is probably due to the fact that the distribution of the reviews (in terms of star rating) is not uniform. Interpreting these peacks, it is logical to think that the reviews are either neutral (50) or relative happy (65). These abnormalies are more visible in MobileApps and Video. This behaviour was not caputered by the previous graph. In our opinion, it was duty to the fact that the 2 peaks were contained in the "main box" for each category. In addition, looking at the tails, it seems that MobileApps has signficant numbers of "haters", with values near 25, and "lovers", with values near 85.

![sentiment headlines](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/sentiment%20headlines.png)
{: .center}
