# [Marek](https://www.gagolewski.com)'s Teaching and Training Data

> *See the comment lines within the files themselves for
> a detailed description of each dataset.*

*Good* datasets are actually hard to find!

Many textbooks consider datasets that are "too easy";
they give their readers the false impression that anything can be modelled
well with statistics and machine learning algorithms.

In practice, you will frequently be dealing with datasets that do not
tell any interesting story. Fear not, this is nothing personal,
you are not stupid or something — it might be not your fault
if you cannot find any useful patterns in your data!

Yet, you might sometimes be forced (by your thesis supervisor, manager, client,
your fake-it-till-you-make-it attitude that wants to prove your point, get
that paper published, show off your data science skills, etc.)
to squeeze something out of it anyway.

It is your **ethical duty** to say **no** to cherry picking,
misleading statements about the significance of your findings,
and so forth. Don't be a bad person.
What goes around, comes around.

Anyway, happy exercising!





## How To Access

### R

```r
airparam <- read.csv("marek/air_quality_2018_param.csv", comment.char="#")
head(airparam)
##   param_id                  param_name param_std_unit_of_measure     param_short_name
## 1      API     Airborne particle index                      none Visibility Reduction
## 2   BPM2.5 BAM  Particles < 2.5 micron                     ug/m3                PM2.5
## 3       CO             Carbon Monoxide                       ppm                   CO
## 4    HPM10                  Hivol PM10                     ug/m3
## 5      NO2            Nitrogen Dioxide                       ppb                  NO2
## 6       O3                       Ozone                       ppb                   O3
```


### Python

```python
import pandas as pd
airparam = pd.read_csv("marek/air_quality_2018_param.csv",
    comment="#")
airparam.head()
##   param_id                   param_name param_std_unit_of_measure      param_short_name
## 0      API      Airborne particle index                      none  Visibility Reduction
## 1   BPM2.5  BAM  Particles < 2.5 micron                     ug/m3                 PM2.5
## 2       CO              Carbon Monoxide                       ppm                    CO
## 3    HPM10                   Hivol PM10                     ug/m3                   NaN
## 4      NO2             Nitrogen Dioxide                       ppb                   NO2
```

To print comment lines, call, e.g.:

```python
import gzip
with gzip.open("marek/air_quality_2018.csv.gz", "rt") as f:
    while True:
        x = f.readline().strip()
        if not x.startswith("#"): break
        print(x)
## The 2018 air quality data in Victoria, Australia
## Sources: https://discover.data.vic.gov.au/dataset/epa-air-watch-all-sites-air-quality-hourly-averages-yearly
## Provided by the Environment Protection Authority Victoria
## Licensed under the Creative Commons Attribution 4.0 International License
## Dataset last update: 22 May 2019
```


### Other (Julia, GNU Octave, ...)

🚧 TO DO 🚧


## See Also

* [Minimalist Data Wrangling with Python](https://datawranglingpy.gagolewski.com)

* [Clustering Benchmarks v1](https://github.com/gagolews/clustering_benchmarks_v1/)

* [Ordinal Regression Benchmarks](https://github.com/gagolews/ordinal_regression_data) (DEPRECATED)
