# Current conditions

Get last measured values of meteostation.

## API Call

### URL

```
https://emeteo.sk/api/get/current_weather
```

### Method

```
GET
```
### Parameters

| Name		     	| Required	| Length	| Type		| Default	| Valid values	| 
| ----------------	| ---------	| --------	| -----		| ---------	|--------------	|	
| **api_id**		| yes 		| 16		| string	|			|
| **api_key**		| yes 		| 32		| string	|			|
| **station_url**	| yes 		| 			| string	|			|
| **format**		| no 		| 			| string	| emeteo	| emeteo

### Result

``` json
{
   "result": {
	  "temperature": 23.7,		// temperature in celsius
	  "humidity": 42.3,		// humidity in percent
	  "pressure": 99824.3,		// absolute pressure in pascals
	  "wind_speed": 3.2,		// one minute wind speed average in m/s
	  "wind_gust": 5.3,		// wind gust in m/s
	  "wind_direction": 167,	// wind direction in degrees
	  "rain": 28.4990,		// sum of rain from midnight in mm
	  "solar_radiation": 38,	// solar radiation in W/m2
	  "uv": 0,			// UV index
	  "measurement_timestamp": 1655833994	// timestamp when datas was measured
   },
   "success": true,
   "errors": [
	  
   ],
   "messages": [
	  
   ],
   "time": 1655834048
}
```