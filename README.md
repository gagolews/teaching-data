# Marek's Teaching/Training Data

> *See comment lines within the files themselves for a detailed description
of each dataset.*


## How To Access

In R:

```r
airlines <- read.csv("nycflights13_airlines.csv.gz", comment.char="#")
head(airlines)

##   carrier                     name
## 1      9E        Endeavor Air Inc.
## 2      AA   American Airlines Inc.
## 3      AS     Alaska Airlines Inc.
## 4      B6          JetBlue Airways
## 5      DL     Delta Air Lines Inc.
## 6      EV ExpressJet Airlines Inc.
```

In Python:

```python
import pandas as pd
airlines = pd.read_csv("nycflights13_airlines.csv.gz",
    comment="#", compression="gzip")
airlines.head()
```

To print comment lines, call, e.g.:

```python
import gzip
with gzip.open("nycflights13_airlines.csv.gz", "rt") as f:
    while True:
        x = f.readline().strip()
        if not x.startswith("#"): break
        print(x)
```


## Marek's Datasets

* [birth_dates](marek/birth_dates.csv)
* [some_birth_dates1](marek/some_birth_dates1.csv),
    [some_birth_dates2](marek/some_birth_dates2.csv),
    [some_birth_dates3](marek/some_birth_dates3.csv)
* [warsaw_weather](marek/warsaw_weather.csv)
* [wikiweather](wikiweather/README.md)
* Apache dir listings:
    [1](marek/index_src_base_R-0.html.txt),
    [2](marek/index_src_base_R-1.html.txt),
    [3](marek/index_src_base_R-2.html.txt),
    [4](marek/index_src_base_R-3.html.txt).
* etc.


## [travel.stackexchange.com](http://travel.stackexchange.com) Data Dumps (simplified)


Licensed under CC-by-SA 3.0;
see [readme.txt](travel_stackexchange_com/readme.txt)
for more details.


* [Badges](travel_stackexchange_com/Badges.csv.gz)
* [Comments](travel_stackexchange_com/Comments.csv.gz)
* [PostLinks](travel_stackexchange_com/PostLinks.csv.gz)
* [Posts](travel_stackexchange_com/Posts.csv.gz)
* [Tags](travel_stackexchange_com/Tags.csv.gz)
* [Users](travel_stackexchange_com/Users.csv.gz)
* [Votes](travel_stackexchange_com/Votes.csv.gz)




## nycflights13

Hadley Wickham's [*nycflights13-0.2.1*](http://cran.r-project.org/package=nycflights13)
(licensed under CC0, gzipped) – on-time data for all flights that departed
NYC (i.e., JFK, LGA, or EWR) in 2013:

* [flights](hadley/nycflights13_flights.csv.gz)
* [airports](hadley/nycflights13_airports.csv.gz)
* [planes](hadley/nycflights13_planes.csv.gz)
* [airlines](hadley/nycflights13_airlines.csv.gz)
* [weather](hadley/nycflights13_weather.csv.gz)

All the logs are available at the webpage of the
[US Department of Transportation](http://www.transtats.bts.gov/DL_SelectFields.asp?Table_ID=236).
Arunkumar Srinivasan’s [github repository](https://github.com/arunsrinivasan/flights) gives some nice
R code to access the 2014 data.


## babynames

Hadley Wickham's [*babynames-0.2.1*](http://cran.r-project.org/package=babynames)
(licensed under CC0, gzipped) – US Baby Names 1880-2014:


* [applicants](hadley/babynames_applicants.csv.gz)
* [babynames](hadley/babynames_babynames.csv.gz)
* [births](hadley/babynames_births.csv.gz)
* [lifetables](hadley/babynames_lifetables.csv.gz)



## fueleconomy

Hadley Wickham's [*fueleconomy-0.1*](http://cran.r-project.org/package=fueleconomy)
(licensed under CC0, gzipped) – fuel economy data from the EPA, 1985-2015:

* [common](hadley/fueleconomy_common.csv.gz)
* [vehicles](hadley/fueleconomy_vehicles.csv.gz)



## nasaweather

Hadley Wickham's [*nasaweather-0.1*](http://cran.r-project.org/package=nasaweather)
(licensed under GPL-3, gzipped):

* [atmos](hadley/nasaweather_atmos.csv.gz)
* [borders](hadley/nasaweather_borders.csv.gz)
* [elev](hadley/nasaweather_elev.csv.gz)
* [glaciers](hadley/nasaweather_glaciers.csv.gz)
* [storms](hadley/nasaweather_storms.csv.gz)



## R Built-ins

The following datasets are included in the *datasets* package
for [GNU R](https://www.r-project.org/):

* [anscombe](r/anscombe.csv)
* [iris](r/iris.csv)
* [titanic](r/titanic.csv) (unstacked, 0-counts removed)
* [tooth_growth](r/tooth_growth.csv)
* [trees](r/trees.csv)
* [world_phones](r/world_phones.csv)

## Other

* [flights](other/flights.csv)
* [lotto](other/lotto.csv)
* [tips](other/tips.csv)
* [titanic3](other/titanic3.csv)
* [winequality-all](other/winequality-all.csv)
* [some_wines1](other/some_wines1.csv), [some_wines2](other/some_wines2.csv)


