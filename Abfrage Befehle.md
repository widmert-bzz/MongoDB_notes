# Count:
```js
.count
```
##### Example:
```js
db.movies.find({"cast" : "Leonardo DiCaprio"}).count()
```
# Sort:
```js
.sort({ year: 1 }
```
##### Example:
	1=ASC                   -1 = DESC 
```
db.movies.find({"cast" : "Leonardo DiCaprio"},{title: 1, year: 1}).sort({ year: -1 })
```
# $AND:
```js
$AND []
```
##### Example:
```js
db.movies.find({  
$and: [{cast: "Leonardo DiCaprio"},  
 {directors: "Martin Scorsese"}]  
 })
```
# Distinct / Unique:
```js
.distinct("year")
```
##### Example:
```js
db.movies.distinct("year")
```

