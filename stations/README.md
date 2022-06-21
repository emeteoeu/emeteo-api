# Current conditions

Get list of all stations, limited to 20 results per call (page).

## API Call

### URL

```
https://emeteo.sk/api/get/stations
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
| **page**			| no 		| 			| integer	| 1			| > 0

### Result

``` json
{
	"result": {
		"stations_count": 5,				// count of all stations
		"current_page": 1,					// nu,ber of current page
		"max_per_page": 20,					// maximum results in one call
		"all_pages": 1,						// count of all pages
		"stations": [
			{
				"station_url": "bernolakovo",	// unique station url
				"name": "Bernol\u00e1kovo",		// station name
				"longitude": 17.33483,			// location longitude
				"latitude": 48.193669,			// location latitude
				"altitude": 128.22,				// location altitude
				"height": 2.02,					// height above ground
				"last_connection": 1655845515	// timestamp of last connection		
			},
			{
				"station_url": "pukanec",
				"name": "Pukanec",
				"longitude": 18.709703,
				"latitude": 48.343102,
				"altitude": 385,
				"height": 2,
				"last_connection": 1655845515
			},
			{
				"station_url": "stara-hora",
				"name": "Sebechleby - Star\u00e1 Hora",
				"longitude": 18.91436,
				"latitude": 48.281233,
				"altitude": 297,
				"height": 3,
				"last_connection": 1655845515
			},
			{
				"station_url": "stare-mesto",
				"name": "Star\u00e9 Mesto",
				"longitude": 17.100213,
				"latitude": 48.145996,
				"altitude": 163,
				"height": 2,
				"last_connection": 1655845515
			},
			{
				"station_url": "vajnory",
				"name": "Vajnory",
				"longitude": 17.202127,
				"latitude": 48.208247,
				"altitude": 132,
				"height": 7,
				"last_connection": 1655845515
			}
		]
	},
	"success": true,
	"errors": [
		
	],
	"messages": [
		
	],
	"time": 1655835892
}
```