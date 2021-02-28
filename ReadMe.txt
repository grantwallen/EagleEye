Eagle Eye - Solution
====================

To Run:

1. Download zip file
2. Extract contents
3. Load solution in Visual Studio 2019
4. Start with or without debugging

5. Test with an API tool (postman/fiddler) using urls: 
    http://localhost:5377/metadata
    http://localhost:5377/metadata/:movieId
    http://localhost:5377/movies/stats
	
Assumptions 
-----------

During the challenge I have made the following assumptions:
    GET /movies/stats
	1. stats.csv uses what I have assumed is milliseconds and the returned result 
	   requires seconds.(Indicated by name change from 'watchDurationMs' in csv file 
	   to 'averageWatchDurationS' in the returned json). For this reason I have returned 
	   seconds not milliseconds. I have also transformed the returned value to integer 
	   as this is inferred in the example json. No rounding has taken place.
	2. The returned data record uses the latest (highest Id) entry to get data from the 
	   csv source file (stats.csv). Some have different titles for different languages 
	   in the source file but the same movieId so the title value may differ in automated 	   tests).
