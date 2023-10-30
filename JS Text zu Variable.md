```js
db.your_collection_name.find().forEach(function(film) {
    var title = film.title;
    var match = title.match(/Staffel (\d+):.*- Part_(\d+)/);

    if (match) {
        var staffel = parseInt(match[1]);
        var teil = parseInt(match[2]);

        if ((staffel < 1 || staffel > 8) || (teil < 1 || teil > 6)) {
            db.your_collection_name.remove({_id: film._id});
        }
    }
});
```