# Spotify-hit-detector
Made By Luke Borkowski

The project is designed to take a CSV of a spotify playlist or a single song using the website exportify.net and analize it for how likely it is to reach the billboard 100. The code scrapes the billboard 100 from 1999-2012 and also takes around 1m songs from spotify and analyzes them based on spotify-given features and creates a Random Forest model based on how likely each song was to be in the billboards. 

-The "Scrape Billboard Data" file will scrape the billboard hot 100 site for the pop songs from 1999-2012

-The "Process Spotify Dataset" file will process the datafile from this Kaggle: https://www.kaggle.com/datasets/rodolfofigueroa/spotify-12m-songs/data

-The "Train the Model..." file will create a Random Forest model based on the previous two datafiles

-The model is then used for any further input in the "use Spotify API..." file.
