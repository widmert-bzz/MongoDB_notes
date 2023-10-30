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

```
db.movies.find()
db.movies.updateOne()
db.movies.deleteOne()
db.movies.deleteMany()
db.movies.findOneAndDelete()
```
