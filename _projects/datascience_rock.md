---
name: What is a good rock album? A Data Science Exploration
tools: [data science, Python, Machine Learning]
image:
description: Data science exploration of rock albums audio features & lyrics sentiment analysis.
---

# What is a good rock album?

Data science exploration of rock albums audio features & lyrics sentiment analysis.

**Goal** of this project was to obtain a quantitative description of what makes a _good_ rock album.

**Highlights** of this project were working on scraping public APIs (Spotify, Discogs, LyricWikia, Genius), dataset cleaning, dimensionality reduction techniques (tSNE, PCA), and visualizations.

Abstract:

>First, I gather data about the rock albums in the “Top 500 Albums of All Time” (Rolling Stone 2012); secondly, I apply different visualization and analysis techniques to this dataset with the objective of uncovering any substantial differences between the albums at the top of the chart and those at the bottom.

Project for _Cognitive Science II_, Spring 2018, University of Copenhagen.

Paper [here](https://github.com/cristianmtr/WhatIsAGoodRockAlbum/blob/master/CristianMitroi-CogSci2-WhatIsAGoodRockAlbum.pdf)

## Details

A lot of the work in this project revolved around gathering the dataset. For this I first collected the list of [Top 500 rock albums](https://www.rollingstone.com/music/music-lists/500-greatest-albums-of-all-time-156826/).

I then scraped the Spotify API for obtaining the track listing for each of the albums. After this I performed a series of data cleaning tasks, in order to make sure the tracks were the correct ones.

I then scraped the Spotify API again to obtain the audio features for each of the tracks. 

I also scraped the lyrics of each of the tracks and extract an overall emotional rating of these. This rating, along with the audio features from Spotify, formed the basis of my exploration.

Finally, I experiment with different techniques for visualizing and comparing the albums in the dataset. I employed dimensionality reduction methods (PCA, tSNE).

I use the 'popularity' feature from Spotify and the 'rating' score from the Discogs API as a measure of critical and listener reception.

### Results

All in all, it seems like the most successful albums are more _danceable_ but are also more varied in their _danceability_. This is further supported by top albums having more variety in terms of _energy_.

Another result, from lyrics analysis, shows that albums popular on Spotify tend to have more _emotionally negative_ lyrics. This, coupled with the previous observation, yields an image of the successful rock album as being both danceable, yet also dark in its lyricism.

Overall, the dataset was not large enough to yield meaningful comparisons. For future research, I would require a dataset of more albums, including albums that had a poor critical and consumer reception, in order to contrast better.

### Challenges

In scraping the Spotify API, I encountered several instances of the same album, either in Remastered, Re-issued, or Extended versions. These were not the versions I intended to use in the dataset. Thus I had to develop a method for searching and obtain the respective IDs of the original albums. I relied on taking the albums with least number of tracks (usually, re-issues have bonus tracks) and with the highest popularity. I needed to use the original albums as I also intended to use the Spotify 'popularity' rating as a means of measuring what is a _good_ album.

<p class="text-center">
{% include button.html link="https://github.com/cristianmtr/WhatIsAGoodRockAlbum" text="Learn More" %}
</p>