# Webscraping_mongo_flask

This  web application that scrapes various websites for data related to the Mission to Mars and displays the information in a single HTML page. 

Approch taken:

#Step 1 - Scraping
Complete your initial scraping using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter.

Jupyter Notebook file called mission_to_mars.ipynb used to complete all of scraping and analysis tasks.
NASA Mars News
Scrape the NASA Mars News Site and collect the latest News Title and Paragragh Text. Assign the text to variables that you can reference later.
Example:
news_title = "NASA's Next Mars Mission to Investigate Interior of Red Planet"

#Use splinter to navigate the site and find the image url for the current Featured Mars Image and assign the url string to a variable called featured_image_url.
Example:
featured_image_url = 'https://www.jpl.nasa.gov/spaceimages/images/largesize/PIA16225_hires.jpg'

Mars Weather
Visit the Mars Weather twitter account here and scrape the latest Mars weather tweet from the page. Save the tweet text for the weather report as a variable called mars_weather.
Example:
mars_weather = 'Sol 1801 (Aug 30, 2017), Sunny, high -21C/-5F, low -80C/-112F, pressure at 8.82 hPa, daylight 06:09-17:55'
Mars Facts
Visit the Mars Facts webpage here and use Pandas to scrape the table containing facts about the planet including Diameter, 

#Use Pandas to convert the data to a HTML table string.

getting Mars Hemisperes data and images:
Visit the USGS Astrogeology site here to obtain high resolution images for each of Mar's hemispheres.

Save both the image url string for the full resolution hemipshere image, and the Hemisphere title containing the hemisphere name. 
Use a Python dictionary to store the data using the keys img_url and title.

Append the dictionary with the image url string and the hemisphere title to a list. This list will contain one dictionary for each hemisphere.

Example:
hemisphere_image_urls = [
    {"title": "Valles Marineris Hemisphere", "img_url": "..."},
    {"title": "Cerberus Hemisphere", "img_url": "..."},
    {"title": "Schiaparelli Hemisphere", "img_url": "..."},
    {"title": "Syrtis Major Hemisphere", "img_url": "..."},
]


#step 2 - MongoDB and Flask Application
Use MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from the URLs above.

I created Jupyter notebook into a Python script called scrape_mars.py with a function called scrape that will execute all of  scraping code from above and return one Python dictionary containing all of the scraped data.

Next,
create a route called /scrape that will import your scrape_mars.py script and call your scrape function.

Store the return value in Mongo as a Python dictionary.
Create a root route / that will query your Mongo database and pass the mars data into an HTML template to display the data.

Create a template HTML file called index.html that will take the mars data dictionary and display all of the data in the appropriate HTML elements.

And Here we go My pages ready with Mars scarpe data!!!!