# AIDI-1100-Project

AIDI_1100_01_FINAL_PROJECT_GROUP_2.ipynb contains the final code.

---
**Group Number:** 2

**Group Members:**

Jaspreet Singh Marwah

Lawrence Wanderi Mwangi

Sherap Gyaltsen

Ayobami Banjoko

Oluwaseun Ogunnubi

Simrandeep Singh Rahi

**Course:** AIDI1100 - Introduction To AI Development

**Submission Date:** 30th October, 2021

---

**Strategy of Code Distribution:**

Part 1 (Scan/Parse): Jaspreet

Part 2 (Track/Store): Lawrence Wanderi Mwangi

Part 3 (Retrieve Data): Sherap Gyaltsen

Part 4 (Visualize): Ayobami Banjoko, Oluwaseun Ogunnubi, Simrandeep Singh Rahi



---

**Program Description:**

*Part 1 (Scan/Parse):* 

First, using the _get_urls() function, the program goes through the list of articles found on https://www.prnewswire.com/news-releases/news-releases-list. It gets the raw html code of the website. Using the BeautifulSoup module, the program parses through the html code and collects the URLs for all the articles released up til a certain date and time. If necessary, the program will keep going to the next page of the website until the URLs of all the articles released till the required date have been obtained.

Then, using _get_articles(), for each URL obtained (where each URL corresponds to one article), the raw HTML code is extracted and parsed through using BeautifulSoup. The program finds all the text from the body of the articles and stores it in a list.

The scrape function is used to conveniently execute both functions based on a specified number of days worth of articles. It then returns a list of all the text from the articles. This function allows this part of the code to act as an individual module. More information regarding this can be found in the "Bonus Work" section of this file.

*Part 2 (Track/Store):*

All the text from the articles is merged into one large string. This string is parsed over using a regex pattern to find all stock symbols within the articles collected.

*Part 3 (Retrieve Data):*

3 of the stock symbols that were collected are chosen for analysis, namely TSLA, GM and LCID. Given a start date, end date, and stock symbol, the stock_data() function will provide information regarding the closing price and volume of the specified stock for each day within the range of dates provided. This function does this by calling the Yahoo Finance API with the help of the yahoo_fin package.

*Part 4 (Visualize):*

generate_visualisations() takes advantage of the plotly and matplotlib libraries to generate interactive time-series plots of the volume and closing price of a given stock within a 60 day period. When the function is called with a stock name, it displays the two plots.

---

**Bonus work:**



*   GitHub was used to colaborate on the project. GitHub link: https://github.com/Zantorym/AIDI-1100-Project
*   The code for part 1 can be used as a module. When imported, the scrape() function will scrape all the latest PRNewswire articles published a specified number of days ago. This module is available on the GitHub repository as "prnewswire_scraper.ipynb".
*   The dataset obtained from part 1 (the text from all the articles) and part 2 (the list of stock symbols) was pickled and uploaded to our GitHub repository for convenience as well as to ensure that all group members were working on the same dataset.
