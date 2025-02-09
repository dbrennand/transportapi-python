# transportapi-python 🚆🚌🚲
Unofficial Python 3.7 API wrapper for the [TransportAPI](https://www.transportapi.com/).

# Dependencies

```
[dev-packages]
black = "*"

[packages]
requests = "*"

[requires]
python_version = "3.7"
```

Install `transportapi-python` using either:
* `pip3 install transportapi-python`, `pipenv install`, `pip3 install -r requirements.txt`, `python setup.py install`.

## Example Usage

* Obtain an [API Key](https://developer.transportapi.com/signup).

See `transportapi_python/transportapi.py` for other parameters.

* Accessing the Train endpoints.

```python
from transportapi_python import Train
from pprint import pprint

# HTTP(S) proxies are supported: https://2.python-requests.org/en/master/user/advanced/#proxies
train = Train(APP_ID="Your app ID here.", API_KEY="Your API key here.")
# Uses the default value station_code: "LBG".
pprint(train.train_timetable())
```

* Accessing Bus endpoints.

```python
from transportapi_python import Bus
from pprint import pprint

# HTTP(S) proxies are supported: https://2.python-requests.org/en/master/user/advanced/#proxies
bus = Bus(APP_ID="Your app ID here.", API_KEY="Your API key here.")
# Uses the default value station_code: "LBG".
pprint(bus.bus_service_info())
```

Usage for `Public`, `Car` and `Bicycle` classes are exactly the same as above.

## Additional Information
* [TransportAPI official API reference](https://developer.transportapi.com/docs?raml=https://transportapi.com/v3/raml/transportapi.raml)

## Changelog

* 0.0.1 - Inital release of transportapi-python. Covered all endpoints of the API. 

## Authors -- Contributors

* **dbrennand** - *Author* - [dbrennand](https://github.com/dbrennand)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) for details.

## Disclaimer
This API wrapper is **unofficial** meaning it has no affiliation with *TransportAPI*. When using their API, you consent to their [terms & conditions](https://www.transportapi.com/terms/) and [privacy policy](https://www.transportapi.com/privacy/).
