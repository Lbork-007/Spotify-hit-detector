# Spotify-hit-detector
Made By Luke Borkowski

The project is designed to take a CSV of a spotify playlist or a single song using the website exportify.net and analize it for how likely it is to reach the billboard 100. The code scrapes the billboard 100 from 1999-2012 and also takes around 1m songs from spotify and analyzes them based on spotify-given features and creates a Random Forest model based on how likely each song was to be in the billboards. 

This project is designed to take an input of a song, and output a likely-hood of it being a hit. This was the idea from the start; however, I first was unsure of which direction this project would go in. There were many ways of approaching a project like this. At first I was using completely different datasets, like the 1 Million Songs dataset, which I eventually decided was not the most effective path to take. Initially, the project was going to analyze MP3 files and cross-examine those with their popularity, but finding a dataset which had enough MP3s for this to be effective was not possible and thus I resorted to an alternative method, instead using a dataset which included 1.2 million songs as well as all of the data that Spotify keeps on the songs. After cleaning this dataset, I scraped the Billboard Top 100 website and gathered a list of every song on the billboard within the same timeframe that the Spotify dataset included. Being sure to also include the album and artist was crucial because there were many songs with the same name.  Once I had both these datasets, I simply fed them both into the Random Forest machine learning algorithm to attempt to correlate the spotify data with its status either on the billboard or not on the billboard. I then saved the model and designed a system that would take an input of either a single spotify link to a song or a CSV of spotify links, and go through Spotify’s “Spotipy” library in order to create a dataset containing each track and its spotify features. The tracks then get sent into the model and the system will return each song’s name and artist along with its likelihood of being on the billboard 100. This system can use any song currently on Spotify and is 97% accurate. This number, however, should be taken with caution, as the ratio of songs on the billboard to songs not on the billboard is very uneven, and thus this testing was incredibly uneven towards songs not on the billboard 100.


-The "Scrape Billboard Data" file will scrape the billboard hot 100 site for the pop songs from 1999-2012

-The "Process Spotify Dataset" file will process the datafile from this Kaggle: https://www.kaggle.com/datasets/rodolfofigueroa/spotify-12m-songs/data

-The "Train the Model..." file will create a Random Forest model based on the previous two datafiles

-The model is then used for any further input in the "use Spotify API..." file.
