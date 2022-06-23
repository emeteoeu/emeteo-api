# eMeteo API

## :warning: API is not working, because is in development. :warning:

Follow us on [Facebook](https://www.facebook.com/emeteoeu) for more information about API.

---

## API ID & API Key request

If you are interested in API ID and API Key, [contact us](https://emeteo.sk/kontakt) with short description of usage our API in your project.


## List of functions

A detailed description of each function is in the directories of this repository.

| Name		     		| Type		| Description	| 
| ----------------		| ---------	| -------------	|
| **api_usage**			| GET 		| Get current usage of your API with max call counts of each function. |
| **current_weather**	| GET 		| Get last measured values of meteostation. |
| **station**			| GET 		| Get station details. |
| **stations**			| GET		| Get list of all stations, limited to 20 results per call (page). |

## Example of success API result

### Request URL

```
https://emeteo.sk/api/get/current_weather?api_id=YOUR_API_ID&api_key=YOUR_API_KEY&station_url=vajnory
```

### Result

``` json
{
   "result": {
	  "temperature": 23.7,
	  "humidity": 42.3,	
	  "pressure": 99824.3,
	  "wind_speed": 3.2,
	  "wind_gust": 5.3,
	  "wind_direction": 167,
	  "rain": 28.4990,
	  "solar_radiation": 38,
	  "uv": 0,
	  "measurement_timestamp": 1655833994
   },
   "success": true,
   "errors": [
	  
   ],
   "messages": [
	  
   ],
   "time": 1655834048
}
```

## Example of wrong API result

### Missing required parameter

``` json
{
    "result": null,
    "success": false,
    "errors": [
        {
            "code": 1000,
            "message": "Parameter station_url is empty."
        }
    ],
    "messages": [],
    "time": 1656001749
}
```

### API exceeds usage limit

``` json
{
    "result": null,
    "success": false,
    "errors": [
        {
            "code": 1004,
            "message": "API exceeds limit of all calls."
        }
    ],
    "messages": [
        "This API has 37 calls for last 24 hours.",
        "Maximum calls of this API is 30 for last 24 hours."
    ],
    "time": 1656001567
}
```

---

## Optional parameters available in all API functions

| Name		     	| Length	| Type		| Default	| Valid values	| Description 	|
| ----------------	| --------	| -----		| ---------	|--------------	| -------------	|
| **json_format**	| 			| string	| min		| min, pretty	| Format of JSON result |