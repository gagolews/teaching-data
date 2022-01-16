# Marek's Teaching/Training Data

> *See comment lines within the files themselves for a detailed description
of each dataset.*

"Good" datasets are actually hard to find!

Many textbooks consider datasets that are "too easy";
they give their readers the false impression that anything can be modelled
well with statistics and machine learning algorithms.

In practice, you will frequently be dealing with datasets that do not
tell any interesting story. Fear not, this is not personal,
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


### Python

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
