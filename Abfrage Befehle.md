# Count:
```js
.count()
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
```js
db.movies.find({
	"cast" : "Leonardo DiCaprio"
},{
	title: 1,
	 year: 1
 }).sort({
	  year: -1 
})
```
# $AND:
```js
$AND : []
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

# $all
```js
$ALL : []
```

finds all documents that have these values(all combinations)
##### Example:
```js
languages :{$all : ["Italian", "French"]}
```

# $or
```js
$or: []
```

finds all documents that have these values(all combinations)
##### Example:
```js
$or: [  
  {title: {$regex: /Part_2$/}},  
  {title: {$regex: /Part_4$/}}  
  ]
```

# $nor
```js
$nor: []
```

finds all documents that have these values(all combinations)
##### Example:
```js
$nor: [  
  { "title": { $regex: /^Staffel [1-8]:/ } }, // Saison außerhalb von 1 bis 8  
  { "title": { $regex: /Part_[1-6]$/ } }  // Teil außerhalb von 1 bis 6  
]
```