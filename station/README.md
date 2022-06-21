# Current conditions

Get station details.

## API Call

### URL

```
https://emeteo.sk/api/get/station
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
| **station_url**	| yes 		| 			| string	| 			| 

### Result

``` json
{
	"result":{
		"station_url": "bernolakovo",	// unique station url
		"name": "Bernol\u00e1kovo",		// station name
		"longitude": 17.33483,			// location longitude
		"latitude": 48.193669,			// location latitude
		"altitude": 128.22,				// location altitude
		"height": 2.02,					// height above ground
		"last_connection": 1655845515	// timestamp of last connection	
	},
	"success":true,
	"errors":[
		
	],
	"messages":[
		
	],
	"time":1655845724
}
```