
```
use MoviesDB;
  
db.movies.insertOne({  
    "MovieId": 14253,  
    "MovieTitle": "Beauty and the Beast",  
    "ReleaseYear": 2016,  
    "Language": "English",  
    "IMDbRating": 6.4,  
    "Genre": "Romance",  
    "Director": "Christophe Gans",  
    "Runtime": 112,  
    "Tomatometer": {  
    "Viewer": {  
      "Rating": 4,  
      "NumVotes": 12345  
    },  
    "Critics": {  
      "Rating": 1,  
      "NumVotes": 500  
    },  
    "Fresh": 75,  
    "Rotten": 25  
  }  
});  
  
db.movies.find();
```