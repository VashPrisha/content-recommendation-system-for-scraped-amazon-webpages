# content-recommendation-system-for-scraped-amazon-webpages
Used Python and NLP techniques, like NLTK and BeautifulSoup, allowing web scraped amazon data for product suggestions. Enhanced user experience by organizing the suggestions in a table based on preferences.

                            MAJOR PROJECT 
                                              NLP and Web Scraping
CONTENT (SMARTPHONE) RECOMMENDATION SYSTEM based on 
SCRAPED AMAZON WEB PAGES DATA

i) CODE:
This code scrapes product information from the first four pages of an Amazon 
search results page for electronics and prints the product name, price, rating, and 
number of user reviews. It uses the ‘requests’ library to fetch the HTML content of 
each page and the ‘BeautifulSoup’ library to parse this content. For each page, it 
locates product containers by searching for HTML elements with the attribute 
‘data-component-type’ set to ‘'s-search-result'’. Within each product container, it 
tries to extract the product name, price (including both whole and fractional parts), 
rating, and number of user reviews using specific class names and tags. If any of 
these details are missing, it provides a default ‘not found’ message. Finally, it 
prints the extracted details for each product, and if a page fails to load, it reports 
the failure along with the status code and URL.

ii) CODE:
Now, for ease of data manipulation this code scrapes product information from the 
first four pages of an Amazon search results page for electronics and saves the data 
into a CSV file named ‘amazon_products.csv’. It uses the ‘requests’ library to fetch 
HTML content from each URL and the ‘BeautifulSoup’ library to parse the 
content. The CSV file is opened in write mode with UTF-8 encoding, and the 
header row is written first. For each page, the code checks if the request is 
successful (status code 200). It then finds all product containers using a specific 
attribute and extracts the product name, price (including whole and fractional 
parts), number of user reviews, and rating. If any detail is missing, a default ‘not 
found’ message is assigned. The extracted information is written to the CSV file 
row by row. If a page fails to load, an error message with the status code and URL 
is printed.

iii) CODE:
This code creates a recommendation system for smartphones using a CSV file 
containing product data from Amazon. It first reads the CSV file into a pandas 
DataFrame, then extracts and converts the ‘Rating’ and ‘Number of user reviews’ 
columns to numeric values, dropping any rows with missing values. These features 
are normalized using MinMaxScaler. A similarity matrix is generated using the 
cosine similarity metric based on the normalized ‘Rating’ and ‘Number of user 
reviews’ features. The ‘recommend_smartphones’ function takes a product name 
and returns a specified number of similar smartphones by finding the index of the 
given product, calculating similarity scores, and sorting them in descending order, 
excluding the product itself. If the product name is not found, an error message is 
printed. Finally, it prints out the recommended smartphones similar to the specified 
product.
