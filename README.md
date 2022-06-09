# Summer-2022-Programming-Challenge
Yiyun Zheng

## Files
1. [Summer\_2022\_Programming\_Challenge.ipynb](Summer\_2022\_Programming\_Challenge.ipynb): A colab notebook which include all the python code. Can open with google colab direct and run first cell to install all necessary module. Since the website is dynamic, I used selenium and headless chrome to get the page source.

	There are 4 parts of process:
	1. web Scraping
		* Get most recent articles and their basic info
		* Get full content of articles
	2. Save and read json file
	3. Sentiment analysis using FLAIR
	4. Data visualization

2. [data.json](data.json): A json file that save the basic data and complete content of the article. Each element in list represent a article, and there are 8 attributes for each article:
	* title
	* excerpt
	* img: url of cover image
	* publish_date
	* article: url of article content
	* full_content: content of article
	* sentiment: positive or negative
	* score: sentiment score

3. [vis.png](vis.png): A png file shows how the sentiment of articles on the website changes over time. Positive score means positive sentiment.

## Summary
Most of the articles show a negative sentiment. This result is not entirely accurate, but it does reflect the relative sentiment among articles. Articles with a negative sentiment score of around 0.99 were significantly more violent, negative words and descriptions than other articles. Some articles with a neutral theme are also classified as negative with low score, which I think is because they like to add some description of the local situation at the end, which is usually negative.

[Southern Africa bloc SADC extends Mozambique mission](https://www.aljazeera.com/news/2022/1/12/southern-africa-bloc-sadc-extends-mozambique-mission) is the only article show positive sentiment, but the score is relatively low (about 0.6). Although the focus of the article is on improving security, it also includes descriptions of chaos , like "At least 3,500 people have died and approximately 820,000 have fled their homes." Therefore,  the article get a positive result with low score is correct (positive but not that positive).