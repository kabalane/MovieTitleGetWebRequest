# MovieTitleGetWebRequest
Get HTTP Request to retrieve movie titles
To solve the challenge, you are requested to write am HTTP GET method to retrieve information from a movie database.

Function Description
Given a string substr, getMovieTitles must perform the following tasks:
1.	Query https://jsonmock.hackerrank.com/api/movies/search/?Title=substr
You can check (https://jsonmock.hackerrank.com/api/movies/search/?Title=Superman)
2.	Initialize the titles array to store total string elements. Store the Title of each movie meeting the search criterion in the titles array
3.	Sort titles in ascending order and return it as your answer.
If you click on the following link, https://jsonmock.hackerrank.com/api/movies/search/?Title=Superman
, you will get the followings:
{"page":1,"per_page":10,"total":2,"total_pages":1,"data":[{"Poster":"https://images-na.ssl-images-amazon.com/images/M/MV5BMjQ4MzcxNDU3N15BMl5BanBnXkFtZTgwOTE1MzMxNzE@._V1_SX300.jpg","Title":"Superman, Spiderman or Batman","Type":"movie","Year":2011,"imdbID":"tt2084949"},{"Poster":"https://images-na.ssl-images-amazon.com/images/M/MV5BN2Q0NjRiYTAtNDJiZC00ODgyLWI4NDMtYzRmYjY3MjZjMmQ0XkEyXkFqcGdeQXVyNTQzMjAxMzA@._V1_SX300.jpg","Title":"The Superman/Aquaman Hour of Adventure","Type":"series","Year":1967,"imdbID":"tt0231046"}]}

The query response from the website is JSON response with the following fields:
-	page: The current page
-	per_page: The maximum number of results per page. 
-	total: The total number of movies in the search result
-	total_pages: The total number of pages which must be queried to get all the results.
-	Data: An array of JSON objects containing movie information where the Title field denotes the title of the movie.
In order to get all results, you may have to make multiple page requests. To request a page by number, your query should read https://jsonmock.hackerrank.com/api/movies/search/?Title=substr&page=pageNumber, replacing substr and pageNumber
