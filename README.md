# HackerNews-Front-Page-Predictor
This project is 2-fold: 
1. scrapes HackerNews articles and saves them to a file
2. runs regression analysis to determine what factors an article has to be more likely to land on the front page

## Libraries used:
- SSL to validate client/server connection to enable scraping
- urllib.request to make the HTTP request and save the server reqponse into a file
- BeautifulSoup for processing the scraped data into a pandas dataframe
- statsmodels.formula.api for running Ordinary Least Squares regression (linear regression) on various attributes of a HackerRank News article

### Independent variables of HackerRank attributes tested include:
- Age since posting (in hours)
- Article points
- Number of comments
- Title length
### Dependent variables include:
- Rank
- Presence on front page (rank >= 30)

#### Spoiler alert:
The most clear logistic relationship showed that the longer that an article was published, the less likely it is to be featured on the front page. This tracks because the front page shouldn't be displaying old news. There is also some indication that the higher number of points would mean the article would be featured on the front page.
