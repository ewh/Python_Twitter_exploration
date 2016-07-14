# README #

## What is this repository for? ##

This repository documents my efforts in learning how to use Python for accessing data from the social web, particularly Twitter.

## How do I use this? ##

#### Summary of set up
* The [code folder](./code/) contains the Python scripts to run.
* The [data folder](./data/) contains the .txt and .JSON files produced by the Python scripts.
* The [notebooks folder](./notebooks/) contains my Jupyter Notebooks, which are my playground as I learn and explore new Python functionality. These are not "final" products but are simply my sandbox for learning.
* The [figures folder](./figures/) will contain the data visualization figures generated by the scripts.

#### Dependencies:
This code is written using Python 3.5
* Python Libraries:
    * **tweepy** - Makes using Twitter's Streaming API easier. [Link](http://docs.tweepy.org/en/v3.4.0/index.html) to the online documentation.
    * **json** - Library to handle the coding and decoding of JavaScript Object Notation (JSON) files. [Link](https://docs.python.org/2.7/library/json.html) to documentation.
    * **pandas** - Library to enable data analysis and modeling, similar to the capabilities provided by languages like R. [Link](http://pandas.pydata.org/) to get pandas.
    * **geopy** - A geocoding toolbox that makes it easy to get the coordinates for a given location. [Link](https://pypi.python.org/pypi/geopy) to documentation.
    * **matplotlib** - A 2D plotting library. [Link](http://matplotlib.org/) to documentation.
    * **mpl\_toolkits** - A toolkit for plotting 2D data on maps directly in Python. [Link](http://matplotlib.org/basemap/) to information and documentation.
    * **numpy** - Package allowing fundamental scientific computing in Python. [Link](http://www.numpy.org/) to more information.

#### Code Usage Explanation
1. Run ***Twitter_Thread_StreamingAPI.py***  
  a. Pipe the output of this code into a .txt file.  
  b. Let the code run for as long as desired.  
  c. Terminate the code when you have enough data.  

2. Run ***Load_Data.py***  
  a. This code asks for the filename generated by Twitter_Thread_StreamingAPI.py  
  b. It outputs a .JSON file of all the tweets in the .txt file provided.  

3. Run ***Create_DataFrame.py***  
  a. This code reads in the .JSON file created by Load_Data.py  
  b. Extracts information from the tweets.  
  c. Imports module from ***Location_to_LatLon.py***  
    1. **Note** - the first time *Location_to_LatLon.py* is run, depending on the length of the location list, it may take a long time to create the dictionary. The code uses the *geopy* toolbox, which requires an internet connection, and if the server is overloaded it can throw an error. This code is prepared to handle these errors.
    2. Once the dictionary created by *Location_to_LatLon.py* exists, any future calls to the script will   
  d. Creates and saves a pandas data frame of the information.  

4. Run ***Tweet_languages_location_analysis.py***  
  a. This code reads in the data frame previously created.  
  b. Analyzes the data frame to calculate several properties of the data.  
  c. Generates and saves:  
    1. Plots histograms of languages.  
    2. Maps of tweet locations to a global map.  



## Who do I talk to? ##

If you have any questions, comments and/or bugs to report, please don't hesitate to message me here or through my e-mail:   aliya.gifford@gmail.com  

Thanks!
