# MySQL_to_MongoDB_with_JDBC
Transfer IMDB data from MySQL to MongoDB using JDBC
# How to use it
It is a gradle project, so you can call the scripts in "build\scripts" or load the whole project use your favourite java ide.

The program will take **five arguments**:  
url of mysql schema, mysql username, mysql password, url of MongoDB, name of MongoDB's database

# MYSQL database structure
- Movie (id, title, releaseYear, runtime, rating, numberOfVotes)  
- Genre (id, name)  
- HasGenre (genreId, movieId)  
  - genreId FK Genre(id)  
  - movieId FK Movie(id)  
- Person (id, name, birthYear, deathYear)  
- ActedIn (personId, movieId)  
  - personId FK Person(id)  
  - movie FK Movie(id)  
- ComposedBy (personId, movieId)  
  - personId FK Person(id)  
  - movie FK Movie(id)  
- DirectedBy (personId, movieId)  
  - personId FK Person(id)  
  - movie FK Movie(id)  
- EditedBy (personId, movieId)  
  - personId FK Person(id)  
  - movie FK Movie(id)  
- ProducedBy (personId, movieId)  
  - personId FK Person(id)  
  - movie FK Movie(id)  
- WrittenBy (personId, movieId)  
  - personId FK Person(id)  
  - movie FK Movie(id)  
# MongoDB database structure
**Movies**  
{  
    _id : … ,  
    title : … ,  
    releaseYear : … ,  
    runtime : … ,  
    rating : … ,  
    numberOfVotes : … ,  
    genres : [ … ]  
}  
**People**
{  
    _id : … ,  
    name : … ,  
    birthYear : … ,  
    deathYear : … ,  
    actor : [ … ] ,  
    composer : [ … ] ,  
    director : [ … ] ,  
    editor : [ … ] ,  
    producer : [ … ] ,  
    writer : [ … ]  
}
