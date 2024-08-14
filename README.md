# HTML-CSS-Scraping-
This project gives an overview of a full web-scraping and data analysis proejct. It helps to understand to identify HTML elements on a page, verify its id and class attributes as well as helps to utilized this understaning to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. This project also helps to learn to scarpe various types of information such as HTML tables and recurring elemts, like multiple news articles on a webpage. 

This project is in the two parts. The first part is related to Scrape titles and preview text from Mars news articles. On the other hand the second part is exploring the information related to scrtape and analyze mars weather data within the given table. The CSV files are given in the assigment and the website named https://static.bc-edx.com/data/web/mars_news/index.html is used to complete the requirments for the first part and the https://static.bc-edx.com/data/web/mars_facts/temperature.html website is used to complete the second part. 

In the first part the first step is to visit the website the following are the code for the first step:

url = 'https://static.bc-edx.com/data/web/mars_news/index.html'
browser.visit(url)

In the second step is to scrape the website. This helps to create a beautiful soup object and use it to extract text elements from the website. Here are the codes for the second step:

html = browser.html
mars_soup = BeautifulSoup(html, "html.parser")
text_elements = mars_soup.find_all("div",class_="list_text")
text_elements

The Step 3 is to Store the Results. This step helps to extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
Store each title-and-preview pair in a Python dictionary. And, give each dictionary two keys: title and preview. An example is the following:

{'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm", 
 'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."
}
Store all the dictionaries in a Python list.
Print the list in your notebook.

The part two is Scrape and Analyze Mars Weather Data. 
Step 1 is to visit the Website. It Uses automated browsing to visit the Mars Temperature Data Site. Inspect the page to identify which elements to scrape. 
Step 2 is to Scrape the Table. It Creates a Beautiful Soup object and use it to scrape the data in the HTML table.
Step 3 is Store the Data. This step assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
id: the identification number of a single transmission from the Curiosity rover
terrestrial_date: the date on Earth
sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
ls: the solar longitude
month: the Martian month
min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
pressure: The atmospheric pressure at Curiosity's location
Step 4 is to Prepare Data for Analysis. This step is to examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
Step 5 is to analyze the Data. This step helps to analyze your dataset by using Pandas functions to answer the following questions:
How many months exist on Mars?
How many Martian (and not Earth) days worth of data exist in the scraped dataset?
What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
Find the average the minimum daily temperature for all of the months.
Plot the results as a bar chart.
Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
Find the average the daily atmospheric pressure of all the months.
Plot the results as a bar chart.
About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
Consider how many days elapse on Earth in the time that Mars circles the Sun once.
Visually estimate the result by plotting the daily minimum temperature.
Step 6 is to Save the Data. This last step is to Export the DataFrame to a CSV file.

Source: https://github.com/JLeigh101/HTML-CSS-Scraping/blob/main/README.md
        https://bootcampspot.instructure.com/courses/5714/pages/11-data-collection?module_item_id=1270348
        ChatGPT
        
