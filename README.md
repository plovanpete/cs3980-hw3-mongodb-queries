# cs3980-hw3-mongodb-queries
Uses the MongoSH to find movies with filters.

## MongoDB part 1: Finding all movies with *a runtime greater than 200* and in the *year 1983*
![mongodbcommandpt1](https://github.com/plovanpete/cs3980-hw3-mongodb-queries/assets/145849883/fe595a60-66ca-4646-a0a8-720a92880a66)
![mongodbcommandpt1 5](https://github.com/plovanpete/cs3980-hw3-mongodb-queries/assets/145849883/7e8b807f-04f4-4262-a7d5-6baf7171714b)

In this query, the command to find the movies is to first do the command: use sample_mflx so that it goes to that collection.
Afterwards, we use ```db.movies.find()``` with our filters inside.

The first filter of the command in db.movies.find() uses ```**{runtime : {$gt :200}**``` which finds the movies that are greater than 200 minutes.

The second filter of the command in db.movies.find() uses **year: 1983** finding movies that were in 1983.

Lastly, the final filter of the command in db.movies.find() uses **{title:1, year:1, runtime:1}** which displays the title, year, and runtime of the movie.



## MongoDB Part 2: Finding all movies after the year *2014* and with an *imdb rating greater than 9*.
![mongodbcommandpt2](https://github.com/plovanpete/cs3980-hw3-mongodb-queries/assets/145849883/5b3079bd-4d01-447d-8862-7b7486b5688a)

In this query, the command to find the movies is to first do the command: use sample_mflx so that it goes to that collection. *(This part can be skipped if we already did this in part 1)*
Afterwards, we use db.movies.find() with our filters inside. 

The first filter of the command in db.movies.find(), uses **year : {$gt :2014}** which finds movies that are greater than the year 2014.

The second filter of the command in db.movies.find() uses **'imdb.rating' : {$gt: 9.0}**, which goes through the imdb, and goes to the class ```rating``` to find what ratings are greater than 9.0.

Lastly, the final filter of the command in db.movies.find() uses **{title:1, year:1, 'imdb.rating':1}** which displays the title, year, and imdb rating of the movie.
