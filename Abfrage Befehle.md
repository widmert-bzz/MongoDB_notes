# Count:
```
.count
```
##### Example:
```
db.movies.find({"cast" : "Leonardo DiCaprio"}).count()
```
# Sort:
```
.sort({ year: -1 }
```
##### Example:
	1=ASC                   -1 = DESC 
```
db.movies.find({"cast" : "Leonardo DiCaprio"},{title: 1, year: 1}).sort({ year: -1 })
```
# $AND:
```
$AND []
```
##### Example:
```
db.movies.find({  
$and: [{cast: "Leonardo DiCaprio"},  
 {directors: "Martin Scorsese"}]  
 })
```