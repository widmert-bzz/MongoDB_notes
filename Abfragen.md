
## find

```js
db.movies.find({  
    cast : /Martinelli/  
},  
 {_id: 0, "cast.$" : 1, title : 1}  
 )

```
## updateOne

```js
db.movies.updateOne(  
  {"title": "The Godfather"},  
  {  
    $set: {  
      "imdb.rating": 9.2,  
      "imdb.votes": 1565120,  
      "tomatoes.viewer.numReviews": 733777,  
      "tomatoes.viewer.meter": 98,  
      "tomatoes.viewer.rating": 4.76  
    }  
  })
```

## updateMany

```js
db.movies.updateMany(  
  {"title": "The Godfather"},  
  {  
    $set: {  
      "imdb.rating": 9.2,  
      "imdb.votes": 1565120,  
      "tomatoes.viewer.numReviews": 733777,  
      "tomatoes.viewer.meter": 98,  
      "tomatoes.viewer.rating": 4.76  
    }  
  }
  ```
## deleteOne

```js
db.users.deleteOne({
	username: "john_doe"
})
  ```
## deleteMany

```js
db.movies.deleteMany({  
  $or: [  
    {title: {$regex: /Part_2$/}},  
    {title: {$regex: /Part_4$/}}  
    ]}  
)
  ```

## findOneAndDelete

```js
db.movies.findOneAndDelete({  
    "imdb.votes": {$gte: 10000},  
    "imdb.rating": {$lte: 5}  
}, {sort: {"wins": 1}});
  ```



```js
db.movies.find()
db.movies.updateOne()
db.movies.deleteOne()
db.movies.deleteMany()
db.movies.findOneAndDelete()
```



