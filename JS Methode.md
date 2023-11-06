```js
let findMoviesByGenre = function(genre, pageNumber, pageSize) {  
    const skipCount = (pageNumber - 1) * pageSize;  
   let movies = db.movies.find({  
        genres: genre  
    }).sort({"imdb.rating": 1}).skip(skipCount).limit(pageSize);  
  
    movies = movies.toArray()  
  
    movies.forEach((movie) => {  
        print(movie.title);  
    });  
}
```

```js
findMoviesByGenre("Drama",1,11)
```