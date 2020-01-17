# People Love Us on Yelp: Conceptualizing A New Yelp Award
## Project 4 in the Metis Data Science Bootcamp
Check out the project slideshow for a demonstration of this concept.

Problem statement: *Using restaurant reviews on Yelp and Natural Language Processing methods, can we create a new Yelp award that will attract reviewers and restaurant-owners to use Yelp?*

"People Love Us on Yelp" was originally a great strategy to raise awareness about Yelp at a time where it was still relatively obscure and help distinguish businesses, but years later it seems to get lost among other other window decals. We can go further into this space to create an award to truly distinguish the cream of the crop in fine dining using the data already available within Yelp reviews. I focused on high-end restaurants in California. In this prototype, I used the California Michelin Guide as a proxy for a judging criterion, using an XGBoost Classifier to determine a restaurant's likelihood of being included in the Michelin Guide.

With thousands of restaurants' reviews, I used Latent Semantic Analysis, a method of topic modeling, to discover the hidden topics discussed in these reviews. To avoid data leakage, I ommitted all words that might reveal whether a restaurant was in the Michelin Guide. Rather than break each review down into single words, I used 2- and 3-word phrases to distinguish "bad food" from "delicious food". 

The most salient text-based features that increased a restaurant's odds dealt with unique dining experiences, luxury food items, and remarkable service. On the other side were topics such as boring or traditional meals, large groups, and noisy environments. 

These features created in topic modeling were used along with other restaurant profile information in an XGBoost classifier.

## Files

[`p04_Yelp_Data_SQL.ipynb`](p04_Yelp_Data_SQL.ipynb) shows the use of SQL to extract the Yelp profile and review data for high-end California restaurants from a larger Yelp database

[`p04_Michelin_Guide_Scraping.ipynb`](p04_Michelin_Guide_Scraping.ipynb) shows the use of BeautifulSoup to scrape the names of every restaurant in the 2019 California Michelin Guide

[`p04_NLP_Topic_Modeling.ipynb`](p04_NLP_Topic_Modeling.ipynb) shows the use of TF-IDF and LSA topic modeling to break down and analyze Yelp reviews for high-end restaurants in California.

[`p04_Data_Clean_and_Classification.ipynb`](p04_Data_Clean_and_Classification.ipynb) shows the process of cleaning the Yelp profile data, preparing it for modeling, and building a classification model using the profile and review analysis data

Slides for the final presentation can be found [here](https://www.slideshare.net/AlisonGlazer/conceptualizing-a-new-yelp-award-with-natural-language-processing)
