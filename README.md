## Bike sharing prediction model

### Usage

To install the library:

```
$ # pip install ie_bike_model  # If I ever upload this to PyPI, which I won't
$ pip install .
```

Basic usage:

```python
>>> import datetime as dt
>>> from ie_bike_model.model import train_and_persist, predict
>>> train_and_persist()
>>> predict({
...     "date": dt.datetime(2011, 1, 1, 0, 0, 0),
...     "weathersit": 1,
...     "temperature_C": 9.84,
...     "feeling_temperature_C": 14.395,
...     "humidity": 81.0,
...     "windspeed": 0.0,
... }, model = "xgboost")
1
```
## Bike Sharing Model - Web App

### Usage

Launch the application and open
http://127.0.0.1:5000/predict?date=2012-10-01T18:00:00&weathersit=1&temperature_C=15&feeling_temperature_C=14&humidity=20&windspeed=5&model=xgboost
with your browser.

### Overview

The `app.py` file contains a simplified application that can be run standalone:

```
$ flask run
```

The rest of the files contain the same functionality in a more structured way.
