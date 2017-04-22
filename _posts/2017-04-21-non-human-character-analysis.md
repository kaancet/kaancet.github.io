---
layout: single
title: "Analysis of Non-human Characters in Movies"
categories: posts
tags: [nonhuman characters, movies, star-wars, python]
excerpt: "Some thoughts and analysis on the role of non-human characters in movies"
---

After watching the latest Star Wars movie, I realized that throughout the whole movie, the only character I liked and related to was the rebel hacked robot K-2SO. This wasn't because rest of the characters were badly written or lacked any depth. Except for Chirrut Îmwe, I really did not get that character as he was somewhere between a comic relief and a wise mentor, but, I digress and this is not a movie review post. After some retrospection I realized that this was the case for most of the movies with non-human characters(NHC) such as the Lord of the Rings franchise, Harry Potter franchise, Pan's Labyrinth, Wall-E and etc.

To continue our example of Star Wars, throughout the whole series, there are multiple NHC's with varying importance on the storyline and all of them - except the infamous JarJar - are adored and some are so culturally ingrained they became the public face of the movie<sup>[[1]](http://www.dailymail.co.uk/news/article-3366666/Luke-president-Storm-Troopers-raid-White-House-new-Star-Wars-film-expects-rake-200m-box-office-weekend.html)</sup>. Even though this can be linked to the fact that those characters are movie specific and it is relatively easier to identify the whole movie - even franchise - from a single movie specific character, it is evident that the use of NHC's use an important role in story telling. Other than these, examples exist that span genres other than science fiction and fantasy such as romcoms and children movies, as they can include animals, objects and imaginary characters as NHC's. 

![r2_and_c3po_gif](/assets/images/NHC/r2-c3po.gif)

I think one of the reasons that NHC's are a strong story telling tool is that they are not bounded by human nature, which includes human psychology, physiology and - most importantly - philosophy. It is possible to create completely absurd and unconventional characters without having to fit them into human morals and ideas. This makes it possible to establish a more customized and flexible storyline because you can craft an NHC that will best suit your plot. Dobby and R2D2 helping out their respective protagonist crews is an example to this as it makes it possible to push the storyline to its boundaries.

To see if there is a correlation between the use of NHC's and good story telling I wanted to analyze the top 10 grossing movies since 2010.

A couple of points regarding the analysis are:
* The dataset was scraped from [this website](http://www.boxofficemojo.com/yearly/chart/) using BeautifulSoup.
* All of the animations were removed due to the fact that the effect of NHC's as described above is intrinsic to animations and including them in the analysis seemed redundant, but given the fact that one third of dataset were animations, the effect of NHC's is already evident.
* The gross box office values are adjusted for infilation but the change in total number of theatres through the years is not accounted for. That's why I used $$ \frac{Gross Box Office}{no. of Theatres} $$ to get the avreage box office of a movie in a theatre.

![gross_vs_NHC](/assets/images/NHC/gross_vs_NHC.png)

The graph shows that the amount of NHC's in a movie positevly effects the gross box office, but it should be noted that the data is, in a sense, 'corrupt', as in the amount of NHC's was determined by me with no concrete definition in mind. Plus, the existence of a NHC might not be directly correlated with the movie box office, considering short and\or background appearences by NHC's, which does not alter the overall course of events in the stroyline. Although I tried my best to not include these NHC's, the dataset is still inherently biased.

To be able to have less biased results I decided to investigate the NHC's in a more confined environment, namely in the Star Wars franchise. I found [this list](http://www.imdb.com/list/ls031379663/) and used the given NHC minutes.

![starwars_NHC](/assets/images/NHC/starwars_NHC.png)

It turns out there is a strong correlation between NHC minutes in Star Wars movies and that movies' box office success and this still holds if we treat Star Wars IV: A New Hope as an outlier, taking into account the science fiction craze and being one of the early decent sci-fi movies.

In conclusion, I believe that the use of NHC's is a powerful tool that could be integrated in storyelling to create better and out-of-the-box stories. Of course the overall effect of NHC's to a movie can not be fully understood by only analysing its effect on the movie's gross box office, but it is the most objective variable that can be studied since quantified commentator insights and public liking measurements can easily be manipulated by generating hype and media presence, further distorting the result. All in all I believe that utilizing NHC's in moderation and in a classy way - yeah I'm looking at you Jar Jar - is useful both for creative and fiscal(yay capitalism) purposes.