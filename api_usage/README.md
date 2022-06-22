# Current conditions

Get current usage of your API with max call counts of each function.

## API Call

### URL

```
https://emeteo.sk/api/get/api_usage
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

### Result

``` json
{
	"result": {
		"api_usage": {				// name of API function
			"max_calls": -2,		// max calls for time in "api_calls_limit_time"
			"current_usage": "112"		// count of current usage in 
		},
		"current_weather": {
			"max_calls": 2000,
			"current_usage": "37"
		},
		"station": {
			"max_calls": -2,
			"current_usage": 0
		},
		"stations": {
			"max_calls": -2,
			"current_usage": 0
		},
		// time from now to past, when API usage is counted
		"api_calls_limit_time": "-24 hours",
		// count of max API calls for time in "api_calls_limit_time"
		"api_calls_limit": 4000,			
		// count of all API calls for time in "api_calls_limit_time"
		"api_calls_current_usage": 149,			
		// count of all API calls which are limited for time in "api_calls_limit_time"
		"api_limited_calls_current_usage": 37	
	},
	"success": true,
	"errors": [],
	"messages": [],
	"time": 1655930706
}
```