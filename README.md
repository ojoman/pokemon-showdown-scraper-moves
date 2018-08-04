# Pokemon Showdown Webscraper

## Overview

![](https://res.cloudinary.com/emanon/image/upload/v1533411957/new_starters_revealed__by_bbrunomoraes-da23c3a.gif)

There are tons of Pokemon resources out there; however, this script allows you to become more familiarized with how web scraping using Selenium works and grants direct access to basic data on Generation 1 to 7 Pokemon via csv files. One can then convert these files into a database and use it for their own personal projects.

## Getting Started
First install the necessary packages in your terminal:
```
$ pip install -r req.txt
```
Simply run the script via "python scraper.py" and watch Selenium scrape data from Pokemon Showdown for you!
```
$ python scraper.py
```


## Note
You can dictate which generation of pokemon data you are scraping by altering the numbers on line 15 of the scraper script. This simply slices out the names of the pokemon_names data array.

```python
for name in pokemon_names[721:807]:
```
```python
Generation 1: [0:151]
Generation 2: [151:251]
Generation 3: [251:386]
Generation 4: [386:493]
Generation 5: [493:649]
Generation 6: [649:721]
Generation 7: [721:807]
```
If you decide to separate the data by Pokemon Generation, be sure to change the path that the file is opening on line 9 accordingly. For instance, if you are scraping for Generation 4:

```python
file = open("./pokemon-data/pokemon-gen4-data.csv", 'w')
```